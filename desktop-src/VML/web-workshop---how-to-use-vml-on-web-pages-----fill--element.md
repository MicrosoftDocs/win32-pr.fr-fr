---
title: Utilisation de l’élément Fill
description: Cet article décrit l’utilisation de l’élément Fill de VML, fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Atelier Web, remplir l’élément
- conception de pages Web, remplir l’élément
- Langage VML (VML), Fill, élément
- VML (langage VML), élément de remplissage
- Vector Graphics, Fill, élément
- Fill, élément
- Éléments VML, remplissage
- Formes VML, élément Fill
- Langage VML (VML), remplissage dégradé
- VML (langage VML), remplissage dégradé
- graphiques vectoriels, remplissage dégradé
- Formes VML, remplissage dégradé
- formes remplies de dégradés
- Langage VML (VML), remplissage de motif
- VML (langage VML), remplissage de motif
- graphiques vectoriels, remplissage de motif
- Formes VML, remplissage de motif
- formes remplies de motifs
- Langage VML (VML), remplissage de l’image
- VML (langage VML), remplissage de l’image
- graphiques vectoriels, remplissage d’image
- Formes VML, remplissage image
- formes pleines d’images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb243e4896443fd36a1b22c2ac3a0ab0bedfb2b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407792"
---
# <a name="using-the-fill-element"></a>Utilisation de l’élément Fill

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Comme vous l’avez appris, vous pouvez utiliser l’attribut de propriété **FillColor** d’un élément de forme prédéfini, tel que `<oval>` ,,,,, `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` , `<arc>` --pour spécifier la couleur utilisée pour remplir la forme. Dans cette rubrique, nous allons vous montrer comment dessiner une forme remplie avec des effets plus avancés.

Vous pouvez placer le `<fill>` sous-élément à l’intérieur de `<shape>` , ou `<shapetype>` , ou n’importe quel élément de forme prédéfini pour décrire comment remplir la forme. Vous pouvez ensuite utiliser les attributs de propriété du `<fill>` sous-élément pour personnaliser l’effet de remplissage, tel que le [remplissage dégradé](#gradient-fill), le [remplissage de motif](#pattern-fill), le [remplissage d’image](#picture-fill).

Dans cette rubrique :

-   [Remplissage dégradé](#gradient-fill)
-   [Remplissage du motif](#pattern-fill)
-   [Remplissage de l’image](#picture-fill)

## <a name="gradient-fill"></a>Remplissage dégradé

Pour dessiner une forme remplie de dégradés, vous pouvez définir l’attribut de propriété de **type** du `<fill>` sous-élément sur « gradient » ou « gradientRadial », puis spécifier d’autres attributs de propriété du `<fill>` sous-élément, tels que **Method**, **color2**, **focus** et **angle**.

**Exemples :**

Pour créer une forme qui est remplie horizontalement, vous pouvez définir l’attribut de propriété de **type** sur « gradient », comme illustré dans la représentation VML suivante :

![horizontal1.gif (3055 octets)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




Si vous modifiez l’attribut de propriété **FillColor** de la forme, la forme est ensuite remplie d’une couleur différente. Vous pouvez ajouter une deuxième couleur en spécifiant l’attribut de propriété **color2** du `<fill>` sous-élément. Par exemple, pour créer une forme qui est remplie à l’aide de deux couleurs, vous pouvez ajouter une deuxième couleur en spécifiant l’attribut de propriété **color2** du `<fill>` sous-élément, comme indiqué dans la représentation VML suivante :

![horizontal2.gif (3127 octets)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




Vous pouvez définir l’attribut de propriété de la **méthode** sur « Linear » ou « Sigma » ou « any » ou « None ». L’effet du dégradé est légèrement différent. En outre, vous pouvez utiliser l’attribut de propriété **angle**,**focus**,**focussize** ou **focusposition** pour modifier la façon dont le dégradé se déplace.

**Exemples :**

 

Pour créer une forme dégradée verticalement, vous pouvez définir l’attribut de propriété angle sur angle = « -90 », comme indiqué dans la représentation VML suivante :

![vertical1.gif (3836 octets)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




Pour créer une forme qui est remplie d’un dégradé Diagonal, vous pouvez définir l’attribut de propriété **angle** sur angle = « -135 », comme illustré dans la représentation VML suivante :

![dialgonalup1.gif (5816 octets)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




Pour créer une forme qui est remplie d’une diagonale dégradée, vous pouvez définir l’attribut de propriété **angle** sur angle = « -45 », comme illustré dans la représentation VML suivante :

![diagonaldown1.gif (5753 octets)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




Pour créer une forme qui est remplie par le dégradé à partir du centre, vous pouvez spécifier `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , comme indiqué dans la représentation VML suivante :

![fromcenter1.gif (4598 octets)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




[![retour au début ](images/top.gif) en haut](#top)

## <a name="pattern-fill"></a>Remplissage du motif

Pour dessiner une forme remplie de motifs, vous pouvez définir l’attribut de propriété de **type** du `<fill>` sous-élément sur « Pattern », puis spécifier d’autres attributs de propriété du `<fill>` sous-élément, tels que **src** et **color2**.

**Exemples :**

Pour créer une forme remplie avec une image de modèle, vous pouvez spécifier l’attribut de propriété de **type** sur « pattern » et faire pointer l’attribut de propriété **src** vers l’emplacement du fichier d’image de modèle, comme indiqué dans la représentation VML suivante :

![pattern1.gif (872 octets)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




Si vous pointez l’attribut de propriété **src** vers un fichier de modèle différent, vous pouvez créer une forme qui est remplie avec un autre modèle. En outre, vous pouvez modifier la couleur en spécifiant une valeur différente pour l’attribut de propriété **FillColor** ou **color2** , comme indiqué dans la représentation VML suivante :

![pattern2.gif (831 octets)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




[![retour au début ](images/top.gif) en haut](#top)

## <a name="picture-fill"></a>Remplissage de l’image

Pour dessiner une forme remplie d’image, vous pouvez définir l’attribut de propriété de **type** du `<fill>` sous-élément sur « Frame », puis spécifier d’autres attributs de propriété du `<fill>` sous-élément, tels que **src** et **color2**.

**Exemples :**

Pour créer une forme remplie avec un fichier image, vous pouvez spécifier l’attribut de propriété de **type** « Frame », puis faire pointer l’attribut de propriété **src** vers l’emplacement du fichier image, comme indiqué dans la représentation VML suivante :

![picture1.gif (8496 octets)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




Vous pouvez facilement créer une forme remplie avec une autre image en pointant l’attribut de propriété **src** vers un autre fichier.

Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .

 

 