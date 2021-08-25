---
title: Synchronisation multi-moteur
description: Cette rubrique traite de la synchronisation de l’accès aux multiples moteurs indépendants présents dans la plupart des GPU modernes.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: 2d250133d8cacb26d933d3774f397de4c949c72b7b58114759791c103d374c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987547"
---
# <a name="multi-engine-synchronization"></a>Synchronisation multi-moteur

La plupart des GPU modernes contiennent plusieurs moteurs indépendants qui fournissent des fonctionnalités spécialisées. Beaucoup possèdent un ou plusieurs moteurs de copie dédiés, et un moteur de calcul, généralement distinct du moteur 3D. Chacun de ces moteurs peut exécuter des commandes en parallèle. Direct3D 12 offre un accès affiné aux moteurs 3D, de calcul et de copie, à l’aide de files d’attente et de listes de commandes.

## <a name="gpu-engines"></a>Moteurs GPU

Le diagramme suivant montre les threads d’UC d’un titre, chacun remplissant une ou plusieurs files d’attente de copie, de calcul et de 3D. La file d’attente 3D peut piloter les trois moteurs GPU. la file d’attente de calcul peut piloter les moteurs de calcul et de copie ; et la file d’attente de copie simplement le moteur de copie.

Étant donné que les différents threads remplissent les files d’attente, il ne peut y avoir aucune garantie simple de l’ordre d’exécution. c’est pourquoi les mécanismes de synchronisation sont nécessaires &mdash; lorsque le titre les requiert.

![quatre threads envoyant des commandes à trois files d’attente](images/gpu-engines.png)

L’illustration suivante montre comment un titre peut planifier le travail sur plusieurs moteurs GPU, y compris la synchronisation inter-moteur, le cas échéant : il affiche les charges de travail par moteur avec les dépendances entre les moteurs. Dans cet exemple, le moteur de copie commence par copier une géométrie nécessaire pour le rendu. Le moteur 3D attend la fin de ces copies et effectue le rendu d’une passe préalable sur la géométrie. Cela est ensuite consommé par le moteur de calcul. Les résultats de la [**répartition**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)du moteur de calcul, ainsi que plusieurs opérations de copie de texture sur le moteur de copie, sont consommées par le moteur 3D pour l’appel de [**dessin**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) final.

![la copie, les graphiques et les moteurs de calcul communiquant](images/gpu-sync.png)

Le pseudo-code suivant illustre comment un titre peut envoyer une telle charge de travail.

``` syntax
// Get per-engine contexts. Note that multiple queues may be exposed
// per engine, however that design is not reflected here.
copyEngine = device->GetCopyEngineContext();
renderEngine = device->GetRenderEngineContext();
computeEngine = device->GetComputeEngineContext();
copyEngine->CopyResource(geometry, ...); // copy geometry
copyEngine->Signal(copyFence, 101);
copyEngine->CopyResource(tex1, ...); // copy textures
copyEngine->CopyResource(tex2, ...); // copy more textures
copyEngine->CopyResource(tex3, ...); // copy more textures
copyEngine->CopyResource(tex4, ...); // copy more textures
copyEngine->Signal(copyFence, 102);
renderEngine->Wait(copyFence, 101); // geometry copied
renderEngine->Draw(); // pre-pass using geometry only into rt1
renderEngine->Signal(renderFence, 201);
computeEngine->Wait(renderFence, 201); // prepass completed
computeEngine->Dispatch(); // lighting calculations on pre-pass (using rt1 as SRV)
computeEngine->Signal(computeFence, 301);
renderEngine->Wait(computeFence, 301); // lighting calculated into buf1
renderEngine->Wait(copyFence, 102); // textures copied
renderEngine->Draw(); // final render using buf1 as SRV, and tex[1-4] SRVs
```

Le pseudo-code suivant illustre la synchronisation entre les moteurs de copie et les moteurs 3D pour effectuer l’allocation de mémoire de type tas par le biais d’une mémoire tampon en anneau. Les titres ont la possibilité de choisir le bon équilibre entre l’optimisation du parallélisme (par le biais d’une mémoire tampon importante) et la réduction de la consommation de mémoire et de la latence (par le biais d’une petite mémoire tampon).

