---
title: Origin, attribut (Fill) (VML)
description: Origin, attribut (Fill) (VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc33ae1f4cf7c588ae9b3f40ff8c445be88192bae1dfc86a3593eea931befb25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959219"
---
# <a name="origin-attribute-fillvml"></a>Origin, attribut (Fill) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le centre d’une image de remplissage. En lecture/écriture. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**S’applique à**

[Remplir](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *élément* Origin = " *expression* " >

**Syntaxe du script**

*Element* . Origin = "*expression*"

*expression* = *élément*. Origin

**Remarques**

Spécifie un point par rapport à l’angle supérieur gauche de l’image ; ce point est traité comme l’origine de l’image. La valeur par défaut est le centre de l’image. Le vecteur est une fraction de la largeur et de la hauteur de l’image.

*Attribut standard VML*

**Exemple**

L’image du remplissage est décalée vers la gauche jusqu’au point 50% de la largeur de la forme.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 