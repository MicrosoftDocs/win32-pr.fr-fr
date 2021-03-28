---
title: Opérations disponibles sur les pools de vignettes
description: Cette section répertorie les opérations que vous pouvez effectuer sur les pools de mosaïques.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6c9ec58e6c9197f107f47cd7fe3513f43030c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199267"
---
# <a name="operations-available-on-tile-pools"></a><span data-ttu-id="97273-103">Opérations disponibles sur les pools de vignettes</span><span class="sxs-lookup"><span data-stu-id="97273-103">Operations available on tile pools</span></span>

<span data-ttu-id="97273-104">Cette section répertorie les opérations que vous pouvez effectuer sur les pools de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="97273-104">This section lists operations that you can perform on tile pools.</span></span>

-   <span data-ttu-id="97273-105">La durée de vie des pools de mosaïques fonctionne comme n’importe quelle autre ressource Direct3D, sauvegardée par le décompte de références, y compris dans ce cas le suivi des mappages à partir des ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="97273-105">The lifetime of tile pools works like any other Direct3D Resource, backed by reference counting, including in this case tracking of mappings from tiled resources.</span></span> <span data-ttu-id="97273-106">Lorsque l’application ne fait plus référence à un pool de mosaïques et que les mappages de vignettes à la mémoire ont disparu et que les accès à l’unité de traitement graphique (GPU) sont terminés, le système d’exploitation libère le pool de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="97273-106">When the application no longer references a tile pool and any tile mappings to the memory are gone and graphics processing unit (GPU) accesses completed, the operating system will deallocate the tile pool.</span></span>
-   <span data-ttu-id="97273-107">Les API liées au partage des surfaces et à la synchronisation fonctionnent pour les pools de mosaïques (mais pas directement sur les ressources en mosaïque).</span><span class="sxs-lookup"><span data-stu-id="97273-107">APIs related to surface sharing and synchronization work for tile pools (but not directly on tiled resources).</span></span> <span data-ttu-id="97273-108">Comme pour les pools de vignettes proposés, les commandes Direct3D qui accèdent à des ressources en mosaïque qui pointent vers un pool de mosaïques sont supprimées si le pool de mosaïques a été partagé et est actuellement acquis par un autre appareil et processus.</span><span class="sxs-lookup"><span data-stu-id="97273-108">Similar to the behavior for offered tile pools, Direct3D commands that access tiled resources that point to a tile pool are dropped if the tile pool has been shared and is currently acquired by another device and process.</span></span>
-   <span data-ttu-id="97273-109">Opération [**ID3D11DeviceContext2 :: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)</span><span class="sxs-lookup"><span data-stu-id="97273-109">[**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation</span></span>
-   <span data-ttu-id="97273-110">[**IDXGIDevice2 :: OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) et [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) Operations : ces API pour générer temporairement de la mémoire sur le système opèrent sur l’ensemble du pool de mosaïques (et ne sont pas disponibles pour les ressources en mosaïque individuelles).</span><span class="sxs-lookup"><span data-stu-id="97273-110">[**IDXGIDevice2::OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) and [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) operations - These APIs for yielding memory temporarily to the system operate on the entire tile pool (and aren't available for individual tiled resources).</span></span> <span data-ttu-id="97273-111">Si une ressource en mosaïque pointe vers une vignette dans un pool de mosaïques proposé, la ressource en mosaïque se comporte comme si elle était proposée (par exemple, le runtime supprime les commandes qui la référencent).</span><span class="sxs-lookup"><span data-stu-id="97273-111">If a tiled resource points to a tile in an offered tile pool, the tiled resource behaves as if it is offered (for example, the runtime drops commands that reference it).</span></span>

<span data-ttu-id="97273-112">Les données ne peuvent pas être copiées directement vers et à partir de la mémoire du pool de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="97273-112">Data can't be copied to and from tile pool memory directly.</span></span> <span data-ttu-id="97273-113">Les accès à la mémoire sont toujours effectués via des ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="97273-113">Accesses to the memory are always done through tiled resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97273-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97273-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97273-115">Création de ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="97273-115">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 