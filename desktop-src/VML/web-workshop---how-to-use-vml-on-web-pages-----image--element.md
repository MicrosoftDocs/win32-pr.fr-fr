---
title: Utilisation de l’élément image
description: Cet article décrit l’utilisation de l’élément image dans VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Atelier Web, élément image
- conception de pages Web, élément image
- Langage VML (VML), élément image
- VML (langage VML), élément image
- graphismes vectoriels, élément image
- élément d’image
- Éléments VML, image
- Formes VML, élément image
- Langage VML (VML), attributs de propriété de rognage
- VML (langage VML), attributs de propriété de rognage
- graphiques vectoriels, attributs de propriété de rognage
- Formes VML, attributs de propriété de rognage
- attributs de propriété de rognage
- Langage VML (VML), attribut de propriété gain
- VML (langage VML), attribut de propriété gain
- graphiques vectoriels, attribut de propriété gain
- Formes VML, attribut de propriété gain
- propriété gain (attribut)
- Langage VML (VML), contraste
- VML (langage VML), contraste
- graphiques vectoriels, contraste
- Formes VML, contraste
- Langage VML (VML), attribut de propriété blacklevel
- VML (langage VML), attribut de propriété blacklevel
- Graphics Vector, attribut de propriété blacklevel
- Formes VML, attribut de propriété blacklevel
- attribut de propriété blacklevel
- Langage VML (VML), luminosité
- VML (langage VML), luminosité
- graphiques vectoriels, luminosité
- Formes VML, luminosité
- Langage VML (VML), attribut de propriété nuances de gris
- VML (langage VML), attribut de propriété de nuances de gris
- graphique vectoriel, attribut de propriété nuances de gris
- Formes VML, attribut de propriété nuances de gris
- attribut de propriété nuances de gris
- Langage VML (VML), attribut de propriété gamma
- VML (langage VML), attribut de propriété gamma
- Graphics Vector, attribut de propriété gamma
- Formes VML, attribut de propriété gamma
- attribut de propriété gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407802"
---
# <a name="using-the-image-element"></a>Utilisation de l’élément image

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Utilisation de `<image>`

Dans cette rubrique, nous allons vous montrer comment utiliser l' `<image>` élément pour afficher des images avec divers effets spéciaux.

Si vous souhaitez afficher une image qui a été chargée à partir d’une source externe, vous devez généralement utiliser l' `<img>` élément fourni en HTML, puis pointer l’attribut de propriété **src** vers l’emplacement du fichier image.

Vous pouvez également utiliser l' `<image>` élément fourni dans Vml. Lorsque vous utilisez l' `<image>` élément, vous pouvez créer un seul fichier image, puis afficher l’image différemment en modifiant les attributs de propriété de l' `<image>` élément. En outre, l' `<image>` élément fournit plusieurs effets spéciaux que vous ne pouvez pas effectuer en utilisant simplement l' `<img>` élément HTML, tel que [rognage](#crop), [contraste](#contrast), [luminosité](#brightness), [gamma](#gamma)et [nuances de gris](#grayscale).

