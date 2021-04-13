---
description: Souvent, les points spécifiés pour les vertex ne correspondent pas exactement aux pixels de l’écran. Dans ce cas, Direct3D applique les règles de pixellisation des triangles pour décider quels pixels s’appliquent à un triangle donné.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Règles de pixellisation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104211158"
---
# <a name="rasterization-rules-direct3d-9"></a>Règles de pixellisation (Direct3D 9)

Souvent, les points spécifiés pour les vertex ne correspondent pas exactement aux pixels de l’écran. Dans ce cas, Direct3D applique les règles de pixellisation des triangles pour décider quels pixels s’appliquent à un triangle donné.

-   [Règles de pixellisation des triangles](#triangle-rasterization-rules)
-   [Règles de point et de ligne](#point-and-line-rules)
-   [Règles de point Sprite](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a>Règles de pixellisation des triangles

Direct3D utilise une convention de remplissage en haut à gauche pour remplir la géométrie. Il s’agit de la même convention que celle utilisée pour les rectangles dans GDI et OpenGL. Dans Direct3D, le centre du pixel est le point déterminant. Si le centre est à l’intérieur d’un triangle, le pixel fait partie du triangle. Les centres de pixels sont des coordonnées entières.

Cette description des règles de pixellisation des triangles utilisées par Direct3D ne s’applique pas nécessairement à tout le matériel disponible. Vos tests peuvent découvrir des variations mineures dans l’implémentation de ces règles.

L’illustration suivante montre un rectangle dont l’angle supérieur gauche se trouve à (0,0) et dont l’angle inférieur droit est (5, 5). Ce rectangle remplit 25 pixels, comme prévu. La largeur du rectangle est définie à droite, moins gauche. La hauteur est définie en tant que bas moins haut.

![illustration d’un carré numéroté divisé en six lignes et colonnes](images/pixmap.png)

Dans la Convention de remplissage en haut à gauche, *Top* fait référence à l’emplacement vertical des étendues horizontales, tandis que *Left* fait référence à l’emplacement horizontal des pixels dans une étendue. Un bord ne peut pas être un bord supérieur, sauf s’il est horizontal. En général, la plupart des triangles ont uniquement des bords gauche et droit. L’illustration suivante montre un bord supérieur et un bord droit.

![illustration d’un carré numéroté qui contient deux triangles](images/triedge.png)

La Convention de remplissage en haut à gauche détermine l’action effectuée par Direct3D lorsqu’un triangle passe au centre d’un pixel. L’illustration suivante montre deux triangles, un à (0, 0), (5, 0) et (5, 5) et l’autre à (0, 5), (0, 0) et (5, 5). Dans ce cas, le premier triangle obtient 15 pixels (en noir), tandis que le second obtient uniquement 10 pixels (indiqué en gris), car la périphérie partagée est le bord gauche du premier triangle.

![illustration d’un carré numéroté qui affiche deux triangles](images/twotris.png)

Si vous définissez un rectangle avec son coin supérieur gauche à (0,5, 0,5) et son coin inférieur droit à (2,5, 4,5), le point central de ce rectangle est (1,5, 2,5). Lorsque le rastériseur Direct3D tessellates ce rectangle, le centre de chaque pixel est sans ambiguïté à l’intérieur de chacun des quatre triangles, et la Convention de remplissage supérieure gauche n’est pas nécessaire. L’illustration suivante montre cela. Les pixels du rectangle sont étiquetés en fonction du triangle dans lequel Direct3D les intègre.

![Affiche un carré numéroté qui contient un rectangle divisé en quatre triangles.](images/noambig.png)

Si vous déplacez le rectangle de l’illustration précédente afin que son coin supérieur gauche se trouve à l’emplacement (1,0, 1,0), à l’angle inférieur droit à (3,0, 5,0) et à son point central à (2,0, 3,0), Direct3D applique la Convention de remplissage en haut à gauche. La plupart des pixels de ce rectangle chevauchent la bordure entre deux ou plusieurs triangles, comme le montre l’illustration suivante.

![illustration d’un carré numéroté qui contient un rectangle divisé en quatre triangles](images/fillrule.png)

Pour les deux rectangles, les mêmes pixels sont affectés, comme indiqué dans l’illustration suivante.

![illustration des pixels affectés par les deux carrés numérotés précédents](images/samepix.png)

## <a name="point-and-line-rules"></a>Règles de point et de ligne

Les points sont restitués de la même façon que les points sprites, qui sont rendus sous forme de quadrilatères alignés sur l’écran et sont donc conformes aux mêmes règles que le rendu de polygones.

Les règles de rendu de ligne sans anticrénelage sont exactement les mêmes que celles pour les [lignes GDI](../gdi/lines.md).

Pour plus d’informations sur le rendu de ligne avec anticrénelage, consultez [**ID3DXLine**](id3dxline.md).

## <a name="point-sprite-rules"></a>Règles de point Sprite

Les points de soulignement et les primitives de correctif sont pixellisés comme si les primitives étaient d’abord fractionnées en triangles et les triangles obtenus pixellisés. Pour plus d’informations, consultez [points sprites (Direct3D 9)](point-sprites.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Systèmes de coordonnées et géométrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
