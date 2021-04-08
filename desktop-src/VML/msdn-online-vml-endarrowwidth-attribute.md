---
title: EndArrowWidth VML (attribut)
description: EndArrowWidth VML (attribut)
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108d65fc1a06ace3d318d54a6416e0d98c0a4652
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730156"
---
# <a name="vml-endarrowwidth-attribute"></a>EndArrowWidth VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit une largeur de flèche pour la fin d’une ligne. En lecture/écriture. **VgArrowheadWidth**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *Element* endarrowwidth = " *expression* " >

**Syntaxe du script**

*Element* . endarrowwidth = "*expression*"

*expression* = *élément*. endarrowwidth

**Remarques**

Ces valeurs comprennent :

-   Restreindre
-   Moyenne (par défaut)
-   Large

*Attribut standard VML*

**Exemple**

Une ligne est dessinée avec une flèche classique larges à la fin du trait.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 