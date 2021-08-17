---
title: Opérations disponibles sur les pools de vignettes
description: Cette section répertorie les opérations que vous pouvez effectuer sur les pools de mosaïques.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c72e15ebe9a8fd2f6725451268d3d03fb7b181442907248d0db44860560aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098321"
---
# <a name="operations-available-on-tile-pools"></a>Opérations disponibles sur les pools de vignettes

Cette section répertorie les opérations que vous pouvez effectuer sur les pools de mosaïques.

-   La durée de vie des pools de mosaïques fonctionne comme n’importe quelle autre ressource Direct3D, sauvegardée par le décompte de références, y compris dans ce cas le suivi des mappages à partir des ressources en mosaïque. Lorsque l’application ne fait plus référence à un pool de mosaïques et que les mappages de vignettes à la mémoire ont disparu et que les accès à l’unité de traitement graphique (GPU) sont terminés, le système d’exploitation libère le pool de mosaïques.
-   Les API liées au partage des surfaces et à la synchronisation fonctionnent pour les pools de mosaïques (mais pas directement sur les ressources en mosaïque). Comme pour les pools de vignettes proposés, les commandes Direct3D qui accèdent à des ressources en mosaïque qui pointent vers un pool de mosaïques sont supprimées si le pool de mosaïques a été partagé et est actuellement acquis par un autre appareil et processus.
-   Opération [**ID3D11DeviceContext2 :: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**IDXGIDevice2 :: OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) et [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) Operations : ces API pour générer temporairement de la mémoire sur le système opèrent sur l’ensemble du pool de mosaïques (et ne sont pas disponibles pour les ressources en mosaïque individuelles). Si une ressource en mosaïque pointe vers une vignette dans un pool de mosaïques proposé, la ressource en mosaïque se comporte comme si elle était proposée (par exemple, le runtime supprime les commandes qui la référencent).

Les données ne peuvent pas être copiées directement vers et à partir de la mémoire du pool de mosaïques. Les accès à la mémoire sont toujours effectués via des ressources en mosaïque.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de ressources en mosaïque](creating-tiled-resources.md)
</dt> </dl>

 

 