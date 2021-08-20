---
title: Utilisation de l’élément Stroke
description: cet article décrit l’utilisation de l’élément Stroke de VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Atelier Web, élément Stroke
- conception de pages Web, élément Stroke
- Langage VML (VML), élément Stroke
- VML (langage VML), élément Stroke
- Vector Graphics, élément Stroke
- Stroke, élément
- Éléments VML, trait
- Formes VML, élément Stroke
- Langage VML (VML), attribut de propriété DashStyle
- VML (langage VML), attribut de propriété DashStyle
- Graphics Vector, propriété DashStyle, attribut
- propriété DashStyle (attribut)
- Langage VML (VML), attribut de propriété Opacity
- VML (langage VML), attribut de propriété Opacity
- Graphics Vector, attribut de propriété Opacity
- attribut de propriété Opacity
- Langage VML (VML), attribut de propriété LineStyle
- VML (langage VML), attribut de propriété LineStyle
- Vector Graphics, attribut LineStyle Property
- attribut LineStyle de la propriété
- Langage VML (VML), attribut de propriété joinstyle
- VML (langage VML), attribut de propriété joinstyle
- Graphics Vector, attribut de propriété joinstyle
- attribut de propriété joinstyle
- Langage VML (VML), attribut de propriété fillType
- VML (langage VML), attribut de propriété fillType
- Graphics Vector, attribut de propriété fillType
- attribut de propriété fillType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cb69452abe5b3d743036f6a4db094da196281b575a6db65aa48535126fd917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057446"
---
# <a name="using-the-stroke-element"></a>Utilisation de l’élément Stroke

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Utilisation de `<stroke>`

Comme vous l’avez appris, vous pouvez utiliser les attributs de propriété **StrokeColor** et **StrokeWeight** d’une forme prédéfinie, telle que `<oval>` , `<line>` ,,, `<polyline>` `<curve>` `<rect>` , `<roundrect>` , `<arc>` --pour spécifier la couleur et le poids du contour d’une forme. Dans cette rubrique, nous allons illustrer comment dessiner une forme avec un contour plus avancé.

