---
title: Opérations disponibles sur les ressources en mosaïque
description: Cette section répertorie les opérations que vous pouvez effectuer sur les ressources en mosaïque.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095357"
---
# <a name="operations-available-on-tiled-resources"></a>Opérations disponibles sur les ressources en mosaïque

Cette section répertorie les opérations que vous pouvez effectuer sur les ressources en mosaïque.

-   void [**ID3D11DeviceContext2 :: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) et [**ID3D11DeviceContext2 :: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) Operations : ces emplacements de mosaïques de points d’opérations dans une ressource en mosaïque aux emplacements dans les pools de mosaïques, ou à la valeur null, ou aux deux. Ces opérations peuvent mettre à jour un sous-ensemble disjoint des pointeurs de mosaïque.
-   \*Opérations Copy () et Update \* () : toutes les API qui peuvent copier des données vers et à partir d’une surface de pool par défaut (par exemple, [**ID3D11DeviceContext1 :: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) et [**ID3D11DeviceContext1 :: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) fonctionnent pour les ressources en mosaïque. La lecture des vignettes non mappées produit 0 et les écritures sur les vignettes non mappées sont supprimées.
-   [**ID3D11DeviceContext2 :: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) et [**ID3D11DeviceContext2 :: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) Operations : ces opérations existent pour copier des vignettes à 64 Ko de granularité vers et à partir de n’importe quelle ressource en mosaïque et une ressource de mémoire tampon dans une disposition de mémoire canonique. Le pilote d’affichage et le matériel effectuent la mémoire « swizzling » nécessaire pour la ressource en mosaïque.
-   Les liaisons de pipeline Direct3D et les créations/liaisons de vues qui fonctionnent sur des ressources non en mosaïque fonctionnent également sur des ressources en mosaïque.

Les contrôles de vignette sont disponibles dans les contextes immédiats ou différés (comme les mises à jour des ressources standard) et à l’exécution, à l’impact des accès ultérieurs aux vignettes (pas les opérations précédemment soumises).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de ressources en mosaïque](creating-tiled-resources.md)
</dt> </dl>

 

 




