---
title: Utilisation de formes prédéfinies
description: Cet article décrit l’utilisation de formes prédéfinies dans VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Atelier Web, formes prédéfinies
- conception de pages Web, formes prédéfinies
- Langage VML (VML), formes prédéfinies
- VML (langage VML), formes prédéfinies
- graphiques vectoriels, formes prédéfinies
- Formes VML, prédéfinies
- formes prédéfinies
- Langage VML (VML), Rect, élément
- VML (langage VML), Rect, élément
- Vector Graphics, Rect, élément
- Rect, élément
- Éléments VML, Rect
- Langage VML (VML), élément roundRect
- VML (langage VML), élément roundRect
- Graphics Vector, élément roundRect
- élément roundRect
- Éléments VML, roundRect
- Langage VML (VML), élément de ligne
- VML (langage VML), élément de ligne
- graphique vectoriel, élément Line
- élément Line
- Éléments VML, ligne
- Langage VML (VML), élément Polyline
- VML (langage VML), élément Polyline
- Graphics Vector, élément Polyline
- élément Polyline
- Éléments VML, polyligne
- Langage VML (VML), élément Curve
- VML (langage VML), élément Curve
- graphique vectoriel, élément Curve
- élément Curve
- Éléments VML, courbe
- Langage VML (VML), élément arc
- VML (langage VML), élément arc
- Vector Graphics, élément arc
- élément arc
- Éléments VML, arc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b410cf288a3ba63e4c1d745fd962a445b0b220b8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407682"
---
# <a name="using-predefined-shapes"></a>Utilisation de formes prédéfinies

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Comme vous l’avez appris, vous pouvez utiliser l' `<oval>` élément de VML pour créer un ovale simple. VML fournit plusieurs autres éléments prédéfinis. Dans cette rubrique, nous allons vous montrer comment dessiner des graphiques à l’aide de ces éléments.

Dans cette rubrique :

-   [rectangulaire](#roundrect)
-   [roundrect](#roundrect)
-   [line](#polyline)
-   [polyligne](#polyline)
-   [courbe](#curve)
-   [arc](#arc)
-   [Résumé](#summary)

## <a name="rect"></a>rect

Vous pouvez utiliser l' `<rect>` élément pour dessiner un rectangle. Vous pouvez ensuite personnaliser le rectangle en spécifiant des attributs de propriété différents.

Par exemple, vous pouvez dessiner un rectangle qui est rempli en bleu en spécifiant **FillColor**= « Blue » et lui attribuer un contour rouge de point 3,5 en spécifiant **StrokeColor**= "Red" **StrokeWeight**= "3.5 PT", comme illustré dans la représentation VML suivante :

![rect1.gif (485 octets)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) . (Remarque : la spécification VML n’a pas de signet pour l' `<rect>` élément.)

[![retour au début ](images/top.gif) en haut](#top)

## <a name="roundrect"></a>roundrect

Vous pouvez utiliser l' `<roundrect>` élément pour dessiner un rectangle avec des angles arrondis. Vous pouvez ensuite personnaliser le rectangle arrondi en spécifiant des attributs de propriété différents.

Par exemple, vous pouvez dessiner un rectangle qui a des angles arrondis de 30% de la plus petite dimension du rectangle **en spécifiant** la valeur de la fonction de taille de ligne (« 0,3 »), la remplir avec le jaune en spécifiant **FillColor**= « Yellow » et lui attribuer un contour rouge à 2 points en spécifiant **StrokeColor**= "Red" **StrokeWeight**= "2pt

![roundrect1.gif (622 octets)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .

[![retour au début ](images/top.gif) en haut](#top)

## <a name="line"></a>line

Vous pouvez utiliser l' `<line>` élément pour créer une ligne droite. Vous pouvez ensuite personnaliser la ligne en spécifiant des attributs de propriété différents.

Par exemple, vous pouvez dessiner une ligne horizontale en spécifiant from = "20 points, 20 points" **to**= "100pt, 20 points", puis en la définissant **à** 2 points et en rouge en spécifiant **StrokeColor**= "Red" **StrokeWeight**= "2pt", comme illustré dans la représentation VML suivante :

![line1.gif (88 octets)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





Vous pouvez dessiner une ligne verticale ou diagonale en spécifiant simplement des valeurs différentes pour les attributs **de propriété from** et **to** , comme indiqué dans la représentation VML suivante :

![line2.gif (86 octets)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .

[![retour au début ](images/top.gif) en haut](#top)

## <a name="polyline"></a>polyligne

Vous pouvez utiliser l' `<polyline>` élément pour définir des formes qui sont créées à partir de segments de ligne connectés. Vous pouvez ensuite personnaliser la forme en spécifiant des attributs de propriété différents.

Par exemple, pour dessiner la forme illustrée dans l’image suivante, vous pouvez taper la représentation VML suivante :

![polyline1.gif (957 octets)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .

[![retour au début ](images/top.gif) en haut](#top)

## <a name="curve"></a>courbe

Vous pouvez utiliser l' `<curve>` élément pour dessiner une courbe de Bézier cubique. Vous pouvez ensuite personnaliser la courbe en spécifiant des attributs de propriété différents.

Par exemple, pour dessiner une courbe comme indiqué dans l’image suivante, vous pouvez taper la représentation VML suivante :

![curve1.gif (992 octets)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .

[![retour au début ](images/top.gif) en haut](#top)

## <a name="arc"></a>arc

Vous pouvez utiliser l' `<arc>` élément pour dessiner un arc qui est défini en tant que segment d’un ovale. L’arc est défini par l’intersection de l’ovale avec les vecteurs RADIUS de début et de fin, en fonction des angles. Les angles sont calculés à l’aide des propriétés d’un cercle (largeur égale à la hauteur), puis mis à l’échelle de anisotropically à la largeur et à la hauteur souhaitées.

Par exemple, vous pouvez dessiner un arc qui démarre à 0 degrés et se termine à 90 degrés en spécifiant **startAngle**= "0" **endangle**= "90", comme illustré dans la représentation VML suivante :

![arc1.gif (410 octets)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





Vous pouvez modifier l’arc en spécifiant des valeurs **startAngle** et **endAngle** différentes, comme indiqué dans la représentation VML suivante :

![arc2.gif (608 octets)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 octets)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .

[![retour au début ](images/top.gif) en haut](#top)

## <a name="summary"></a>Résumé

Vous pouvez utiliser des éléments prédéfinis VML tels que `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` et `<arc>` pour dessiner facilement des graphiques sur une page Web, puis personnaliser ces graphiques en modifiant simplement leurs attributs de propriété.

 

 