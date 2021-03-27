---
title: Présentation des textures dans Direct3D 11
description: Une ressource de texture est une collection structurée de données conçue pour stocker des texels.
ms.assetid: d745093e-2d51-4d45-a88a-caa0ca58b2ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fcafdfb9caf53a27e60956c8182ae3ef95008e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840306"
---
# <a name="introduction-to-textures-in-direct3d-11"></a>Présentation des textures dans Direct3D 11

Une ressource de texture est une collection structurée de données conçue pour stocker des texels. Un Texel représente la plus petite unité d’une texture qui peut être lue ou écrite par le pipeline. Contrairement aux mémoires tampons, les textures peuvent être filtrées par des échantillonneurs de texture, car elles sont lues par des unités de nuanceur. Le type de texture affecte la manière dont la texture est filtrée. Chaque Texel contient des composants de 1 à 4, organisés dans l’un des formats DXGI définis par l' \_ énumération de format DXGI.

Les textures sont créées en tant que ressource structurée avec une taille connue. Toutefois, chaque texture peut être typée ou sans type lorsque la ressource est créée, à condition que le type soit entièrement spécifié à l’aide d’une vue lorsque la texture est liée au pipeline.

## <a name="texture-types"></a>Types de texture

Il existe plusieurs types de textures : 1D, 2D, 3D, qui peuvent être créées avec ou sans des mipmaps. Direct3D 11 prend également en charge les tableaux de texture et les textures à échantillonnages.

