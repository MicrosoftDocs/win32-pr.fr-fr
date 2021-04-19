---
title: Attribut width VML
description: Attribut width VML
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b3d4917d76b3c8820186b04b2e77537e6a6ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510475"
---
# <a name="vml-width-attribute"></a>Attribut width VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la largeur de la forme. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "width : *expression* " >

**Syntaxe du script**

*Element* . style. Width = "*expression*"

*expression* = *Element*. style. Width

**Remarques**

L’attribut **Width** est semblable à l’attribut **Width** HTML standard pour les styles.

Les unités peuvent être mappées à l’élément parent ou peuvent être en unités absolues.

Ces valeurs comprennent :



| Valeur      | Description                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Position par défaut d’un élément dans le Flow de la page.                                                                                                          |
| units      | Nombre avec un indicateur d’unités absolues (cm, mm, in, PT, PC ou px) ou un indicateur d’unités relatives (em ou ex). Si aucune unité n’est donnée, les pixels (PX) sont pris en compte. |
| percentage | Valeur exprimée sous la forme d’un pourcentage de la largeur de l’objet parent.                                                                                                    |



 

*Attribut standard VML*

**Voir aussi**

[Unités](msdn-online-vml-units.md)

**Exemple**

La largeur de la forme est 25.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



[Exemple d’attribut width](/previous-versions/bb264101(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 