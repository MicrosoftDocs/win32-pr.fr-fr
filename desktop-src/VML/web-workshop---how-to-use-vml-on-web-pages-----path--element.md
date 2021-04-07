---
title: Utilisation de l’élément Path
description: Utilisation de l’élément Path
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Atelier Web, élément Path
- conception de pages Web, élément Path
- Langage VML (VML), élément Path
- VML (langage VML), élément Path
- Vector Graphics, élément Path
- élément Path
- Éléments VML, chemin d’accès
- Formes VML, élément Path
- Langage VML (VML), personnalisation des contours de forme
- VML (langage VML), personnalisation des contours de forme
- graphiques vectoriels, personnalisation des contours de forme
- Formes VML, personnalisation des plans
- personnalisation des contours de forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba82d0ab946ef8937b68b4934f9c4d928bd25225
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729749"
---
# <a name="using-the-path-element"></a>Utilisation de l’élément Path

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Vous avez appris que vous pouvez utiliser les éléments de forme prédéfinis VML, tels que `<oval>` ,,,,, `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` et `<arc>` pour dessiner une forme. Dans cette rubrique, nous allons vous montrer comment utiliser le `<path>` sous-élément pour personnaliser le contour d’une forme.

Vous pouvez placer le `<path>` sous-élément à l’intérieur de l' `<shape>` `<shapetype>` élément ou. Vous pouvez ensuite utiliser les attributs de propriété du `<path>` sous-élément pour personnaliser le contour de la forme.

Par exemple, pour dessiner la forme personnalisée illustrée dans l’image suivante, vous pouvez utiliser le `<path>` sous-élément pour définir le contour de la forme, comme indiqué dans la représentation VML suivante :

![shape1.gif (1301 octets)](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   Les valeurs `m 8,65` indiquent que le dessin commence au point (8, 65).
-   Les valeurs `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indiquent qu’une ligne droite commence au point actuel (8, 65) et se termine au point donné (72, 65), qui devient le nouveau point actuel. Une nouvelle ligne commence au point actuel (72, 65) et se termine au point donné, qui devient le nouveau point actuel, et ainsi de suite, jusqu’au point final (60, 100).
-   `x` indique que le chemin d’accès se fermera par une ligne droite qui commence au point actuel (60, 100) et se termine au point d’origine (8, 65).
-   `e` indique l’arrêt du dessin.

Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858391) .

 

 