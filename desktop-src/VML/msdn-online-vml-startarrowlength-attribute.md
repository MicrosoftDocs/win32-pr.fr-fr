---
title: StartArrowLength VML (attribut)
description: StartArrowLength VML (attribut)
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25446737118c546727d769d54d98e4503faaadd063102fa98a417ebea13c976d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119395829"
---
# <a name="vml-startarrowlength-attribute"></a>StartArrowLength VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit la longueur de la flèche pour le début d’une ligne. En lecture/écriture. **VgArrowheadLength**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *Element* startarrowlength = " *expression* " >

**Syntaxe du script**

*Element* . startarrowlength = "*expression*"

*expression* = *élément*. startarrowlength

**Remarques**

Ces valeurs comprennent :

-   Court
-   Moyenne (par défaut)
-   Long

Attribut standard VML

**Exemple**

Une ligne est dessinée avec une petite flèche classique au début du trait.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 