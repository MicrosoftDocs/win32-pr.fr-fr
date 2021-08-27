---
title: FitShape VML (attribut)
description: FitShape VML (attribut)
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0adbb6fd92f296156cf2f95cf2b714cfacd2f193f8e1e1b912e6637b9e8d5cd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099249"
---
# <a name="vml-fitshape-attribute"></a>FitShape VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit si le texte est ajusté au cadre englobant d’une forme. En lecture/écriture. **VgTriState**.

**S’applique à**

[TextPath](msdn-online-vml-textpath-element.md)

**Syntaxe de balise**

<v : *Element* fitshape = " *expression* " >

**Syntaxe du script**

*Element* . fitshape = "*expression*"

*expression* = *élément*. fitshape

**Remarques**

Si la **valeur est true**, étire le texte vers les bords de la zone qui définit la forme entière. La valeur par défaut est **False**.

*Attribut standard VML*

**Exemple**

Le texte est étiré pour s’ajuster à la forme.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 