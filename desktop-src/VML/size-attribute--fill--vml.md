---
title: Size, attribut (Fill) (VML)
description: Size, attribut (Fill) (VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941054"
---
# <a name="size-attribute-fillvml"></a>Size, attribut (Fill) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la taille de l’image pour le remplissage. En lecture/écriture. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**S’applique à**

[Complète](msdn-online-vml-fill-element.md)

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



 

 