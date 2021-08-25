---
title: Attribut AltHRef (Stroke) (VML)
description: Attribut AltHRef (Stroke) (VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0cbdbe82330d154675b135f7e9f35869c8f47e25715680d97df05e5511a01e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867440"
---
# <a name="althref-attribute-strokevml"></a>Attribut AltHRef (Stroke) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Spécifie une autre référence pour une image. En lecture/écriture. **Chaîne**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *Element* o :althref = " *expression* " >

**Syntaxe du script**

*Element* . althref = "*expression*"

*expression* = *élément*. althref

**Remarques**

Prend en charge la préservation des données PICT via des roundtripping HTML. Lors de l’écriture HTML, l’autre représentation (c’est-à-dire, les données PICT d’origine si le fichier provient du Macintosh) est enregistrée. Lors de la lecture HTML, **AltHRef** est privilégié sur **src**.

*Microsoft Office Attribut extensions*

**Exemple**

Le trait de la forme a un **AltHRef** qui pointe vers un fichier nommé myimage.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 