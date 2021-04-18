---
title: Control1 VML (attribut)
description: Control1 VML (attribut)
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88516592c371a19a7a3b001a708c507d3103927a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512732"
---
# <a name="vml-control1-attribute"></a>Control1 VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le premier point de contrôle d’une courbe de Bézier. En lecture/écriture. **VgVector2D**.

**S’applique à**

[Apprendre](msdn-online-vml-curve-element.md)

**Syntaxe de balise**

<v : *Element* Control1 = " *expression* " >

**Syntaxe du script**

*Element* . Control1 = "*expression*"

*expression* = *élément*. Control1

**Remarques**

Définit le premier point de contrôle d’une courbe de Bézier cubique dans l’espace de coordonnées de l’élément parent. Si le parent n’est pas un élément VML, l' [unité](msdn-online-vml-units.md) par défaut est un pixel (mais dans, cm, mm, PT, PC peut également être spécifié). La valeur par défaut est 10, 10.

*Attribut standard VML*

**Exemple**

La courbe est souriante. Elle commence à gauche et se termine à droite. Les deux points de contrôle sont situés le long de la procédure de façon à extraire la courbe vers le dessous pour obtenir l’apparence d’un sourire.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 