---
title: Size, attribut (Fill) (VML)
description: Size, attribut (Fill) (VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26568151961fb2186f8cf49ae25d9f2835665b8fd52a96a4d3a79e954c50ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754144"
---
# <a name="size-attribute-fillvml"></a>Size, attribut (Fill) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit la taille de l’image pour le remplissage. En lecture/écriture. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**S’applique à**

[Remplir](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *Element* size = " *expression* " >

**Syntaxe du script**

*Element* . Size = "*expression * * *"**

*expression* = *Element*. Size

**Remarques**

La valeur par défaut est la taille de l’image d’origine. Les tailles supérieures à shapewill affichent une version agrandie mais tronquée de l’image.

*Attribut standard VML*

**Exemple**

Bien que la taille d’origine de l’image soit de 50 à 50 points, l’image est affichée sous la forme d’une image 10 par 10 au centre du remplissage.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 