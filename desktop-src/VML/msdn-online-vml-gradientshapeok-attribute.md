---
title: GradientShapeOK VML (attribut)
description: GradientShapeOK VML (attribut)
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382672"
---
# <a name="vml-gradientshapeok-attribute"></a>GradientShapeOK VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si un tracé de dégradé est constitué de chemins d’accès concentriques répétés. En lecture/écriture. **VgTriState**.

**S’applique à**

[Chemin d’accès](msdn-online-vml-path-element.md)

**Syntaxe de balise**

<v : *Element* gradientshapeok = " *expression* " >

**Syntaxe du script**

*Element* . gradientshapeok = "*expression*"

*expression* = *élément*. gradientshapeok

**Remarques**

Si la **valeur est true**, le tracé est rempli avec un dégradé concentrique en utilisant le chemin d’accès comme forme répétée du dégradé. La valeur par défaut est **false**.

*Attribut standard VML*

**Exemple**

Le tracé est rempli avec un remplissage dégradé concentrique constitué de rectangles répétés.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 