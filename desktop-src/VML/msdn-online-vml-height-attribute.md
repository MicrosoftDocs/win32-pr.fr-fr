---
title: Attribut de hauteur VML
description: Attribut de hauteur VML
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41751e4863fdb128dbbedf2e3abf8e7f0a6736d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101840"
---
# <a name="vml-height-attribute"></a>Attribut de hauteur VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Spécifie la hauteur de la forme. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "height : *expression* " >

**Syntaxe du script**

*Element* . style. Height = "*expression*"

*expression* = *Element*. style. Height

**Remarques**

L’attribut **Height** est semblable à l’attribut **Height** HTML standard pour les styles.

Les unités peuvent être mappées à l’élément parent ou peuvent être en unités absolues.

Ces valeurs comprennent :



| Valeur      | Description                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Position par défaut d’un élément dans le Flow de la page.                                                                                                          |
| units      | Nombre avec un indicateur d’unités absolues (cm, mm, in, PT, PC ou px) ou un indicateur d’unités relatives (em ou ex). Si aucune unité n’est donnée, les pixels (PX) sont pris en compte. |
| percentage | Valeur exprimée sous la forme d’un pourcentage de la hauteur de l’objet parent.                                                                                                   |



 

*Attribut standard VML*

**Voir aussi**

[Unités](msdn-online-vml-units.md)

**Exemple**

La hauteur de la forme est définie sur 30.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



[Exemple d’attribut Height](/previous-versions/bb229671(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 