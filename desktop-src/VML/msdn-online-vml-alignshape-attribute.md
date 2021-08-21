---
title: AlignShape VML (attribut)
description: AlignShape VML (attribut)
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00e1fe8d07fb04c198ced2e2eb50d6ef0e6c020984d2d8cf12a3ca37cf09d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125312"
---
# <a name="vml-alignshape-attribute"></a>AlignShape VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si une image est alignée sur une forme. En lecture/écriture. **VgTriState**.

**S’applique à**

[Remplir](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *Element* alignshape = " *expression* " >

**Syntaxe du script**

*Element* . alignshape = "*expression*"

*expression* = *élément*. alignshape

**Remarques**

Si la **valeur est true**, l’image utilisée pour créer le remplissage est alignée avec la forme. Si la **valeur est false**, l’image utilisée pour créer le remplissage est alignée avec la fenêtre. La valeur par défaut est **True**.

*Attribut standard VML*

**Exemple**

L’image de remplissage en mosaïque créée à partir de myimage.gif est alignée avec la fenêtre, et non la forme ; même si la forme est pivotée, l’image ne l’est pas.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 