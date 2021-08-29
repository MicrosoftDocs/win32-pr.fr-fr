---
title: Utilisation de l’espace de coordonnées local
description: Utilisation de l’espace de coordonnées local
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- Atelier Web, espace de coordonnées local
- conception de pages Web, espace de coordonnées local
- Langage VML (VML), espace de coordonnées local
- VML (langage VML), espace de coordonnées local
- graphiques vectoriels, espace de coordonnées local
- espace de coordonnées local
- Formes VML, espace de coordonnées local
- Langage VML (VML), regroupement de formes
- VML (langage VML), regrouper des formes
- graphiques vectoriels, grouper des formes
- Formes VML, regroupement
- regroupement de formes
- Langage VML (VML), mise à l’échelle des formes
- VML (langage VML), mise à l’échelle des formes
- graphiques vectoriels, mise à l’échelle des formes
- Formes VML, mise à l’échelle
- mise à l’échelle des formes
- Langage VML (VML), formes de dimensionnement
- VML (langage VML), formes de redimensionnement
- graphiques vectoriels, formes de dimensionnement
- Formes VML, redimensionnement
- dimensionnement des formes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7449890bc28088f9464976ad89a4cce359655bb1f7a6577001856ccd99155a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057082"
---
# <a name="using-local-coordinate-space"></a>Utilisation de l’espace de coordonnées local

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Comme vous l’avez appris, vous pouvez spécifier les attributs de style de **largeur** et de **hauteur** pour définir la taille d’une zone conteneur dans laquelle le contenu d’une forme ou d’un groupe sera rendu. Dans cette rubrique, nous allons expliquer l’espace de coordonnées local et la façon dont il est utilisé dans VML pour mettre à l’échelle des formes.

Si vous avez été invité à dessiner un rectangle de 1 pouce sur un morceau de papier de grille, la première chose à faire est de commencer (le point d’origine). Ensuite, vous devez déterminer comment mapper un pouce aux cellules du papier de la grille (coordonnée).

De même, lorsque le contenu d’une forme ou d’un groupe est rendu à l’intérieur de sa zone conteneur sur une page Web, le point d’origine et la coordonnée doivent être définis. VML fournit un espace de coordonnées local pour permettre à chaque forme ou groupe de définir son propre point et sa coordonnée d’origine. Si vous ne spécifiez pas d’espace de coordonnées, celui par défaut est utilisé. Par défaut, l’origine commence dans l’angle supérieur gauche de la zone conteneur.

Par exemple, la représentation VML de l’ovale rouge illustré ci-dessous ne spécifie pas les attributs de propriété **coordsize** et **coordorigin** . Par conséquent, un espace de coordonnées local par défaut est utilisé. La taille de l’ovale est de 100 points (largeur) par 75 points (hauteur). Vous pouvez redimensionner l’ovale en spécifiant une largeur ou une hauteur différente, comme vous l’avez appris dans la rubrique mettre à l' [échelle les formes](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) .

