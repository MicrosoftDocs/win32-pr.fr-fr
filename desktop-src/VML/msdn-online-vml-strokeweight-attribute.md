---
title: StrokeWeight VML (attribut)
description: StrokeWeight VML (attribut)
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abac5efa964607fdd942c8dff31a4a124d424aa5fbfeede27abc6164fddef087
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680679"
---
# <a name="vml-strokeweight-attribute"></a>StrokeWeight VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit l’épaisseur du pinceau qui dessine le tracé d’une forme. En lecture/écriture. **VGLength**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* StrokeWeight = " *expression* " >

**Syntaxe du script**

*Element* . StrokeWeight = "*expression*"

*expression* = *élément*. StrokeWeight

**Remarques**

La valeur est dupliquée à partir de l’attribut **Weight** de l’élément **Stroke** . Si un nombre est spécifié, mais qu’aucune unité n’est ajoutée, l’unité de mesure par défaut est l’UME. Si aucune valeur n’est spécifiée, la valeur par défaut est 1 pixel (1px).

Pour les scripts, toutefois, l’unité de mesure par défaut est en points.

*Attribut standard VML*

**Voir aussi**

[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)

**Exemple**

L’épaisseur du trait de la forme est 1 point.


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemple d’attribut StrokeWeight](/previous-versions/bb264095(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 