---
title: Attribut VML V-Rotate-Letters
description: Attribut VML V-Rotate-Letters
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779f7878b01765416560dacaed5e3b81a1e00a25d4bf7c53e0071c8bb487d16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123779"
---
# <a name="vml-v-rotate-letters-attribute"></a>Attribut VML V-Rotate-Letters

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si les lettres du texte sont pivotées. En lecture/écriture. **VgTriState**.

**S’applique à**

[TextPath](msdn-online-vml-textpath-element.md)

**Syntaxe de balise**

<v : *Element* style = "v-Rotate-Letters : *expression* " >

**Syntaxe du script**

*Element* . style. v-Rotate-letters = "*expression*"

*expression* = *Element*. style. v-Rotate-lettres

**Remarques**

Si la **valeur est true**, les lettres du texte sont pivotées de 90 degrés. La valeur par défaut est **False**.

*Attribut standard VML*

**Exemple**

Les lettres sont pivotées de 90 degrés.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 