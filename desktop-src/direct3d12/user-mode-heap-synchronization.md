---
title: Synchronisation multi-moteur
description: Cette rubrique traite de la synchronisation de l’accès aux multiples moteurs indépendants présents dans la plupart des GPU modernes.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d60704e411a1ba45dd4902ad9101a416391743dd
ms.sourcegitcommit: 622d149edf775af5a9633c2d12ccfddf7000b8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/31/2020
ms.locfileid: "104548489"
---
# <a name="multi-engine-synchronization"></a><span data-ttu-id="b56df-103">Synchronisation multi-moteur</span><span class="sxs-lookup"><span data-stu-id="b56df-103">Multi-engine synchronization</span></span>

<span data-ttu-id="b56df-104">La plupart des GPU modernes contiennent plusieurs moteurs indépendants qui fournissent des fonctionnalités spécialisées.</span><span class="sxs-lookup"><span data-stu-id="b56df-104">Most modern GPUs contain multiple independent engines that provide specialized functionality.</span></span> <span data-ttu-id="b56df-105">Beaucoup possèdent un ou plusieurs moteurs de copie dédiés, et un moteur de calcul, généralement distinct du moteur 3D.</span><span class="sxs-lookup"><span data-stu-id="b56df-105">Many have one or more dedicated copy engines, and a compute engine, usually distinct from the 3D engine.</span></span> <span data-ttu-id="b56df-106">Chacun de ces moteurs peut exécuter des commandes en parallèle.</span><span class="sxs-lookup"><span data-stu-id="b56df-106">Each of these engines can execute commands in parallel with each other.</span></span> <span data-ttu-id="b56df-107">Direct3D 12 offre un accès affiné aux moteurs 3D, de calcul et de copie, à l’aide de files d’attente et de listes de commandes.</span><span class="sxs-lookup"><span data-stu-id="b56df-107">Direct3D 12 provides fine-grained access to the 3D, compute, and copy engines, using queues and command lists.</span></span>

## <a name="gpu-engines"></a><span data-ttu-id="b56df-108">Moteurs GPU</span><span class="sxs-lookup"><span data-stu-id="b56df-108">GPU engines</span></span>

<span data-ttu-id="b56df-109">Le diagramme suivant montre les threads d’UC d’un titre, chacun remplissant une ou plusieurs files d’attente de copie, de calcul et de 3D.</span><span class="sxs-lookup"><span data-stu-id="b56df-109">The following diagram shows a title's CPU threads, each populating one or more of the copy, compute, and 3D queues.</span></span> <span data-ttu-id="b56df-110">La file d’attente 3D peut piloter les trois moteurs GPU. la file d’attente de calcul peut piloter les moteurs de calcul et de copie ; et la file d’attente de copie simplement le moteur de copie.</span><span class="sxs-lookup"><span data-stu-id="b56df-110">The 3D queue can drive all three GPU engines; the compute queue can drive the compute and copy engines; and the copy queue simply the copy engine.</span></span>

<span data-ttu-id="b56df-111">Étant donné que les différents threads remplissent les files d’attente, il ne peut y avoir aucune garantie simple de l’ordre d’exécution. c’est pourquoi les mécanismes de synchronisation sont nécessaires &mdash; lorsque le titre les requiert.</span><span class="sxs-lookup"><span data-stu-id="b56df-111">As the different threads populate the queues, there can be no simple guarantee of the order of execution, hence the need for synchronization mechanisms&mdash;when the title requires them.</span></span>

![quatre threads envoyant des commandes à trois files d’attente](images/gpu-engines.png)

<span data-ttu-id="b56df-113">L’illustration suivante montre comment un titre peut planifier le travail sur plusieurs moteurs GPU, y compris la synchronisation inter-moteur, le cas échéant : il affiche les charges de travail par moteur avec les dépendances entre les moteurs.</span><span class="sxs-lookup"><span data-stu-id="b56df-113">The following image illustrate how a title might schedule work across multiple GPU engines, including inter-engine synchronization where necessary: it shows the per-engine workloads with inter-engine dependencies.</span></span> <span data-ttu-id="b56df-114">Dans cet exemple, le moteur de copie commence par copier une géométrie nécessaire pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="b56df-114">In this example, the copy engine first copies some geometry necessary for rendering.</span></span> <span data-ttu-id="b56df-115">Le moteur 3D attend la fin de ces copies et effectue le rendu d’une passe préalable sur la géométrie.</span><span class="sxs-lookup"><span data-stu-id="b56df-115">The 3D engine waits for these copies to complete, and renders a pre-pass over the geometry.</span></span> <span data-ttu-id="b56df-116">Cela est ensuite consommé par le moteur de calcul.</span><span class="sxs-lookup"><span data-stu-id="b56df-116">This is then consumed by the compute engine.</span></span> <span data-ttu-id="b56df-117">Les résultats de la [**répartition**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)du moteur de calcul, ainsi que plusieurs opérations de copie de texture sur le moteur de copie, sont consommées par le moteur 3D pour l’appel de [**dessin**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) final.</span><span class="sxs-lookup"><span data-stu-id="b56df-117">The results of the compute engine [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch), along with several texture copy operations on the copy engine, are consumed by the 3D engine for the final [**Draw**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) call.</span></span>

![la copie, les graphiques et les moteurs de calcul communiquant](images/gpu-sync.png)

<span data-ttu-id="b56df-119">Le pseudo-code suivant illustre comment un titre peut envoyer une telle charge de travail.</span><span class="sxs-lookup"><span data-stu-id="b56df-119">The following pseudo-code illustrates how a title might submit such a workload.</span></span>

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

