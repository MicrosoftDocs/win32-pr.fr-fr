---
title: From, attribut (Line) (VML)
description: From, attribut (Line) (VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950b3cae8e3b73efdc3a92bdc49a0b9e4366e224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730005"
---
# <a name="from-attribute-linevml"></a>From, attribut (Line) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le point de départ d’une ligne. En lecture/écriture. **VgVector2D**.

**S’applique à**

[Ligne](msdn-online-vml-line-element.md)

**Syntaxe de balise**

<v : *élément* from = " *expression* " >

**Syntaxe du script**

*Element* . from = "*expression*"

*expression* = *élément*. from

**Remarques**

Définit le point de départ de la ligne dans l’espace de coordonnées de l’élément parent. Si le parent n’est pas un élément VML, l' [unité](msdn-online-vml-units.md) par défaut est un pixel (mais dans, cm, mm, PT, PC peut également être spécifié). La valeur par défaut est 0, 0.

*Attribut standard VML*

**Exemple**

La ligne commence à un emplacement de 10 points vers le haut et de 10 points à droite du coin supérieur gauche de l’espace parent.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 