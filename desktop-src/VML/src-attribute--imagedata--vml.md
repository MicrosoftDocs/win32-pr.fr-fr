---
title: Attribut SRC (ImageData) (VML)
description: Attribut SRC (ImageData) (VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031303"
---
# <a name="src-attribute-imagedatavml"></a>Attribut SRC (ImageData) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit une source pour l’image. En lecture/écriture. **Chaîne**.

**S’applique à**

[ImageData](msdn-online-vml-imagedata-element.md)

**Syntaxe de balise**

<v : *Element* SRC = " *expression* " >

**Syntaxe du script**

*Element* . src = "*expression*"

*expression* = *élément*. SRC

**Remarques**

Cet attribut doit toujours être utilisé avec l’élément [ImageData](msdn-online-vml-imagedata-element.md) et pointer vers des données d’image valides pour qu’une image soit affichée. Si cet attribut apparaît sans [href](https://www.bing.com/search?q=HRef) ou [title](title-attribute--imagedata--vml.md), l’image est liée.

*Attribut standard VML*

**Exemple**

La source de l’image est un fichier nommé « kids.jpg ».


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 