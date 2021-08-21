---
title: Attribut gamma VML
description: Attribut gamma VML
ms.assetid: 47a4d10e-f5ef-457b-92dd-bce5dae59b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c333bcb30a66aa9a87bc8402d64734e40504a0c49a38a8543c7fa97acfee7e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118845402"
---
# <a name="vml-gamma-attribute"></a>Attribut gamma VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit la quantité de contraste pour une image. En lecture/écriture. **VgNumber**.

**S’applique à**

[ImageData](msdn-online-vml-imagedata-element.md)

**Syntaxe de balise**

<v : *Element* gamma = " *expression* " >

**Syntaxe du script**

*Element* . gamma = "*expression*"

*expression* = . gamma ( *élément*)

**Remarques**

La diminution de la valeur gamma inférieure à 1 modifie une image pour la rendre plus contrastée, tandis que les valeurs supérieures à 1 diminuent le contraste. Les valeurs utiles sont comprises entre 0,3 et environ 3. La valeur par défaut est 0.

*Attribut standard VML*

**Exemple**


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gamma=".7" src="gamera.jpg"/>
   </v:shape>
```



 

 