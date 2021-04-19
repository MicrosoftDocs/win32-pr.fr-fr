---
title: Attribut de couleur (trait) (VML)
description: Attribut de couleur (trait) (VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa91522adcba5fa854d4749dc257f5489969270
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511506"
---
# <a name="color-attribute-strokevml"></a>Attribut de couleur (trait) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la couleur d’un trait. En lecture/écriture. **VgColor**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *Element* Color = " *expression* " >

**Syntaxe du script**

*Element* . Color = "*expression*"

*expression* = *Element*. Color

**Remarques**

Remplace l’attribut **StrokeColor** d’une forme. La valeur par défaut est **noir**.

*Attribut standard VML*

**Exemple**

La couleur du trait de la forme est **verte**, et non **rouge**.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 