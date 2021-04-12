---
title: Attribut DashStyle de VML
description: Attribut DashStyle de VML
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4651af9ade605166121c7225925e3bf1ed8264ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315317"
---
# <a name="vml-dashstyle-attribute"></a>Attribut DashStyle de VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Spécifie le motif de point et de tiret pour un trait. En lecture/écriture. **VgLineDashStyle**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *Element* DashStyle = " *expression* " >

**Syntaxe du script**

*Element* . DashStyle = "*expression*"

*expression* = *Element*. DashStyle

**Remarques**

Ces valeurs comprennent :

-   Unie (par défaut)
-   ShortDash
-   ShortDot
-   ShortDashDot
-   ShortDashDotDot
-   Points
-   Tiret
-   LongDash
-   Tiret-point
-   LongDashDot
-   LongDashDotDot

L’attribut **DashStyle** permet à l’utilisateur de spécifier un modèle de tirets personnalisé. Cette opération s’effectue à l’aide d’une série de nombres. Les styles de tirets sont définis en termes de longueur du tiret (partie dessinée du trait) et de la longueur de l’espace entre les tirets. Les longueurs sont exprimées par rapport à la largeur de la ligne : la longueur de « 1 » est égale à la largeur de la ligne. Le style d' **extrémité** est appliqué à chaque tiret, le style de flèche n’est pas. La chaîne définit d’abord la longueur du tiret, puis la longueur de l’espace. Cela peut être répété pour former des styles de tiret complexes. La chaîne doit toujours contenir une paire de nombres ; Si elle contient un nombre impair de nombres, la dernière peut être ignorée.

Le tableau suivant répertorie des valeurs typiques et une description de l’effet prévu. « 0 » implique un point qui doit être quatre symétrique (avec des extrémités arrondies, il doit s’agir d’un cercle). Si le capuchon de fin de ligne est « plat », une visionneuse doit choisir un tiret de système d’exploitation intégré si possible (en d’autres termes. un point rapide à dessiner. Le tableau suivant présente quelques exemples.



| DashStyle     | Description                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| « 2 2 »         | Tirets courts. Chaque tiret et l’espace entre est le double de la largeur de la ligne.                        |
| « 0 2 »         | Pointillé. L’espace entre est le double de la largeur de la ligne.                                                  |
| « 2 2 0 2 »     | Tiret cadratin-point.                                                                                      |
| « 2 2 0 2 0 2 » | Bref tiret-point-point.                                                                                  |
| « 1 2 »         | Cédé. Chaque tiret correspond à la largeur de la ligne, tandis que chaque espace est deux fois plus large que la largeur de la ligne.            |
| « 4 2 »         | Bord. Chaque tiret correspond à quatre fois la largeur de la ligne, tandis que chaque espace est deux fois plus large que la largeur de la ligne. |
| « 8 2 »         | Long Dash.                                                                                           |
| « 4 2 1 2 »     | Tiret-point.                                                                                            |
| « 8 2 1 2 »     | Long tiret-point.                                                                                       |
| « 8 2 1 2 1 2 » | Long tiret-point-point.                                                                                   |



 

*Attribut standard VML*

**Exemple**

La forme a un style de tiret d’alternance des tirets et des points.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200,200, 200,1 x e">
   <v:stroke dashstyle="dashdot"/>
   </v:shape>
```



 

 