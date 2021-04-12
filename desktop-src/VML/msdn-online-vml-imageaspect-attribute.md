---
title: ImageAspect VML (attribut)
description: ImageAspect VML (attribut)
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315617"
---
# <a name="vml-imageaspect-attribute"></a>ImageAspect VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la manière dont les proportions de l’image du trait sont conservées. En lecture/écriture. **Chaîne**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v :

élément *imageaspect = "* expression *" >*

**Syntaxe du script**

Element *. imageaspect = "* expression *"*

*=* élément expression *. imageaspect*

**Remarques**

Ces valeurs comprennent :



| Valeur   | Description                                |
|---------|--------------------------------------------|
| Ignorer  | Ignorer les problèmes d’aspect.                      |
| Au moins | L’image est au moins aussi grande que la fonction **ImageSize**. |
| AtMost  | L’image n’est pas **supérieure à image**.     |



 

Dans chaque cas, l’attribut **ImageSize** est ajusté pour conserver l’aspect de l’image.

*Attribut standard VML*

**Exemple**

L’image du trait sera au moins aussi grande que la taille de l’image.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 