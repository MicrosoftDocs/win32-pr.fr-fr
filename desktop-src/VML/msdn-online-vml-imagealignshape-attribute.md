---
title: ImageAlignShape VML (attribut)
description: ImageAlignShape VML (attribut)
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86090936556ba8a4f022024f292293b396d953d46962423a222b172adc2a15f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600467"
---
# <a name="vml-imagealignshape-attribute"></a>ImageAlignShape VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine l’alignement de l’image de trait. En lecture/écriture. **VgTriState**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v :

élément *imagealignshape = "* expression *" >*

**Syntaxe du script**

Element *. imagealignshape = "* expression *"*

*=* élément expression *. imagealignshape*

**Remarques**

Si la **valeur est true**, aligne l’image avec la forme, sinon aligne l’image avec la fenêtre. La valeur par défaut est **True**.

*Attribut standard VML*

**Exemple**

L’image est alignée avec la fenêtre.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 