<span data-ttu-id="b56df-120">Le pseudo-code suivant illustre la synchronisation entre les moteurs de copie et les moteurs 3D pour effectuer l’allocation de mémoire de type tas par le biais d’une mémoire tampon en anneau.</span><span class="sxs-lookup"><span data-stu-id="b56df-120">The following pseudo-code illustrates synchronization between the copy and 3D engines to accomplish heap-like memory allocation via a ring buffer.</span></span> <span data-ttu-id="b56df-121">Les titres ont la possibilité de choisir le bon équilibre entre l’optimisation du parallélisme (par le biais d’une mémoire tampon importante) et la réduction de la consommation de mémoire et de la latence (par le biais d’une petite mémoire tampon).</span><span class="sxs-lookup"><span data-stu-id="b56df-121">Titles have the flexibility to choose the right balance between maximizing parallelism (via a large buffer) and reducing memory consumption and latency (via a small buffer).</span></span>

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

## <a name="multi-engine-scenarios"></a><span data-ttu-id="b56df-122">Scénarios multi-moteur</span><span class="sxs-lookup"><span data-stu-id="b56df-122">Multi-engine scenarios</span></span>

<span data-ttu-id="b56df-123">Direct3D 12 vous permet d’éviter une exécution accidentelle en inefficacité due à des délais de synchronisation inattendus.</span><span class="sxs-lookup"><span data-stu-id="b56df-123">Direct3D 12 allows you to avoid accidentally running into inefficiencies caused by unexpected synchronization delays.</span></span> <span data-ttu-id="b56df-124">Elle vous permet également d’introduire la synchronisation à un niveau supérieur où la synchronisation requise peut être déterminée avec une plus grande certitude.</span><span class="sxs-lookup"><span data-stu-id="b56df-124">It also allows you to introduce synchronization at a higher level where the required synchronization can be determined with greater certainty.</span></span> <span data-ttu-id="b56df-125">Un deuxième problème que les adresses multimoteurs consiste à rendre les opérations coûteuses plus explicites, ce qui comprend des transitions entre la 3D et la vidéo qui étaient traditionnellement coûteuses en raison de la synchronisation entre plusieurs contextes de noyau.</span><span class="sxs-lookup"><span data-stu-id="b56df-125">A second issue that multi-engine addresses is to make expensive operations more explicit, which includes transitions between 3D and video that were traditionally costly because of synchronization between multiple kernel contexts.</span></span>

<span data-ttu-id="b56df-126">En particulier, les scénarios suivants peuvent être traités avec Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="b56df-126">In particular, the following scenarios can be addressed with Direct3D 12.</span></span>

-   <span data-ttu-id="b56df-127">Fonctionnement du GPU asynchrone et de faible priorité.</span><span class="sxs-lookup"><span data-stu-id="b56df-127">Asynchronous and low priority GPU work.</span></span> <span data-ttu-id="b56df-128">Cela permet l’exécution simultanée de tâches GPU de faible priorité et d’opérations atomiques qui permettent à un thread GPU de consommer les résultats d’un autre thread non synchronisé sans blocage.</span><span class="sxs-lookup"><span data-stu-id="b56df-128">This enables concurrent execution of low priority GPU work and atomic operations that enable one GPU thread to consume the results of another unsynchronized thread without blocking.</span></span>
-   <span data-ttu-id="b56df-129">Travail de calcul à priorité élevée.</span><span class="sxs-lookup"><span data-stu-id="b56df-129">High priority compute work.</span></span> <span data-ttu-id="b56df-130">Avec le calcul en arrière-plan, il est possible d’interrompre le rendu 3D pour effectuer une petite quantité de travail de calcul à priorité élevée.</span><span class="sxs-lookup"><span data-stu-id="b56df-130">With background compute it is possible to interrupt 3D rendering to do a small amount of high priority compute work.</span></span> <span data-ttu-id="b56df-131">Les résultats de ce travail peuvent être obtenus tôt pour un traitement supplémentaire sur le processeur.</span><span class="sxs-lookup"><span data-stu-id="b56df-131">The results of this work can be obtained early for additional processing on the CPU.</span></span>
-   <span data-ttu-id="b56df-132">Travail de calcul en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b56df-132">Background compute work.</span></span> <span data-ttu-id="b56df-133">Une file d’attente à faible priorité distincte pour les charges de travail de calcul permet à une application d’utiliser des cycles GPU de rechange pour effectuer un calcul en arrière-plan sans impact négatif sur les tâches de rendu principal (ou autres).</span><span class="sxs-lookup"><span data-stu-id="b56df-133">A separate low priority queue for compute workloads allows an application to utilize spare GPU cycles to perform background computation without negative impact on the primary rendering (or other) tasks.</span></span> <span data-ttu-id="b56df-134">Les tâches en arrière-plan peuvent inclure la décompression des ressources ou la mise à jour des simulations ou des structures d’accélération.</span><span class="sxs-lookup"><span data-stu-id="b56df-134">Background tasks may include decompression of resources or updating simulations or acceleration structures.</span></span> <span data-ttu-id="b56df-135">Les tâches en arrière-plan doivent être régulièrement synchronisées sur le processeur (environ une fois par trame) pour éviter la blocage ou le ralentissement du travail de premier plan.</span><span class="sxs-lookup"><span data-stu-id="b56df-135">Background tasks should be synchronized on the CPU infrequently (approximately once per frame) to avoid stalling or slowing foreground work.</span></span>
-   <span data-ttu-id="b56df-136">Diffusion et téléchargement de données.</span><span class="sxs-lookup"><span data-stu-id="b56df-136">Streaming and uploading data.</span></span> <span data-ttu-id="b56df-137">Une file d’attente de copie distincte remplace les concepts D3D11 des données initiales et la mise à jour des ressources.</span><span class="sxs-lookup"><span data-stu-id="b56df-137">A separate copy queue replaces the D3D11 concepts of initial data and updating resources.</span></span> <span data-ttu-id="b56df-138">Bien que l’application soit responsable de plus de détails dans le modèle Direct3D 12, cette responsabilité est fournie avec Power.</span><span class="sxs-lookup"><span data-stu-id="b56df-138">Although the application is responsible for more details in the Direct3D 12 model, this responsibility comes with power.</span></span> <span data-ttu-id="b56df-139">L’application peut contrôler la quantité de mémoire système dédiée à la mise en mémoire tampon des données de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="b56df-139">The application can control how much system memory is devoted to buffering upload data.</span></span> <span data-ttu-id="b56df-140">L’application peut choisir quand et comment (processeur vs GPU, bloquant et non bloquant) la synchronisation et peut suivre la progression et contrôler la quantité de travail en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="b56df-140">The app can choose when and how (CPU vs GPU, blocking vs non-blocking) to synchronize, and can track progress and control the amount of queued work.</span></span>
-   <span data-ttu-id="b56df-141">Parallélisme accru.</span><span class="sxs-lookup"><span data-stu-id="b56df-141">Increased parallelism.</span></span> <span data-ttu-id="b56df-142">Les applications peuvent utiliser des files d’attente plus profondes pour les charges de travail en arrière-plan (par exemple, le décodage vidéo) lorsqu’elles ont des files d’attente distinctes pour le travail de premier plan.</span><span class="sxs-lookup"><span data-stu-id="b56df-142">Applications can use deeper queues for background workloads (e.g. video decode) when they have separate queues for foreground work.</span></span>

