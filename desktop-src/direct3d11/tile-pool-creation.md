---
title: Création d’un pool de vignettes
description: Un pool de mosaïques est créé par le biais de l’API ID3D11Device CreateBuffer en passant l' \_ \_ \_ indicateur de pool de mosaïques divers de la ressource d3d11 \_ dans le membre MiscFlags de la \_ structure DESC de mémoire tampon d3d11 \_ vers laquelle pointe le paramètre pDesc.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990589"
---
# <a name="tile-pool-creation"></a><span data-ttu-id="3e4a4-103">Création d’un pool de vignettes</span><span class="sxs-lookup"><span data-stu-id="3e4a4-103">Tile pool creation</span></span>

<span data-ttu-id="3e4a4-104">Un pool de mosaïques est créé via l’API [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) en passant l’indicateur de [**\_ \_ \_ \_ pool de mosaïques divers de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) dans le membre **MiscFlags** de  la structure [**\_ \_ desc de mémoire tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) vers laquelle pointe le paramètre pDesc.</span><span class="sxs-lookup"><span data-stu-id="3e4a4-104">A tile pool is created via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API by passing the [**D3D11\_RESOURCE\_MISC\_TILE\_POOL**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag in the **MiscFlags** member of the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure that the *pDesc* parameter points to.</span></span>

<span data-ttu-id="3e4a4-105">Les applications peuvent créer un ou plusieurs pools de mosaïques par appareil Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3e4a4-105">Applications can create one or more tile pools per Direct3D device.</span></span> <span data-ttu-id="3e4a4-106">La taille totale de chaque pool de mosaïques est limitée à la limite de taille des ressources de Direct3D 11, soit environ 1/4 de RAM de l’unité de traitement graphique (GPU).</span><span class="sxs-lookup"><span data-stu-id="3e4a4-106">The total size of each tile pool is restricted to Direct3D 11's resource size limit, which is roughly 1/4 of graphics processing unit (GPU) RAM.</span></span>

<span data-ttu-id="3e4a4-107">Un pool de mosaïques est constitué de 64 Ko, mais le système d’exploitation (pilote d’affichage) gère l’ensemble du pool comme une ou plusieurs allocations en arrière-plan : la répartition n’est pas visible pour les applications.</span><span class="sxs-lookup"><span data-stu-id="3e4a4-107">A tile pool is made of 64KB tiles, but the operating system (display driver) manages the entire pool as one or more allocations behind the scenes—the breakdown is not visible to applications.</span></span> <span data-ttu-id="3e4a4-108">Les ressources en mosaïque définissent le contenu en pointant sur les vignettes d’un pool de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="3e4a4-108">Tiled resources define content by pointing at tiles within a tile pool.</span></span> <span data-ttu-id="3e4a4-109">Le démappage d’une vignette à partir d’une ressource en mosaïque est effectué en pointant la vignette sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3e4a4-109">Unmapping a tile from a tiled resource is done by pointing the tile to **NULL**.</span></span> <span data-ttu-id="3e4a4-110">Ces vignettes non mappées ont des règles sur le comportement des lectures ou des écritures.</span><span class="sxs-lookup"><span data-stu-id="3e4a4-110">Such unmapped tiles have rules about the behavior of reads or writes.</span></span> <span data-ttu-id="3e4a4-111">Pour plus d’informations, consultez le [suivi des risques et les ressources de pool de mosaïques](hazard-tracking-versus-tile-pool-resources.md).</span><span class="sxs-lookup"><span data-stu-id="3e4a4-111">For info, see [Hazard tracking versus tile pool resources](hazard-tracking-versus-tile-pool-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e4a4-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e4a4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e4a4-113">Mappages dans un pool de vignettes</span><span class="sxs-lookup"><span data-stu-id="3e4a4-113">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




