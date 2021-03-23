---
title: Ressources en mosaïque de volume (Direct3D 12)
description: Les textures de volume (3D) peuvent être utilisées en tant que ressources en mosaïque, en notant que la résolution des vignettes est à trois dimensions.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42679155bbd8dc2cec560d2724e430c860f54bc0
ms.sourcegitcommit: 05e7efd3d8de6926d08802669f37e825a2fa2f46
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "104548504"
---
# <a name="volume-tiled-resources-direct3d-12"></a><span data-ttu-id="d3c06-103">Ressources en mosaïque de volume (Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="d3c06-103">Volume tiled resources (Direct3D 12)</span></span>

<span data-ttu-id="d3c06-104">Les textures de volume (3D) peuvent être utilisées en tant que ressources en mosaïque, en notant que la résolution des vignettes est à trois dimensions.</span><span class="sxs-lookup"><span data-stu-id="d3c06-104">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="d3c06-105">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="d3c06-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="d3c06-106">API de ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="d3c06-106">Tiled Resource APIs</span></span>](#tiled-resource-apis)
-   [<span data-ttu-id="d3c06-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3c06-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="d3c06-108">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="d3c06-108">Overview</span></span>

<span data-ttu-id="d3c06-109">Les ressources en mosaïque découplent un objet ressource D3D de la mémoire de stockage (les ressources du passé ont une relation 1:1 avec leur mémoire de stockage).</span><span class="sxs-lookup"><span data-stu-id="d3c06-109">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="d3c06-110">Cela permet un large éventail de scénarios intéressants, tels que la diffusion en continu dans les données de texture et la réutilisation ou la réduction de l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d3c06-110">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage.</span></span>

<span data-ttu-id="d3c06-111">les ressources en mosaïque de texture 2D sont prises en charge dans D3D 11.2.</span><span class="sxs-lookup"><span data-stu-id="d3c06-111">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="d3c06-112">La prise en charge facultative des textures en mosaïque 3D est disponible pour D3D12 et D3D 11,3 (reportez-vous au [**\_ niveau des \_ ressources \_ en mosaïque D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).</span><span class="sxs-lookup"><span data-stu-id="d3c06-112">Optional support for 3D tiled textures is available for D3D12 and D3D11.3 (refer to [**D3D12\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).</span></span>

<span data-ttu-id="d3c06-113">Les dimensions de ressource typiques utilisées dans la mosaïque sont les vignettes de 4 x 4 pour les textures 2D et les vignettes 4 x 4 x 4 pour les textures 3D.</span><span class="sxs-lookup"><span data-stu-id="d3c06-113">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



| <span data-ttu-id="d3c06-114">Bits/pixel (1 échantillon/pixel)</span><span class="sxs-lookup"><span data-stu-id="d3c06-114">Bits/pixel (1 sample/pixel)</span></span> | <span data-ttu-id="d3c06-115">Dimensions de la mosaïque (pixels, x h x d)</span><span class="sxs-lookup"><span data-stu-id="d3c06-115">Tile dimensions (pixels, w x h x d)</span></span> |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="d3c06-116">8</span><span class="sxs-lookup"><span data-stu-id="d3c06-116">8</span></span>                           | <span data-ttu-id="d3c06-117">64x32x32</span><span class="sxs-lookup"><span data-stu-id="d3c06-117">64x32x32</span></span>                            |
| <span data-ttu-id="d3c06-118">16</span><span class="sxs-lookup"><span data-stu-id="d3c06-118">16</span></span>                          | <span data-ttu-id="d3c06-119">32x32x32</span><span class="sxs-lookup"><span data-stu-id="d3c06-119">32x32x32</span></span>                            |
| <span data-ttu-id="d3c06-120">32</span><span class="sxs-lookup"><span data-stu-id="d3c06-120">32</span></span>                          | <span data-ttu-id="d3c06-121">32x32x16</span><span class="sxs-lookup"><span data-stu-id="d3c06-121">32x32x16</span></span>                            |
| <span data-ttu-id="d3c06-122">64</span><span class="sxs-lookup"><span data-stu-id="d3c06-122">64</span></span>                          | <span data-ttu-id="d3c06-123">32x16x16</span><span class="sxs-lookup"><span data-stu-id="d3c06-123">32x16x16</span></span>                            |
| <span data-ttu-id="d3c06-124">128</span><span class="sxs-lookup"><span data-stu-id="d3c06-124">128</span></span>                         | <span data-ttu-id="d3c06-125">16x16x16</span><span class="sxs-lookup"><span data-stu-id="d3c06-125">16x16x16</span></span>                            |
| <span data-ttu-id="d3c06-126">BC 1, 4</span><span class="sxs-lookup"><span data-stu-id="d3c06-126">BC 1,4</span></span>                      | <span data-ttu-id="d3c06-127">128x64x16</span><span class="sxs-lookup"><span data-stu-id="d3c06-127">128x64x16</span></span>                           |
| <span data-ttu-id="d3c06-128">BC 2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="d3c06-128">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="d3c06-129">64x64x16</span><span class="sxs-lookup"><span data-stu-id="d3c06-129">64x64x16</span></span>                            |

<span data-ttu-id="d3c06-130">Notez que les formats suivants ne sont pas pris en charge avec les ressources en mosaïque : formats 96bpp, formats vidéo, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 G8B8 \_ \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="d3c06-130">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="d3c06-131">Dans les diagrammes ci-dessous, gris foncé représente des vignettes NULL.</span><span class="sxs-lookup"><span data-stu-id="d3c06-131">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="d3c06-132">Mappage par défaut des ressources en mosaïque 3D de la texture (MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="d3c06-132">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="d3c06-133">Mappage par défaut des ressources en mosaïque 3D de la texture (deuxième MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="d3c06-133">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="d3c06-134">Ressource mosaïque 3D de texture (MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="d3c06-134">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="d3c06-135">Ressource mosaïque 3D de texture (deuxième MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="d3c06-135">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="d3c06-136">Ressource mosaïque 3D de texture (vignette simple)</span><span class="sxs-lookup"><span data-stu-id="d3c06-136">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="d3c06-137">Ressource mosaïque 3D de texture (zone uniforme)</span><span class="sxs-lookup"><span data-stu-id="d3c06-137">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="d3c06-138">Mappage par défaut des ressources en mosaïque 3D de la texture (MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="d3c06-138">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![mappage par défaut d’une ressource 3D en mosaïque](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="d3c06-140">Mappage par défaut des ressources en mosaïque 3D de la texture (deuxième MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="d3c06-140">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![affiche le deuxième MIP le plus détaillé](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="d3c06-142">Ressource mosaïque 3D de texture (MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="d3c06-142">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="d3c06-143">Le code suivant configure une ressource en mosaïque 3D au MIP le plus détaillé.</span><span class="sxs-lookup"><span data-stu-id="d3c06-143">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![MIP le plus détaillé pour une texture à trois dimensions](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="d3c06-145">Ressource mosaïque 3D de texture (deuxième MIP le plus détaillé)</span><span class="sxs-lookup"><span data-stu-id="d3c06-145">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="d3c06-146">Le code suivant configure une ressource en mosaïque 3D et le deuxième MIP le plus détaillé :</span><span class="sxs-lookup"><span data-stu-id="d3c06-146">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![deuxième MIP le plus détaillé pour une texture à trois dimensions](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="d3c06-148">Ressource mosaïque 3D de texture (vignette simple)</span><span class="sxs-lookup"><span data-stu-id="d3c06-148">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="d3c06-149">Le code suivant configure une seule ressource de mosaïque :</span><span class="sxs-lookup"><span data-stu-id="d3c06-149">The following code sets up a Single Tile resource:</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![une seule ressource à trois dimensions en mosaïque](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="d3c06-151">Ressource mosaïque 3D de texture (zone uniforme)</span><span class="sxs-lookup"><span data-stu-id="d3c06-151">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="d3c06-152">Le code suivant configure une ressource de zone en mosaïque uniforme (Notez l’instruction `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="d3c06-152">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

``` syntax
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![un cadre uniforme](images/vtr-tex3d-uniform.png)

## <a name="tiled-resource-apis"></a><span data-ttu-id="d3c06-154">API de ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="d3c06-154">Tiled Resource APIs</span></span>

<span data-ttu-id="d3c06-155">Les mêmes appels d’API sont utilisés pour les ressources en mosaïque 2D et 3D :</span><span class="sxs-lookup"><span data-stu-id="d3c06-155">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="d3c06-156">Énumérations</span><span class="sxs-lookup"><span data-stu-id="d3c06-156">Enums</span></span>

-   <span data-ttu-id="d3c06-157">[**D3D12 \_ Niveau des \_ ressources \_ en mosaïque**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : détermine le niveau de prise en charge des ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="d3c06-157">[**D3D12\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="d3c06-158">[**D3D12 \_ FORMAT \_ de format**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) de ressource : utilisé pour tester la prise en charge des ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="d3c06-158">[**D3D12\_FORMAT\_SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="d3c06-159">[**D3D12 \_ \_ \_ \_ Indicateurs de niveau de qualité**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) multi-échantillonnage : détermine la prise en charge des ressources en mosaïque dans une ressource à échantillonnage multiple.</span><span class="sxs-lookup"><span data-stu-id="d3c06-159">[**D3D12\_MULTISAMPLE\_QUALITY\_LEVEL\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="d3c06-160">[**D3D12 \_ \_ \_ Indicateurs de copie de vignette**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : contient des indicateurs pour la copie vers et à partir de ressources en mosaïque swizzled et de mémoires tampons linéaires.</span><span class="sxs-lookup"><span data-stu-id="d3c06-160">[**D3D12\_TILE\_COPY\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="d3c06-161">Structures</span><span class="sxs-lookup"><span data-stu-id="d3c06-161">Structs</span></span>

-   <span data-ttu-id="d3c06-162">[**D3D12 \_ \_ \_ Coordonnée des ressources en mosaïque**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : contient la référence de coordonnée x, y et z et la référence de sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="d3c06-162">[**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="d3c06-163">Notez qu’il existe une structure d’assistance [**: \_ \_ \_ coordonnée de ressource en mosaïque CD3DX12**](cd3dx12-tiled-resource-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="d3c06-163">Note there is a helper structure: [**CD3DX12\_TILED\_RESOURCE\_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).</span></span>
-   <span data-ttu-id="d3c06-164">[**D3D12 \_ \_ \_ Taille**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) de la zone de vignette : spécifie la taille et le nombre de vignettes de la région en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="d3c06-164">[**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="d3c06-165">[**D3D12 \_ \_Forme de vignette**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : la forme de la vignette est une largeur, une hauteur et une profondeur dans des texels.</span><span class="sxs-lookup"><span data-stu-id="d3c06-165">[**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="d3c06-166">[**D3D12 \_ \_ \_ \_ Options D3D12 de données**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) de la fonctionnalité : contient le niveau de la couche de ressources de mosaïques pris en charge et un booléen, *VolumeTiledResourcesSupported*, indique si les ressources en mosaïque de volume sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d3c06-166">[**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : holds the supported tile resource tier level and a boolean, *VolumeTiledResourcesSupported*, indicated whether volume tiled resources are supported.</span></span>

<span data-ttu-id="d3c06-167">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d3c06-167">Methods</span></span>

-   <span data-ttu-id="d3c06-168">[**ID3D12Device :: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : utilisé pour déterminer quelles fonctionnalités, et à quel niveau, sont prises en charge par le matériel actuel.</span><span class="sxs-lookup"><span data-stu-id="d3c06-168">[**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="d3c06-169">[**ID3D12GraphcisCommandList :: CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copie les vignettes de la mémoire tampon vers la ressource en mosaïque, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="d3c06-169">[**ID3D12GraphcisCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="d3c06-170">[**ID3D12CommandQueue :: UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : met à jour les mappages des emplacements de mosaïques dans les ressources en mosaïque aux emplacements de mémoire dans un tas de ressources.</span><span class="sxs-lookup"><span data-stu-id="d3c06-170">[**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a resource heap.</span></span>
-   <span data-ttu-id="d3c06-171">[**ID3D12CommandQueue :: CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copie les mappages d’une ressource en mosaïque source vers une ressource en mosaïque de destination.</span><span class="sxs-lookup"><span data-stu-id="d3c06-171">[**ID3D12CommandQueue::CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="d3c06-172">[**ID3D12Device :: GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : obtient des informations sur la façon dont une ressource en mosaïque est divisée en mosaïques.</span><span class="sxs-lookup"><span data-stu-id="d3c06-172">[**ID3D12Device::GetResourceTiling**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3c06-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3c06-173">Related topics</span></span>
* [<span data-ttu-id="d3c06-174">Liaison de ressource</span><span class="sxs-lookup"><span data-stu-id="d3c06-174">Resource Binding</span></span>](resource-binding.md)
