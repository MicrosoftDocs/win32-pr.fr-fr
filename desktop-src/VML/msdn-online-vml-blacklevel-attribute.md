---
title: BlackLevel VML (attribut)
description: BlackLevel VML (attribut)
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe31c9507468efd27aac9d9729a4f2ee3ddce449398b4a68bd7d79b2d029b8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057907"
---
# <a name="vml-blacklevel-attribute"></a>BlackLevel VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 