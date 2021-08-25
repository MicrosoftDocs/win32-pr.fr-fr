---
title: ID, attribut (Fill) (VML)
description: ID, attribut (Fill) (VML)
ms.assetid: 56865772-51bd-4729-8e56-6b00e3c6bed0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f317cef4d588444f5c01770dafd5b56af0d2bca48ee228ff789a11b46348bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007869"
---
# <a name="id-attribute-fillvml"></a>ID, attribut (Fill) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Nom qui fournit un identificateur unique pour un remplissage. En lecture/écriture. **Chaîne**.

**S’applique à**

[Remplir](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *élément* ID = « *expression* » >

**Syntaxe du script**

*Element* . ID = "*expression*"

*expression* = *élément*. ID

**Remarques**

Utilisez **ID** pour faire référence à un remplissage spécifique. Une fois que vous avez créé un remplissage et lui avez attribué un ID, vous pouvez utiliser le nom de l’ID lorsque vous souhaitez manipuler le remplissage.

*Attribut standard VML*

**Exemple**

La forme a un ID de remplissage appelé « myfill ».


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill id="myfill"/>
   </v:shape>
```



 

 