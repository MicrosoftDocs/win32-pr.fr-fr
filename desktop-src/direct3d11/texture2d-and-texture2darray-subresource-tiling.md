---
title: Restitution des sous-ressources Texture2D et Texture2DArray sous forme de mosaïque
description: Ces tableaux montrent comment les sous-ressources Texture2D et Texture2DArray sont présentées en mosaïque.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382283"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a><span data-ttu-id="1c7e5-103">Restitution des sous-ressources Texture2D et Texture2DArray sous forme de mosaïque</span><span class="sxs-lookup"><span data-stu-id="1c7e5-103">Texture2D and Texture2DArray subresource tiling</span></span>

<span data-ttu-id="1c7e5-104">Ces tableaux montrent comment les sous-ressources [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) et [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) sont présentées en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-104">These tables show how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources are tiled.</span></span> <span data-ttu-id="1c7e5-105">Les valeurs de ces tables ne comptent pas la fin de la compression MIP.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-105">The values in these tables don't count tail mip packing.</span></span>

<span data-ttu-id="1c7e5-106">Ce tableau montre comment les sous-ressources [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) et [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) avec un nombre d’échantillons de 1 sont en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-106">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with multisample counts of 1 are tiled.</span></span>



| <span data-ttu-id="1c7e5-107">Bits/pixel (1 échantillon/pixel)</span><span class="sxs-lookup"><span data-stu-id="1c7e5-107">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="1c7e5-108">Dimensions de la mosaïque (pixels, WxH)</span><span class="sxs-lookup"><span data-stu-id="1c7e5-108">Tile Dimensions (Pixels, WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="1c7e5-109">8</span><span class="sxs-lookup"><span data-stu-id="1c7e5-109">8</span></span>                           | <span data-ttu-id="1c7e5-110">256 x 256</span><span class="sxs-lookup"><span data-stu-id="1c7e5-110">256x256</span></span>                       |
| <span data-ttu-id="1c7e5-111">16</span><span class="sxs-lookup"><span data-stu-id="1c7e5-111">16</span></span>                          | <span data-ttu-id="1c7e5-112">256 x 128</span><span class="sxs-lookup"><span data-stu-id="1c7e5-112">256x128</span></span>                       |
| <span data-ttu-id="1c7e5-113">32</span><span class="sxs-lookup"><span data-stu-id="1c7e5-113">32</span></span>                          | <span data-ttu-id="1c7e5-114">128 x 128</span><span class="sxs-lookup"><span data-stu-id="1c7e5-114">128x128</span></span>                       |
| <span data-ttu-id="1c7e5-115">64</span><span class="sxs-lookup"><span data-stu-id="1c7e5-115">64</span></span>                          | <span data-ttu-id="1c7e5-116">128x64</span><span class="sxs-lookup"><span data-stu-id="1c7e5-116">128x64</span></span>                        |
| <span data-ttu-id="1c7e5-117">128</span><span class="sxs-lookup"><span data-stu-id="1c7e5-117">128</span></span>                         | <span data-ttu-id="1c7e5-118">64 x 64</span><span class="sxs-lookup"><span data-stu-id="1c7e5-118">64x64</span></span>                         |
| <span data-ttu-id="1c7e5-119">BC1, 4</span><span class="sxs-lookup"><span data-stu-id="1c7e5-119">BC1,4</span></span>                       | <span data-ttu-id="1c7e5-120">512x256</span><span class="sxs-lookup"><span data-stu-id="1c7e5-120">512x256</span></span>                       |
| <span data-ttu-id="1c7e5-121">BC2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="1c7e5-121">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="1c7e5-122">256 x 256</span><span class="sxs-lookup"><span data-stu-id="1c7e5-122">256x256</span></span>                       |



 

<span data-ttu-id="1c7e5-123">Les nombres de bits de format non pris en charge avec les ressources en mosaïque sont les formats 96 BPP, les formats vidéo, le \_ format dxgi \_ R1 \_ UNORM, le \_ format dxgi \_ R8G8 B8G8 UNORM et le \_ \_ format dxgi \_ \_ \_ \_ R8R8 G8B8 UNORM.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-123">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="1c7e5-124">Ce tableau montre comment les sous-ressources [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) et [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) avec différents nombres d’échantillons sont en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-124">This table shows how [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) subresources with various multisample counts are tiled.</span></span>



| <span data-ttu-id="1c7e5-125">Nombre d’échantillons</span><span class="sxs-lookup"><span data-stu-id="1c7e5-125">Multisample Count</span></span>           | <span data-ttu-id="1c7e5-126">Diviser les dimensions de mosaïque ci-dessus par (WxH)</span><span class="sxs-lookup"><span data-stu-id="1c7e5-126">Divide Tile Dimensions Above by (WxH)</span></span> |
|-----------------------------|-------------------------------|
| <span data-ttu-id="1c7e5-127">1</span><span class="sxs-lookup"><span data-stu-id="1c7e5-127">1</span></span>                           | <span data-ttu-id="1c7e5-128">individuelles</span><span class="sxs-lookup"><span data-stu-id="1c7e5-128">1x1</span></span>                           |
| <span data-ttu-id="1c7e5-129">2</span><span class="sxs-lookup"><span data-stu-id="1c7e5-129">2</span></span>                           | <span data-ttu-id="1c7e5-130">2 x 1</span><span class="sxs-lookup"><span data-stu-id="1c7e5-130">2x1</span></span>                           |
| <span data-ttu-id="1c7e5-131">4</span><span class="sxs-lookup"><span data-stu-id="1c7e5-131">4</span></span>                           | <span data-ttu-id="1c7e5-132">2x2</span><span class="sxs-lookup"><span data-stu-id="1c7e5-132">2x2</span></span>                           |
| <span data-ttu-id="1c7e5-133">8</span><span class="sxs-lookup"><span data-stu-id="1c7e5-133">8</span></span>                           | <span data-ttu-id="1c7e5-134">4x2</span><span class="sxs-lookup"><span data-stu-id="1c7e5-134">4x2</span></span>                           |
| <span data-ttu-id="1c7e5-135">16</span><span class="sxs-lookup"><span data-stu-id="1c7e5-135">16</span></span>                          | <span data-ttu-id="1c7e5-136">4x4</span><span class="sxs-lookup"><span data-stu-id="1c7e5-136">4x4</span></span>                           |



 

<span data-ttu-id="1c7e5-137">Seuls les nombres d’échantillons 1 et 4 sont requis (et autorisés) pour être pris en charge avec les ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-137">Only sample counts 1 and 4 are required (and allowed) to be supported with tiled resources.</span></span> <span data-ttu-id="1c7e5-138">Les ressources en mosaïque ne prennent pas en charge 2, 8 et 16, même si elles sont affichées.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-138">Tiled resources don't currently support 2, 8, and 16 even though they are shown.</span></span>

<span data-ttu-id="1c7e5-139">Les implémentations peuvent choisir de prendre en charge les modes d’échantillonnage 2, 8 et/ou 16 pour les ressources non en mosaïque, même si la ressource en mosaïque ne les prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-139">Implementations can choose to support 2, 8, and/or 16 sample multisample antialiasing (MSAA) mode for non-tiled resources even though tiled resource don't support them.</span></span>

<span data-ttu-id="1c7e5-140">Les ressources en mosaïque avec des nombres d’échantillons supérieurs à 1 ne peuvent pas utiliser les formats 128 BPP.</span><span class="sxs-lookup"><span data-stu-id="1c7e5-140">Tiled resources with sample counts larger than 1 can't use 128 bpp formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c7e5-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1c7e5-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c7e5-142">Mode de mosaïque de la zone d’une ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="1c7e5-142">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 