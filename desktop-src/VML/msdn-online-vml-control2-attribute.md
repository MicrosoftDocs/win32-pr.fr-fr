---
title: Control2 VML (attribut)
description: Control2 VML (attribut)
ms.assetid: fd0f92fa-ae70-46c9-bfbe-fad8deea34f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 702c0eee9ba861a73ec6d9f0fd07cca22a551c92c5add5498cd0e33522419fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999249"
---
# <a name="vml-control2-attribute"></a>Control2 VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le deuxième point de contrôle d’une courbe de Bézier. En lecture/écriture. **VgVector2D**.

**S’applique à**

[Apprendre](msdn-online-vml-curve-element.md)

**Syntaxe de balise**

<v : *Element* Control2 = " *expression* " >

**Syntaxe du script**

*Element* . Control2 = "*expression*"

*expression* = *élément*. Control2

**Remarques**

Définit le deuxième point de contrôle d’une courbe de Bézier cubique dans l’espace de coordonnées de l’élément parent. Si le parent n’est pas un élément VML, l' [unité](msdn-online-vml-units.md) par défaut est un pixel (mais dans, cm, mm, PT, PC peut également être spécifié). La valeur par défaut est 20,0.

*Attribut standard VML*

**Exemple**

La courbe est souriante. Elle commence à gauche et se termine à droite. Les deux points de contrôle sont situés le long de la procédure de façon à extraire la courbe vers le dessous pour obtenir l’apparence d’un sourire.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 