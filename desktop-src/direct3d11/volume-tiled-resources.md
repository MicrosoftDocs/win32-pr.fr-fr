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
# <a name="volume-tiled-resources"></a>Ressources en mosaïque de volume

Les textures de volume (3D) peuvent être utilisées en tant que ressources en mosaïque, en notant que la résolution des vignettes est à trois dimensions.

-   [Vue d'ensemble](#overview)
-   [API de ressources en mosaïque de D3D 11.3](#d3d113-tiled-resource-apis)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Les ressources en mosaïque découplent un objet ressource D3D de la mémoire de stockage (les ressources du passé ont une relation 1:1 avec leur mémoire de stockage). Cela permet un large éventail de scénarios intéressants, tels que la diffusion en continu dans les données de texture et la réutilisation ou la réduction de l’utilisation de la mémoire

les ressources en mosaïque de texture 2D sont prises en charge dans D3D 11.2. D3D12 et D3D 11.3 ajoutent la prise en charge des textures en mosaïque 3D.

Les dimensions de ressource typiques utilisées dans la mosaïque sont les vignettes de 4 x 4 pour les textures 2D et les vignettes 4 x 4 x 4 pour les textures 3D.



|                             |                                     |
|-----------------------------|-------------------------------------|
| Bits/pixel (1 échantillon/pixel) | Dimensions de la mosaïque (pixels, x h x d) |
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1, 4                      | 128x64x16                           |
| BC 2, 3, 5, 6, 7                | 64x64x16                            |



 

Notez que les formats suivants ne sont pas pris en charge avec les ressources en mosaïque : formats 96bpp, formats vidéo, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 G8B8 \_ \_ UNORM.

Dans les diagrammes ci-dessous, gris foncé représente des vignettes NULL.

-   [Mappage par défaut des ressources en mosaïque 3D de la texture (MIP le plus détaillé)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [Mappage par défaut des ressources en mosaïque 3D de la texture (deuxième MIP le plus détaillé)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [Ressource mosaïque 3D de texture (MIP le plus détaillé)](#texture-3d-tiled-resource-most-detailed-mip)
-   [Ressource mosaïque 3D de texture (deuxième MIP le plus détaillé)](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [Ressource mosaïque 3D de texture (vignette simple)](#texture-3d-tiled-resource-single-tile)
-   [Ressource mosaïque 3D de texture (zone uniforme)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Mappage par défaut des ressources en mosaïque 3D de la texture (MIP le plus détaillé)

![mappage par défaut du MIP le plus détaillé](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Mappage par défaut des ressources en mosaïque 3D de la texture (deuxième MIP le plus détaillé)

![mappage par défaut du deuxième MIP le plus détaillé](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Ressource mosaïque 3D de texture (MIP le plus détaillé)

Le code suivant configure une ressource en mosaïque 3D au MIP le plus détaillé.

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Ressource mosaïque 3D de texture (deuxième MIP le plus détaillé)

Le code suivant configure une ressource en mosaïque 3D et le deuxième MIP le plus détaillé :

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

### <a name="texture-3d-tiled-resource-single-tile"></a>Ressource mosaïque 3D de texture (vignette simple)

Le code suivant configure une seule ressource de mosaïque :

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

### <a name="texture-3d-tiled-resource-uniform-box"></a>Ressource mosaïque 3D de texture (zone uniforme)

Le code suivant configure une ressource de zone en mosaïque uniforme (Notez l’instruction `trSize.bUseBox = true;) :`

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

## <a name="d3d113-tiled-resource-apis"></a>API de ressources en mosaïque de D3D 11.3

Les mêmes appels d’API sont utilisés pour les ressources en mosaïque 2D et 3D :

Énumérations

-   [**D3d11 \_ Niveau des \_ ressources \_ en mosaïque**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : détermine le niveau de prise en charge des ressources en mosaïque.
-   [**D3d11 \_ FORMAT \_ de format**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) de ressource : utilisé pour tester la prise en charge des ressources en mosaïque.
-   [**D3d11 \_ \_Indicateur de \_ niveau de \_ qualité \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) multi-échantillonnage : détermine la prise en charge des ressources en mosaïque dans une ressource à échantillonnage multiple.
-   [**D3d11 \_ \_ \_ Indicateurs de copie de vignette**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : contient des indicateurs pour la copie vers et à partir de ressources en mosaïque swizzled et de mémoires tampons linéaires.

Structures

-   [**D3d11 \_ \_ \_ Coordonnée des ressources en mosaïque**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : contient la référence de coordonnée x, y et z et la référence de sous-ressource. Notez qu’il existe une classe d’assistance : \_ coordonnée de la ressource en mosaïque CD3D11 \_ \_ .
-   [**D3d11 \_ \_ \_ Taille**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) de la zone de vignette : spécifie la taille et le nombre de vignettes de la région en mosaïque.
-   [**D3d11 \_ \_Forme de vignette**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : la forme de la vignette est une largeur, une hauteur et une profondeur dans des texels.
-   [**D3d11 \_ Données de fonctionnalité \_ \_ d3d11 \_ options1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): contient le niveau de niveau de ressource de vignette pris en charge.

Méthodes

-   [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : utilisé pour déterminer quelles fonctionnalités, et à quel niveau, sont prises en charge par le matériel actuel.
-   [**ID3D11DeviceContext2 :: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copie les vignettes de la mémoire tampon vers la ressource en mosaïque, ou vice versa.
-   [**ID3D11DeviceContext2 :: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : met à jour les mappages des emplacements des vignettes dans les ressources en mosaïque aux emplacements de mémoire dans un pool de mosaïques.
-   [**ID3D11DeviceContext2 :: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copie les mappages d’une ressource en mosaïque source vers une ressource en mosaïque de destination.
-   [**ID3D11DeviceContext2 :: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : obtient des informations sur la façon dont une ressource en mosaïque est divisée en mosaïques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 