-   [Textures 1D](#1d-textures)
-   [Tableaux de texture 1D](#1d-texture-arrays)
-   [Textures 2D et tableaux de texture 2D](#2d-textures-and-2d-texture-arrays)
-   [Textures 3D](#3d-textures)

### <a name="1d-textures"></a>Textures 1D

Une texture 1D dans sa forme la plus simple contient des données de texture qui peuvent être traitées par une coordonnée de texture unique. Il peut être visualisé sous la forme d’un tableau de texels, comme indiqué dans l’illustration suivante. les textures 1D sont représentées par l’interface [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) .

![illustration d’une texture 1D](images/d3d10-1d-texture.png)

Chaque Texel contient un certain nombre de composants de couleur en fonction du format des données stockées. Pour augmenter la complexité, vous pouvez créer une texture 1D avec des niveaux de mipmap, comme indiqué dans l’illustration suivante.

![illustration d’une texture 1D avec des niveaux de mipmap](images/d3d10-resource-texture1d.png)

Un niveau de mipmap est une texture qui est une puissance de deux plus petite que le niveau supérieur. Le niveau le plus élevé contient le plus de détails, chaque niveau suivant étant plus petit. Pour un mipmap 1D, le plus petit niveau contient un Texel. En outre, les niveaux MIP diminuent toujours jusqu’à 1:1. Quand des des mipmaps sont générés pour une texture de taille impaire, le niveau inférieur suivant est toujours égal à la taille (sauf si le niveau le plus bas atteint 1). Par exemple, le diagramme illustre une texture 5x1 dont le niveau le plus bas suivant est une texture 2x1, dont le niveau MIP suivant (et le dernier) est une texture de taille de 1x1. Les niveaux sont identifiés par un index appelé LOD (niveau de détail) qui est utilisé pour accéder à la plus petite texture lors du rendu de la géométrie qui n’est pas aussi proche de l’appareil photo.

### <a name="1d-texture-arrays"></a>Tableaux de texture 1D

Direct3D 11 prend également en charge les tableaux de textures. Un tableau de texture 1D est également représenté par l’interface [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) . Un tableau de textures 1D se présente conceptuellement comme dans l’illustration suivante.

![illustration d’un tableau de textures 1D](images/d3d10-resource-texture1darray.png)

Ce tableau de texture contient trois textures. Chacune des trois textures a une largeur de texture de 5 (qui est le nombre d’éléments dans la première couche). Chaque texture contient également un mipmap de couche 3.

Tous les tableaux de texture dans Direct3D sont un tableau homogène de textures. Cela signifie que chaque texture d’un tableau de texture doit avoir le même format de données et la même taille (y compris la largeur de texture et le nombre de niveaux de mipmap). Vous pouvez créer des tableaux de texture de différentes tailles, à condition que toutes les textures dans chaque tableau correspondent à la taille.

### <a name="2d-textures-and-2d-texture-arrays"></a>Textures 2D et tableaux de texture 2D

Une ressource Texture2D contient une grille 2D de texels. Chaque Texel est adressable par un vecteur u, v. Étant donné qu’il s’agit d’une ressource de texture, elle peut contenir des niveaux de mipmap et des sous-ressources. les textures 2D sont représentées par l’interface [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) . Une ressource de texture 2D entièrement remplie ressemble à l’illustration suivante.

![illustration d’une ressource de texture 2D](images/d3d10-resource-texture2d.png)

Cette ressource de texture contient une seule texture 3x5 avec trois niveaux de mipmap.

Une ressource de tableau de texture 2D est un tableau homogène de textures 2D ; autrement dit, chaque texture a le même format de données et les mêmes dimensions (y compris les niveaux de mipmap). Un tableau de textures 2D est également représenté par l’interface [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) . Elle présente une disposition similaire à celle du tableau de texture 1D, à ceci près que les textures contiennent maintenant des données 2D, comme indiqué dans l’illustration suivante.

![illustration d’un tableau de textures 2D](images/d3d10-resource-texture2darray.png)

Ce tableau de texture contient trois textures ; chaque texture est 3x5 avec deux niveaux de mipmap.

### <a name="using-a-2d-texture-array-as-a-texture-cube"></a>Utilisation d’un tableau de texture 2D comme cube de texture

Un cube de texture est un tableau de textures 2D qui contient 6 textures, une pour chaque visage du cube. Un cube de texture entièrement rempli ressemble à l’illustration suivante.

![illustration d’un tableau de textures 2D représentant un cube de texture](images/d3d10-resource-texturecube.png)

Un tableau de textures 2D qui contient 6 textures peut être lu dans les nuanceurs avec les fonctions intrinsèques de mappage de cube, une fois qu’elles sont liées au pipeline avec une vue de texture de cube. Les cubes de texture sont adressés à partir du nuanceur avec un vecteur 3D qui pointe vers le centre du cube de texture.

> [!Note]  
> Les appareils que vous créez avec le [**\_ niveau de fonctionnalité 10 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) et versions ultérieures peuvent prendre en charge des tableaux de cubes de texture dans lesquels le nombre de textures est égal au nombre de cubes de texture dans un tableau multiplié par six. Les appareils que vous créez avec le [**\_ niveau de fonctionnalité 10 0**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) ne prennent en charge qu’un seul cube de texture de six visages. En outre, Direct3D 11 ne prend pas en charge les cubemaps partiels.

 

### <a name="3d-textures"></a>Textures 3D

Une ressource de texture 3D (également appelée texture de volume) contient un volume 3D de texels. Comme il s’agit d’une ressource de texture, elle peut contenir des niveaux de mipmap. les textures 3D sont représentées par l’interface [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) . Une texture 3D entièrement remplie ressemble à l’illustration suivante.

![illustration d’une ressource de texture 3D](images/d3d10-resource-texture3d.png)

Quand une tranche mipmap 3D est liée en tant que sortie de la cible de rendu (avec une vue de cible de rendu), la texture 3D se comporte de la même manière qu’un tableau de texture 2D avec n tranches. La tranche de rendu particulière est choisie à partir de l’étape Geometry-Shader, en déclarant un composant scalaire des données de sortie comme la \_ valeur système SV RenderTargetArrayIndex.

Il n’existe aucun concept de tableau de texture 3D ; par conséquent, une sous-ressource de texture 3D est un niveau mipmap unique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Textures](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




