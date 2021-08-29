---
title: Attribut VML V-caractères de hauteur identique
description: Attribut VML V-caractères de hauteur identique
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219d9f06e120ccc86bfa41c1cfff69b7feb64d68b1343732d45f57f26d952b21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864149"
---
# <a name="vml-v-same-letter-heights-attribute"></a>Attribut VML V-caractères de hauteur identique

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si toutes les lettres auront la même hauteur, quel que soit le cas initial. En lecture/écriture. **VgTriState**.

**S’applique à**

[TextPath](msdn-online-vml-textpath-element.md)

**Syntaxe de balise**

<v : *Element* style = "v-after-letter-largers : *expression* " >

**Syntaxe du script**

*Element* . style. v-comflat-hauteur = "*expression*"

*expression* = *Element*. style. v-Lettres identiques

**Remarques**

Si la **valeur est true**, les lettres minuscules sont étirées jusqu’à la hauteur des lettres majuscules. La valeur par défaut est **False**.

*Attribut standard VML*

**Exemple**

Toutes les lettres auront la même hauteur, quelle que soit la casse.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 