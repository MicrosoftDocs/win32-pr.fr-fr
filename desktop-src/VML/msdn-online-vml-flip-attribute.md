---
title: Attribut Flip VML
description: Attribut Flip VML
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730148"
---
# <a name="vml-flip-attribute"></a>Attribut Flip VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Change l’orientation d’une forme. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "Flip : *expression* " >

**Syntaxe du script**

*Element* . style. Flip = "*expression*"

*expression* = *Element*. style. Flip

**Remarques**

Ces valeurs comprennent :



| Valeur | Description                                           |
|-------|-------------------------------------------------------|
| x     | Retournez le long de l’axe y, en inversant les coordonnées *x*. |
| y     | Retournez le long de l’axe *x*, en inversant les coordonnées y. |
| xy    | Retournez le long de l’axe y et de l’axe *x*.                  |
| yx    | Retournez sur l’axe des *x* et de l’axe des *y*.                |



 

*Attribut standard VML*

**Voir aussi**

[VgFlipOrientation](msdn-online-vector-markup-language-object-model-reference.md)

**Exemple**

La forme est retournée le long de l’axe *y* en inversant les coordonnées *x* .


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



[Exemple d’attribut Flip](/previous-versions/bb229670(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 