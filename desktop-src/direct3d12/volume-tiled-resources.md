---
title: Ressources en mosaïque de volume (Direct3D 12)
description: Les textures de volume (3D) peuvent être utilisées en tant que ressources en mosaïque, en notant que la résolution des vignettes est à trois dimensions.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d6e9b4d7ae9ad4b93bae5cf29749c293bf7f55ea7fa35a1e1ca71040218e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123514"
---
# <a name="volume-tiled-resources-direct3d-12"></a>Ressources en mosaïque de volume (Direct3D 12)

Les textures de volume (3D) peuvent être utilisées en tant que ressources en mosaïque, en notant que la résolution des vignettes est à trois dimensions.

## <a name="overview"></a>Vue d’ensemble

Les ressources en mosaïque découplent un objet de ressource Direct3D de sa mémoire de sauvegarde (les ressources du passé ont une relation 1:1 avec leur mémoire de stockage). Cela permet un large éventail de scénarios intéressants, tels que la diffusion en continu dans les données de texture et la réutilisation ou la réduction de l’utilisation de la mémoire.

les ressources en mosaïque de texture 2D sont prises en charge dans Direct3D 11,2. La prise en charge facultative des textures en mosaïque 3D est disponible pour Direct3D 12 et Direct3D 11,3 (reportez-vous à [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).

Les dimensions de ressource typiques utilisées dans la mosaïque sont les vignettes de 4 x 4 pour les textures 2D et les vignettes 4 x 4 x 4 pour les textures 3D.

| Bits/pixel (1 échantillon/pixel) | Dimensions de la mosaïque (pixels, x h x d) |
|-----------------------------|-------------------------------------|
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1, 4                      | 128x64x16                           |
| BC 2, 3, 5, 6, 7                | 64x64x16                            |

Notez que les formats suivants ne sont pas pris en charge avec les ressources en mosaïque : les formats 96bpp, les formats vidéo, les **R1_UNORM**, les **R8G8_B8G8_UNORM** **R8R8_G8B8_UNORM**.

Dans les diagrammes ci-dessous, le gris foncé représente des vignettes NULL.

* [Mappage par défaut des ressources en mosaïque 3D de la texture (MIP le plus détaillé)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
* [Mappage par défaut des ressources en mosaïque 3D de la texture (deuxième MIP le plus détaillé)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
* [Ressource mosaïque 3D de texture (MIP le plus détaillé)](#texture-3d-tiled-resource-most-detailed-mip)
* [Ressource mosaïque 3D de texture (deuxième MIP le plus détaillé)](#texture-3d-tiled-resource-second-most-detailed-mip)
* [Ressource mosaïque 3D de texture (vignette simple)](#texture-3d-tiled-resource-single-tile)
* [Ressource mosaïque 3D de texture (zone uniforme)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Mappage par défaut des ressources en mosaïque 3D de la texture (MIP le plus détaillé)

![mappage par défaut d’une ressource à trois dimensions en mosaïque](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Mappage par défaut des ressources en mosaïque 3D de la texture (deuxième MIP la plus détaillée)

![affiche le deuxième MIP le plus détaillé](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Ressource mosaïque 3D de texture (MIP le plus détaillé)

Le code suivant configure une ressource en mosaïque 3D au MIP le plus détaillé.

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord{};
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize{};
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![MIP le plus détaillé pour une texture à trois dimensions](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Ressource mosaïque 3D de texture (deuxième MIP la plus détaillée)

Le code suivant configure une ressource en mosaïque 3D et le deuxième MIP le plus détaillé.

```cpp
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

### <a name="texture-3d-tiled-resource-single-tile"></a>Ressource mosaïque 3D de texture (vignette simple)

Le code suivant configure une seule ressource de mosaïque.

```cpp
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

![une ressource à trois dimensions en une seule mosaïque](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a>Ressource mosaïque 3D de texture (zone uniforme)

Le code suivant configure une ressource de zone en mosaïque uniforme (Notez l’instruction `trSize.bUseBox = true;) :`

```cpp
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

## <a name="tiled-resource-apis"></a>API de ressources en mosaïque

Les mêmes appels d’API sont utilisés pour les ressources en mosaïque 2D et 3D.

Énumérations

* [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : détermine le niveau de prise en charge des ressources en mosaïque.
* [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2) : utilisé pour tester la prise en charge des ressources en mosaïque.
* [**D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : détermine la prise en charge des ressources en mosaïque dans une ressource à échantillonnage multiple.
* [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : contient des indicateurs pour la copie vers et à partir de ressources en mosaïque swizzled et de mémoires tampons linéaires.

Structures

* [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : contient les informations de référence sur les coordonnées x, y et z, ainsi que sur les sous-ressources. Notez qu’il existe une structure d’assistance : [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).
* [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) : spécifie la taille et le nombre de vignettes de la région en mosaïque.
* [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) : la forme de la vignette est une largeur, une hauteur et une profondeur dans les texels.
* [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : contient le niveau de la ressource de mosaïque pris en charge et un booléen, *VolumeTiledResourcesSupported*, indique si les ressources en mosaïque de volume sont prises en charge.

Méthodes

* [**ID3D12Device :: CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : utilisé pour déterminer quelles fonctionnalités, et à quel niveau, sont prises en charge par le matériel actuel.
* [**ID3D12GraphicsCommandList :: CopyTiles**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copie les vignettes de la mémoire tampon vers la ressource en mosaïque, ou vice versa.
* [**ID3D12CommandQueue :: UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : met à jour les mappages des emplacements de mosaïques dans les ressources en mosaïque aux emplacements de mémoire dans un tas de ressources.
* [**ID3D12CommandQueue :: CopyTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copie les mappages d’une ressource en mosaïque source vers une ressource en mosaïque de destination.
* [**ID3D12Device :: GetResourceTiling**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : obtient des informations sur la façon dont une ressource en mosaïque est divisée en mosaïques.

## <a name="related-topics"></a>Rubriques connexes

* [Liaison de ressource](resource-binding.md)