<span data-ttu-id="b56df-143">Dans Direct3D 12, le concept de file d’attente de commandes est la représentation d’API d’une séquence de travail à peu près série soumise par l’application.</span><span class="sxs-lookup"><span data-stu-id="b56df-143">In Direct3D 12 the concept of a command queue is the API representation of a roughly serial sequence of work submitted by the application.</span></span> <span data-ttu-id="b56df-144">Les barrières et autres techniques permettent d’exécuter ce travail dans un pipeline ou dans le désordre, mais l’application ne voit qu’une seule chronologie d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="b56df-144">Barriers and other techniques allow this work to be executed in a pipeline or out of order, but the application only sees a single completion timeline.</span></span> <span data-ttu-id="b56df-145">Cela correspond au contexte immédiat dans D3D11.</span><span class="sxs-lookup"><span data-stu-id="b56df-145">This corresponds to the immediate context in D3D11.</span></span>

## <a name="synchronization-apis"></a><span data-ttu-id="b56df-146">API de synchronisation</span><span class="sxs-lookup"><span data-stu-id="b56df-146">Synchronization APIs</span></span>

### <a name="devices-and-queues"></a><span data-ttu-id="b56df-147">Appareils et files d’attente</span><span class="sxs-lookup"><span data-stu-id="b56df-147">Devices and queues</span></span>

<span data-ttu-id="b56df-148">L’appareil Direct3D 12 a des méthodes pour créer et récupérer des files d’attente de commandes de différents types et priorités.</span><span class="sxs-lookup"><span data-stu-id="b56df-148">The Direct3D 12 device has methods to create and retrieve command queues of different types and priorities.</span></span> <span data-ttu-id="b56df-149">La plupart des applications doivent utiliser les files d’attente de commandes par défaut, car elles permettent l’utilisation partagée par d’autres composants.</span><span class="sxs-lookup"><span data-stu-id="b56df-149">Most applications should use the default command queues because these allow for shared usage by other components.</span></span> <span data-ttu-id="b56df-150">Les applications avec des exigences de concurrence supplémentaires peuvent créer des files d’attente supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b56df-150">Applications with additional concurrency requirements can create additional queues.</span></span> <span data-ttu-id="b56df-151">Les files d’attente sont spécifiées par le type de liste de commandes qu’elles consomment.</span><span class="sxs-lookup"><span data-stu-id="b56df-151">Queues are specified by the command list type that they consume.</span></span>