[![retour au début ](images/top.gif) en haut](#top)

## <a name="crop"></a>coup

Vous pouvez utiliser les attributs de propriété **CropBottom**, **CropTop**, **CropLeft** et **CropRight** de l' `<image>` élément pour afficher différentes images rognées à partir du même fichier image.

La valeur de ces attributs de rognage représente le pourcentage réduit à partir du bord de l’image. La valeur peut être n’importe quel nombre compris entre 0 et 1. Par défaut, la valeur est définie sur 0, ce qui indique l’absence de rognage à partir du bord. La valeur 0,1 indique un rognage de 10 pour cent par rapport à la limite, la valeur 0,15 indique un rognage de 15 pour cent à partir du bord, et ainsi de suite.

Par exemple, pour afficher cinq images rognées du même fichier image, vous pouvez utiliser l' `<image>` élément et spécifier différentes valeurs de rognage, comme illustré dans la représentation VML suivante :

![image1.jpg (5770 octets)](images/image1.jpg)![image1 \-2.jpg (1969 octets)](images/image1-2.jpg)![image1 \-3.jpg (1148 octets)](images/image1-3.jpg)![image1 \-4.jpg (1686 octets)](images/image1-4.jpg)![image1 \-5.jpg (1364 octets)](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





La première image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , n’a pas de valeur de rognage. Par conséquent, 100% de l’image d’origine s’affiche à une taille de 100 points par 80 points.

La deuxième image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , a des valeurs de rognage. `cropbottom="0.2"` indique que 20 pour cent de l’image seront rognés du bas ; `cropright="0.15"` indique que 15% de l’image seront rognés du bord droit. L’image restante est ensuite affichée à une taille de 85 points de 64 points.

De même, les troisième, quatrième et cinquième images ont des valeurs de rognage. L’image d’origine est rognée en fonction des valeurs de rognage et est ensuite affichée en fonction de la valeur de largeur et de hauteur.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="contrast"></a>élevé

Vous pouvez utiliser l’attribut de propriété **gain** de l' `<image>` élément pour afficher les différentes images qui ont des paramètres de contraste différents.

La valeur de l’attribut de propriété **gain** peut être n’importe quel nombre. Par défaut, la valeur est 1, ce qui indique l’utilisation du même contraste que l’image d’origine. La valeur 0 indique aucun contraste. Plus le nombre est élevé, plus le contraste est élevé.

Par exemple, pour afficher cinq images avec différents paramètres de contraste, vous pouvez utiliser l' `<image>` élément et définir une valeur différente pour l’attribut de propriété **gain** , comme indiqué dans la représentation VML suivante :

![image1.jpg (5770 octets)](images/image1.jpg)![image2 \-2.jpg (270 octets)](images/image2-2.jpg)![image2 \-3.jpg (1919 octets)](images/image2-3.jpg)![image2 \-4.jpg (3143 octets)](images/image2-4.jpg)![image2 \-5.jpg (1724 octets)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





Lorsque l’attribut de propriété **gain** a la valeur 0, l’image entière est grisée, car il n’y a aucun contraste. Le contraste est plus perceptible lorsque l’attribut de propriété **gain** a la valeur 3 que lorsqu’il est défini sur 0,5. Le contraste est inversé lorsque l’attribut de propriété **gain** est défini sur une valeur négative telle que-0,4.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="brightness"></a>luminosité

Vous pouvez utiliser l’attribut de propriété **blacklevel** de l' `<image>` élément pour afficher les différentes images qui ont des paramètres de luminosité différents.

La valeur de l’attribut de propriété **blacklevel** peut être n’importe quelle valeur comprise entre 0 et 1. Par défaut, la valeur est 0, ce qui indique que le niveau de luminosité dans l’image d’origine est préservé. La valeur 1 indique le niveau de luminosité le plus élevé.

Par exemple, pour afficher cinq images qui ont des paramètres de luminosité différents, vous pouvez utiliser l' `<image>` élément et définir une valeur différente pour l’attribut de propriété **blacklevel** , comme indiqué dans la représentation VML suivante :

![image1.jpg (5770 octets)](images/image1.jpg)![image3 \-2.jpg (2579 octets)](images/image3-2.jpg)![image3 \-3.jpg (2330 octets)](images/image3-3.jpg)![image3 \-4.jpg (2727 octets)](images/image3-4.jpg)![image3 \-5.jpg (2435 octets)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





[![retour au début ](images/top.gif) en haut](#top)

## <a name="grayscale"></a>nuances de gris

Vous pouvez utiliser l’attribut de propriété **nuances de gris** de l' `<image>` élément pour afficher des images avec ou sans nuances de gris.

La valeur de l’attribut de propriété **nuances de gris** peut être true ou false. Par défaut, la valeur est définie sur false afin que l’image s’affiche en couleur. Si la valeur est définie sur true, l’image sera affichée en nuances de gris.

Par exemple, comme indiqué dans l’image suivante, la première image utilise le paramètre par défaut (false) de l’attribut nuances de gris ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ). Par conséquent, l’image est affichée en couleur.

La deuxième image affecte la valeur true à l’attribut nuances de gris ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ). Par conséquent, l’image est affichée en nuances de gris, comme illustré dans la représentation VML suivante :

![image1.jpg (5770 octets)](images/image1.jpg)![image4 \-2.jpg (2138 octets)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





[![retour au début ](images/top.gif) en haut](#top)

## <a name="gamma"></a>gamma

Vous pouvez utiliser l’attribut de propriété **gamma** de l' `<image>` élément pour afficher les images qui ont des paramètres gamma différents.

La valeur de l’attribut de propriété gamma peut être n’importe quelle valeur comprise entre 0 et 1. Par défaut, la valeur est définie sur 1.

Par exemple, pour afficher trois images qui ont des paramètres gamma différents, vous pouvez utiliser l' `<image>` élément et définir une valeur différente de l’attribut de propriété **gamma** , comme indiqué dans la représentation VML suivante :

![image5 \-1.jpg (2714 octets)](images/image5-1.jpg)![image5 \-2.jpg (2729 octets)](images/image5-2.jpg)![image5 \-3.jpg (2726 octets)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .

 

 