---
title: Portage de Direct3D 11 vers Direct3D 12
description: Cette section fournit des conseils sur le portage d’un moteur graphique Direct3D 11 personnalisé vers Direct3D 12.
ms.assetid: 9EB4AC6B-AFDD-4673-8EB3-54272C151784
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ccf4a0bd10032d94ecaf4a88cc442f3a7ad516
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012928"
---
# <a name="porting-from-direct3d-11-to-direct3d-12"></a>Portage de Direct3D 11 vers Direct3D 12

Cette section fournit des conseils sur le portage d’un moteur graphique Direct3D 11 personnalisé vers Direct3D 12.

-   [Création de l’appareil](#device-creation)
-   [Ressources validées](#committed-resources)
-   [Ressources réservées](#reserved-resources)
-   [Téléchargement de données](#uploading-data)
-   [Nuanceurs et objets nuanceur](#shaders-and-shader-objects)
-   [Envoi du travail au GPU](#submitting-work-to-the-gpu)
-   [Synchronisation UC/GPU](#cpugpu-synchronization)
-   [Liaison de ressource](#resource-binding)
-   [État de la ressource](#resource-state)
-   [Chaînes d’échange](#swapchains)
-   [Correction du rendu des fonctions](#fixed-function-rendering)
-   [Les chances et les extrémités](#odds-and-ends)
-   [Rubriques connexes](#related-topics)

## <a name="device-creation"></a>Création de l’appareil

Direct3D 11 et Direct3D 12 partagent un modèle de création d’appareil similaire. Les pilotes Direct3D 12 existants sont tous **D3D_FEATURE_LEVEL_11_0** ou plus, vous pouvez donc ignorer les anciens niveaux de fonctionnalités et les limitations associées.

Gardez également à l’esprit qu’avec Direct3D 12, vous devez énumérer explicitement les informations de l’appareil à l’aide des interfaces DXGI. Dans Direct3D 11, vous pouviez *chaîner* à l’appareil dxgi à partir de l’appareil Direct3D, ce qui n’est pas pris en charge pour Direct3D 12.

La création d’un périphérique logiciel WARP sur Direct3D 12 s’effectue en fournissant un adaptateur explicite obtenu à partir de **IDXGIFactory4 :: EnumWarpAdapter**. Le périphérique WARP pour Direct3D 12 est disponible uniquement sur les systèmes sur lesquels la fonctionnalité facultative des **Outils Graphics** est activée.

> [!NOTE]
> Il n’y a pas d’équivalent à **D3D11CreateDeviceAndSwapChain**. Même avec Direct3D 11, nous déconseillons l’utilisation de cette fonction, car il est souvent préférable de créer l’appareil et utilise permutation dans des étapes distinctes.

## <a name="committed-resources"></a>Ressources validées

Les objets créés avec les interfaces suivantes dans Direct3D 11, traduisent en ce qui est appelé « ressources validées » dans Direct3D 12. Une ressource validée est une ressource qui a à la fois un espace d’adressage virtuel et des pages physiques associés. il s’agit d’un concept du modèle de mémoire Microsoft Windows Device Driver 2 (WDD2), sur lequel Direct3D 12 est basé.

Ressources Direct3D 11 :

-   [**ID3D11Resource**](/windows/win32/api/d3d11/nn-d3d11-id3d11resource)
-   [**ID3D11Buffer**](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) et [ **ID3D11Device :: CreateBuffer**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createbuffer)
-   [**ID3D11Texture1D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture1d) et [ **ID3D11Device : CreateTexture1D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture1d)
-   [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) et [ **ID3D11Device :: CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d)
-   [**ID3D11Texture3D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture3d) et [ **ID3D11Device :: CreateTexture3D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture3d)

Dans Direct3D 12, ceux-ci sont tous représentés par [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) et [**ID3D12Device :: CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

## <a name="reserved-resources"></a>Ressources réservées

Les ressources réservées sont des ressources où seul l’espace d’adressage virtuel a été alloué, la mémoire physique n’est pas allouée jusqu’à l’appel de [**ID3D12Device :: CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap). Il s’agit essentiellement du même concept que les ressources en mosaïque dans Direct3D 11.

Les indicateurs ([**\_ \_ \_ indicateur divers de ressource d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)) utilisés dans Direct3D 11 pour configurer des ressources en mosaïque, puis les mapper à la mémoire physique.

-   \_Ressource d3d11 \_ en \_ mosaïque diverse
-   \_Pool de \_ \_ mosaïques \_ diverses de la ressource d3d11

## <a name="uploading-data"></a>Téléchargement de données

Dans Direct3D 11, il existe une seule chronologie (les appels suivant une séquence, tels que les données initialisées avec [**des \_ \_ données**](/windows/win32/api/d3d11/ns-d3d11-d3d11_subresource_data)de sous-ressource d3d11, puis un appel est effectué à [**ID3D11DeviceContext :: UpdateSubresource**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), puis un appel à [**ID3D11DeviceContext :: Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)). Le nombre de copies créées des données n’est pas évident pour un développeur Direct3D 11.

Dans Direct3D 12, il existe deux chronologies, la chronologie GPU (configurée par les appels à [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)et [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) à partir de la mémoire mappée) et la chronologie de l’UC (déterminée par les appels à [**Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)). Les fonctions d’assistance sont fournies (dans le fichier d3dx12. h), appelées [**updatesubresources par**](updatesubresources1.md) qui utilisent une chronologie partagée. Il existe plusieurs variantes de cette fonction d’assistance, une qui utilise [**ID3D12Device :: GetCopyableFootprints**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints), une autre qui utilise un mécanisme d’allocation de tas et une autre qui utilise un mécanisme d’allocation de pile. Ces fonctions d’assistance copient les ressources dans le GPU et le processeur, via une zone intermédiaire de la mémoire.

En général, le GPU et le processeur disposent chacun de leur propre copie d’une ressource liée à leur propre chronologie. L’approche de la chronologie partagée gère de la même manière deux copies.

## <a name="shaders-and-shader-objects"></a>Nuanceurs et objets nuanceur

Dans Direct3D 11, il y a beaucoup de création d’objets de nuanceur et d’État, et de définir l’état de ces objets, à l’aide des méthodes de création [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) et des méthodes Set [**ID3D11DeviceContext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) . En général, un grand nombre d’appels sont passés à ces méthodes, qui sont ensuite combinés au moment du traçage par le pilote pour définir l’état de pipeline approprié.

Dans Direct3D 12, ce paramètre de l’état du pipeline a été combiné en un objet unique ([**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) pour un moteur de calcul, et [**CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) pour un moteur graphique), qui est ensuite attaché à une liste de commandes avant l’appel de dessin avec un appel à [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Ces appels remplacent tous les appels individuels pour définir les nuanceurs, la disposition d’entrée, l’état de fusion, l’état du rastériseur, l’état du stencil de profondeur, etc., dans Direct3D 11

- Méthodes de l’appareil 11 : ``CreateInputLayout`` , ``CreateXShader`` , ``CreateDepthStencilState`` , andd ``CreateRasterizerState`` .
- Méthodes du contexte de périphérique 11 :  ``IASetInputLayout`` , ``xxSetShader`` ,, ``OMSetBlendState`` ``OMSetDepthStencilState`` et ``RSSetState`` .

Alors que Direct3D 12 peut prendre en charge des objets BLOB de nuanceurs compilés plus anciens, les nuanceurs doivent être générés à l’aide du nuanceur 5,1 avec les API FXC/D3DCompile, ou à l’aide du nuanceur modèle 6 à l’aide du compilateur DXC DXIL. Vous devez valider la prise en charge de Shader Model 6 avec [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) et **D3D12_FEATURE_SHADER_MODEL**.

## <a name="submitting-work-to-the-gpu"></a>Envoi du travail au GPU

dans Direct3D 11, il n’y a que peu de contrôle sur la façon dont le travail est soumis, il est en grande partie géré par le pilote, bien que certains contrôles soient activés via les appels [**ID3D11DeviceContext :: Flush**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-flush) et [**IDXGISwapChain1 ::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) .

Dans Direct3D 12, l’envoi de travail est très explicite et contrôlé par l’application. La construction principale pour l’envoi de travail est le [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist), qui est utilisé pour enregistrer toutes les commandes des applications (et est assez similaire au concept du contexte différé ID3D11). Le magasin de stockage pour une liste de commandes est fourni par [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator), ce qui permet à l’application de gérer l’utilisation de la mémoire de la liste de commandes en exposant réellement la mémoire que le pilote Direct3D 12 va utiliser pour stocker la liste de commandes.

Enfin, [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) est une file d’attente premier sorti, qui stocke l’ordre correct des listes de commandes à envoyer au GPU. La liste de commandes suivante de la file d’attente est envoyée par le pilote uniquement quand une liste de commandes a terminé l’exécution sur le GPU.

Dans Direct3D 11, il n’existe pas de concept explicite de file d’attente de commandes. Dans le cadre de l’installation courante de Direct3D 12, la liste des commandes **D3D12_COMMAND_LIST_TYPE_DIRECT** actuellement ouvertes pour le frame actuel peut être considérée comme analogue au contexte immédiat de Direct3D 11. Cela fournit la plupart des fonctions.


| D3D11DeviceContext                  | Liste ID3D12GraphicsCommand     |
|-------------------------------------|--------------------------------|
| ClearDepthStencilView               | ClearDepthStencilView          |
| ClearRenderTargetView               | ClearRenderTargetView          |
| ClearUnorderedAccess*               | ClearUnorderedAccess*          |
| Dessin, DrawInstanced                 | DrawInstanced                  |
| DrawIndexed, DrawIndexedInstanced   | DrawIndexedInstanced           |
| Dispatch                            | Dispatch                       |
| IASetInputLayout, xxSetShader, etc. | SetPipelineState               |
| OMSetBlendState                     | OMSetBlendFactor               |
| OMSetDepthStencilState              | OMSetStencilRef                |
| OMSetRenderTargets                  | OMSetRenderTargets             |
| RSSetViewports                      | RSSetViewports                 |
| RSSetScissorRects                   | RSSetScissorRects              |
| IASetPrimitiveTopology              | IASetPrimitiveTopology         |
| IASetVertexBuffers                  | IASetVertexBuffers             |
| IASetIndexBuffer                    | IASetIndexBuffer               |
| ResolveSubresource                  | ResolveSubresource             |
| CopySubresourceRegion               | CopyBufferRegion               |
| UpdateSubresource                   | CopyTextureRegion              |
| CopyResource                        | CopyResource                   |

> [!NOTE]
> Une liste de commandes créée avec **D3D12_COMMAND_LIST_TYPE_BUNDLE** est semblable dans un contexte différé. Direct3D 12 prend également en charge le abiilty pour accéder à certaines fonctionnalités d’un *contexte immédiat* , de façon simultanée au rendu via **D3D12_COMMAND_LIST_TYPE_COPY** et **D3D12_COMMAND_LIST_TYPE_COMPUTE** les types de listes de commandes.

## <a name="cpugpu-synchronization"></a>Synchronisation UC/GPU

La synchronisation de l’UC/GPU de Direct3D 11 était largement automatique et il n’était pas nécessaire que l’application conserve l’état de la mémoire physique.

dans Direct3D 12, l’application doit gérer les deux chronologies (UC et GPU) de manière explicite. Cela implique que les informations doivent être conservées, par l’application, sur les ressources requises par le GPU et sur la durée. Cela signifie également que l’application est chargée de s’assurer que le contenu des ressources (ressources validées, tas, allocateurs de commandes, par exemple) ne change pas tant que le GPU n’a pas fini de les utiliser.

L’objet principal pour la synchronisation des chronologies est l’objet [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) . L’opération des délimitations est relativement simple, elle permet au GPU de signaler quand il a terminé une tâche. Le GPU et le processeur peuvent tous les deux signaler et peuvent attendre les limites.

En général, l’approche est que lors de l’envoi d’une liste de commandes pour exécution, un signal de clôture est transmis par le GPU à la fin de l’opération (quand il a terminé la lecture des données), ce qui permet au processeur de réutiliser ou de détruire les ressources.

Dans Direct3D 11, l’indicateur [**ID3D11DeviceContext :: Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map) indicateur d3d11 \_ \_ Write \_ ignore fondamentalement traité chaque ressource comme une fourniture infinie de mémoire à laquelle l’application pourrait écrire (processus appelé « changement de nom »). Dans Direct3D 12, le processus est explicite : la mémoire supplémentaire doit être allouée et les délimiteurs doivent être utilisés pour synchroniser les opérations. Les mémoires tampons en anneau (comprenant des mémoires tampons volumineuses) peuvent être une bonne technique pour cela, reportez-vous au scénario de mémoire tampon en anneau dans [gestion des ressources basée sur](fence-based-resource-management.md)les délimitations.

![utilisation d’une mémoire tampon en anneau](images/ring-buffer-1.png)

## <a name="resource-binding"></a>Liaison de ressource

Les vues dans Direct3D 11 (vues des ressources de nuanceur, vues de cible de rendu, etc.) ont été en grande partie remplacées dans Direct3D 12 par le concept de descripteur. Les méthodes de création existent toujours dans Direct3D 12 (comme [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview) et [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)), qui sont appelées après la création du tas de descripteur, pour écrire les données dans le tas. La liaison dans Direct3D 12 est maintenant gérée par les handles de descripteur décrits dans une signature racine et envoyée à l’aide des méthodes [**SetGraphicsRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) ou [**SetComputeRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) .

Les signatures racines détaillent les mappages entre le numéro d’emplacement de signature racine et les tables de descripteurs, où la table de descripteurs peut contenir des références aux ressources disponibles pour les nuanceurs vertex, les nuanceurs de pixels et les autres nuanceurs, tels que les mémoires tampons constantes, les vues de ressources de nuanceur et les échantillonneurs. Cette flexibilité déconnecte l’espace de registres HLSL de l’espace de liaison de l’API dans Direct3D 12, contrairement à Direct3D 11, où il existe un mappage un-à-un entre eux.

L’une des implications de ce système est que l’application est chargée de renommer les tables de descripteurs, ce qui permet aux développeurs de comprendre le coût des performances de la modification d’un seul descripteur par appel de dessin.

Une nouvelle fonctionnalité de Direct3D 12 est qu’une application peut contrôler quels descripteurs sont partagés entre les différentes étapes du nuanceur. Dans Direct3D 11, les ressources telles que UAVs sont partagées entre toutes les étapes du nuanceur. En activant la désactivation des descripteurs pour certaines étapes de nuanceur, les registres utilisés par les descripteurs qui ont été désactivés sont disponibles pour être utilisés par les descripteurs activés pour une étape de nuanceur particulière.

Le tableau suivant présente un exemple de signature racine.



| Emplacement du paramètre racine | Entrée de table de descripteur         |
|---------------------|--------------------------------|
| 0                   | Plage du descripteur VS B0-B13     |
| 1                   | Plage du descripteur VS T0-T127    |
| 2                   | Plage du descripteur VS S0-S16     |
| 3                   | Plage du descripteur PS B0-B13     |
| ...                 |                                |
| 14                  | Plage de descripteurs DS S0-16      |
| 15                  | Plage de descripteurs partagés U0-U63 |



 

## <a name="resource-state"></a>État de la ressource

Dans Direct3D 11, l’état des ressources n’est pas géré par l’application, mais par le pilote.

Dans Direct3D 12, le maintien de l’état de la ressource devient la responsabilité de l’application, pour activer le parallélisme complet dans l’enregistrement des listes de commandes : l’application doit gérer les chronologies d’enregistrement pour les listes de commandes (qui peuvent être effectuées en parallèle) et les chronologies d’exécution qui doivent être séquentielles.

Une transition d’état de ressource est gérée par la méthode [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) . En premier lieu, l’application doit informer le pilote lorsque l’utilisation des ressources change. Par exemple, si une ressource est utilisée en tant que cible de rendu, puis qu’elle doit être utilisée comme entrée d’un nuanceur de sommets lors de l’appel de dessin suivant, cela peut nécessiter un léger blocage dans l’opération GPU pour terminer l’opération de la cible de rendu avant de gérer le nuanceur de sommets.

Ce système permet une synchronisation fine des grains (les cabinets GPU) du pipeline graphique, ainsi que des vidages du cache et éventuellement des modifications de la disposition de la mémoire (par exemple, affichage de la cible de rendu sur la décompression de la vue du stencil de profondeur).

C’est ce qu’on appelle un cloisonnement de transition. Il existe d’autres types de barrières, dans Direct3D 11, [**ID3D11DeviceContext2 :: TiledResourceBarrier**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) a activé la même mémoire physique que celle utilisée par deux ressources en mosaïque différentes. Dans Direct3D 12, on parle de « barrière d’alias ». Les barrières d’alias peuvent être utilisées pour les ressources en mosaïque et placées dans Direct3D 12. En outre, il existe la barrière UAV. Dans Direct3D 11, toutes les opérations de distribution et de dessin UAV doivent être sérialisées, même si ces opérations peuvent être canalisées ou fonctionner en parallèle. Pour Direct3D 12, cette restriction est supprimée par l’ajout d’une barrière UAV. Une barrière UAV garantit que les opérations UAV sont séquentielles. ainsi, si une deuxième opération requiert que la première soit terminée, la seconde est forcée à attendre par l’ajout du cloisonnement. L’opération par défaut pour UAVs est simplement que les opérations se poursuivent aussi rapidement que possible.

Il existe clairement des gains de performances si une charge de travail peut être parallélisée.

## <a name="swapchains"></a>Chaînes d’échange

La chaîne de permutation DXGI est la base des chaînes de permutation dans Direct3D 11 et 12. Il existe quelques différences mineures, dans Direct3D 11, les trois types de chaînes de permutation sont séquentiel, ignorer et retourner \_ séquentiellement. Pour Direct3D 12, il n’existe que deux types : retournement \_ séquentiel et Flip \_ ignore. Comme indiqué ci-dessus, vous devez créer explicitement votre utilise permutation via **IDXGIFactory4**, ou une version ultérieure, et utiliser la même interface pour toute énumération d’adaptateur.

Dans Direct3D 11, il existe une rotation automatique de la mémoire tampon d’arrière-plan : seule une vue de cible de rendu est nécessaire pour la mémoire tampon d’arrière-plan 0. Dans la rotation de la mémoire tampon Direct3D 12 est explicite, il doit y avoir une vue de la cible de rendu pour chaque mémoire tampon d’arrière-plan. Utilisez la méthode [**IDXGISwapChain3 :: GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) pour sélectionner celle vers laquelle effectuer le rendu. Là encore, cette flexibilité supplémentaire permet une plus grande parallélisation.

> [!NOTE]
> Bien qu’il existe de nombreuses façons de configurer votre application, en général, les applications ont un **ID3D12CommandAllocator** par mémoire tampon de chaîne d’échange. Cela permet à l’application de passer à la création d’un ensemble de commandes pour le frame suivant pendant que le GPU restitue le précédent.

## <a name="fixed-function-rendering"></a>Correction du rendu des fonctions

Dans Direct3D 11, il existait quelques méthodes qui ont simplifié différentes opérations de niveau supérieur, telles que [**GenerateMips**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips) (création de chaînes MIP complètes) et [**DrawAuto**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto) (en utilisant la sortie de flux comme entrée de nuanceur sans autre entrée de l’application). Ces méthodes ne sont pas disponibles dans Direct3D 12, l’application doit gérer ces opérations en créant des nuanceurs pour les exécuter.

## <a name="odds-and-ends"></a>Les chances et les extrémités

Le tableau suivant présente un certain nombre de fonctionnalités qui sont similaires entre Direct3D 11 et 12, mais ne sont pas identiques.



| Direct3D 11                                                                            | Direct3D 12                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Query**](/windows/win32/api/d3d11/nn-d3d11-id3d11query)                                              | [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) permet de regrouper les requêtes, réduisant ainsi le coût.                                                                                                                                                                                                                                                                                                                                     |
| [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate)                                      | Le prédicat est désormais activé en faisant en sorte que les données soient dans une mémoire tampon entièrement transparente. L’objet [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate) de Direct3D 11 est remplacé par [**ID3D12Resource :: Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map), qui doit suivre un appel à [**ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) et une opération de synchronisation GPU à l’aide d’une barrière pour attendre que les données soient prêtes. Reportez-vous à [predicate](predication.md). |
| Compteur caché UAV/SO                                                                  | L’application est responsable de l’allocation et de la gestion des compteurs SO/UAV. Reportez-vous aux compteurs de [sortie Stream](stream-output-counters.md) et aux [compteurs UAV](uav-counters.md).                                                                                                                                                                                                                                                             |
| MinLOD dynamique des ressources (niveau de détail minimal)                                       | Cette valeur a été déplacée vers le descripteur SRV static MinLOD.                                                                                                                                                                                                                                                                                                                                                                                 |
| Dessin \* indirect/[**DispatchIndirect**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-dispatchindirect) | Les méthodes indirectes de dessin sont toutes fusionnées dans la méthode à une [**ExecuteIndirect**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) .                                                                                                                                                                                                                                                                                                        |
| Les formats DepthStencil sont entrelacés                                                   | Les formats DepthStencil sont planaires. Par exemple, un format de 24 bits de profondeur, 8 bits de stencil sont stockés au format 24/8/24/8... etc. dans Direct3D 11, mais en tant que 24/24/24... suivi de 8/8/8... dans Direct3D 12. Notez que chaque plan est sa propre sous-ressource dans D3D12 (reportez-vous aux sous- [ressources](subresources.md)).                                                                                                                    |
| [**ResizeTilePool**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)                   | Les ressources réservées peuvent être mappées à plusieurs tas. Lorsqu’un pool de mosaïques aurait été augmenté dans D3D11, un segment de mémoire supplémentaire peut être alloué dans D3D12 à la place.                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Didacticiels vidéo sur DirectX Advanced Learning : Guide de Portage DirectX 11 vers DirectX 12](https://www.youtube.com/watch?v=BV64mdOCgZo)
</dt> <dt>

[Comprendre Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Utilisation de Direct3D 11, Direct3D 10 et Direct2D](direct3d-12-interop.md)
</dt> </dl>