<span data-ttu-id="b56df-152">Reportez-vous aux méthodes de création suivantes de [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span><span class="sxs-lookup"><span data-stu-id="b56df-152">Refer to the following creation methods of [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span></span>

-   <span data-ttu-id="b56df-153">[**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : crée une file d’attente de commandes en fonction des informations contenues dans une structure [**\_ \_ \_ desc de file d’attente de commandes Direct3D 12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .</span><span class="sxs-lookup"><span data-stu-id="b56df-153">[**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : creates a command queue based on information in a [**Direct3D 12\_COMMAND\_QUEUE\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) structure.</span></span>
-   <span data-ttu-id="b56df-154">[**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : crée une liste de commandes de type [**liste de \_ commandes Direct3D \_ \_ 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span><span class="sxs-lookup"><span data-stu-id="b56df-154">[**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : creates a command list of type [**Direct3D 12\_COMMAND\_LIST\_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>
-   <span data-ttu-id="b56df-155">[**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : crée une clôture, en notant les indicateurs dans les [**\_ \_ indicateurs**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags)de délimitation Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="b56df-155">[**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : creates a fence, noting the flags in [**Direct3D 12\_FENCE\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags).</span></span> <span data-ttu-id="b56df-156">Les délimiteurs sont utilisés pour synchroniser les files d’attente.</span><span class="sxs-lookup"><span data-stu-id="b56df-156">Fences are used to synchronize queues.</span></span>

<span data-ttu-id="b56df-157">Les files d’attente de tous les types (3D, Compute et Copy) partagent la même interface et sont toutes basées sur une liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="b56df-157">Queues of all types (3D, compute and copy) share the same interface and are all command-list based.</span></span>

<span data-ttu-id="b56df-158">Reportez-vous aux méthodes suivantes de [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span><span class="sxs-lookup"><span data-stu-id="b56df-158">Refer to the following methods of [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span></span>

-   <span data-ttu-id="b56df-159">[**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : envoie un tableau de listes de commandes pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b56df-159">[**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : submits an array of command lists for execution.</span></span> <span data-ttu-id="b56df-160">Chaque liste de commandes définie par [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).</span><span class="sxs-lookup"><span data-stu-id="b56df-160">Each command list being defined by [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>
-   <span data-ttu-id="b56df-161">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : définit une valeur de clôture lorsque la file d’attente (exécutée sur le GPU) atteint un certain point.</span><span class="sxs-lookup"><span data-stu-id="b56df-161">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : sets a fence value when the queue (running on the GPU) reaches a certain point.</span></span>
-   <span data-ttu-id="b56df-162">[**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : la file d’attente attend que la clôture spécifiée atteigne la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b56df-162">[**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : the queue waits until the specified fence reaches the specified value.</span></span>

<span data-ttu-id="b56df-163">Notez que les offres groupées ne sont pas consommées par les files d’attente et, par conséquent, ce type ne peut pas être utilisé pour créer une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="b56df-163">Note that bundles are not consumed by any queues and therefore this type cannot be used to create a queue.</span></span>

### <a name="fences"></a><span data-ttu-id="b56df-164">Délimitations</span><span class="sxs-lookup"><span data-stu-id="b56df-164">Fences</span></span>

<span data-ttu-id="b56df-165">L’API multi-moteur fournit des API explicites à créer et à synchroniser à l’aide de délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="b56df-165">The multi-engine API provides explicit APIs to create and synchronize using fences.</span></span> <span data-ttu-id="b56df-166">Une barrière est une construction de synchronisation contrôlée par une valeur UINT64.</span><span class="sxs-lookup"><span data-stu-id="b56df-166">A fence is a synchronization construct controlled by a UINT64 value.</span></span> <span data-ttu-id="b56df-167">Les valeurs de clôture sont définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="b56df-167">Fence values are set by the application.</span></span> <span data-ttu-id="b56df-168">Une opération de signal modifie la valeur de la clôture et une opération d’attente se bloque jusqu’à ce que la clôture ait atteint la valeur demandée ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b56df-168">A signal operation modifies the fence value and a wait operation blocks until the fence has reached the requested value or greater.</span></span> <span data-ttu-id="b56df-169">Un événement peut être déclenché lorsqu’une clôture atteint une certaine valeur.</span><span class="sxs-lookup"><span data-stu-id="b56df-169">An event can be fired when a fence reaches a certain value.</span></span>

<span data-ttu-id="b56df-170">Reportez-vous aux méthodes de l’interface [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) .</span><span class="sxs-lookup"><span data-stu-id="b56df-170">Refer to the methods of the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface.</span></span>

-   <span data-ttu-id="b56df-171">[**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : retourne la valeur actuelle de la clôture.</span><span class="sxs-lookup"><span data-stu-id="b56df-171">[**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : returns the current value of the fence.</span></span>
-   <span data-ttu-id="b56df-172">[**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : provoque le déclenchement d’un événement lorsque la clôture atteint une valeur donnée.</span><span class="sxs-lookup"><span data-stu-id="b56df-172">[**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : causes an event to fire when the fence reaches a given value.</span></span>
-   <span data-ttu-id="b56df-173">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : définit la clôture sur la valeur donnée.</span><span class="sxs-lookup"><span data-stu-id="b56df-173">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : sets the fence to the given value.</span></span>

<span data-ttu-id="b56df-174">Les délimitations autorisent l’accès de l’UC à la valeur de clôture actuelle, ainsi que les attentes et les signaux de l’UC.</span><span class="sxs-lookup"><span data-stu-id="b56df-174">Fences allow CPU access to the current fence value, and CPU waits and signals.</span></span>

<span data-ttu-id="b56df-175">La méthode [**signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) de l’interface [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) met à jour une clôture du côté processeur.</span><span class="sxs-lookup"><span data-stu-id="b56df-175">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) method on the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface updates a fence from the CPU side.</span></span> <span data-ttu-id="b56df-176">Cette mise à jour a lieu immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b56df-176">This update occurs immediately.</span></span> <span data-ttu-id="b56df-177">La méthode [**signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) sur [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) met à jour une clôture du côté GPU.</span><span class="sxs-lookup"><span data-stu-id="b56df-177">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) method on [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) updates a fence from the GPU side.</span></span> <span data-ttu-id="b56df-178">Cette mise à jour a lieu après l’exécution de toutes les autres opérations de la file d’attente de commandes.</span><span class="sxs-lookup"><span data-stu-id="b56df-178">This update occurs after all other operations on the command queue have been completed.</span></span>

<span data-ttu-id="b56df-179">Tous les nœuds d’une installation multi-moteur peuvent lire et réagir à toute clôture qui atteint la valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="b56df-179">All nodes in a multi-engine setup can read and react to any fence reaching the right value.</span></span>

<span data-ttu-id="b56df-180">Les applications définissent leurs propres valeurs de clôture, un bon point de départ peut être d’incrémenter une clôture une fois par frame.</span><span class="sxs-lookup"><span data-stu-id="b56df-180">Applications set their own fence values, a good starting point might be increasing a fence once per frame.</span></span>

<span data-ttu-id="b56df-181">Une clôture *peut* être *reroulée*.</span><span class="sxs-lookup"><span data-stu-id="b56df-181">A fence *may* be *rewound*.</span></span> <span data-ttu-id="b56df-182">Cela signifie que la valeur de la clôture n’a pas besoin d’être incrémentée uniquement.</span><span class="sxs-lookup"><span data-stu-id="b56df-182">This means that the fence value does not need to solely increment.</span></span> <span data-ttu-id="b56df-183">Si une opération de **signal** est mise en file d’attente sur deux files d’attente de commandes différentes, ou si deux threads d’UC appellent le **signal** sur une clôture, il peut y avoir une course pour déterminer quel **signal** se termine en dernier et, par conséquent, quelle valeur de clôture est celle qui restera.</span><span class="sxs-lookup"><span data-stu-id="b56df-183">If a **Signal** operation is enqueued on two different command queues, or if two CPU threads are both calling **Signal** on a fence, there may be a race to determine which **Signal** completes last, and therefore which fence value is the one which will remain.</span></span> <span data-ttu-id="b56df-184">Si une clôture est reroulée, toute nouvelle attente (y compris les demandes **SetEventOnCompletion** ) est comparée à la nouvelle valeur de clôture inférieure, et peut donc ne pas être satisfaite, même si la valeur de la clôture avait déjà été suffisamment élevée pour les satisfaire.</span><span class="sxs-lookup"><span data-stu-id="b56df-184">If a fence is rewound, any new waits (including **SetEventOnCompletion** requests) will be compared against the new lower fence value, and therefore may not be satisfied, even if the fence value had previously been high enough to satisfy them.</span></span> <span data-ttu-id="b56df-185">Si une course se produit, entre une valeur qui *répond à une* attente en suspens, et une valeur inférieure qui ne l’est pas, l’attente est satisfaite, quelle que soit la valeur restante.</span><span class="sxs-lookup"><span data-stu-id="b56df-185">If a race does occur, between a value which will satisfy an outstanding wait, and a lower value which will not, the wait *will* be satisfied regardless of which value remains afterwards.</span></span>

<span data-ttu-id="b56df-186">Les API de clôture fournissent des fonctionnalités de synchronisation puissantes, mais elles peuvent créer des problèmes de débogage potentiellement difficiles.</span><span class="sxs-lookup"><span data-stu-id="b56df-186">The fence APIs provide powerful synchronization functionality but can create potentially difficult to debug issues.</span></span> <span data-ttu-id="b56df-187">Il est recommandé d’utiliser chaque clôture uniquement pour indiquer la progression d’une chronologie afin d’éviter les concurrences entre les signaleurs.</span><span class="sxs-lookup"><span data-stu-id="b56df-187">It is recommended that each fence only be used to indicate progress on one timeline to prevent races between signalers.</span></span>

### <a name="copy-and-compute-command-lists"></a><span data-ttu-id="b56df-188">Copier et calculer des listes de commandes</span><span class="sxs-lookup"><span data-stu-id="b56df-188">Copy and compute command lists</span></span>

<span data-ttu-id="b56df-189">Les trois types de liste de commandes utilisent l’interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) , mais seul un sous-ensemble des méthodes est pris en charge pour la copie et le calcul.</span><span class="sxs-lookup"><span data-stu-id="b56df-189">All three types of command list use the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface, however only a subset of the methods are supported for copy and compute.</span></span>

<span data-ttu-id="b56df-190">Les listes de commandes de copie et de calcul peuvent utiliser les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="b56df-190">Copy and compute command lists can use the following methods.</span></span>

-   [<span data-ttu-id="b56df-191">**Fermer**</span><span class="sxs-lookup"><span data-stu-id="b56df-191">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [<span data-ttu-id="b56df-192">**CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="b56df-192">**CopyBufferRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="b56df-193">**CopyResource**</span><span class="sxs-lookup"><span data-stu-id="b56df-193">**CopyResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="b56df-194">**CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="b56df-194">**CopyTextureRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="b56df-195">**CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="b56df-195">**CopyTiles**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="b56df-196">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="b56df-196">**Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [<span data-ttu-id="b56df-197">**ResourceBarrier**</span><span class="sxs-lookup"><span data-stu-id="b56df-197">**ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

<span data-ttu-id="b56df-198">Les listes de commandes Compute peuvent également utiliser les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="b56df-198">Compute command lists can also use the following methods.</span></span>

-   [<span data-ttu-id="b56df-199">**ClearState**</span><span class="sxs-lookup"><span data-stu-id="b56df-199">**ClearState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [<span data-ttu-id="b56df-200">**ClearUnorderedAccessViewFloat**</span><span class="sxs-lookup"><span data-stu-id="b56df-200">**ClearUnorderedAccessViewFloat**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="b56df-201">**ClearUnorderedAccessViewUint**</span><span class="sxs-lookup"><span data-stu-id="b56df-201">**ClearUnorderedAccessViewUint**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="b56df-202">**DiscardResource**</span><span class="sxs-lookup"><span data-stu-id="b56df-202">**DiscardResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [<span data-ttu-id="b56df-203">**Dispatch**</span><span class="sxs-lookup"><span data-stu-id="b56df-203">**Dispatch**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="b56df-204">**ExecuteIndirect**</span><span class="sxs-lookup"><span data-stu-id="b56df-204">**ExecuteIndirect**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [<span data-ttu-id="b56df-205">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="b56df-205">**SetComputeRoot32BitConstant**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="b56df-206">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="b56df-206">**SetComputeRoot32BitConstants**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [<span data-ttu-id="b56df-207">**SetComputeRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="b56df-207">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="b56df-208">**SetComputeRootDescriptorTable**</span><span class="sxs-lookup"><span data-stu-id="b56df-208">**SetComputeRootDescriptorTable**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [<span data-ttu-id="b56df-209">**SetComputeRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="b56df-209">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="b56df-210">**SetComputeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="b56df-210">**SetComputeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [<span data-ttu-id="b56df-211">**SetComputeRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="b56df-211">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="b56df-212">**SetDescriptorHeaps**</span><span class="sxs-lookup"><span data-stu-id="b56df-212">**SetDescriptorHeaps**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [<span data-ttu-id="b56df-213">**SetPipelineState**</span><span class="sxs-lookup"><span data-stu-id="b56df-213">**SetPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [<span data-ttu-id="b56df-214">**SetPredication**</span><span class="sxs-lookup"><span data-stu-id="b56df-214">**SetPredication**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

<span data-ttu-id="b56df-215">Les listes de commandes Compute doivent définir un PSO Compute lors de l’appel de [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).</span><span class="sxs-lookup"><span data-stu-id="b56df-215">Compute command lists must set a compute PSO when calling [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).</span></span>

<span data-ttu-id="b56df-216">Les offres groupées ne peuvent pas être utilisées avec des listes de commandes ou des files d’attente de calcul ou de copie.</span><span class="sxs-lookup"><span data-stu-id="b56df-216">Bundles cannot be used with compute or copy command lists or queues.</span></span>

## <a name="pipelined-compute-and-graphics-example"></a><span data-ttu-id="b56df-217">Exemple de calcul et de graphique en pipeline</span><span class="sxs-lookup"><span data-stu-id="b56df-217">Pipelined compute and graphics example</span></span>

<span data-ttu-id="b56df-218">Cet exemple montre comment la synchronisation des limites peut être utilisée pour créer un pipeline de travail de calcul sur une file d’attente (référencée par `pComputeQueue` ) consommée par les graphismes qui fonctionnent sur la file d’attente `pGraphicsQueue` .</span><span class="sxs-lookup"><span data-stu-id="b56df-218">This example shows how fence synchronization can be used to create a pipeline of compute work on a queue (referenced by `pComputeQueue`) that's consumed by graphics work on queue `pGraphicsQueue`.</span></span> <span data-ttu-id="b56df-219">Le calcul et le travail graphique sont canalisés avec la file d’attente de graphiques qui consomment le résultat du calcul du travail à partir de plusieurs frames, et un événement de processeur est utilisé pour limiter le travail total mis en file d’attente dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="b56df-219">The compute and graphics work is pipelined with the graphics queue consuming the result of compute work from several frames back, and a CPU event is used to throttle the total work queued overall.</span></span>

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

<span data-ttu-id="b56df-220">Pour prendre en charge ce traitement en pipeline, il doit y avoir une mémoire tampon de `ComputeGraphicsLatency+1` copies différentes des données transmises de la file d’attente de calcul à la file d’attente Graphics.</span><span class="sxs-lookup"><span data-stu-id="b56df-220">To support this pipelining, there must be a buffer of `ComputeGraphicsLatency+1` different copies of the data passing from the compute queue to the graphics queue.</span></span> <span data-ttu-id="b56df-221">Les listes de commandes doivent utiliser UAVs et indirection pour lire et écrire à partir de la « version » appropriée des données dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b56df-221">The command lists must use UAVs and indirection to read and write from the appropriate “version” of the data in the buffer.</span></span> <span data-ttu-id="b56df-222">La file d’attente de calcul doit attendre jusqu’à ce que la file d’attente de graphiques ait fini de lire les données du frame N avant de pouvoir écrire le frame `N+ComputeGraphicsLatency` .</span><span class="sxs-lookup"><span data-stu-id="b56df-222">The compute queue must wait until the graphics queue has finished reading from the data for frame N before it can write frame `N+ComputeGraphicsLatency`.</span></span>

<span data-ttu-id="b56df-223">Notez que le volume de la file d’attente de calcul qui a fonctionné par rapport à l’UC ne dépend pas directement de la quantité de mémoire tampon requise. Toutefois, la mise en file d’attente du travail GPU au-delà de la quantité d’espace de mémoire tampon disponible est moins importante.</span><span class="sxs-lookup"><span data-stu-id="b56df-223">Note that the amount of compute queue worked relative to the CPU does not depend directly on the amount of buffering required, however, queuing GPU work beyond the amount of buffer space available is less valuable.</span></span>

<span data-ttu-id="b56df-224">Un autre mécanisme permettant d’éviter l’indirection consisterait à créer plusieurs listes de commandes correspondant à chacune des versions « renommées » des données.</span><span class="sxs-lookup"><span data-stu-id="b56df-224">An alternative mechanism to avoid indirection would be to create multiple command lists corresponding to each of the “renamed” versions of the data.</span></span> <span data-ttu-id="b56df-225">L’exemple suivant utilise cette technique lors de l’extension de l’exemple précédent pour permettre aux files d’attente de calcul et de graphiques de s’exécuter de manière plus asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b56df-225">The next example uses this technique while extending the previous example to allow the compute and graphics queues to run more asynchronously.</span></span>

## <a name="asynchronous-compute-and-graphics-example"></a><span data-ttu-id="b56df-226">Exemple de calcul et de graphique asynchrone</span><span class="sxs-lookup"><span data-stu-id="b56df-226">Asynchronous compute and graphics example</span></span>

<span data-ttu-id="b56df-227">L’exemple suivant permet aux graphiques de s’afficher de manière asynchrone à partir de la file d’attente de calcul.</span><span class="sxs-lookup"><span data-stu-id="b56df-227">This next example allows graphics to render asynchronously from the compute queue.</span></span> <span data-ttu-id="b56df-228">Il y a toujours une quantité fixe de données mises en mémoire tampon entre les deux étapes. Toutefois, le travail Graphics fonctionne de façon indépendante et utilise le résultat le plus à jour de l’étape de calcul, comme indiqué sur le processeur lorsque le travail graphique est mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="b56df-228">There is still a fixed amount of buffered data between the two stages, however now graphics work proceeds independently and uses the most up-to-date result of the compute stage as known on the CPU when the graphics work is queued.</span></span> <span data-ttu-id="b56df-229">Cela peut s’avérer utile si les graphiques fonctionnent en cours de mise à jour par une autre source, par exemple une entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b56df-229">This would be useful if the graphics work was being updated by another source, for example user input.</span></span> <span data-ttu-id="b56df-230">Il doit y avoir plusieurs listes de commandes pour autoriser le `ComputeGraphicsLatency` fonctionnement des frames de graphiques en cours de vol à la fois, et la fonction `UpdateGraphicsCommandList` représente la mise à jour de la liste de commandes pour inclure les données d’entrée les plus récentes et lire les données de calcul à partir de la mémoire tampon appropriée.</span><span class="sxs-lookup"><span data-stu-id="b56df-230">There must be multiple command lists to allow the `ComputeGraphicsLatency` frames of graphics work to be in flight at a time, and the function `UpdateGraphicsCommandList` represents updating the command list to include the most recent input data and read from the compute data from the appropriate buffer.</span></span>

<span data-ttu-id="b56df-231">La file d’attente de calcul doit toujours attendre que la file d’attente de graphiques se termine par les mémoires tampons de canal, mais une troisième délimitation ( `pGraphicsComputeFence` ) est introduite afin que la progression de la lecture de graphiques par rapport au travail de calcul et à la progression des graphiques en général puisse être suivie.</span><span class="sxs-lookup"><span data-stu-id="b56df-231">The compute queue must still wait for the graphics queue to finish with the pipe buffers, but a third fence (`pGraphicsComputeFence`) is introduced so that the progress of graphics reading compute work versus graphics progress in general can be tracked.</span></span> <span data-ttu-id="b56df-232">Cela reflète le fait que les trames graphiques consécutives pouvaient lire à partir du même résultat de calcul ou ignorer un résultat de calcul.</span><span class="sxs-lookup"><span data-stu-id="b56df-232">This reflects the fact that now consecutive graphics frames could read from the same compute result or could skip a compute result.</span></span> <span data-ttu-id="b56df-233">Une conception plus efficace mais légèrement plus compliquée utilise uniquement la délimitation de graphique unique et stocke un mappage aux frames de calcul utilisés par chaque frame graphique.</span><span class="sxs-lookup"><span data-stu-id="b56df-233">A more efficient but slightly more complicated design would use just the single graphics fence and store a mapping to the compute frames used by each graphics frame.</span></span>

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

## <a name="multi-queue-resource-access"></a><span data-ttu-id="b56df-234">Accès aux ressources de plusieurs files d’attente</span><span class="sxs-lookup"><span data-stu-id="b56df-234">Multi-queue resource access</span></span>

<span data-ttu-id="b56df-235">Pour accéder à une ressource sur plusieurs files d’attente, une application doit respecter les règles suivantes.</span><span class="sxs-lookup"><span data-stu-id="b56df-235">To access a resource on more than one queue an application must adhere to the following rules.</span></span>

-   <span data-ttu-id="b56df-236">L’accès aux ressources (reportez-vous aux [**\_ \_ États de ressource Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) est déterminé par la classe type de file d’attente objet de file d’attente.</span><span class="sxs-lookup"><span data-stu-id="b56df-236">Resource access (refer to [**Direct3D 12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) is determined by queue type class not queue object.</span></span> <span data-ttu-id="b56df-237">Il existe deux classes de type de file d’attente : Compute/3D queue est une classe de type, Copy est une deuxième classe de type.</span><span class="sxs-lookup"><span data-stu-id="b56df-237">There are two type classes of queue: Compute/3D queue is one type class, Copy is a second type class.</span></span> <span data-ttu-id="b56df-238">Par conséquent, une ressource qui a un obstacle à l’état de la \_ ressource du nuanceur non-pixel \_ \_ sur une file d’attente 3D peut être utilisée dans cet État sur n’importe quelle file d’attente de calcul ou 3D, sous réserve des exigences de synchronisation qui requièrent la sérialisation de la plupart des écritures.</span><span class="sxs-lookup"><span data-stu-id="b56df-238">So a resource that has a barrier to the NON\_PIXEL\_SHADER\_RESOURCE state on one 3D queue can be used in that state on any 3D or Compute queue, subject to synchronization requirements which require most writes to be serialized.</span></span> <span data-ttu-id="b56df-239">Les États de ressource partagés entre les deux classes de type (source de copie \_ et \_ destination de copie) sont considérés comme différents États pour chaque classe de type.</span><span class="sxs-lookup"><span data-stu-id="b56df-239">The resource states that are shared between the two type classes (COPY\_SOURCE and COPY\_DEST) are considered different states for each type class.</span></span> <span data-ttu-id="b56df-240">Ainsi, si une ressource effectue une transition vers COPY \_ dest sur une file d’attente de copie, elle n’est pas accessible en tant que destination de copie à partir de files d’attente de calcul ou 3D, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="b56df-240">So that if a resource transitions to COPY\_DEST on a Copy queue it is not accessible as a copy destination from 3D or Compute queues and vice versa.</span></span>

    <span data-ttu-id="b56df-241">Pour résumer.</span><span class="sxs-lookup"><span data-stu-id="b56df-241">To summarize.</span></span>

    -   <span data-ttu-id="b56df-242">Une file d’attente « Object » est une file d’attente unique.</span><span class="sxs-lookup"><span data-stu-id="b56df-242">A queue "object" is any single queue.</span></span>
    -   <span data-ttu-id="b56df-243">Un « type » de file d’attente est l’un des trois suivants : Compute, 3D et Copy.</span><span class="sxs-lookup"><span data-stu-id="b56df-243">A queue "type" is any one of these three: Compute, 3D, and Copy.</span></span>
    -   <span data-ttu-id="b56df-244">Une file d’attente « classe de type » est l’un des deux suivants : Compute/3D et Copy.</span><span class="sxs-lookup"><span data-stu-id="b56df-244">A queue "type class" is any one of these two: Compute/3D and Copy.</span></span>

-   <span data-ttu-id="b56df-245">Les indicateurs de copie (copie \_ dest et \_ source de copie) utilisés comme États initiaux représentent les États de la classe de type 3D/Compute.</span><span class="sxs-lookup"><span data-stu-id="b56df-245">The COPY flags (COPY\_DEST and COPY\_SOURCE) used as initial states represent states in the 3D/Compute type class.</span></span> <span data-ttu-id="b56df-246">Pour utiliser une ressource initialement sur une file d’attente de copie, elle doit démarrer dans un État commun.</span><span class="sxs-lookup"><span data-stu-id="b56df-246">To use a resource initially on a Copy queue it should start in the COMMON state.</span></span> <span data-ttu-id="b56df-247">L’État commun peut être utilisé pour toutes les utilisations dans une file d’attente de copie à l’aide des transitions d’État implicites.</span><span class="sxs-lookup"><span data-stu-id="b56df-247">The COMMON state can be used for all usages on a Copy queue using the implicit state transitions.</span></span> 
-   <span data-ttu-id="b56df-248">Bien que l’état des ressources soit partagé entre toutes les files d’attente de calcul et 3D, il n’est pas autorisé à écrire simultanément dans la ressource sur des files d’attente différentes.</span><span class="sxs-lookup"><span data-stu-id="b56df-248">Although resource state is shared across all Compute and 3D queues, it is not permitted to write to the resource simultaneously on different queues.</span></span> <span data-ttu-id="b56df-249">« Simultanément » signifie non synchronisé, en notant que l’exécution non synchronisée n’est pas possible sur un matériel.</span><span class="sxs-lookup"><span data-stu-id="b56df-249">"Simultaneously" here means unsynchronized, noting unsynchronized execution is not possible on some hardware.</span></span> <span data-ttu-id="b56df-250">Les règles suivantes s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="b56df-250">The following rules apply.</span></span>

    -   <span data-ttu-id="b56df-251">Une seule file d’attente peut écrire dans une ressource à la fois.</span><span class="sxs-lookup"><span data-stu-id="b56df-251">Only one queue can write to a resource at a time.</span></span>
    -   <span data-ttu-id="b56df-252">Plusieurs files d’attente peuvent lire à partir de la ressource tant qu’elles ne lisent pas les octets modifiés par le writer (la lecture simultanée d’octets génère des résultats non définis).</span><span class="sxs-lookup"><span data-stu-id="b56df-252">Multiple queues can read from the resource as long as they don’t read the bytes being modified by the writer (reading bytes being simultaneously written produces undefined results).</span></span>
    -   <span data-ttu-id="b56df-253">Une clôture doit être utilisée pour la synchronisation après l’écriture avant qu’une autre file d’attente puisse lire les octets écrits ou n’avoir aucun accès en écriture.</span><span class="sxs-lookup"><span data-stu-id="b56df-253">A fence must be used to synchronize after writing before another queue can read the written bytes or make any write access.</span></span>

-   <span data-ttu-id="b56df-254">Les mémoires tampons d’arrière-plan en cours de présentation doivent être dans l' \_ \_ État commun état de la ressource Direct3D 12 \_ .</span><span class="sxs-lookup"><span data-stu-id="b56df-254">Back buffers being presented must be in the Direct3D 12\_RESOURCE\_STATE\_COMMON state.</span></span> 

## <a name="related-topics"></a><span data-ttu-id="b56df-255">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b56df-255">Related topics</span></span>

[<span data-ttu-id="b56df-256">Guide de programmation Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b56df-256">Direct3D 12 programming guide</span></span>](directx-12-programming-guide.md)

[<span data-ttu-id="b56df-257">Utilisation de barrières de ressources pour synchroniser les États des ressources dans Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b56df-257">Using resource barriers to synchronize resource states in Direct3D 12</span></span>](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[<span data-ttu-id="b56df-258">Gestion de la mémoire dans Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b56df-258">Memory management in Direct3D 12</span></span>](memory-management.md)
