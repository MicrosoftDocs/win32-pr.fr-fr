---
title: Attribut VML StartAngle
description: Attribut VML StartAngle
ms.assetid: 334ae52a-cde4-427e-8080-ec789b4d9d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e779d343061ef65decb1dd21f615e054d561da28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031485"
---
# <a name="vml-startangle-attribute"></a>Attribut VML StartAngle

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le point de départ de l’arc. Lecture/écriture. [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .

**S’applique à**

[Arc](msdn-online-vml-arc-element.md)

**Syntaxe de balise**

<v : *Element* endAngle = " *expression* " >

**Syntaxe du script**

*Element* . endAngle = "*expression*"

*expression* = *élément*. endAngle

**Remarques**

L’arc est défini en tant que trait dessiné le long d’un ovale délimité par les attributs de **style** d’une forme. Le début du trait est défini par un angle mesuré à partir de l’angle droit (12 heures) dans le sens des aiguilles d’une montre. La valeur par défaut est 0 degré.

Attribut standard VML

**Exemple**

L’arc est souriant. Le point de départ est au point de 90 degré d’un ovale inscrit dans le cadre englobant de la forme. Le point de terminaison se trouve au point de 270 de l’ovale.


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 