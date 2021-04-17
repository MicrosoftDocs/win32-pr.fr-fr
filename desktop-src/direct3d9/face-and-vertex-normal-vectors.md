---
description: Chaque face d’une maille possède un vecteur normal d’unité perpendiculaire, comme indiqué dans l’illustration suivante.
ms.assetid: 86e2a460-7b58-4612-8f72-5a4e864ceb58
title: Vecteurs normaux de face et de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0ef6fd8eba85b770cbfe71477655ddbafd8ee7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564704"
---
# <a name="face-and-vertex-normal-vectors-direct3d-9"></a>Vecteurs normaux de face et de vertex (Direct3D 9)

Chaque face d’une maille possède un vecteur normal d’unité perpendiculaire, comme indiqué dans l’illustration suivante. La direction du vecteur est déterminée par l’ordre dans lequel les vertex sont définis et selon que le système de coordonnées est droitier ou gauche. La face normale pointe à l’extérieur du visage. Dans Direct3D, seul le recto d’une face est visible. Une face avant est une face dans laquelle les sommets sont définis dans l’ordre des aiguilles d’une montre.

![illustration d’un vecteur normal pour une face avant](images/nrmlvect.png)

Tout visage qui n’est pas une face avant est une face arrière. Direct3D n’affiche pas toujours les faces arrière ; par conséquent, les faces arrière sont considérées comme étant en suspens. Vous pouvez modifier le mode d’élimination pour restituer les faces arrière si vous le souhaitez. Pour plus d’informations, consultez élimination de l' [État (Direct3D 9)](culling-state.md) .

Direct3D utilise l’unité de vertex Normals pour les effets d’ombrage, d’éclairage et de texture Gouraud. L’illustration suivante montre des exemples de normales.

![illustration des normales des vertex](images/vertnrml.png)

Lors de l’application de l’ombrage Gouraud à un polygone, Direct3D utilise les normales des sommets pour calculer l’angle entre la source de lumière et l’aire. Il calcule les valeurs de couleur et d’intensité pour les vertex et les interpole pour chaque point sur toutes les surfaces de la primitive. Direct3D calcule la valeur d’intensité de la lumière en utilisant l’angle. Plus l’angle est grand, moins la lumière est éclairée sur l’aire.

Si vous créez un objet qui est plat, définissez les normales des sommets de manière à ce qu’elles pointent perpendiculairement à la surface, comme indiqué dans l’illustration suivante.

![illustration d’une surface plate composée de deux triangles avec des normales de vertex](images/flatvert.png)

Toutefois, il est plus probable que votre objet soit constitué de bandes triangulaires et que les triangles ne soient pas coplanés. Un moyen simple d’obtenir un ombrage lissé sur tous les triangles de la bande consiste à calculer d’abord le vecteur normal de surface pour chaque facette polygonale à laquelle le vertex est associé. La normale du vertex peut être définie pour créer un angle égal avec chaque surface normale. Toutefois, cette méthode peut ne pas être suffisamment efficace pour les primitives complexes.

Cette méthode est illustrée par le diagramme suivant, qui illustre deux surfaces, S1 et S2 vu le bord ci-dessus. Les vecteurs normaux pour S1 et S2 sont affichés en bleu. Le vecteur de la normale du vertex est affiché en rouge. L’angle que le vecteur de la normale du vertex effectue avec la normale de surface de S1 est le même que l’angle entre la normale du vertex et la surface normale de S2. Lorsque ces deux surfaces sont éclairées et grisées à l’aide de l’ombrage Gouraud, le résultat est un bord lisse et correctement arrondi entre eux.

![diagramme de deux surfaces (S1 et S2) et leurs vecteurs normaux et vecteur normal de vertex](images/gvert.png)

Si la normale du vertex se rapproche de l’une des visages avec laquelle elle est associée, elle provoque l’augmentation ou la diminution de l’intensité de la lumière pour les points de cette surface, en fonction de l’angle qu’elle effectue avec la source de lumière. Le diagramme suivant montre un exemple. Là encore, ces surfaces sont vues latéralement. La normale au vertex se rapproche de S1, provoquant ainsi un angle plus petit avec la source de lumière que si la normale du vertex avait des angles égaux avec les normales de surface.

![diagramme de deux surfaces (S1 et S2) avec un vecteur de la normale de vertex qui se rapproche d’une face](images/gvert2.png)

Vous pouvez utiliser l’ombrage Gouraud pour afficher des objets dans une scène 3D avec des bords tranchants. Pour ce faire, dupliquez les vecteurs normaux des sommets à n’importe quelle intersection des visages où un bord aigu est requis, comme indiqué dans l’illustration suivante.

![illustration des vecteurs normaux de vertex dupliqués à des arêtes aiguës](images/shade1.png)

Si vous utilisez les méthodes DrawPrimitive pour restituer votre scène, définissez l’objet avec des bords nets comme une liste de triangles, plutôt qu’une bande triangulaire. Lorsque vous définissez un objet en tant que bande triangulaire, Direct3D le traite comme un seul Polygone composé de plusieurs visages triangulaires. L’ombrage Gouraud est appliqué à la fois sur chaque face du polygone et entre les faces adjacentes. Le résultat est un objet qui est progressivement ombré d’un visage à l’autres. Étant donné qu’une liste de triangles est un polygone composé d’une série de faces triangulaires disjointes, Direct3D applique l’ombrage Gouraud sur chaque face du polygone. Toutefois, il n’est pas appliqué d’un visage à un visage. Si deux ou plusieurs triangles d’une liste triangulaire sont adjacents, ils semblent avoir un bord aigu entre eux.

Une autre solution consiste à passer à l’ombrage plat lors du rendu d’objets avec des bords nets. Il s’agit de la méthode la plus efficace, mais cela peut entraîner la non-affichage des objets de la scène comme les objets qui sont grisés à l’Gouraud.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Systèmes de coordonnées et géométrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



