---
title: Color, attribut (Fill) (VML)
description: Color, attribut (Fill) (VML)
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ec72cab0562ae675ca2e22992369a7c0ad6534207cd2a6f6141f56c64e2f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125379"
---
# <a name="color-attribute-fillvml"></a>Color, attribut (Fill) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit la couleur d’un remplissage. En lecture/écriture. **VgColor**.

**S’applique à**

[Remplir](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *Element* Color = " *expression* " >

**Syntaxe du script**

*Element* . Color = "*expression*"

*expression* = *Element*. Color

**Remarques**

Remplace l’attribut **FillColor** d’une forme. La valeur par défaut est **blanc**.

*Attribut standard VML*

**Exemple**

La couleur de remplissage de la forme est verte.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 