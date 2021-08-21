---
title: Utilisation de l’élément Typedeforme
description: Utilisation de l’élément Typedeforme
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Atelier Web, élément Typedeforme
- conception de pages Web, élément Typedeforme
- Langage VML (VML), élément Typedeforme
- VML (langage VML), élément Typedeforme
- Graphics Vector, élément Typedeforme
- élément Typedeforme
- Éléments VML, Typedeforme
- Formes VML, élément Typedeforme
- Langage VML (VML), définition des formes fréquemment utilisées
- VML (langage VML), définition des formes fréquemment utilisées
- graphiques vectoriels, définition des formes fréquemment utilisées
- définition des formes fréquemment utilisées
- Formes VML, définition fréquemment utilisées
- Langage VML (VML), instanciation de copies de formes
- VML (langage VML), instanciation de copies de formes
- graphiques vectoriels, instanciation de copies de formes
- instanciation de copies de formes
- Formes VML, instanciation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d815d9f5f911e1a34d558496881ae606819d328a501c635ff463a84f2926ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512646"
---
# <a name="using-the-shapetype-element"></a>Utilisation de l’élément Typedeforme

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Dans cette rubrique, nous allons vous montrer comment utiliser l' `<shapetype>` élément pour définir vos propres formes fréquemment utilisées, puis instancier ou créer des formes à partir du Typedeforme.

Si vous souhaitez dessiner de nombreuses formes qui ont des propriétés identiques ou similaires, il serait fastidieux de taper les mêmes attributs de propriété pour chaque forme. VML fournit l' `<shapetype>` élément afin que vous puissiez définir un prototype de forme. Vous pouvez ensuite utiliser l' `<shape>` élément pour instancier de nombreuses copies de formes à partir du même Typedeforme.

Vous pouvez suivre les trois étapes pour définir un Typedeforme, puis instancier une forme à partir du Typedeforme :

1.  Tapez un `<shapetype>` élément et attribuez-lui un nom en spécifiant l’attribut ID.
2.  Décrivez le Typedeforme à l’aide de ses attributs ou de ses sous-éléments de propriété.
3.  Instanciez une forme en tapant un `<shape>` élément et faites référence à l’attribut de type de la forme à l’attribut ID de Typedeforme.

Par exemple, vous tapez les lignes suivantes pour créer un Typedeforme nommé « MyShape » :


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



Ensuite, vous modifiez le format Typedeforme en définissant des attributs de propriété, tels que `fillcolor="red" strokecolor="blue"` . Vous pouvez aussi utiliser des sous-éléments à l’intérieur de Typedeforme, tels que `<path>` , `<fill>` , `<stroke>` (nous parlerons de ces sous-éléments dans les rubriques ultérieures).


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



Ensuite, vous instanciez une forme à partir du « MyShape » Typedeforme en spécifiant `type="#MyShape"` , comme illustré dans la représentation VML suivante. Cette forme hérite de toutes les propriétés de la « MyShape » de Typedeforme et s’affiche dans sa zone conteneur à une taille de 100 par 80.


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



Vous pouvez instancier une autre forme à partir du « MyShape » de Typedeforme en spécifiant `type="#MyShape"` et en substituant certaines propriétés, telles que `fillcolor="maroon"` , comme indiqué dans la représentation VML suivante. Cette forme hérite de toutes les propriétés de la « MyShape » de Typedeforme, à l’exception de la propriété FillColor, et s’affiche dans sa zone conteneur à une taille de 70 par 90.


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



Voici la représentation VML complète de l’exemple précédent :

![Type1 \-1.gif (477 octets)](images/type1-1.gif)![Type1 \-2.gif (471 octets)](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





Comme vous l’avez appris, quand une forme est instanciée à partir d’un Typedeforme, elle hérite de tous les attributs de propriété du Typedeforme. Vous pouvez remplacer tout ou partie des attributs hérités en redéfinissant les attributs à l’intérieur de l' `<shape>` élément. N’oubliez pas que l’héritage n’est qu’un seul niveau. Cela est dû au fait que seul un `<shape>` élément peut référencer un `<shapetype>` élément. Un `<shapetype>` élément ne peut pas faire référence à un autre `<shapetype>` élément.

En outre, un Typedeforme n’appartient à aucun groupe. Par conséquent, l' `<shapetype>` élément peut apparaître de lui-même ou à l’intérieur d’un `<group>` élément. Vous pouvez avoir de nombreuses formes dans différents groupes qui font référence à la même Typedeforme. Si une unité Typedeforme apparaît à l’intérieur d’un groupe, une forme vivant dans un autre groupe peut toujours faire référence à ce Typedeforme.

Par exemple, dans la représentation VML suivante, Rect1 et Rect2 sont dans groupa, et Rect3 est dans GroupB. Les trois rectangles sont instanciés à partir de MyShape Typedeforme.


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858387) .

 

 