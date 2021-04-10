---
title: Attribut angle (remplissage) (VML)
description: Attribut angle (remplissage) (VML)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031768"
---
# <a name="angle-attribute-fillvml"></a>Attribut angle (remplissage) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit l’angle d’un dégradé. En lecture/écriture. [VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .

**S’applique à**

[Complète](msdn-online-vml-fill-element.md)

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



 

 