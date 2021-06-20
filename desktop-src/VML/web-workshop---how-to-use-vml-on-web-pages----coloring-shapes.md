---
title: Colorer les formes
description: Cet article décrit les formes de coloration dans VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Atelier Web, formes de coloration
- conception de pages Web, colorer les formes
- Langage VML (VML), colorer les formes
- VML (langage VML), formes de coloration
- graphiques vectoriels, colorer les formes
- Formes VML, coloration
- colorer les formes
- Langage VML (VML), noms de couleur de mot clé
- VML (langage VML), noms de couleur de mot clé
- graphiques vectoriels, noms de couleur de mot clé
- noms des couleurs des mots clés
- Langage VML (VML), triplets RVB
- VML (langage VML), triplets RGB
- graphiques vectoriels, triplets RGB
- Triplets RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c203debd01d4234ae58900a023944511f9fc73c1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407742"
---
# <a name="coloring-shapes"></a>Colorer les formes

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Comme nous l’avons mentionné dans les sections précédentes, vous pouvez utiliser « Red » pour représenter une couleur en rouge, « Blue » pour représenter une couleur en bleu, et ainsi de suite. Dans cette rubrique, nous allons vous montrer comment dessiner des formes dans les couleurs de votre choix.

VML étend la syntaxe des couleurs HTML et CSS. Lorsque le type d’attribut d’un élément VML est Color, tel que **FillColor** et **StrokeColor** , vous pouvez exprimer la couleur à l’aide d’un [nom de couleur de mot clé](#keyword-color-name) ou d’un [triplet RVB](#rgb-triplet).

[![retour au début ](images/top.gif) en haut](#top)

## <a name="keyword-color-name"></a>Nom de la couleur du mot clé

Le code HTML 4,0 définit une liste de noms de couleurs de mot clé. Il s’agit de l’Aqua, du noir, du bleu, de la fuchsia, du gris, du vert, de la chaux, du marron, de la marine, de l’Olivier, du violet, du rouge, de l’argent, du bleu vert et du jaune. La valeur RVB pour ces 16 couleurs est définie dans la [spécification HTML 4,0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .

Par exemple, vous pouvez dessiner un rectangle rempli en jaune en spécifiant `fillcolor="yellow"` , et lui attribuer un contour bleu en spécifiant `strokecolor="blue"` , comme illustré dans la représentation VML suivante :

![color1.gif (305 octets)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





[![retour au début ](images/top.gif) en haut](#top)

## <a name="rgb-triplet"></a>Triplet RVB

Si la couleur n’est pas un [nom de couleur de mot clé](#keyword-color-name), vous pouvez exprimer la couleur sous la forme d’un triple nombre décimal ou d’une tripleté hexadécimale RVB. Avec les triplets RVB, vous pouvez spécifier des valeurs pour les composants rouge, vert et bleu de la couleur, en affectant à chaque composant une valeur comprise entre 0 et 255 en décimal, ou 00 à FF en hexadécimal.

Par exemple, vous pouvez créer un rectangle rempli avec une couleur personnalisée avec une valeur RVB de 253, 249, 186 en décimal en spécifiant `fillcolor="rgb(253,249, 186)"` ou `fillcolor="#FDF9BA"` , comme indiqué dans la représentation VML suivante. Au format hexadécimal, la valeur 253 devient FD, 249 devient F9 et 186 devient BA.

![color2.gif (305 octets)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





Si le RVB au format hexadécimal a un modèle tel que XXYYZZ, vous pouvez l’abréger en XYZ. Par exemple, « \# 66FF99 » peut être écrit en tant que « \# 6F9 ».

[![retour au début ](images/top.gif) en haut](#top)

## <a name="summary"></a>Résumé

Dans VML, vous pouvez représenter une couleur dans l’un des formats suivants :

1.  FillColor = "Blue"
2.  FillColor = "RGB (0, 0255)"
3.  FillColor = " \# 0000FF"

 

 