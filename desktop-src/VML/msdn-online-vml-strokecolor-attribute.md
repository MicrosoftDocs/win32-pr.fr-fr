---
title: StrokeColor VML (attribut)
description: StrokeColor VML (attribut)
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a419813c5bd9db4370320f9f181477013136c70265f4ba1d8572a38ae9e3c473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124232"
---
# <a name="vml-strokecolor-attribute"></a>StrokeColor VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit la couleur du pinceau qui dessine le tracé d’une forme. En lecture/écriture. [IVgColor](msdn-online-vml-ivgcolor.md).

**S’applique à**

[Forme](shape-element--vml.md)

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

 

 