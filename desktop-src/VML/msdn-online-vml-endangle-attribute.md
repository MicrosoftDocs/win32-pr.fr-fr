---
title: EndAngle VML (attribut)
description: EndAngle VML (attribut)
ms.assetid: fc8276dc-8f61-42f4-b405-e92ca31e4637
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b22f157a1ccfc2337baa0bb5de747332bb78d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316361"
---
# <a name="vml-endangle-attribute"></a>EndAngle VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le point de terminaison de l’arc. Lecture/écriture. [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .

**S’applique à**

[Arc](msdn-online-vml-arc-element.md)

**Syntaxe de balise**

<v : *Element* endAngle = " *expression* " >

**Syntaxe du script**

*Element* . endAngle = "*expression*"

*expression* = *élément*. endAngle

**Remarques**

L’arc est défini en tant que trait dessiné le long d’un ovale délimité par les attributs de **style** d’une forme. La fin du trait est définie par un angle mesuré à partir de l’angle droit (12 heures) dans le sens des aiguilles d’une montre. La valeur par défaut est 90 degrés.

*Attribut standard VML*

**Exemple**

L’arc est souriant. Le point de départ est au point de 90 degré d’un ovale inscrit dans le cadre englobant de la forme. Le point de terminaison se trouve au point de 270 de l’ovale.


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 