---
title: Regroupement de formes
description: Cet article décrit le regroupement de formes dans VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Atelier Web, regroupement de formes
- conception de pages Web, regroupement de formes
- Langage VML (VML), regroupement de formes
- VML (langage VML), regrouper des formes
- graphiques vectoriels, grouper des formes
- Formes VML, regroupement
- regroupement de formes
- Langage VML (VML), élément de groupe
- VML (langage VML), élément de groupe
- Vector Graphics, Group, élément
- élément de groupe
- Éléments VML, groupe
- Langage VML (VML), espace de coordonnées local
- VML (langage VML), espace de coordonnées local
- graphiques vectoriels, espace de coordonnées local
- espace de coordonnées local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e0c3073f55d23c15734b5d5ddfa886e7291530
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407702"
---
# <a name="grouping-shapes"></a>Regroupement de formes

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Comme vous l’avez appris, vous pouvez facilement dessiner des formes individuelles à l’aide de VML. Dans cette section, nous allons expliquer les avantages du regroupement de formes et la façon de regrouper des formes.

Si vous aviez de nombreuses formes qui devaient être mises à l’échelle, déplacées ou pivotées ensemble, vous pouvez trouver fastidieux de définir les attributs individuellement pour chaque forme. En outre, vous risquez d’obtenir des erreurs. Il serait préférable de regrouper les formes, puis de définir les attributs de l’ensemble du groupe.

Dans VML, vous pouvez utiliser l' `<group>` élément pour regrouper de nombreuses formes afin qu’elles puissent être transformées en une seule unité. Par exemple, comme indiqué dans la représentation VML suivante, vous pouvez facilement regrouper deux formes.


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



Lorsque les formes sont regroupées, elles utilisent l' [espace de coordonnées local](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) du groupe. Par conséquent, les formes d’un groupe peuvent être mises à l’échelle et déplacées ensemble. Vous verrez d’autres exemples dans la rubrique utiliser l’espace de coordonnées local.

À l’intérieur d’un groupe, vous pouvez avoir autant de formes ou de groupes que vous le souhaitez. Lorsqu’un groupe est à l’intérieur d’un autre groupe, il est appelé « groupe imbriqué ». Il n’existe aucune limitation quant aux niveaux d’imbrication.

Par exemple, les lignes suivantes illustrent un groupe imbriqué de 3 niveaux. Shape3 et Shape4 sont dans GroupC. Shape2 et GroupC sont dans GroupB. Shape1 et GroupB se trouvent dans groupa.


```HTML
<body>
   <v:group id="GroupA"...>
      <v:shape id="Shape1"...></v:shape>
      <v:group id="GroupB"...>
         <v:shape id="Shape2"...></v:shape>
         <v:group id="GroupC"...>
            <v:shape id="Shape3"...></v:shape>
            <v:shape id="Shape4"...></v:shape>
         </v:group>
      </v:group>
   </v:group>
</body>
```



Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858388) .

[![retour au début ](images/top.gif) en haut](#top)

## <a name="summary"></a>Résumé

Vous pouvez utiliser l' `<group>` élément pour regrouper de nombreuses formes afin qu’elles puissent être transformées en une seule unité.

 

 