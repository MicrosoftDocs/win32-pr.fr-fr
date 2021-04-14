---
title: Restitution de la sous-ressource Texture3D sous forme de mosaïque
description: Ce tableau montre comment les sous-ressources Texture3D sont présentées en mosaïque.
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991025"
---
# <a name="texture3d-subresource-tiling"></a><span data-ttu-id="e8eb8-103">Restitution de la sous-ressource Texture3D sous forme de mosaïque</span><span class="sxs-lookup"><span data-stu-id="e8eb8-103">Texture3D subresource tiling</span></span>

<span data-ttu-id="e8eb8-104">Ce tableau montre comment les sous-ressources [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) sont présentées en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="e8eb8-104">This table shows how [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) subresources are tiled.</span></span> <span data-ttu-id="e8eb8-105">Les valeurs de cette table ne comptent pas la fin de la compression MIP.</span><span class="sxs-lookup"><span data-stu-id="e8eb8-105">The values in this table don't count tail mip packing.</span></span>

<span data-ttu-id="e8eb8-106">Cette table prend la mosaïque [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) et divise les dimensions x/y par 4 et ajoute 16 couches de profondeur.</span><span class="sxs-lookup"><span data-stu-id="e8eb8-106">This table takes the [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) tiling and divides the x/y dimensions by 4 each and adds 16 layers of depth.</span></span> <span data-ttu-id="e8eb8-107">Toutes les vignettes du premier plan (plan 2D des vignettes définissant les 16 premières couches de profondeur) apparaissent avant les plans suivants.</span><span class="sxs-lookup"><span data-stu-id="e8eb8-107">All the tiles for the first plane (2D plane of tiles defining the first 16 layers of depth) appear before the subsequent planes.</span></span>

> [!Note]  
> <span data-ttu-id="e8eb8-108">La prise en charge de [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) dans les ressources en mosaïque n’est pas exposée dans l’implémentation initiale des ressources en mosaïque, mais les formes de mosaïque souhaitées sont répertoriées ici, car le support peut être pris en compte dans une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e8eb8-108">[**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) support in tiled resources isn't exposed in the initial implementation of tiled resources, but the desired tile shapes are listed here because support might be consideration in a future release.</span></span>

 



| <span data-ttu-id="e8eb8-109">Bits/pixel (1 échantillon/pixel)</span><span class="sxs-lookup"><span data-stu-id="e8eb8-109">Bits/Pixel (1 sample/pixel)</span></span> | <span data-ttu-id="e8eb8-110">Dimensions de la mosaïque (pixels, WxHxD)</span><span class="sxs-lookup"><span data-stu-id="e8eb8-110">Tile Dimensions (Pixels, WxHxD)</span></span> |
|-----------------------------|---------------------------------|
| <span data-ttu-id="e8eb8-111">8</span><span class="sxs-lookup"><span data-stu-id="e8eb8-111">8</span></span>                           | <span data-ttu-id="e8eb8-112">64x32x32</span><span class="sxs-lookup"><span data-stu-id="e8eb8-112">64x32x32</span></span>                        |
| <span data-ttu-id="e8eb8-113">16</span><span class="sxs-lookup"><span data-stu-id="e8eb8-113">16</span></span>                          | <span data-ttu-id="e8eb8-114">32x32x32</span><span class="sxs-lookup"><span data-stu-id="e8eb8-114">32x32x32</span></span>                        |
| <span data-ttu-id="e8eb8-115">32</span><span class="sxs-lookup"><span data-stu-id="e8eb8-115">32</span></span>                          | <span data-ttu-id="e8eb8-116">32x32x16</span><span class="sxs-lookup"><span data-stu-id="e8eb8-116">32x32x16</span></span>                        |
| <span data-ttu-id="e8eb8-117">64</span><span class="sxs-lookup"><span data-stu-id="e8eb8-117">64</span></span>                          | <span data-ttu-id="e8eb8-118">32x16x16</span><span class="sxs-lookup"><span data-stu-id="e8eb8-118">32x16x16</span></span>                        |
| <span data-ttu-id="e8eb8-119">128</span><span class="sxs-lookup"><span data-stu-id="e8eb8-119">128</span></span>                         | <span data-ttu-id="e8eb8-120">16x16x16</span><span class="sxs-lookup"><span data-stu-id="e8eb8-120">16x16x16</span></span>                        |
| <span data-ttu-id="e8eb8-121">BC1, 4</span><span class="sxs-lookup"><span data-stu-id="e8eb8-121">BC1,4</span></span>                       | <span data-ttu-id="e8eb8-122">128x64x16</span><span class="sxs-lookup"><span data-stu-id="e8eb8-122">128x64x16</span></span>                       |
| <span data-ttu-id="e8eb8-123">BC2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="e8eb8-123">BC2,3,5,6,7</span></span>                 | <span data-ttu-id="e8eb8-124">64x64x16</span><span class="sxs-lookup"><span data-stu-id="e8eb8-124">64x64x16</span></span>                        |



 

<span data-ttu-id="e8eb8-125">Les nombres de bits de format non pris en charge avec les ressources en mosaïque sont les formats 96 BPP, les formats vidéo, le \_ format dxgi \_ R1 \_ UNORM, le \_ format dxgi \_ R8G8 B8G8 UNORM et le \_ \_ format dxgi \_ \_ \_ \_ R8R8 G8B8 UNORM.</span><span class="sxs-lookup"><span data-stu-id="e8eb8-125">Format bit counts not supported with tiled resources are 96 bpp formats, video formats, DXGI\_FORMAT\_R1\_UNORM, DXGI\_FORMAT\_R8G8\_B8G8\_UNORM, and DXGI\_FORMAT\_R8R8\_G8B8\_UNORM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8eb8-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8eb8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8eb8-127">Mode de mosaïque de la zone d’une ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="e8eb8-127">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 