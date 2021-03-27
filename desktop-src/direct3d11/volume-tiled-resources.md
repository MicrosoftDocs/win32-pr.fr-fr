---
title: Ressources en mosaïque de volume (graphiques Direct3D 11)
description: Les textures de volume (3D) peuvent être utilisées en tant que ressources en mosaïque, en notant que la résolution des vignettes est à trois dimensions.
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb8b35e522ef3298abad1322d6fb7a2fe65bfcf
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "103679054"
---
# <a name="volume-tiled-resources"></a><span data-ttu-id="99a26-103">Ressources en mosaïque de volume</span><span class="sxs-lookup"><span data-stu-id="99a26-103">Volume Tiled Resources</span></span>

<span data-ttu-id="99a26-104">Les textures de volume (3D) peuvent être utilisées en tant que ressources en mosaïque, en notant que la résolution des vignettes est à trois dimensions.</span><span class="sxs-lookup"><span data-stu-id="99a26-104">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="99a26-105">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="99a26-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="99a26-106">API de ressources en mosaïque de D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="99a26-106">D3D11.3 Tiled Resource APIs</span></span>](#d3d113-tiled-resource-apis)
-   [<span data-ttu-id="99a26-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99a26-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="99a26-108">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="99a26-108">Overview</span></span>

<span data-ttu-id="99a26-109">Les ressources en mosaïque découplent un objet ressource D3D de la mémoire de stockage (les ressources du passé ont une relation 1:1 avec leur mémoire de stockage).</span><span class="sxs-lookup"><span data-stu-id="99a26-109">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="99a26-110">Cela permet un large éventail de scénarios intéressants, tels que la diffusion en continu dans les données de texture et la réutilisation ou la réduction de l’utilisation de la mémoire</span><span class="sxs-lookup"><span data-stu-id="99a26-110">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage</span></span>

<span data-ttu-id="99a26-111">les ressources en mosaïque de texture 2D sont prises en charge dans D3D 11.2.</span><span class="sxs-lookup"><span data-stu-id="99a26-111">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="99a26-112">D3D12 et D3D 11.3 ajoutent la prise en charge des textures en mosaïque 3D.</span><span class="sxs-lookup"><span data-stu-id="99a26-112">D3D12 and D3D11.3 add support for 3D tiled textures.</span></span>

<span data-ttu-id="99a26-113">Les dimensions de ressource typiques utilisées dans la mosaïque sont les vignettes de 4 x 4 pour les textures 2D et les vignettes 4 x 4 x 4 pour les textures 3D.</span><span class="sxs-lookup"><span data-stu-id="99a26-113">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



|                             |                                     |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="99a26-114">Bits/pixel (1 échantillon/pixel)</span><span class="sxs-lookup"><span data-stu-id="99a26-114">Bits/pixel (1 sample/pixel)</span></span> | <span data-ttu-id="99a26-115">Dimensions de la mosaïque (pixels, x h x d)</span><span class="sxs-lookup"><span data-stu-id="99a26-115">Tile dimensions (pixels, w x h x d)</span></span> |
| <span data-ttu-id="99a26-116">8</span><span class="sxs-lookup"><span data-stu-id="99a26-116">8</span></span>                           | <span data-ttu-id="99a26-117">64x32x32</span><span class="sxs-lookup"><span data-stu-id="99a26-117">64x32x32</span></span>                            |
| <span data-ttu-id="99a26-118">16</span><span class="sxs-lookup"><span data-stu-id="99a26-118">16</span></span>                          | <span data-ttu-id="99a26-119">32x32x32</span><span class="sxs-lookup"><span data-stu-id="99a26-119">32x32x32</span></span>                            |
| <span data-ttu-id="99a26-120">32</span><span class="sxs-lookup"><span data-stu-id="99a26-120">32</span></span>                          | <span data-ttu-id="99a26-121">32x32x16</span><span class="sxs-lookup"><span data-stu-id="99a26-121">32x32x16</span></span>                            |
| <span data-ttu-id="99a26-122">64</span><span class="sxs-lookup"><span data-stu-id="99a26-122">64</span></span>                          | <span data-ttu-id="99a26-123">32x16x16</span><span class="sxs-lookup"><span data-stu-id="99a26-123">32x16x16</span></span>                            |
| <span data-ttu-id="99a26-124">128</span><span class="sxs-lookup"><span data-stu-id="99a26-124">128</span></span>                         | <span data-ttu-id="99a26-125">16x16x16</span><span class="sxs-lookup"><span data-stu-id="99a26-125">16x16x16</span></span>                            |
| <span data-ttu-id="99a26-126">BC 1, 4</span><span class="sxs-lookup"><span data-stu-id="99a26-126">BC 1,4</span></span>                      | <span data-ttu-id="99a26-127">128x64x16</span><span class="sxs-lookup"><span data-stu-id="99a26-127">128x64x16</span></span>                           |
| <span data-ttu-id="99a26-128">BC 2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="99a26-128">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="99a26-129">64x64x16</span><span class="sxs-lookup"><span data-stu-id="99a26-129">64x64x16</span></span>                            |



 

<span data-ttu-id="99a26-130">Notez que les formats suivants ne sont pas pris en charge avec les ressources en mosaïque : formats 96bpp, formats vidéo, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 G8B8 \_ \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="99a26-130">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="99a26-131">Dans les diagrammes ci-dessous, gris foncé représente des vignettes NULL.</span><span class="sxs-lookup"><span data-stu-id="99a26-131">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="99a26-132">Mappage par défaut des ressources en mosaïque 3D de la texture (MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="99a26-132">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="99a26-133">Mappage par défaut des ressources en mosaïque 3D de la texture (deuxième MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="99a26-133">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="99a26-134">Ressource mosaïque 3D de texture (MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="99a26-134">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="99a26-135">Ressource mosaïque 3D de texture (deuxième MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="99a26-135">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="99a26-136">Ressource mosaïque 3D de texture (vignette simple)</span><span class="sxs-lookup"><span data-stu-id="99a26-136">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="99a26-137">Ressource mosaïque 3D de texture (zone uniforme)</span><span class="sxs-lookup"><span data-stu-id="99a26-137">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="99a26-138">Mappage par défaut des ressources en mosaïque 3D de la texture (MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="99a26-138">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![mappage par défaut du MIP le plus détaillé](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="99a26-140">Mappage par défaut des ressources en mosaïque 3D de la texture (deuxième MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="99a26-140">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![mappage par défaut du deuxième MIP le plus détaillé](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="99a26-142">Ressource mosaïque 3D de texture (MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="99a26-142">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="99a26-143">Le code suivant configure une ressource en mosaïque 3D au MIP le plus détaillé.</span><span class="sxs-lookup"><span data-stu-id="99a26-143">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![mappage le plus détaillé d’une ressource en mosaïque 3D](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="99a26-145">Ressource mosaïque 3D de texture (deuxième MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="99a26-145">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="99a26-146">Le code suivant configure une ressource en mosaïque 3D et le deuxième MIP le plus détaillé :</span><span class="sxs-lookup"><span data-stu-id="99a26-146">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![deuxième mappage le plus détaillé d’une ressource en mosaïque 3D](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="99a26-148">Ressource mosaïque 3D de texture (vignette simple)</span><span class="sxs-lookup"><span data-stu-id="99a26-148">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="99a26-149">Le code suivant configure une seule ressource de mosaïque :</span><span class="sxs-lookup"><span data-stu-id="99a26-149">The following code sets up a Single Tile resource:</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![une seule vignette](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="99a26-151">Ressource mosaïque 3D de texture (zone uniforme)</span><span class="sxs-lookup"><span data-stu-id="99a26-151">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="99a26-152">Le code suivant configure une ressource de zone en mosaïque uniforme (Notez l’instruction `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="99a26-152">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![un cadre uniforme](images/vtr-tex3d-uniform.png)

## <a name="d3d113-tiled-resource-apis"></a><span data-ttu-id="99a26-154">API de ressources en mosaïque de D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="99a26-154">D3D11.3 Tiled Resource APIs</span></span>

<span data-ttu-id="99a26-155">Les mêmes appels d’API sont utilisés pour les ressources en mosaïque 2D et 3D :</span><span class="sxs-lookup"><span data-stu-id="99a26-155">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="99a26-156">Énumérations</span><span class="sxs-lookup"><span data-stu-id="99a26-156">Enums</span></span>

-   <span data-ttu-id="99a26-157">[**D3d11 \_ Niveau des \_ ressources \_ en mosaïque**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : détermine le niveau de prise en charge des ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="99a26-157">[**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="99a26-158">[**D3d11 \_ FORMAT \_ de format**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) de ressource : utilisé pour tester la prise en charge des ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="99a26-158">[**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="99a26-159">[**D3d11 \_ \_Indicateur de \_ niveau de \_ qualité \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) multi-échantillonnage : détermine la prise en charge des ressources en mosaïque dans une ressource à échantillonnage multiple.</span><span class="sxs-lookup"><span data-stu-id="99a26-159">[**D3D11\_CHECK\_MULTISAMPLE\_QUALITY\_LEVELS\_FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="99a26-160">[**D3d11 \_ \_ \_ Indicateurs de copie de vignette**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : contient des indicateurs pour la copie vers et à partir de ressources en mosaïque swizzled et de mémoires tampons linéaires.</span><span class="sxs-lookup"><span data-stu-id="99a26-160">[**D3D11\_TILE\_COPY\_FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="99a26-161">Structures</span><span class="sxs-lookup"><span data-stu-id="99a26-161">Structures</span></span>

-   <span data-ttu-id="99a26-162">[**D3d11 \_ \_ \_ Coordonnée des ressources en mosaïque**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : contient la référence de coordonnée x, y et z et la référence de sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="99a26-162">[**D3D11\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="99a26-163">Notez qu’il existe une classe d’assistance : \_ coordonnée de la ressource en mosaïque CD3D11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="99a26-163">Note there is a helper class: CD3D11\_TILED\_RESOURCE\_COORDINATE.</span></span>
-   <span data-ttu-id="99a26-164">[**D3d11 \_ \_ \_ Taille**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) de la zone de vignette : spécifie la taille et le nombre de vignettes de la région en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="99a26-164">[**D3D11\_TILE\_REGION\_SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="99a26-165">[**D3d11 \_ \_Forme de vignette**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : la forme de la vignette est une largeur, une hauteur et une profondeur dans des texels.</span><span class="sxs-lookup"><span data-stu-id="99a26-165">[**D3D11\_TILE\_SHAPE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="99a26-166">[**D3d11 \_ Données de fonctionnalité \_ \_ d3d11 \_ options1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): contient le niveau de niveau de ressource de vignette pris en charge.</span><span class="sxs-lookup"><span data-stu-id="99a26-166">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): holds the supported tile resource tier level.</span></span>

<span data-ttu-id="99a26-167">Méthodes</span><span class="sxs-lookup"><span data-stu-id="99a26-167">Methods</span></span>

-   <span data-ttu-id="99a26-168">[**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : utilisé pour déterminer quelles fonctionnalités, et à quel niveau, sont prises en charge par le matériel actuel.</span><span class="sxs-lookup"><span data-stu-id="99a26-168">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="99a26-169">[**ID3D11DeviceContext2 :: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copie les vignettes de la mémoire tampon vers la ressource en mosaïque, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="99a26-169">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="99a26-170">[**ID3D11DeviceContext2 :: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : met à jour les mappages des emplacements des vignettes dans les ressources en mosaïque aux emplacements de mémoire dans un pool de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="99a26-170">[**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a tile pool.</span></span>
-   <span data-ttu-id="99a26-171">[**ID3D11DeviceContext2 :: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copie les mappages d’une ressource en mosaïque source vers une ressource en mosaïque de destination.</span><span class="sxs-lookup"><span data-stu-id="99a26-171">[**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="99a26-172">[**ID3D11DeviceContext2 :: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : obtient des informations sur la façon dont une ressource en mosaïque est divisée en mosaïques.</span><span class="sxs-lookup"><span data-stu-id="99a26-172">[**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99a26-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99a26-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99a26-174">Fonctionnalités Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="99a26-174">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




