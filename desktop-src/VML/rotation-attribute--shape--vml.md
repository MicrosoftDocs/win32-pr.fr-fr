---
title: Attribut rotation (Shape) (VML)
description: Attribut rotation (Shape) (VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031806"
---
# <a name="rotation-attribute-shapevml"></a>Attribut rotation (Shape) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit l’angle de rotation d’une forme. En lecture/écriture. [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "rotation : *expression* " >

**Syntaxe du script**

*Element* . rotation = "*expression*"

*expression* = *Element*. rotation

**Remarques**

La valeur en degrés peut être positive ou négative, et les valeurs supérieures à 360 sont modulées sur un cercle de 360 degrés. Les angles positifs sont dans le sens horaire. La valeur par défaut est 0.

Notez que la forme est repositionnée après la rotation pour refléter les nouvelles coordonnées du rectangle englobant.

Notez également que pour les scripts, l’attribut de **style** n’est pas utilisé et que la **rotation** est traitée comme un attribut direct de la forme.

L’attribut **rotation** est semblable à l’attribut de **rotation** HTML standard pour les styles.

*Attribut standard VML*

**Voir aussi**

**Exemple**

Le rectangle sera incliné 45 degrés.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



[Exemple d’attribut de rotation](/previous-versions/bb264091(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 