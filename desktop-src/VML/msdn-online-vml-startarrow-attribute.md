---
title: StartArrow VML (attribut)
description: StartArrow VML (attribut)
ms.assetid: 484dfcdb-f68d-40f9-9a83-18abb054d1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2c17569750c1e655a5538ca5bf233e49f827e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941168"
---
# <a name="vml-startarrow-attribute"></a>StartArrow VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la pointe de flèche pour le début d’une ligne. En lecture/écriture. **Chaîne**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *Element* StartArrow = " *expression* " >

**Syntaxe du script**

*Element* . StartArrow = "*expression*"

*expression* = *élément*. StartArrow

**Remarques**

Ces valeurs comprennent :

-   Aucun (par défaut)
-   Bloquer
-   Classique
-   Losange
-   Ovale
-   Ouvrir

Attribut standard VML

**Exemple**

Une ligne est dessinée avec une flèche classique au début du trait.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke StartArrow="classic"/>
   </v:line>
```



 

 