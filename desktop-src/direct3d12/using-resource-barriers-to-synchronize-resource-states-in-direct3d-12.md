---
title: Utilisation de barrières de ressources pour synchroniser les états des ressources dans Direct3D 12
description: Pour réduire l’utilisation globale du processeur et activer le traitement multithread et le prétraitement des pilotes, Direct3D 12 déplace la responsabilité de la gestion de l’État par ressource du pilote Graphics vers l’application.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df27e7997b4f3f56ae8e87688e5cc136dc7eb87d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343474"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a>Utilisation de barrières de ressources pour synchroniser les états des ressources dans Direct3D 12

Pour réduire l’utilisation globale du processeur et activer le traitement multithread et le prétraitement des pilotes, Direct3D 12 déplace la responsabilité de la gestion de l’État par ressource du pilote Graphics vers l’application. Un exemple d’État par ressource est de savoir si une ressource de texture est actuellement accessible par le biais d’un nuanceur Affichage des ressources ou en tant que vue de la cible de rendu. Dans Direct3D 11, les pilotes devaient suivre cet État en arrière-plan. Cela s’avère coûteux du point de vue de l’UC et complique de manière significative tout type de conception multithread. Dans Microsoft Direct3D 12, la majeure partie de l’État par ressource est gérée par l’application avec une seule API, [**ID3D12GraphicsCommandList :: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).