``` syntax
device->CreateBuffer(&ringCB);
for(int i=1;i++){
  if(i > length) copyEngine->Wait(fence1, i - length);
  copyEngine->Map(ringCB, value%length, WRITE, pData); // copy new data
  copyEngine->Signal(fence2, i);
  renderEngine->Wait(fence2, i);
  renderEngine->Draw(); // draw using copied data
  renderEngine->Signal(fence1, i);
}

// example for length = 3:
// copyEngine->Map();
// copyEngine->Signal(fence2, 1); // fence2 = 1  
// copyEngine->Map();
// copyEngine->Signal(fence2, 2); // fence2 = 2
// copyEngine->Map();
// copyEngine->Signal(fence2, 3); // fence2 = 3
// copy engine has exhausted the ring buffer, so must wait for render to consume it
// copyEngine->Wait(fence1, 1); // fence1 == 0, wait
// renderEngine->Wait(fence2, 1); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 1); // fence1 = 1, copy engine now unblocked
// renderEngine->Wait(fence2, 2); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 2); // fence1 = 2
// renderEngine->Wait(fence2, 3); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 3); // fence1 = 3
// now render engine is starved, and so must wait for the copy engine
// renderEngine->Wait(fence2, 4); // fence2 == 3, wait
```

## <a name="multi-engine-scenarios"></a>Scénarios multi-moteur

Direct3D 12 vous permet d’éviter une exécution accidentelle en inefficacité due à des délais de synchronisation inattendus. Elle vous permet également d’introduire la synchronisation à un niveau supérieur où la synchronisation requise peut être déterminée avec une plus grande certitude. Un deuxième problème que les adresses multimoteurs consiste à rendre les opérations coûteuses plus explicites, ce qui comprend des transitions entre la 3D et la vidéo qui étaient traditionnellement coûteuses en raison de la synchronisation entre plusieurs contextes de noyau.

En particulier, les scénarios suivants peuvent être traités avec Direct3D 12.

-   Fonctionnement du GPU asynchrone et de faible priorité. Cela permet l’exécution simultanée de tâches GPU de faible priorité et d’opérations atomiques qui permettent à un thread GPU de consommer les résultats d’un autre thread non synchronisé sans blocage.
-   Travail de calcul à priorité élevée. Avec le calcul en arrière-plan, il est possible d’interrompre le rendu 3D pour effectuer une petite quantité de travail de calcul à priorité élevée. Les résultats de ce travail peuvent être obtenus tôt pour un traitement supplémentaire sur le processeur.
-   Travail de calcul en arrière-plan. Une file d’attente à faible priorité distincte pour les charges de travail de calcul permet à une application d’utiliser des cycles GPU de rechange pour effectuer un calcul en arrière-plan sans impact négatif sur les tâches de rendu principal (ou autres). Les tâches en arrière-plan peuvent inclure la décompression des ressources ou la mise à jour des simulations ou des structures d’accélération. Les tâches en arrière-plan doivent être régulièrement synchronisées sur le processeur (environ une fois par trame) pour éviter la blocage ou le ralentissement du travail de premier plan.
-   Diffusion et téléchargement de données. Une file d’attente de copie distincte remplace les concepts D3D11 des données initiales et la mise à jour des ressources. Bien que l’application soit responsable de plus de détails dans le modèle Direct3D 12, cette responsabilité est fournie avec Power. L’application peut contrôler la quantité de mémoire système dédiée à la mise en mémoire tampon des données de téléchargement. L’application peut choisir quand et comment (processeur vs GPU, bloquant et non bloquant) la synchronisation et peut suivre la progression et contrôler la quantité de travail en file d’attente.
-   Parallélisme accru. Les applications peuvent utiliser des files d’attente plus profondes pour les charges de travail en arrière-plan (par exemple, le décodage vidéo) lorsqu’elles ont des files d’attente distinctes pour le travail de premier plan.

