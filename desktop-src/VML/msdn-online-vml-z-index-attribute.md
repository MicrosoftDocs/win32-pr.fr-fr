---
title: Attribut Z-index VML
description: Attribut Z-index VML
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc358719f3fa15fa40293e40eef924bd248286c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941056"
---
# <a name="vml-z-index-attribute"></a>Attribut Z-index VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine l’ordre d’affichage des formes qui se chevauchent. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "z-index : *expression* " >

**Syntaxe du script**

*Element* . style. ZIndex = "*expression*"

*expression* = *Element*. style. ZIndex

**Remarques**

L’attribut **z-index** est similaire à l’attribut **z-index** HTML standard pour les styles.

Ces valeurs comprennent :



| Valeur | Description                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto  | L’ordre dans lequel les formes apparaissent dans la page HTML sera utilisé, de bas en haut.                                                                                                                         |
| order | Nombre qui représente la priorité d’empilage. Une forme avec un nombre plus élevé s’affiche comme si elle wereoverlapping (au début) d’une forme avec un nombre inférieur. Vous pouvez utiliser des nombres négatifs. |



 

*Attribut standard VML*

**Exemple**

La forme rouge s’affiche dans l’avant de la forme bleue, car elle a un index z plus élevé.


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



[Exemple d’attribut Z-index](/previous-versions/ms530275(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 