Vous pouvez placer le `<stroke>` sous-élément à l’intérieur de `<shape>` , ou `<shapetype>` , ou n’importe quel élément de forme prédéfini pour décrire comment dessiner le contour de la forme. Vous pouvez ensuite utiliser les attributs de propriété (par exemple, [DashStyle](#dashstyle), [Opacity](#opacity), [LineStyle](#linestyle), [joinstyle](#joinstyle), [fillType](#filltype) ) du `<stroke>` sous-élément pour personnaliser le plan.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="dashstyle"></a>DashStyle

Vous pouvez utiliser l’attribut de propriété **DashStyle** du `<stroke>` sous-élément pour dessiner un contour avec différents styles de tirets.

**Exemples :**

Si vous spécifiez `<v:stroke dashstyle="solid" />` à l’intérieur de l' `<line>` élément, vous pouvez créer une ligne pleine, comme illustré dans la représentation VML suivante :

![solid.gif (96 octets)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





Si vous modifiez l’attribut de propriété **DashStyle** en « dot », vous pouvez créer une ligne en pointillés, comme illustré dans la représentation VML suivante :

![dot.gif (144 octets)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





Si vous modifiez l’attribut de propriété **DashStyle** en « Dash », vous pouvez créer une ligne de tirets, comme indiqué dans la représentation VML suivante :

![dash.gif (137 octets)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





Si vous modifiez l’attribut de propriété **DashStyle** en « tiret point », vous pouvez créer une ligne avec un style en pointillés et en pointillés, comme illustré dans la représentation VML suivante :

![dashdot.gif (145 octets)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





Si vous modifiez l’attribut de propriété **DashStyle** en « longdash », vous pouvez créer une ligne avec un style Dash long, comme illustré dans la représentation VML suivante :

![longdash.gif (123 octets)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





Si vous modifiez l’attribut de propriété **DashStyle** en « longdashdot », vous pouvez créer une ligne avec un style tirets longs et pointillés, comme illustré dans la représentation VML suivante :

![longdashdot.gif (135 octets)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





Si vous placez `<v:stroke dashstyle="dashdot" />` à l’intérieur de l' `<rect>` élément, vous pouvez créer un rectangle avec une bordure en pointillés et en pointillés, comme illustré dans la représentation VML suivante :

![rect.gif (615 octets)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





[![retour au début ](images/top.gif) en haut](#top)

## <a name="opacity"></a>opacity

Vous pouvez utiliser l’attribut de propriété **Opacity** du `<stroke>` sous-élément pour dessiner un contour avec différents styles d’opacité. La valeur de l’attribut de propriété **Opacity** peut être n’importe quel nombre compris entre 0 et 1. Par défaut, il s’agit de 1, ce qui indique une opacité totale.

**Exemples :**

La représentation VML suivante crée une ligne avec une opacité complète :

![line1.gif (96 octets)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





Si vous ajoutez `<v:stroke opacity="0.5" />` à l’intérieur de l' `<line>` élément, vous pouvez créer une ligne avec une opacité de 50%, comme indiqué dans la représentation VML suivante :

![line2.gif (108 octets)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





[![retour au début ](images/top.gif) en haut](#top)

## <a name="linestyle"></a>LineStyle

Vous pouvez utiliser l’attribut de propriété **LineStyle** du `<stroke>` sous-élément pour dessiner un plan avec différents styles de ligne.

**Exemples :**

Si vous spécifiez `<v:stroke linestyle="single" />` à l’intérieur de l' `<rect>` élément, vous pouvez créer un rectangle avec un seul plan, comme indiqué dans la représentation VML suivante :

![single.gif (537 octets)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





Si vous modifiez l’attribut de propriété **LineStyle** en « thinthin », vous pouvez créer un rectangle avec le contour (1:1:1), comme indiqué dans la représentation VML suivante :

![thinthin.gif (642 octets)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





Si vous modifiez l’attribut de propriété **LineStyle** en « thinthick », vous pouvez créer un rectangle avec le contour (1:1:2), comme indiqué dans la représentation VML suivante :

![thinthick.gif (646 octets)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





Si vous modifiez l’attribut de propriété **LineStyle** en « thickthin », vous pouvez créer un rectangle avec le contour (2:1:1), comme indiqué dans la représentation VML suivante :

![thickthin.gif (676 octets)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





Si vous modifiez l’attribut de propriété **LineStyle** en « thickbetweenthin », vous pouvez créer un rectangle avec le contour (1:1:2:1:1), comme indiqué dans la représentation VML suivante :

![thickbthin.gif (669 octets)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





[![retour au début ](images/top.gif) en haut](#top)

## <a name="joinstyle"></a>joinstyle

Vous pouvez utiliser l’attribut **joinstyle** du `<stroke>` sous-élément pour définir la manière dont les lignes sont jointes.

Par exemple, pour créer une forme qui a la structure de jointures circulaires, comme indiqué dans l’illustration suivante, vous pouvez spécifier `<v:stroke joinstyle="round" />` à l’intérieur de l' `<polyline>` élément, comme indiqué dans la représentation VML suivante :

![round.gif (660 octets)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





Si vous modifiez l’attribut de propriété **joinstyle** en « biseau », vous pouvez créer une forme qui a le contour biseau-Join, comme illustré dans la représentation VML suivante :

![bevel.gif (650 octets)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





Si vous affectez à l’attribut de propriété **joinstyle** la valeur « Mitre », vous pouvez créer une forme qui a la structure de jointure Mitre, comme illustré dans la représentation VML suivante :

![miter.gif (702 octets)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





[![retour au début ](images/top.gif) en haut](#top)

## <a name="filltype"></a>fillType

Vous pouvez utiliser l’attribut de propriété **fillType** du `<stroke>` sous-élément pour dessiner un contour avec divers effets de remplissage.

**Exemples :**

Si vous spécifiez `<v:stroke filltype="solid" />` à l’intérieur de l' `<roundrect>` élément, vous pouvez créer un rectangle à coins arrondis avec le contour plein, comme indiqué dans la représentation VML suivante :

![solid.gif (701 octets)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





Si vous modifiez l’attribut de propriété **fillType** en « pattern », que vous pointez l’attribut de propriété **src** sur l’emplacement du fichier d’image de modèle et que vous définissez l’attribut de propriété **color2** sur la deuxième couleur du motif, vous pouvez créer un rectangle arrondi avec une structure de motif, comme illustré dans la représentation VML suivante :

![pattern.gif (1055 octets)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





Si vous modifiez l’attribut de propriété **fillType** en « vignette » et que vous pointez l’attribut de propriété **src** sur l’emplacement du fichier image, vous pouvez créer un rectangle à coins arrondis avec un contour en mosaïque, comme illustré dans la représentation VML suivante :

![tile.gif (6617 octets)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





Si vous modifiez l’attribut de propriété **fillType** en « Frame » et que vous pointez l’attribut de propriété **src** sur l’emplacement du fichier image, vous pouvez créer un rectangle à coins arrondis avec un contour d’image, comme illustré dans la représentation VML suivante :

![frame.gif (6203 octets)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .

 

 