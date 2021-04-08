---
title: CoordOrigin VML (attribut)
description: CoordOrigin VML (attribut)
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb08d35aac7e26cc15aa7699439ea9f7ab4dba94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842345"
---
# <a name="vml-coordorigin-attribute"></a>CoordOrigin VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Spécifie l’origine de l’unité de coordonnée du rectangle qui délimite une forme. En lecture/écriture. [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* coordorigin = " *expression* " >

**Syntaxe du script**

*Element* . coordorigin = "*expression*"

*expression* = *élément*. coordorigin

**Remarques**

Si cette valeur n’est pas spécifiée, les coordonnées d’origine sont (0,0) dans le coin supérieur gauche du cadre englobant de la forme.

La valeur x de **CoordSize** est ajoutée à la valeur x de **CoordOrigin** pour déterminer la plage des valeurs horizontales. Par exemple, si la valeur x de **CoordOrigin** est-100 et la valeur x de **CoordSize** est 200, les unités horizontales vont de-100 à + 100. Si la valeur x de **CoordOrigin** est 100 et la valeur x de **CoordSize** est 200, les unités horizontales sont comprises entre 100 et 300, le tout dans le cadre englobant. Il en va de même pour les valeurs y.

Notez que cet attribut est un vecteur et que les unités sont du même type que [CoordSize](msdn-online-vml-coordsize-attribute.md) .

Dans les scripts, étant donné qu’il s’agit d’un vecteur 2D, vous pouvez accéder aux valeurs x et y séparément, et vous pouvez également déterminer le type d’unités attendu.

*Attribut standard VML*

**Exemple**

Le centre du cadre englobant sera l’origine (0,0) du tracé de la forme. Comme **CoordOrigin** est « -500-500 » et **CoordSize** est « 1000 1000 », les unités horizontale et verticale vont de-500 à + 500. Le coin supérieur gauche du tracé se trouve au centre de la zone englobante définie par les points gauche et supérieur tels que définis par **style**.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemple d’attribut CoordOrigin](/previous-versions/bb229664(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 