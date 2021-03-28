---
title: Opérations disponibles sur les ressources en mosaïque
description: Cette section répertorie les opérations que vous pouvez effectuer sur les ressources en mosaïque.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029634"
---
# <a name="operations-available-on-tiled-resources"></a><span data-ttu-id="2b6aa-103">Opérations disponibles sur les ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b6aa-103">Operations available on tiled resources</span></span>

<span data-ttu-id="2b6aa-104">Cette section répertorie les opérations que vous pouvez effectuer sur les ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="2b6aa-104">This section lists operations that you can perform on tiled resources.</span></span>

-   <span data-ttu-id="2b6aa-105">void [**ID3D11DeviceContext2 :: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) et [**ID3D11DeviceContext2 :: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) Operations : ces emplacements de mosaïques de points d’opérations dans une ressource en mosaïque aux emplacements dans les pools de mosaïques, ou à la valeur null, ou aux deux.</span><span class="sxs-lookup"><span data-stu-id="2b6aa-105">void [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) and [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) operations - These operations point tile locations in a tiled resource to locations in tile pools, or to NULL, or to both.</span></span> <span data-ttu-id="2b6aa-106">Ces opérations peuvent mettre à jour un sous-ensemble disjoint des pointeurs de mosaïque.</span><span class="sxs-lookup"><span data-stu-id="2b6aa-106">These operations can update a disjoint subset of the tile pointers.</span></span>
-   <span data-ttu-id="2b6aa-107">\*Opérations Copy () et Update \* () : toutes les API qui peuvent copier des données vers et à partir d’une surface de pool par défaut (par exemple, [**ID3D11DeviceContext1 :: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) et [**ID3D11DeviceContext1 :: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) fonctionnent pour les ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="2b6aa-107">Copy\*() and Update\*() operations - All the APIs that can copy data to and from a default pool surface (for example, [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) and [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) work for tiled resources.</span></span> <span data-ttu-id="2b6aa-108">La lecture des vignettes non mappées produit 0 et les écritures sur les vignettes non mappées sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="2b6aa-108">Reading from unmapped tiles produces 0 and writes to unmapped tiles are dropped.</span></span>
-   <span data-ttu-id="2b6aa-109">[**ID3D11DeviceContext2 :: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) et [**ID3D11DeviceContext2 :: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) Operations : ces opérations existent pour copier des vignettes à 64 Ko de granularité vers et à partir de n’importe quelle ressource en mosaïque et une ressource de mémoire tampon dans une disposition de mémoire canonique.</span><span class="sxs-lookup"><span data-stu-id="2b6aa-109">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) operations - These operations exist for copying tiles at 64KB granularity to and from any tiled resource and a buffer resource in a canonical memory layout.</span></span> <span data-ttu-id="2b6aa-110">Le pilote d’affichage et le matériel effectuent la mémoire « swizzling » nécessaire pour la ressource en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="2b6aa-110">The display driver and hardware perform any memory "swizzling" necessary for the tiled resource.</span></span>
-   <span data-ttu-id="2b6aa-111">Les liaisons de pipeline Direct3D et les créations/liaisons de vues qui fonctionnent sur des ressources non en mosaïque fonctionnent également sur des ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="2b6aa-111">Direct3D pipeline bindings and view creations / bindings that would work on non-tiled resources work on tiled resources as well.</span></span>

<span data-ttu-id="2b6aa-112">Les contrôles de vignette sont disponibles dans les contextes immédiats ou différés (comme les mises à jour des ressources standard) et à l’exécution, à l’impact des accès ultérieurs aux vignettes (pas les opérations précédemment soumises).</span><span class="sxs-lookup"><span data-stu-id="2b6aa-112">Tile controls are available on immediate or deferred contexts (just like updates to typical resources) and upon execution impact subsequent accesses to the tiles (not previously submitted operations).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b6aa-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b6aa-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b6aa-114">Création de ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b6aa-114">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




