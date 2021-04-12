---
description: Une primitive 3D est une collection de vertex qui forment une seule entité 3D. La primitive la plus simple est une collection de points dans un système de coordonnées 3D, appelée liste de points.
ms.assetid: vs|directx_sdk|~\primitives.htm
title: Primitives (graphiques Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38916e85add69574a2437b0e48c209b14a341e44
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108455"
---
# <a name="primitives-direct3d-9-graphics"></a>Primitives (graphiques Direct3D 9)

Une primitive 3D est une collection de vertex qui forment une seule entité 3D. La primitive la plus simple est une collection de points dans un système de coordonnées 3D, appelée liste de points.

Souvent, les primitives 3D sont des polygones. Un polygone est une figure 3D fermée délimitée par au moins trois vertex. Le polygone le plus simple est un triangle. Microsoft Direct3D utilise des triangles pour composer la plupart de ses polygones, car les trois vertex d’un triangle sont assurés comme étant coplanaires. Le rendu des vertex non planés est inefficace. Vous pouvez combiner des triangles pour former des polygones et des maillages de grande taille et complexes.

L’illustration suivante montre un cube. Deux triangles forment chaque face du cube. Le jeu entier de triangles forme une primitive cubique. Vous pouvez appliquer des textures et des matériaux aux surfaces de primitives pour qu’elles apparaissent comme une forme unie unique. Pour plus d’informations, consultez [Materials (Direct3D 9)](materials.md) et [textures Direct3D (Direct3D 9)](direct3d-textures.md).

![illustration d’un cube avec deux triangles sur chaque visage](images/cube3d.png)

Vous pouvez également utiliser des triangles pour créer des primitives dont les surfaces semblent être des courbes lissées. L’illustration suivante montre comment une sphère peut être simulée avec des triangles. Une fois qu’un matériau est appliqué, le cercle est courbé lorsqu’il est rendu. Cela est particulièrement vrai si vous utilisez l’ombrage Gouraud. Pour plus d’informations, consultez l' [Ombrage Gouraud](shading-modes.md).

![illustration d’une sphère simulée à l’aide d’un triangle](images/sphere3d.png)

Les périphériques Direct3D peuvent créer et manipuler les types de primitives suivants.

-   [Listes de points](point-lists.md)
-   [Listes de lignes](line-lists.md)
-   [Bandes](line-strips.md)
-   [Listes de triangles](triangle-lists.md)
-   [Bandes triangulaires](triangle-strips.md)
-   [Ventilateurs triangulaires (Direct3D 9)](triangle-fans.md)

Vous pouvez restituer des types primitifs à partir d’une application C++ avec l’une des méthodes de rendu de l’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
