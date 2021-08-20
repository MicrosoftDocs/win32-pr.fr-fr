---
title: Attribut de couleur (trait) (VML)
description: Attribut de couleur (trait) (VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17b3dd30d95765c98ec754526349b2bdc274696112043065fa7ddc7d894b582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125369"
---
# <a name="color-attribute-strokevml"></a>Attribut de couleur (trait) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 