-   [Utilisation de l’API ResourceBarrier pour gérer l’État par ressource](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [États des ressources](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [États initiaux pour les ressources](#initial-states-for-resources)
    -   [Restrictions relatives à l’état des ressources en lecture/écriture](#readwrite-resource-state-restrictions)
    -   [États des ressources pour la présentation des mémoires tampons d’arrière-plan](#resource-states-for-presenting-back-buffers)
    -   [Rejet des ressources](#discarding-resources)
-   [Transitions d’État implicites](#implicit-state-transitions)
    -   [Promotion de l’État commun](#common-state-promotion)
    -   [État d’atténuation commun](#state-decay-to-common)
    -   [Impact sur les performances](#performance-implications)
-   [Fractionner les barrières](#split-barriers)
-   [Exemple de scénario de cloisonnement de ressources](#resource-barrier-example-scenario)
-   [Exemple de promotion et d’atténuation de l’État commun](#common-state-promotion-and-decay-sample)
-   [Exemple de barrières divisées](#example-of-split-barriers)
-   [Rubriques connexes](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a>Utilisation de l’API ResourceBarrier pour gérer l’État par ressource

[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifie le pilote graphique des situations dans lesquelles le pilote peut avoir besoin de synchroniser plusieurs accès à la mémoire dans laquelle une ressource est stockée. La méthode est appelée avec une ou plusieurs structures de description de la barrière des ressources qui indiquent le type de cloisonnement des ressources déclaré.

Il existe trois types de barrières des ressources :

-   **Transition barrière** : une barrière de transition indique qu’un ensemble de sous-ressources est en transition entre différentes utilisations. Une structure de [**barrière de \_ transition de ressource \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) est utilisée pour spécifier la sous-ressource qui est en transition, ainsi que les États *avant* et *après* de la sous-ressource.

    Le système vérifie que les transitions de sous-ressources dans une liste de commandes sont cohérentes avec les transitions précédentes dans la même liste de commandes. La couche de débogage suit plus en détail l’état des sous-ressources pour trouver d’autres erreurs, mais cette validation est conservatrice et non exhaustive.

    Notez que vous pouvez utiliser l' \_ \_ indicateur de ressource D3D12 \_ de tous les sous- \_ ressources pour spécifier que toutes les sous-ressources d’une ressource sont en cours de transition.

-   **Barrière d’alias** : une barrière d’alias indique une transition entre les utilisations de deux ressources différentes qui ont des mappages qui se chevauchent dans le même tas. Cela s’applique aux ressources réservées et placées. Une structure de [**barrière d' \_ alias des ressources \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) est utilisée pour spécifier la ressource *avant* et la ressource *après* .

    Notez qu’une ou les deux ressources peuvent avoir la valeur NULL, ce qui indique qu’une ressource en mosaïque peut provoquer des alias. Pour plus d’informations sur l’utilisation des ressources en mosaïque, consultez [ressources](../direct3d11/tiled-resources.md) en mosaïque et [ressources en mosaïque de volume](volume-tiled-resources.md).

-   **Barrière de vue d’accès non triée (UAV)** : une barrière UAV indique que tous les accès UAV, à la fois en lecture ou en écriture, à une ressource particulière doivent se terminer entre tous les futurs accès UAV, en lecture ou en écriture. Il n’est pas nécessaire pour une application de placer une barrière UAV entre deux appels de dessin ou de distribution qui lisent uniquement à partir d’un UAV. En outre, il n’est pas nécessaire de placer une barrière UAV entre deux appels de dessin ou de distribution qui écrivent dans le même UAV si l’application sait qu’il est possible d’exécuter l’accès UAV dans n’importe quel ordre. Une structure de [**\_ \_ \_ barrière UAV de ressource D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) est utilisée pour spécifier la ressource UAV à laquelle s’applique le cloisonnement. L’application peut spécifier la valeur NULL pour le UAV du cloisonnement, ce qui indique que tout accès UAV peut nécessiter le cloisonnement.

Quand [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) est appelé avec un tableau de descriptions de cloisonnement de ressources, l’API se comporte comme si elle était appelée une fois pour chaque élément, dans l’ordre dans lequel elles ont été fournies.

À un moment donné, une sous-ressource se trouve dans un seul État, déterminé par l’ensemble des indicateurs d' [**\_ \_ États de ressource D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) fournis à [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier). L’application doit s’assurer que les États *Before* et *after* des appels consécutifs à **ResourceBarrier** conviennent.

> [!TIP]
>
> Dans la mesure du possible, les applications doivent regrouper plusieurs transitions dans un seul appel d’API.

 

### <a name="resource-states"></a>États des ressources

Pour obtenir la liste complète des États des ressources qu’une ressource peut passer d’une ressource à l’autre, consultez la rubrique de référence pour l’énumération des [**\_ \_ États des ressources D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .

Pour les cloisonnements de ressources fractionnées, consultez également les [**\_ indicateurs de \_ barrière \_ de ressources D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).

### <a name="initial-states-for-resources"></a>États initiaux pour les ressources

Les ressources peuvent être créées avec n’importe quel état initial spécifié par l’utilisateur (valide pour la description de la ressource), avec les exceptions suivantes :

-   Le chargement des segments de mémoire doit commencer dans la lecture générique état de la ressource State D3D12 \_ \_ \_ \_ qui est une combinaison or au niveau du bit :
    -   \_ \_ Sommet de l’état de la ressource D3D12 \_ \_ et \_ \_ mémoire tampon constante
    -   \_ \_ \_ Mémoire tampon d’index d’état de ressource D3D12 \_
    -   SOURCE de copie de l' \_ \_ État de la ressource D3D12 \_ \_
    -   \_Ressource du \_ \_ \_ \_ nuanceur de non-pixel \_ de l’état de ressource D3D12
    -   \_Ressource de \_ \_ \_ nuanceur de pixels d’état de ressource D3D12 \_
    -   \_ \_ \_ Argument indirect de l’état de la ressource D3D12 \_
-   Les segments de mémoire readback doivent démarrer dans l’état de la copie de destination de l’état de la \_ ressource D3D12 \_ \_ \_ .
-   Les mémoires tampons d’annulation de chaîne de permutation commencent automatiquement par l' \_ État commun de l’état de ressource D3D12 \_ \_ .

Pour qu’un segment de mémoire puisse être la cible d’une opération de copie GPU, le tas doit d’abord être transféré à l’état de copie de destination de l’état de la \_ ressource D3D12 \_ \_ \_ . Toutefois, les ressources créées sur les tas de chargement doivent commencer dans et ne peuvent pas être modifiées à partir de l' \_ État de lecture générique puisque seul l’UC est en cours d’écriture. À l’inverse, les ressources validées créées dans des segments de mémoire READBACK doivent démarrer dans et ne peuvent pas changer à partir de l’état de copie de \_ destination.

### <a name="readwrite-resource-state-restrictions"></a>Restrictions relatives à l’état des ressources en lecture/écriture

Les bits d’utilisation de l’état des ressources qui sont utilisés pour décrire un état de ressource sont divisés en États en lecture seule et en lecture/écriture. La rubrique de référence pour [**les \_ \_ États de ressource D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indique le niveau d’accès en lecture/écriture pour chaque bit de l’énumération.

Au maximum, un seul bit de lecture/écriture peut être défini pour n’importe quelle ressource. Si un bit d’écriture est défini, aucun bit en lecture seule ne peut être défini pour cette ressource. Si aucun bit d’écriture n’est défini, vous pouvez définir n’importe quel nombre de bits de lecture.

### <a name="resource-states-for-presenting-back-buffers"></a>États des ressources pour la présentation des mémoires tampons d’arrière-plan

Avant qu’une mémoire tampon d’arrière-plan ne soit présentée, elle doit être dans l' \_ État commun de l’état de ressource D3D12 \_ \_ . Notez que l’état de ressource D3D12 de l’état \_ \_ de ressource \_ présent est un synonyme de l' \_ État de ressource D3D12 \_ \_ commun et qu’ils ont tous les deux la valeur 0. Si [**IDXGISwapChain ::P renvoyée**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (ou [**IDXGISwapChain1 ::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) est appelé sur une ressource qui n’est pas actuellement dans cet État, un avertissement de couche de débogage est émis.

### <a name="discarding-resources"></a>Rejet des ressources

Toutes les sous-ressources d’une ressource doivent se trouver dans l’état de la cible de rendu \_ , ou en \_ lecture seule, pour les cibles de rendu/les ressources de stencil de profondeur, lorsque [**ID3D12GraphicsCommandList ::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) est appelée.

## <a name="implicit-state-transitions"></a>Transitions d’État implicites

Les ressources peuvent uniquement être « promues » en dehors de l' \_ État de ressource D3D12 \_ \_ . De même, les ressources ne sont que de la « atténuation » de l' \_ État de ressource D3D12 \_ \_ .

### <a name="common-state-promotion"></a>Promotion de l’État commun

Toutes les ressources de mémoire tampon et les textures avec l' \_ indicateur de ressource D3D12 \_ autoriser l' \_ \_ \_ ensemble d’indicateurs d’accès simultané sont promues implicitement de \_ l’état de ressource D3D12 \_ \_ commun à l’état approprié lors du premier accès GPU, y compris la \_ lecture générique pour couvrir tout scénario de lecture. Toutes les ressources de l’État commun sont accessibles comme si elles étaient dans un État unique avec

<dl> 1 indicateur d’écriture, ou  
1 ou plusieurs indicateurs de lecture  
</dl>

Les ressources peuvent être promues à partir de l’État commun en fonction du tableau suivant :



| Indicateur d’État                    | Mémoires tampons et Simultaneous-Access textures                             | Textures à accès non simultané                                     |
|-------------------------------|----------------------------------------------|--------------------------------------|
| \_mémoire tampon de vertex et \_ constante \_ | Oui                                          | Non                                   |
| \_mémoire tampon d’index                 | Oui                                          | Non                                   |
| cible de rendu \_                | Oui                                          | Non                                   |
| accès non ordonné \_             | Oui                                          | Non                                   |
| écriture de profondeur \_                  | º<sup>\*</sup>                              | Non                                   |
| lecture de profondeur \_                   | º<sup>\*</sup>                              | Non                                   |
| \_ressource de \_ nuanceur non pixel \_  | Oui                                          | Oui                                  |
| \_ressource de nuanceur de pixels \_       | Oui                                          | Oui                                  |
| DIFFUSER \_ en continu                   | Oui                                          | Non                                   |
| \_argument indirect            | Oui                                          | Non                                   |
| COPIER la \_ dest.                    | Oui                                          | Oui                                  |
| COPIER la \_ source                  | Oui                                          | Oui                                  |
| RÉSOUDRE la \_ dest.                 | Oui                                          | Non                                   |
| RÉSOUDRE la \_ source               | Oui                                          | Non                                   |
| PRÉDICATION                   | Oui                                          | Non                                   |



 

<sup>\*</sup>Les ressources de stencil de profondeur doivent être des textures d’accès non simultanées et ne peuvent donc jamais être promues implicitement.

Quand cet accès se produit, la promotion agit comme une barrière de ressources implicite. Pour les accès suivants, les barrières des ressources sont nécessaires pour modifier l’état des ressources si nécessaire. Notez que la promotion d’un état de lecture promu en un état de lecture multiple est valide, mais ce n’est pas le cas pour les États d’écriture.  
Par exemple, si une ressource de l’État commun est promue en \_ ressource de nuanceur \_ de pixels dans un appel de dessin, elle peut toujours être promue en NON_PIXEL \_ ressource de nuanceur \_ | \_ \_ Ressource de nuanceur de pixels dans un autre appel de dessin. Toutefois, s’il est utilisé dans une opération d’écriture, telle qu’une destination de copie, barrière de transition d’état de ressource par rapport aux États de lecture promus combinés, ici NON_PIXEL \_ ressource de nuanceur \_ | La \_ \_ ressource de nuanceur de pixels, pour copier la \_ destination, est nécessaire.  
De même, si elle est promue de commun à copie de \_ destination, un cloisonnement est toujours nécessaire pour effectuer la transition de la destination de copie \_ à la cible de rendu \_ .

Notez que la promotion de l’État commun est « gratuite » en ce qu’il n’est pas nécessaire que le GPU exécute des attentes de synchronisation. La promotion représente le fait que les ressources dans l’État commun ne doivent pas nécessiter d’autres opérations GPU ou un suivi des pilotes pour prendre en charge certains accès.

### <a name="state-decay-to-common"></a>État d’atténuation commun

Le retournement de la promotion de l’État commun est la désintégration de l' \_ État de ressource D3D12 \_ \_ courant. Les ressources qui répondent à certaines exigences sont considérées comme sans État et retournent efficacement à l’État commun lorsque l’exécution d’une opération [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) est terminée. La désintégration n’a pas lieu entre les listes de commandes exécutées ensemble dans le même appel **ExecuteCommandLists** .

Les ressources suivantes s’atténueront quand une opération [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) sera effectuée sur le GPU :

-   Ressources faisant l’objet d’un accès sur une file d’attente de copie, *ou*
-   Des ressources de mémoire tampon sur n’importe quel type de file d’attente, *ou*
-   Les ressources de texture sur tout type de file d’attente qui ont l' \_ indicateur de ressource D3D12 autoriser l’ensemble d’indicateurs d' \_ \_ \_ \_ accès simultané, *ou*
-   Toute ressource promue implicitement en état lecture seule.

À l’instar de la promotion de l’État commun, la désintégration est gratuite dans le fait qu’aucune synchronisation supplémentaire n’est nécessaire. La combinaison de la promotion et de la dégradation de l’État commun permet d’éliminer de nombreuses transitions [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) inutiles. Dans certains cas, cela peut apporter des améliorations significatives en matière de performances.

Les mémoires tampons et les ressources de Simultaneous-Access sont réaffectées à l’État commun, qu’elles aient été explicitement migrées à l’aide de barrières de ressources ou qu’elles soient promues implicitement.

### <a name="performance-implications"></a>Impact sur les performances

Lors de l’enregistrement de transitions [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explicites sur des ressources dans l’État commun, il est correct d’utiliser l’état de \_ ressource D3D12 \_ \_ commun ou tout état pouvant être promu en tant que valeur de la *forêt* dans la structure de barrière de transition de \_ ressource D3D12 \_ \_ . Cela permet une gestion d’État traditionnelle qui ignore la désintégration automatique des mémoires tampons et des textures à accès simultané. Cela peut cependant ne pas être souhaitable, car l’évitement des appels **ResourceBarrier** de transition avec les ressources connues comme étant dans l’État commun peut améliorer les performances de manière significative. Les barrières des ressources peuvent être onéreuses. Ils sont conçus pour forcer les vidages du cache, les modifications de la disposition de la mémoire et d’autres synchronisations qui peuvent ne pas être nécessaires pour les ressources qui sont déjà dans l’État commun. Une liste de commandes qui utilise une barrière de ressources d’un État non commun à un autre État non courant sur une ressource actuellement en état commun peut entraîner une surcharge importante.

Évitez également les transitions [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explicites vers l' \_ État de ressource D3D12 \_ \_ courant, sauf si cela est absolument nécessaire (par exemple, l’accès suivant se trouve dans une file d’attente de commandes de copie qui nécessite une ressource commençant dans l’État commun). Une transition excessive vers l’État commun peut ralentir considérablement les performances du GPU.

En résumé, essayez de vous appuyer sur la promotion et la désintégration de l’État commun chaque fois que sa sémantique vous permet de quitter sans émettre d’appels [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) .

## <a name="split-barriers"></a>Fractionner les barrières

Un cloisonnement de transition de ressource avec l’indicateur de barrière de ressources D3D12 de \_ \_ \_ \_ début \_ uniquement commence une barrière de fractionnement et le cloisonnement de transition est dit en attente. Alors que le cloisonnement est en attente, la ressource (Sub) ne peut pas être lue ou écrite par le GPU. La seule barrière de transition légale qui peut être appliquée à une ressource (Sub) avec un cloisonnement en attente est l’une avec les mêmes États *avant* et *après* et l’indicateur de barrière de la \_ ressource D3D12 \_ \_ \_ End \_ only, lequel entrave termine la transition en attente.

Les barrières fractionnées fournissent des indications au GPU qu’une ressource dans l’état *a* sera ensuite utilisée dans l’état *B* ultérieurement. Cela donne au GPU la possibilité d’optimiser la charge de travail de transition, ce qui peut réduire ou éliminer les blocages d’exécution. L’émission de la barrière de fin uniquement garantit que toutes les tâches de transition GPU sont terminées avant de passer à la commande suivante.

L’utilisation de cloisonnements peut contribuer à améliorer les performances, en particulier dans les scénarios impliquant plusieurs moteurs ou lorsque les ressources sont en cours de lecture/écriture dans une ou plusieurs listes de commandes.

## <a name="resource-barrier-example-scenario"></a>Exemple de scénario de cloisonnement de ressources

Les extraits de code suivants illustrent l’utilisation de la méthode [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) dans un exemple de Multi-Threading.

Création de la vue du stencil de profondeur, transition vers un état accessible en écriture.


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



Création de la vue de mémoire tampon de vertex, en la remplaçant d’un État commun à une destination, puis d’une destination à un état de lecture générique.


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



Création de la vue de la mémoire tampon d’index, première modification d’un État commun à une destination, puis d’une destination à un état de lecture générique.


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



Création de textures et de vues de ressources de nuanceur. La texture passe d’un État commun à une destination, puis d’une destination à une ressource de nuanceur de pixels.


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



Début d’un frame ; elle utilise non seulement [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) pour indiquer que la mémoire tampon de mise en mémoire tampon doit être utilisée comme cible de rendu, mais elle initialise également la ressource de frame (qui appelle **ResourceBarrier** sur la mémoire tampon du stencil de profondeur).


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



Fin d’un frame, indiquant que la mémoire tampon d’arrière-plan est maintenant utilisée.


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



L’initialisation d’une ressource Frame, appelée au début d’un frame, fait passer la mémoire tampon du stencil de profondeur à l’État inscriptible.


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



Les barrières sont échangées en milieu de trame, ce qui permet de faire passer le mappage des ombres de l’état accessible en lecture.


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



La méthode Finish est appelée lorsqu’une image est terminée, ce qui fait passer le mappage de l’ombre à un État commun.


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a>Exemple de promotion et d’atténuation de l’État commun

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a>Exemple de barrières divisées

L’exemple suivant montre comment utiliser une barrière Split pour réduire les blocages de pipeline. Le code qui suit n’utilise pas de barrières divisées :

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

Le code suivant utilise des barrières divisées :

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a>Rubriques connexes

[Didacticiels vidéo sur DirectX Advanced Learning : barrières des ressources et suivi de l’État](https://www.youtube.com/watch?v=nmB2XMasz2o)

[Synchronisation multi-moteur](./user-mode-heap-synchronization.md)

[Envoi de travail dans Direct3D 12](command-queues-and-command-lists.md)

[Examiner les barrières de l’état des ressources D3D12](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

