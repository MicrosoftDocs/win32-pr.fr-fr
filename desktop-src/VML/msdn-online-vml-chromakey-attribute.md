---
title: Chromakey VML (attribut)
description: Chromakey VML (attribut)
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315635"
---
# <a name="vml-chromakey-attribute"></a>Chromakey VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la valeur de couleur de l’image qui sera traitée comme transparente. En lecture/écriture. **VgColor**.

**S’applique à**

[ImageData](msdn-online-vml-imagedata-element.md)

**Syntaxe de balise**

<v : *Element* chromakey = " *expression* " >

**Syntaxe du script**

*Element* . chromakey = "*expression*"

*expression* = *élément*. chromakey

**Remarques**

Utilisez cet attribut pour rendre des parties d’une image transparentes en masquant la transparence à une couleur spécifique. Par exemple, si vous définissez la valeur **chromakey** en **noir**, toute partie de l’image qui est noire est transparente et la couleur de remplissage « s’affiche » dans cette partie de l’image.

*Attribut standard VML*

**Exemple**

Les zones de l’image qui sont de couleur noire unie deviennent transparentes, ce qui permet à la couleur de remplissage verte de s’afficher à la place dans ces zones.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 