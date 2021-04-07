---
title: Attribut Top VML
description: Attribut Top VML
ms.assetid: faad0c76-3566-4a51-962b-971667df2025
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c76a39035bc3dd3f0ae348280561e614d7dab4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728244"
---
# <a name="vml-top-attribute"></a>Attribut Top VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la position de la forme par rapport à l’élément situé au-dessus de celui-ci dans le déroulement de la page. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "Top : *expression* " >

**Syntaxe du script**

*Element* . style.Top = "*expression*"

*expression* = *élément*. style.Top

**Remarques**

L’attribut **Top** est semblable à l’attribut HTML **Top** standard pour les styles.

Les unités peuvent être mappées à l’élément parent ou peuvent être en unités absolues. Cet attribut ne peut pas être écrit pour les formes ancrées en ligne.

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

Le bord supérieur de la forme est de 5 pixels au-dessous de l’objet qui le précède dans le déroulement de la page.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:5;left:1;width:20;height:20">
   </v:rect>
```



[Exemple d’attribut Top](/previous-versions/bb264098(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 