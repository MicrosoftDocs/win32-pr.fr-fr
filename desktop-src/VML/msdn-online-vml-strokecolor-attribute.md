---
title: StrokeColor VML (attribut)
description: StrokeColor VML (attribut)
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d379f41f3d2c1f03349beae8d0420a7c1a26429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031400"
---
# <a name="vml-strokecolor-attribute"></a>StrokeColor VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la couleur du pinceau qui dessine le tracé d’une forme. En lecture/écriture. [IVgColor](msdn-online-vml-ivgcolor.md).

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* StrokeColor = " *expression* " >

**Syntaxe du script**

*Element* . StrokeColor = "*expression*"

*expression* = *élément*. StrokeColor

**Remarques**

La valeur est dupliquée à partir de l’attribut **Color** de l’élément [Stroke](msdn-online-vml-stroke-element.md) .

*Attribut standard VML*

**Exemple**

La couleur du trait du rectangle est rouge.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemple d’attribut StrokeColor](/previous-versions/bb264093(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 