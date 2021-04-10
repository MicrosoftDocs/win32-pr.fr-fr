---
title: BlackLevel VML (attribut)
description: BlackLevel VML (attribut)
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5394f8b218f2eb577aa63ead5ae940fe2a49029f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031451"
---
# <a name="vml-blacklevel-attribute"></a>BlackLevel VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit l’intensité du noir dans une image. En lecture/écriture. **VgNumber**.

**S’applique à**

[ImageData](msdn-online-vml-imagedata-element.md)

**Syntaxe de balise**

<v : *Element* blacklevel = " *expression* " >

**Syntaxe du script**

*Element* . blacklevel = "*expression*"

*expression* = *élément*. blacklevel

**Remarques**

Permet de modifier le niveau de couleur afin que les noirs apparaissent comme des véritables noirs, et que toutes les autres couleurs soient visibles en tant que nuances au-dessus du noir. La valeur par défaut est 0. Bien qu’un nombre quelconque entre le nombre positif et l’infini négatif soit autorisé, les valeurs inférieures à-0,5 s’affichent en noir et les valeurs supérieures à 0,5 s’affichent comme tout en blanc.

*Attribut standard VML*

**Exemple**

L’image sera affichée avec des tons très sombres.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 