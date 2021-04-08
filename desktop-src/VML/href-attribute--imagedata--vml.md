---
title: Attribut HRef (ImageData) (VML)
description: Attribut HRef (ImageData) (VML)
ms.assetid: vs|vml|~\shape\image\image_href.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ea1c5a5eb4c37773d012c1ff888aa372cb7717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727429"
---
# <a name="href-attribute-imagedatavml"></a>Attribut HRef (ImageData) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit une URL pour une image. En lecture/écriture. **Chaîne**.

**S’applique à**

[ImageData](msdn-online-vml-imagedata-element.md)

**Syntaxe de balise**

<v : *Element* o :href = " *expression* " >

**Syntaxe du script**

*Element* . href = "*expression*"

*expression* = *élément*. href

**Remarques**

Lorsque l’utilisateur clique sur la forme, le navigateur charge l’URL. L’attribut **href** est similaire à l’attribut HTML **href** standard des points d’ancrage.

L’utilisation de cet attribut facilite la création d’images buttonswith sur une page Web.

Cet attribut est utilisé par Microsoft Office uniquement si une image a été liée et incorporée. Microsoft Word dispose d’une interface utilisateur pour l’insertion d’images de cette façon.

*Attribut extensions Microsoft Office*

**Exemple**

Quand l’utilisateur clique sur l’image, le navigateur charge la page d’accueil de Microsoft Corporation.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata o:href="https://www.microsoft.com" src="kids.jpg"/>
   </v:shape>
```



 

 