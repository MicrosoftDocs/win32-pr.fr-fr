---
title: Attribut FillColor de VML
description: Attribut FillColor de VML
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbacd688d25745222b5dcaf62691bff8546dad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511095"
---
# <a name="vml-fillcolor-attribute"></a>Attribut FillColor de VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la couleur du pinceau qui remplit le tracé fermé d’une forme. En lecture/écriture. [IVgColor](msdn-online-vml-ivgcolor.md) .

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *élément* FillColor = " *expression* " >

**Syntaxe du script**

*Element* . FillColor = "*expression*"

*expression* = *élément*. FillColor

**Remarques**

La valeur **FillColor** est dupliquée à partir de l’attribut **Color** de l’élément **Fill** .

*Attribut standard VML*

**Voir aussi**

[Forme](shape-element--vml.md), [remplissage](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)

**Exemple**

La couleur de remplissage du rectangle est rouge.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemple d’attribut FillColor](/previous-versions/bb229668(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 