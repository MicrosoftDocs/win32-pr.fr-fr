---
title: FitPath VML (attribut)
description: FitPath VML (attribut)
ms.assetid: f15775ed-f7b7-45d9-83ed-e307daf7451b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8863fb4d8a382ac9ccddaf7cc55fe5e8ceeff221dc1f816e340fa0a78cf9d7b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124782"
---
# <a name="vml-fitpath-attribute"></a>FitPath VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit si le texte correspond au tracé d’une forme. En lecture/écriture. **VgTriState**.

**S’applique à**

[TextPath](msdn-online-vml-textpath-element.md)

**Syntaxe de balise**

<v : *Element* fitpath = " *expression* " >

**Syntaxe du script**

*Element* . fitpath = "*expression*"

*expression* = *élément*. fitpath

**Remarques**

Si la **valeur est true**, redimensionne le texte pour remplir le tracé sur lequel il se trouve. La valeur par défaut est **False**.

*Attribut standard VML*

**Exemple**

Le texte correspond au chemin d’accès.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitpath="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 