![oval1.gif (627 octets)](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





Lorsque la forme devient plus complexe, ou lorsque vous souhaitez regrouper plusieurs formes et les mettre à l’échelle, vous devez utiliser la fonctionnalité d’espace de coordonnées locale fournie dans VML.

Pour chaque forme ou groupe, vous pouvez utiliser les attributs de propriété **coordsize** et **coordorigin** pour définir l’espace de coordonnées local de la forme ou du groupe. L’attribut **coordsize** spécifie le nombre d’unités le long de la largeur et la hauteur de la zone conteneur. L’attribut **coordorigin** définit la coordonnée dans l’angle supérieur gauche de la zone conteneur. Toutes les informations relatives à la position (telles que la largeur, la hauteur, la gauche, le haut, le chemin d’accès, etc.) sont exprimées en termes d’unité dans l’espace de coordonnées local.

Par exemple, comme indiqué dans la représentation VML suivante, `width: 100pt; height: 100pt;` définit la taille de la zone conteneur pour que la forme soit 100 points de 100 points.

![cord1.gif (836 octets)](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   `coordsize="21600,21600"` définit la taille de l’espace de coordonnées local pour la forme sur 21600 unités par 21600 unités. Par conséquent, une unité dans l’espace de coordonnées local est équivalente au point 1/216.
-   `path="m10800,0l0,10800,10800,21600,21600,10800xe"` définit le contour de la forme sous forme de losange. Comme nous l’avons appris, toutes les informations relatives à la position (telles que la largeur, la hauteur, la gauche, le haut, le chemin d’accès, etc.) sont exprimées en termes d’unité dans l’espace de coordonnées local. Par conséquent, 10800 dans le `<path>` signifie 10800 unités, ce qui équivaut à 50 points.

Lorsque vous souhaitez redimensionner cette forme de losange, il vous suffit de spécifier une largeur ou une hauteur différente. vous n’êtes pas obligé de modifier une valeur dans le `<path>` . Pour cette forme complexe, si vous n’avez pas utilisé la fonctionnalité espace de coordonnées local, vous devez modifier chaque valeur dans le `<path>` chaque fois que vous souhaitez la redimensionner.

Par exemple, vous pouvez mettre à l’échelle la forme en losange en spécifiant simplement une largeur ou une hauteur différente, comme indiqué dans la représentation VML suivante :

![cord2.gif (1692 octets)](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





Vous pouvez également utiliser l’espace de coordonnées local dans l' `<group>` élément afin que le contenu de toutes les formes dans le groupe soit mis à l’échelle ensemble en fonction de la même coordonnée. Ensuite, chaque fois que vous souhaitez mettre à l’échelle ou déplacer un groupe de formes, modifiez simplement la largeur et la hauteur, ou les paramètres **coordsize** et **coordorigin** du groupe.

Par exemple, dans la représentation VML suivante, `<v:group style='... width:200pt;height:200pt;'>` définit la taille de la zone conteneur pour que le groupe soit 200 points de 200 points.

![cord3.gif (645 octets)](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   `coordsize="1000,1000"` définit la taille de l’espace de coordonnées local pour que le groupe soit de 1000 unités par unité de 1000. Par conséquent, 1 unité dans l’espace de coordonnées local est équivalente au point 1/5.
-   `coordorigin="-500,-500"` définit l’angle supérieur gauche de la zone conteneur sur « -500,-500 ». Par conséquent, le système de coordonnées à l’intérieur de la zone conteneur est compris entre-500 et 500 le long de l’axe x, et-500 à 500 le long de l’axe y. En d’autres termes, le centre de la zone conteneur a la valeur « 0,0 ».
-   `<v:oval style='... width:400;height:300;'>` définit la taille de la zone conteneur pour l’ovale rouge sur 400 unités (largeur) par 300 unités (hauteur). Étant donné qu’une unité dans l’espace de coordonnées local est équivalente au point 1/5, la taille de la zone conteneur pour l’ovale rouge est de 80 points (largeur) de 60 points (hauteur).

De même, la taille de la zone conteneur pour le roundRect vert est de 50 points (largeur) de 40 points (hauteur).

Lorsque vous souhaitez redimensionner l’ovale rouge et le roundRect vert, modifiez simplement `<v:group style='... width:200pt;height:200pt;'>` . C’est-ce que vous n’avez pas besoin de modifier individuellement la taille des deux formes.

Par exemple, si vous remplacez `<v:group style='... width:200pt;height:200pt;'>` par `<v:group style='... width:300pt;height:300pt;'>` , les formes deviennent plus volumineuses, comme illustré dans l’image suivante :

![cord4.gif (943 octets)](images/cord4.gif)



Vous remarquerez également que les formes se trouvent différemment. Cela est dû au fait que les formes sont dessinées à partir de « 0, 0 », qui se trouve au centre de la zone conteneur. Étant donné que vous augmentez la taille de la zone conteneur, le centre de la zone conteneur est également déplacé.

Si vous remplacez `coordorigin="-500,-500"` par `coordorigin="0,0"` , comme indiqué dans l’image suivante, vous remarquerez que l’ovale rouge et le roundRect vert sont déplacés vers le nouvel emplacement. Cela est dû au fait que « 0, 0 » se trouve désormais dans l’angle supérieur gauche de la zone conteneur.

![cord5.gif (648 octets)](images/cord5.gif)



Il est également important de noter que la zone conteneur n’établit pas de zone de découpage. Les graphiques peuvent être dessinés en dehors des limites de la zone conteneur. La zone conteneur sert simplement à mapper l’espace de coordonnées local à l’espace de page.

Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858382) .

 

 