---
title: Systèmes à plusieurs adaptateurs
description: Décrit la prise en charge dans Direct3D 12 pour les systèmes sur lesquels plusieurs adaptateurs sont installés, couvrant les scénarios dans lesquels votre application cible explicitement plusieurs adaptateurs GPU et les scénarios où les pilotes utilisent implicitement plusieurs adaptateurs GPU pour le compte de votre application.
ms.assetid: CC4C6594-D48F-40C1-93EE-9F98532BC038
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d7d3985c880c4d1732a96b98ac6d3c6579dab8e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012940"
---
# <a name="multi-adapter-systems"></a>Systèmes à plusieurs adaptateurs

Décrit la prise en charge dans Direct3D 12 pour les systèmes sur lesquels plusieurs adaptateurs sont installés, couvrant les scénarios dans lesquels votre application cible explicitement plusieurs adaptateurs GPU et les scénarios où les pilotes utilisent implicitement plusieurs adaptateurs GPU pour le compte de votre application.

## <a name="multi-adapter-overview"></a>Vue d’ensemble de plusieurs adaptateurs

Une carte GPU peut être n’importe quelle carte (Graphics ou Compute, discrète ou intégrée), de n’importe quel fabricant, qui prend en charge Direct3D 12.

Plusieurs adaptateurs sont référencés en tant que *nœuds*. Un certain nombre d’éléments, tels que les files d’attente, s’appliquent à chaque nœud. par conséquent, s’il y a deux nœuds, il y aura deux files d’attente 3D par défaut. D’autres éléments, tels que l’état du pipeline et les signatures de la racine et de la commande, peuvent faire référence à un ou plusieurs ou à l’ensemble des nœuds, comme indiqué dans le diagramme.

![les files d’attente s’appliquent à chaque carte graphique](images/multigpu.png)

## <a name="sharing-heaps-across-adapters"></a>Partage des segments de mémoire entre les adaptateurs

Consultez la rubrique [tas partagés](shared-heaps.md) .

## <a name="multi-adapter-apis-and-node-masks"></a>API à plusieurs adaptateurs et masques de nœud

Comme pour les API Direct3D précédentes, chaque ensemble de cartes liées est énuméré comme un objet [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) unique. Toutes les sorties attachées à un adaptateur dans le lien sont énumérées comme attachées à l’objet **IDXGIAdapter3** unique.

Votre application peut déterminer le nombre de cartes physiques associées à un appareil donné en appelant [**ID3D12Device :: GetNodeCount**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount).

De nombreuses API dans Direct3D 12 acceptent un *masque de nœud* (masque de bits), qui indique l’ensemble des nœuds auxquels l’appel d’API fait référence. Chaque nœud a un index de base zéro. Mais dans le masque de nœud, zéro se traduit par le bit 1 ; 1 est converti en bit 2 ; et ainsi de suite.

### <a name="single-nodes"></a>Nœuds uniques

Lors de l’appel des API (nœud unique) suivantes, votre application spécifie un nœud unique avec lequel l’appel d’API sera associé. La plupart du temps, cela est spécifié par un masque de nœud. Chaque bit du masque correspond à un nœud unique. Pour toutes les API décrites dans cette section, vous devez définir exactement un bit dans le masque de nœud.

-   [**D3D12 \_ \_ \_ Description de la file d’attente de commandes**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) : a un membre *NodeMask* .
-   [**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : crée une file d’attente à partir d’une structure de [**\_ \_ file d’attente \_ de commandes D3D12 DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .
-   [**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : prend un paramètre *nodeMask* .
-   [**D3D12 \_ \_ \_ Description du tas du descripteur**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) : a un membre *NodeMask* .
-   [**CreateDescriptorHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap) : crée un tas de descripteur à partir d’une structure [**\_ desc du \_ tas \_ du descripteur D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) .
-   [**D3D12 \_ \_ \_ Description du segment de mémoire de requête**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) : a un membre *NodeMask* .
-   [**CreateQueryHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap) : crée un segment de requête à partir d’une structure [**\_ desc du \_ tas \_ de requêtes D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) .

### <a name="multiple-nodes"></a>Nœuds multiples

Lors de l’appel des API (plusieurs nœuds) suivantes, votre application spécifie un ensemble de nœuds avec lesquels l’appel d’API sera associé. Vous spécifiez l’affinité de nœud comme masque de nœud, éventuellement avec plusieurs bits définis. Si votre application transmet 0 pour ce masque de bits, le pilote Direct3D 12 le convertit en masque de bits 1 (indiquant que l’objet est associé au nœud 0).

-   [**D3D12 \_ \_Niveau de \_ partage \_ entre nœuds**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier) : détermine la prise en charge du partage inter-nœuds.
-   [**D3D12 \_ \_ \_ \_ Options D3D12 données**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) de la fonctionnalité : structure référençant le [**\_ \_ niveau de \_ partage \_ entre nœuds D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier).
-   [**D3D12 \_ \_ \_ Architecture des données de fonctionnalités**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) : contient un membre *NodeIndex* .
-   [**D3D12 \_ DESC de l' \_ \_ état \_ du pipeline Graphics**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) : a un membre *NodeMask* .
-   [**CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) : crée un objet d’état de pipeline Graphics à partir d’une structure d' [**\_ \_ \_ état \_ de pipeline D3D12 Graphics**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) .
-   [**D3D12 \_ Description de \_ l' \_ état \_ du pipeline de calcul**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) : a un membre *NodeMask* .
-   [**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) : crée un objet d’état de pipeline de calcul à partir d’une structure d' [**\_ \_ \_ état \_ de pipeline de calcul D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) .
-   [**CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature): prend un paramètre *nodeMask* .
-   [**D3D12 \_ \_ \_ Description**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc)de la signature de commande : a un membre *NodeMask* .
-   [**CreateCommandSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) : crée un objet de signature de commande à partir d’une structure [**\_ desc de \_ signature \_ de commande D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc) .

### <a name="resource-creation-apis"></a>API de création de ressources

Les API suivantes masquent les masques de nœud.

-   [**D3D12 \_ \_Propriétés du tas**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) : contient à la fois des membres *CreationNodeMask* et *VisibleNodeMask* .
-   [**GetResourceAllocationInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) : a un paramètre *visibleMask* .
-   [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) : a un paramètre *nodeMask* .

Lors de la création d’une ressource réservée, aucun index ou masque de nœud n’est spécifié. La ressource réservée peut être mappée sur un segment de mémoire sur n’importe quel nœud (en suivant les règles de partage entre nœuds).

La méthode [**MakeResident**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident) fonctionne en interne avec les files d’attente d’adaptateur, il n’est pas nécessaire que votre application spécifie quoi que ce soit.

Lors de l’appel des API [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) suivantes, votre application n’a pas besoin de spécifier un ensemble de nœuds auxquels l’appel d’API sera associé, car l’appel d’API s’applique à tous les nœuds.

-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
-   [**GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
-   [**SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
-   [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
-   [**CreateSampler**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsampler)
-   [**CopyDescriptors**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
-   [**CopyDescriptorsSimple**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
-   [**CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
-   [**OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle) : avec une *barrière* comme paramètre. Avec une *ressource* ou un *segment de mémoire* en tant que paramètres, cette méthode n’accepte pas les nœuds en tant que paramètres, car les masques de nœud sont hérités des objets créés précédemment.
-   [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
-   [**CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)
-   [**CreateUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
-   [**CreateDepthStencilView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview)
-   [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)

## <a name="related-topics"></a>Rubriques connexes

[Guide de programmation de Direct3D 12](directx-12-programming-guide.md)