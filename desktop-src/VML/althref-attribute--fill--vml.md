---
title: Attribut AltHRef (Fill) (VML)
description: Attribut AltHRef (Fill) (VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463310"
---
# <a name="althref-attribute-fillvml"></a>Attribut AltHRef (Fill) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit une autre référence pour une image. En lecture/écriture. **Chaîne**.

**S’applique à**

[Complète](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *Element* o :althref = " *expression* " >

**Syntaxe du script**

*Element* . althref = "*expression*"

*expression* = *élément*. althref

**Remarques**

Prend en charge la préservation des données PICT via des roundtripping HTML. Lors de l’écriture HTML, l’autre représentation (les données PICT d’origine si le fichier provient d’Apple Macintosh) est enregistrée. Lors de la lecture HTML, **AltHRef** est privilégié sur **src**.

*Attribut extensions Microsoft Office*

**Exemple**

Le remplissage de la forme a un **AltHRef** qui pointe vers un fichier nommé myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 