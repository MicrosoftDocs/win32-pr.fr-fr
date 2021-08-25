---
title: Attribut VML V-Text-KERN
description: Attribut VML V-Text-KERN
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5ca41b66c05af673839ccbc8ba9eb95cf652eb223cd4dd3915799e91ff6c69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974629"
---
# <a name="vml-v-text-kern-attribute"></a>Attribut VML V-Text-KERN

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si le crénage est activé. En lecture/écriture. **VgTriState**.

**S’applique à**

[TextPath](msdn-online-vml-textpath-element.md)

**Syntaxe de balise**

<v : *Element* style = "v-Text-Kern : *expression* " >

**Syntaxe du script**

*Element* . style. v-Text-KERN = "*expression*"

*expression* = *Element*. style. v-Text-KERN

**Remarques**

Si la **valeur est true**, le crénage est activé. La valeur par défaut est **False**. Le crénage est la suppression de l’espace entre certaines paires de lettres pour compenser les letterformss irréguliers. Par exemple, si le crénage est activé, un espace supplémentaire entre un « T » majuscule et un « i » minuscule serait supprimé.

*Attribut standard VML*

**Exemple**

Le crénage est activé.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 