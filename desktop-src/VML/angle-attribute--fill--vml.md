---
title: Attribut angle (remplissage) (VML)
description: Attribut angle (remplissage) (VML)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aff7b330d11c95c39176d9cdcd42a839a03a6283fca706cfbc913314ea03b47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864259"
---
# <a name="angle-attribute-fillvml"></a>Attribut angle (remplissage) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit l’angle d’un dégradé. En lecture/écriture. [VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .

**S’applique à**

[Remplir](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : angle d' *élément* = « *expression* » >

**Syntaxe du script**

*Element* . angle = "*expression*"

*expression* = *Element*. angle

**Remarques**

Le vecteur d’un dégradé est perpendiculaire au vecteur du sens de fusion d’une couleur à l’autre. La valeur par défaut est 0 (zéro) degrés, qui est un vecteur horizontal de gauche à droite. Les angles positifs font pivoter le dégradé dans un sens dans le sens inverse des aiguilles d’une montre.

*Attribut standard VML*

**Exemple**

Le remplissage de la forme est composé d’un dégradé de deux couleurs, en allant du bleu au rouge à un angle de 45 degrés. Le rouge se trouve dans le coin supérieur gauche et le bleu dans le coin inférieur droit.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 