Dans Direct3D 12, le concept de file d’attente de commandes est la représentation d’API d’une séquence de travail à peu près série soumise par l’application. Les barrières et autres techniques permettent d’exécuter ce travail dans un pipeline ou dans le désordre, mais l’application ne voit qu’une seule chronologie d’achèvement. Cela correspond au contexte immédiat dans D3D11.

## <a name="synchronization-apis"></a>API de synchronisation

### <a name="devices-and-queues"></a>Appareils et files d’attente

L’appareil Direct3D 12 a des méthodes pour créer et récupérer des files d’attente de commandes de différents types et priorités. La plupart des applications doivent utiliser les files d’attente de commandes par défaut, car elles permettent l’utilisation partagée par d’autres composants. Les applications avec des exigences de concurrence supplémentaires peuvent créer des files d’attente supplémentaires. Les files d’attente sont spécifiées par le type de liste de commandes qu’elles consomment.

Reportez-vous aux méthodes de création suivantes de [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).

-   [**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : crée une file d’attente de commandes en fonction des informations contenues dans une structure [**\_ \_ \_ desc de file d’attente de commandes Direct3D 12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .
-   [**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : crée une liste de commandes de type [**liste de \_ commandes Direct3D \_ \_ 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).
-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : crée une clôture, en notant les indicateurs dans les [**\_ \_ indicateurs**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags)de délimitation Direct3D 12. Les délimiteurs sont utilisés pour synchroniser les files d’attente.

Les files d’attente de tous les types (3D, Compute et Copy) partagent la même interface et sont toutes basées sur une liste de commandes.

Reportez-vous aux méthodes suivantes de [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).

-   [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : envoie un tableau de listes de commandes pour l’exécution. Chaque liste de commandes définie par [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).
-   [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : définit une valeur de clôture lorsque la file d’attente (exécutée sur le GPU) atteint un certain point.
-   [**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : la file d’attente attend que la clôture spécifiée atteigne la valeur spécifiée.

Notez que les offres groupées ne sont pas consommées par les files d’attente et, par conséquent, ce type ne peut pas être utilisé pour créer une file d’attente.

### <a name="fences"></a>Délimitations

L’API multi-moteur fournit des API explicites à créer et à synchroniser à l’aide de délimiteurs. Une barrière est une construction de synchronisation contrôlée par une valeur UINT64. Les valeurs de clôture sont définies par l’application. Une opération de signal modifie la valeur de la clôture et une opération d’attente se bloque jusqu’à ce que la clôture ait atteint la valeur demandée ou supérieure. Un événement peut être déclenché lorsqu’une clôture atteint une certaine valeur.

Reportez-vous aux méthodes de l’interface [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) .

-   [**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : retourne la valeur actuelle de la clôture.
-   [**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : provoque le déclenchement d’un événement lorsque la clôture atteint une valeur donnée.
-   [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : définit la clôture sur la valeur donnée.

Les délimitations autorisent l’accès de l’UC à la valeur de clôture actuelle, ainsi que les attentes et les signaux de l’UC.

La méthode [**signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) de l’interface [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) met à jour une clôture du côté processeur. Cette mise à jour a lieu immédiatement. La méthode [**signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) sur [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) met à jour une clôture du côté GPU. Cette mise à jour a lieu après l’exécution de toutes les autres opérations de la file d’attente de commandes.

Tous les nœuds d’une installation multi-moteur peuvent lire et réagir à toute clôture qui atteint la valeur appropriée.

Les applications définissent leurs propres valeurs de clôture, un bon point de départ peut être d’incrémenter une clôture une fois par frame.

Une clôture *peut* être *reroulée*. Cela signifie que la valeur de la clôture n’a pas besoin d’être incrémentée uniquement. Si une opération de **signal** est mise en file d’attente sur deux files d’attente de commandes différentes, ou si deux threads d’UC appellent le **signal** sur une clôture, il peut y avoir une course pour déterminer quel **signal** se termine en dernier et, par conséquent, quelle valeur de clôture est celle qui restera. Si une clôture est reroulée, toute nouvelle attente (y compris les demandes **SetEventOnCompletion** ) est comparée à la nouvelle valeur de clôture inférieure, et peut donc ne pas être satisfaite, même si la valeur de la clôture avait déjà été suffisamment élevée pour les satisfaire. Si une course se produit, entre une valeur qui *répond à une* attente en suspens, et une valeur inférieure qui ne l’est pas, l’attente est satisfaite, quelle que soit la valeur restante.

Les API de clôture fournissent des fonctionnalités de synchronisation puissantes, mais elles peuvent créer des problèmes de débogage potentiellement difficiles. Il est recommandé d’utiliser chaque clôture uniquement pour indiquer la progression d’une chronologie afin d’éviter les concurrences entre les signaleurs.

### <a name="copy-and-compute-command-lists"></a>Copier et calculer des listes de commandes

Les trois types de liste de commandes utilisent l’interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) , mais seul un sous-ensemble des méthodes est pris en charge pour la copie et le calcul.

Les listes de commandes de copie et de calcul peuvent utiliser les méthodes suivantes.

-   [**Plus**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyTiles**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**Initialisation**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

Les listes de commandes Compute peuvent également utiliser les méthodes suivantes.

-   [**ClearState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [**ClearUnorderedAccessViewFloat**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**ClearUnorderedAccessViewUint**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**ExecuteIndirect**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [**SetComputeRoot32BitConstant**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetComputeRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetComputeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

Les listes de commandes Compute doivent définir un PSO Compute lors de l’appel de [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Les offres groupées ne peuvent pas être utilisées avec des listes de commandes ou des files d’attente de calcul ou de copie.

## <a name="pipelined-compute-and-graphics-example"></a>Exemple de calcul et de graphique en pipeline

Cet exemple montre comment la synchronisation des limites peut être utilisée pour créer un pipeline de travail de calcul sur une file d’attente (référencée par `pComputeQueue` ) consommée par les graphismes qui fonctionnent sur la file d’attente `pGraphicsQueue` . Le calcul et le travail graphique sont canalisés avec la file d’attente de graphiques qui consomment le résultat du calcul du travail à partir de plusieurs frames, et un événement de processeur est utilisé pour limiter le travail total mis en file d’attente dans son ensemble.

```cpp
void PipelinedComputeGraphics()
{
    const UINT CpuLatency = 3;
    const UINT ComputeGraphicsLatency = 2;

    HANDLE handle = CreateEvent(nullptr, FALSE, FALSE, nullptr);

    UINT64 FrameNumber = 0;

    while (1)
    {
        if (FrameNumber > ComputeGraphicsLatency)
        {
            pComputeQueue->Wait(pGraphicsFence,
                FrameNumber - ComputeGraphicsLatency);
        }

        if (FrameNumber > CpuLatency)
        {
            pComputeFence->SetEventOnFenceCompletion(
                FrameNumber - CpuLatency,
                handle);
            WaitForSingleObject(handle, INFINITE);
        }

        ++FrameNumber;

        pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
        pComputeQueue->Signal(pComputeFence, FrameNumber);
        if (FrameNumber > ComputeGraphicsLatency)
        {
            UINT GraphicsFrameNumber = FrameNumber - ComputeGraphicsLatency;
            pGraphicsQueue->Wait(pComputeFence, GraphicsFrameNumber);
            pGraphicsQueue->ExecuteCommandLists(1, &pGraphicsCommandList);
            pGraphicsQueue->Signal(pGraphicsFence, GraphicsFrameNumber);
        }
    }
}
```

Pour prendre en charge ce traitement en pipeline, il doit y avoir une mémoire tampon de `ComputeGraphicsLatency+1` copies différentes des données transmises de la file d’attente de calcul à la file d’attente Graphics. Les listes de commandes doivent utiliser UAVs et indirection pour lire et écrire à partir de la « version » appropriée des données dans la mémoire tampon. La file d’attente de calcul doit attendre jusqu’à ce que la file d’attente de graphiques ait fini de lire les données du frame N avant de pouvoir écrire le frame `N+ComputeGraphicsLatency` .

Notez que le volume de la file d’attente de calcul qui a fonctionné par rapport à l’UC ne dépend pas directement de la quantité de mémoire tampon requise. Toutefois, la mise en file d’attente du travail GPU au-delà de la quantité d’espace de mémoire tampon disponible est moins importante.

Un autre mécanisme permettant d’éviter l’indirection consisterait à créer plusieurs listes de commandes correspondant à chacune des versions « renommées » des données. L’exemple suivant utilise cette technique lors de l’extension de l’exemple précédent pour permettre aux files d’attente de calcul et de graphiques de s’exécuter de manière plus asynchrone.

## <a name="asynchronous-compute-and-graphics-example"></a>Exemple de calcul et de graphique asynchrone

L’exemple suivant permet aux graphiques de s’afficher de manière asynchrone à partir de la file d’attente de calcul. Il y a toujours une quantité fixe de données mises en mémoire tampon entre les deux étapes. Toutefois, le travail Graphics fonctionne de façon indépendante et utilise le résultat le plus à jour de l’étape de calcul, comme indiqué sur le processeur lorsque le travail graphique est mis en file d’attente. Cela peut s’avérer utile si les graphiques fonctionnent en cours de mise à jour par une autre source, par exemple une entrée d’utilisateur. Il doit y avoir plusieurs listes de commandes pour autoriser le `ComputeGraphicsLatency` fonctionnement des frames de graphiques en cours de vol à la fois, et la fonction `UpdateGraphicsCommandList` représente la mise à jour de la liste de commandes pour inclure les données d’entrée les plus récentes et lire les données de calcul à partir de la mémoire tampon appropriée.

La file d’attente de calcul doit toujours attendre que la file d’attente de graphiques se termine par les mémoires tampons de canal, mais une troisième délimitation ( `pGraphicsComputeFence` ) est introduite afin que la progression de la lecture de graphiques par rapport au travail de calcul et à la progression des graphiques en général puisse être suivie. Cela reflète le fait que les trames graphiques consécutives pouvaient lire à partir du même résultat de calcul ou ignorer un résultat de calcul. Une conception plus efficace mais légèrement plus compliquée utilise uniquement la délimitation de graphique unique et stocke un mappage aux frames de calcul utilisés par chaque frame graphique.

```cpp
void AsyncPipelinedComputeGraphics()
{
    const UINT CpuLatency{ 3 };
    const UINT ComputeGraphicsLatency{ 2 };

    // The compute fence is at index 0; the graphics fence is at index 1.
    ID3D12Fence* rgpFences[]{ pComputeFence, pGraphicsFence };
    HANDLE handles[2];
    handles[0] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    handles[1] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    UINT FrameNumbers[]{ 0, 0 };

    ID3D12GraphicsCommandList* rgpGraphicsCommandLists[CpuLatency];
    CreateGraphicsCommandLists(ARRAYSIZE(rgpGraphicsCommandLists),
        rgpGraphicsCommandLists);

    // Graphics needs to wait for the first compute frame to complete; this is the
    // only wait that the graphics queue will perform.
    pGraphicsQueue->Wait(pComputeFence, 1);

    while (true)
    {
        for (auto i = 0; i < 2; ++i)
        {
            if (FrameNumbers[i] > CpuLatency)
            {
                rgpFences[i]->SetEventOnCompletion(
                    FrameNumbers[i] - CpuLatency,
                    handles[i]);
            }
            else
            {
                ::SetEvent(handles[i]);
            }
        }


        auto WaitResult = ::WaitForMultipleObjects(2, handles, FALSE, INFINITE);
        if (WaitResult > WAIT_OBJECT_0 + 1) continue;
        auto Stage = WaitResult - WAIT_OBJECT_0;
        ++FrameNumbers[Stage];

        switch (Stage)
        {
        case 0:
        {
            if (FrameNumbers[Stage] > ComputeGraphicsLatency)
            {
                pComputeQueue->Wait(pGraphicsComputeFence,
                    FrameNumbers[Stage] - ComputeGraphicsLatency);
            }
            pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
            pComputeQueue->Signal(pComputeFence, FrameNumbers[Stage]);
            break;
        }
        case 1:
        {
            // Recall that the GPU queue started with a wait for pComputeFence, 1
            UINT64 CompletedComputeFrames = min(1,
                pComputeFence->GetCompletedValue());
            UINT64 PipeBufferIndex =
                (CompletedComputeFrames - 1) % ComputeGraphicsLatency;
            UINT64 CommandListIndex = (FrameNumbers[Stage] - 1) % CpuLatency;
            // Update graphics command list based on CPU input and using the appropriate
            // buffer index for data produced by compute.
            UpdateGraphicsCommandList(PipeBufferIndex,
                rgpGraphicsCommandLists[CommandListIndex]);

            // Signal *before* new rendering to indicate what compute work
            // the graphics queue is DONE with
            pGraphicsQueue->Signal(pGraphicsComputeFence, CompletedComputeFrames - 1);
            pGraphicsQueue->ExecuteCommandLists(1,
                rgpGraphicsCommandLists + PipeBufferIndex);
            pGraphicsQueue->Signal(pGraphicsFence, FrameNumbers[Stage]);
            break;
        }
        }
    }
}
```

## <a name="multi-queue-resource-access"></a>Accès aux ressources de plusieurs files d’attente

Pour accéder à une ressource sur plusieurs files d’attente, une application doit respecter les règles suivantes.

-   L’accès aux ressources (reportez-vous aux [**\_ \_ États de ressource Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) est déterminé par la classe type de file d’attente objet de file d’attente. Il existe deux classes de type de file d’attente : Compute/3D queue est une classe de type, Copy est une deuxième classe de type. Par conséquent, une ressource qui a un obstacle à l’état de la \_ ressource du nuanceur non-pixel \_ \_ sur une file d’attente 3D peut être utilisée dans cet État sur n’importe quelle file d’attente de calcul ou 3D, sous réserve des exigences de synchronisation qui requièrent la sérialisation de la plupart des écritures. Les États de ressource partagés entre les deux classes de type (source de copie \_ et \_ destination de copie) sont considérés comme différents États pour chaque classe de type. Ainsi, si une ressource effectue une transition vers COPY \_ dest sur une file d’attente de copie, elle n’est pas accessible en tant que destination de copie à partir de files d’attente de calcul ou 3D, et vice versa.

    Pour résumer.

    -   Une file d’attente « Object » est une file d’attente unique.
    -   Un « type » de file d’attente est l’un des trois suivants : Compute, 3D et Copy.
    -   Une file d’attente « classe de type » est l’un des deux suivants : Compute/3D et Copy.

-   Les indicateurs de copie (copie \_ dest et \_ source de copie) utilisés comme États initiaux représentent les États de la classe de type 3D/Compute. Pour utiliser une ressource initialement sur une file d’attente de copie, elle doit démarrer dans un État commun. L’État commun peut être utilisé pour toutes les utilisations dans une file d’attente de copie à l’aide des transitions d’État implicites. 
-   Bien que l’état des ressources soit partagé entre toutes les files d’attente de calcul et 3D, il n’est pas autorisé à écrire simultanément dans la ressource sur des files d’attente différentes. « Simultanément » signifie non synchronisé, en notant que l’exécution non synchronisée n’est pas possible sur un matériel. Les règles suivantes s’appliquent.

    -   Une seule file d’attente peut écrire dans une ressource à la fois.
    -   Plusieurs files d’attente peuvent lire à partir de la ressource tant qu’elles ne lisent pas les octets modifiés par le writer (la lecture simultanée d’octets génère des résultats non définis).
    -   Une clôture doit être utilisée pour la synchronisation après l’écriture avant qu’une autre file d’attente puisse lire les octets écrits ou n’avoir aucun accès en écriture.

-   Les mémoires tampons d’arrière-plan en cours de présentation doivent être dans l' \_ \_ État commun état de la ressource Direct3D 12 \_ . 

## <a name="related-topics"></a>Rubriques connexes

[Guide de programmation Direct3D 12](directx-12-programming-guide.md)

[Utilisation de barrières de ressources pour synchroniser les États des ressources dans Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[Gestion de la mémoire dans Direct3D 12](memory-management.md)
