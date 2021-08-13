---
title: EndArrowLength VML (attribut)
description: EndArrowLength VML (attribut)
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb11c07300127acd2446c7c2c643e0a891957d63f7650044514427f3e8535d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601349"
---
# <a name="vml-endarrowlength-attribute"></a>EndArrowLength VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit une longueur de flèche pour la fin d’une ligne. En lecture/écriture. **VgArrowheadLength**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *Element* endarrowlength = " *expression* " >

**Syntaxe du script**

*Element* . endarrowlength = "*expression*"

*expression* = *élément*. endarrowlength

**Remarques**

Ces valeurs comprennent :

-   Court
-   Moyenne (par défaut)
-   Long

*Attribut standard VML*

**Exemple**

Une ligne est dessinée avec une petite flèche classique à la fin du trait.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowlength="short"/>
   </v:line>
```



 

 