---
title: StartArrowWidth VML (attribut)
description: StartArrowWidth VML (attribut)
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d427db8e504fca57fc77b24b7b5fa1360ed7716276cd67b43c55ee8d0552d8f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513239"
---
# <a name="vml-startarrowwidth-attribute"></a>StartArrowWidth VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit la largeur de la flèche pour le début d’une ligne. En lecture/écriture. **VgArrowheadWidth**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *Element* startarrowwidth = " *expression* " >

**Syntaxe du script**

*Element* . startarrowwidth = "*expression*"

*expression* = *élément*. startarrowwidth

**Remarques**

Ces valeurs comprennent :

-   Restreindre
-   Moyenne (par défaut)
-   Large

Attribut standard VML

**Exemple**

Une ligne est dessinée avec une flèche classique larges au début du trait.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 