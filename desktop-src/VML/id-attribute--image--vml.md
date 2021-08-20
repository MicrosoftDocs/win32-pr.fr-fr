---
title: ID, attribut (image) (VML)
description: ID, attribut (image) (VML)
ms.assetid: d85a6d56-5896-4ac0-85c7-0edc72928c62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3d09c2f3ec4a58e303c54ca9fd191b6872f7e3b12b30f9a8707be54108f46c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117939486"
---
# <a name="id-attribute-imagevml"></a>ID, attribut (image) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit un nom qui fournit un identificateur unique pour une image. En lecture/écriture. **Chaîne**.

**S’applique à**

[ImageData](msdn-online-vml-imagedata-element.md)

**Syntaxe de balise**

<v : *élément* ID = « *expression* » >

**Syntaxe du script**

*Element* . ID = "*expression*"

*expression* = *élément*. ID

**Remarques**

Utilisez **ID** pour faire référence à une image spécifique. Une fois que vous avez créé une image et lui avez attribué un ID, vous pouvez utiliser le nom de l’ID lorsque vous souhaitez manipuler l’image.

**Attribut standard VML**

**Exemple**

La forme a un ID **ImageData** appelé « myImage ».


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata id="myimage" src="kids.jpg"/>
   </v:shape>
```



 

 