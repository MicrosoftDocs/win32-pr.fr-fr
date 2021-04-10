---
title: FocusPosition VML (attribut)
description: FocusPosition VML (attribut)
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102317"
---
# <a name="vml-focusposition-attribute"></a>FocusPosition VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le centre d’un dégradé radial. En lecture/écriture. **VgVector2D**.

**S’applique à**

[Complète](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *Element* focusposition = " *expression* " >

**Syntaxe du script**

*Element* . focusposition = "*expression*"

*expression* = *élément*. focusposition

**Remarques**

Spécifie les dégradés radiaux positionfor centraux. Le vecteur est une fraction de la largeur et de la hauteur de la forme. Le premier est un pourcentage du remplissage jusqu’au bord gauche ; le deuxième est un pourcentage du remplissage vers le haut. La valeur par défaut est 0,0. Pour positionner un remplissage radial au centre d’une forme, utilisez la valeur 50%, 50%.

*Attribut standard VML*

**Exemple**

Le remplissage radial est centré afin que le bleu démarre au centre et rayonne vers l’extérieur, passant progressivement en rouge au moment où il atteint les bords extérieurs et les angles.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 