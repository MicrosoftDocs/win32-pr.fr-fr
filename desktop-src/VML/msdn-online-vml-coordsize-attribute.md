---
title: CoordSize VML (attribut)
description: CoordSize VML (attribut)
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509658"
---
# <a name="vml-coordsize-attribute"></a>CoordSize VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Spécifie les unités horizontales et verticales du rectangle qui délimite une forme. En lecture/écriture. [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* coordsize = " *expression* " >

**Syntaxe du script**

*Element* . coordsize = "*expression*"

*expression* = *élément*. coordsize

**Remarques**

S’il n’est pas spécifié, la taille de la coordonnée est identique à celle du cadre englobant de la forme.

Notez que cet attribut est un vecteur et que les unités sont relatives à la longueur et à la largeur du rectangle englobant.

Notez également que le mappage entre **coordsize** et le cadre englobant peut être transformé en anisotrope. Assurez-vous que les **coordsize Width** et **coordsize Height** sont identiques à la largeur et à la **hauteur** du **style** si vous ne souhaitez pas déformer la forme.

Dans les scripts, étant donné qu’il s’agit d’un vecteur 2D, vous pouvez accéder aux valeurs x et y séparément, et vous pouvez également déterminer le type d’unités attendu.

*Attribut standard VML*

**Exemple**

La forme est supérieure à 100 points et 100 points de large, mais chaque unité horizontale et verticale dans l’espace de coordonnées est 1/10 d’un point.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemple d’attribut CoordSize](/previous-versions/bb229665(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 