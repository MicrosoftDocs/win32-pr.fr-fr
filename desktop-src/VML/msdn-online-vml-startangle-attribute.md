---
title: Attribut VML StartAngle
description: Attribut VML StartAngle
ms.assetid: 334ae52a-cde4-427e-8080-ec789b4d9d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7237c20acb3e2b9a5b2445dc1ffed4e23a93bb55958831f5607410cde092dbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796159"
---
# <a name="vml-startangle-attribute"></a>Attribut VML StartAngle

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 