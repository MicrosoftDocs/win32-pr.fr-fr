---
title: VML V-Text-Spacing (attribut)
description: VML V-Text-Spacing (attribut)
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382306"
---
# <a name="vml-v-text-spacing-attribute"></a>VML V-Text-Spacing (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la quantité d’espacement du texte. En lecture/écriture. **VgNumber**.

**S’applique à**

[TextPath](msdn-online-vml-textpath-element.md)

**Syntaxe de balise**

<v : *Element* style = "v-Text-Spacing : *expression* " >

**Syntaxe du script**

*Element* . style. v-Text-spacing = "*expression*"

*expression* = *élément*. style. v-espacement du texte

**Remarques**

La valeur par défaut est 100. Pour plus d’informations sur l’espacement du texte, consultez l’attribut [V-Text-Spacing-mode](msdn-online-vml-v-text-spacing-mode-attribute.md) .

*Attribut standard VML*

**Exemple**

L’letterSpacing entre chaque lettre est serré par 200 unités.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 