---
title: Sur l’attribut (TextPath) (VML)
description: Sur l’attribut (TextPath) (VML)
ms.assetid: b4a88473-6d5f-42b3-afd6-86f602c83724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7b1361bc0600ecca64e252ac25254d26b340cfd34a481de9424017de3381ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345812"
---
# <a name="on-attribute-textpathvml"></a>Sur l’attribut (TextPath) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit si le texte est affiché. En lecture/écriture. **VgTriState**.

**S’applique à**

[TextPath](msdn-online-vml-textpath-element.md)

**Syntaxe de balise**

<v : *Element* on = " *expression* " >

**Syntaxe du script**

*Element* . on = "*expression*"

*expression* = *élément*. on

**Remarques**

La valeur par défaut est **False**. Cette valeur doit être définie sur **true** pour afficher du texte sur un tracé de texte.

*Attribut standard VML*

**Exemple**

Le texte du tracé de texte s’affiche.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 