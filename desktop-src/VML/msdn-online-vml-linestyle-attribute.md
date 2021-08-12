---
title: VML (attribut LineStyle)
description: VML (attribut LineStyle)
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90be9c2aceeb3663f55c92e1140eb6a12f66aa23dd8856d0da63f0a306d8cd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598282"
---
# <a name="vml-linestyle-attribute"></a>VML (attribut LineStyle)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le style de ligne du trait. En lecture/écriture. **Chaîne**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *élément* LineStyle = " *expression* " >

**Syntaxe du script**

*Element* . LineStyle = "*expression*"

*expression* = *Element*. LineStyle

**Remarques**

Ces valeurs comprennent :

-   Unique (valeur par défaut)
-   ThinThin
-   ThinThick
-   ThickThin
-   ThickBetweenThin

*Attribut standard VML*

**Exemple**

Une double ligne est dessinée avec deux traits fins.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 