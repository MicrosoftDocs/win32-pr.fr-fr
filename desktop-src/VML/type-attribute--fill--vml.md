---
title: Attribut type (Fill) (VML)
description: Attribut type (Fill) (VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883318c82758178ee9693a1199cb76c5798e351ec809aecb54fe7d0a266d85d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596140"
---
# <a name="type-attribute-fillvml"></a>Attribut type (Fill) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine le type de remplissage. En lecture/écriture. **VgFillType**.

**S’applique à**

[Remplir](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : type d' *élément* = « *expression* » >

**Syntaxe du script**

*Element* . type = "*expression*"

*expression* = *Element*. type

**Remarques**

Ces valeurs comprennent :



| Type           | Description                                                             |
|----------------|-------------------------------------------------------------------------|
| Solid          | Le motif de remplissage est plein. Par défaut.                                     |
| dégradé       | Les couleurs de remplissage se combinent dans un dégradé linéaire de bas en haut. |
| gradientradial | Les couleurs de remplissage se combinent dans un dégradé radial.                    |
| tile           | L’image de remplissage est en mosaïque.                                                |
| modèle        | L’image est utilisée pour créer un modèle à l’aide des couleurs de remplissage.            |
| frame          | L’image est étirée pour remplir la forme.                               |



 

**Attribut standard VML**

**Exemple**

Un remplissage de premier plan rouge et un remplissage d’arrière-plan bleu sont créés à l’aide du modèle de l’image myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 