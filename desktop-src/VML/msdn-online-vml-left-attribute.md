---
title: Attribut VML à gauche
description: Attribut VML à gauche
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17810d7635d4b8194f2bd2df258a900cb534581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463599"
---
# <a name="vml-left-attribute"></a>Attribut VML à gauche

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine la position de la forme par rapport à l’élément à gauche dans le Workflow. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "left : *expression* " >

**Syntaxe du script**

*Element* . style. Left = "*expression*"

*expression* = *Element*. style. Left

**Remarques**

L’attribut **Left** est semblable à l’attribut HTML standard **Left** pour les styles.

Les unités peuvent être mappées à l’élément parent ou peuvent être en unités absolues. Cet attribut ne sera pas écrit pour les formes ancrées en ligne.

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

La valeur de gauche de la forme est définie sur 1 dans l’exemple ci-dessous.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemple d’attribut Left](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 