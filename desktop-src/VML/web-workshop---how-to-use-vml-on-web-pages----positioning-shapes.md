---
title: Positionnement des formes
description: cet article décrit le positionnement des formes dans VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Atelier Web, positionnement des formes
- conception de pages Web, positionnement des formes
- Langage VML (VML), positionnement des formes
- VML (langage VML), positionnement des formes
- graphiques vectoriels, positionner des formes
- Formes VML, positionnement
- positionnement des formes
- Langage VML (VML), style de position statique
- VML (langage VML), style de position statique
- graphiques vectoriels, style de position statique
- style de position statique
- Langage VML (VML), style de position relative
- VML (langage VML), style de position relative
- graphiques vectoriels, style de position relative
- style de position relative
- Langage VML (VML), style de position absolue
- VML (langage VML), style de position absolue
- graphiques vectoriels, style de position absolue
- style de position absolue
- Langage VML (VML), style de position de l’index z
- VML (langage VML), style de position de l’index z
- graphiques vectoriels, style de position de l’index z
- style de position de l’index z
- Langage VML (VML), style de la position de rotation
- VML (langage VML), style de position de rotation
- graphiques vectoriels, style de position de rotation
- style de position de rotation
- Langage VML (VML), retourner le style de position
- VML (langage VML), retourner le style de position
- graphiques vectoriels, retourner le style de position
- retourner le style de position
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4f9747ffafc5f4c4aa9f90cc880c83e7fbee7de35f5c419efc40062b47115a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512760"
---
# <a name="positioning-shapes"></a>Positionnement des formes

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Vous avez appris à dessiner et à colorier des formes sur une page Web à l’aide de VML. Dans cette rubrique, vous allez utiliser VML pour positionner les graphiques avec précision sur une page Web.

VML utilise la même syntaxe que celle définie dans les sections [Model Model](https://www.w3.org/TR/PR-CSS2/box.mdl) et [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) de [CSS2](https://www.w3.org/TR/PR-CSS2/) pour positionner les formes sur une page Web. Vous pouvez utiliser [static](#static), [relative](#relative)ou [Absolute](#absolute) pour déterminer où se trouve le point de base sur une page Web. Vous pouvez ensuite utiliser les attributs de style **supérieur** et **gauche** pour spécifier le décalage à partir du point de base auquel la zone conteneur pour la forme est positionnée.

Vous pouvez également utiliser [z-index](#z-index) pour spécifier l’ordre de plan des formes sur une page Web.

En outre, VML fournit une [rotation](#rotation) et un [retournement](#flip) pour faire pivoter ou retourner des formes.

Dans cette rubrique :

-   [static](#static)
-   [relative](#relative)
-   [absolute](#absolute)
-   [index z](#z-index)
-   [CRIC](#rotation)
-   [flip](#flip)
-   [Résumé](#summary)

## <a name="static"></a>static

Le style de position par défaut est static, ce qui indique aux navigateurs de positionner la forme au point actuel (le point de base) dans le déroulement du texte et d’ignorer les paramètres dans les attributs de style **supérieur** et **gauche** .

Par exemple, dans la représentation VML suivante, l’ovale rouge est positionné juste après le texte « début de la forme : », comme illustré dans l’image suivante :

![Shape1 \-ps.gif (2123 octets)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





[![retour au début ](images/top.gif) en haut](#top)

## <a name="relative"></a>relative

L’affectation de la valeur « relative » à l’attribut de style position vous permet de placer la zone conteneur avec un décalage à partir du point actuel (le point de base) dans le déroulement du texte. Le décalage est déterminé par les paramètres dans les attributs de style **supérieur** et **gauche** . N’oubliez pas que la zone conteneur positionnée sur relative occupe de l’espace dans le texte.

Par exemple, dans la représentation VML suivante, l’ovale rouge est positionné à 20 points à partir de la gauche et 10 points à partir du haut par rapport au point actuel dans le texte, comme illustré dans l’image suivante :

![shape3.gif (2048 octets)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





[![retour au début ](images/top.gif) en haut](#top)

## <a name="absolute"></a>absolute

La définition de l’attribut de style position sur « Absolute » vous permet de placer la zone conteneur sur une distance exacte de l’angle supérieur gauche (le point de base) de son élément parent (l’élément positionné qui contient la forme). Sachez que la zone conteneur qui est positionnée comme absolue n’occupe pas de place dans le texte.

Par exemple, dans la représentation VML suivante, l’ovale rouge est contenu dans l' `<body>` élément (la page Web entière); par conséquent, le point de base se trouve dans l’angle supérieur gauche de la page Web. La zone conteneur pour l’ovale est positionnée exactement à 20 points à partir de la gauche et de 10 points à partir du haut, par rapport à l’angle supérieur gauche de la page Web, comme illustré dans l’image suivante :

![shape2.gif (2006 octets)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





[![retour au début ](images/top.gif) en haut](#top)

## <a name="z-index"></a>z-index

Il est possible de positionner une forme qui chevauche une autre forme. Normalement, le graphique qui est listé en dernier dans le code HTML apparaît en haut.

Dans VML, vous pouvez contrôler l’ordre de plan à l’aide de l’attribut de style **z-index** . La valeur de cet attribut peut être zéro, un entier positif ou un entier négatif. Le graphique qui a une plus grande valeur d’index z est affiché en haut du graphique qui a une plus petite valeur d’index z. Lorsque les deux graphiques ont la même valeur z-index, le graphique qui est listé en dernier dans le code HTML apparaît en haut.

Par exemple, dans la représentation VML suivante, l’ovale rouge s’affiche en haut du rectangle bleu. Cela est dû au fait que la valeur z-index de l’ovale rouge est supérieure à la valeur z-index du rectangle bleu.

![shape4.gif (572 octets)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





Si vous modifiez l’index z, comme indiqué dans la représentation VML suivante, l’ovale rouge se déplacera en arrière-plan du rectangle bleu.

![shape5.gif (469 octets)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





Si vous fournissez un entier négatif, vous pouvez utiliser z-index pour positionner les graphiques derrière le texte normal, comme indiqué dans la représentation VML suivante.

![shape6.gif (2125 octets)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





[![retour au début ](images/top.gif) en haut](#top)

## <a name="rotation"></a>CRIC

Vous pouvez utiliser l’attribut de style de **rotation** pour spécifier le nombre de degrés d’activation d’une forme sur son axe. Une valeur positive indique une rotation dans le sens des aiguilles d’une montre ; une valeur négative indique une rotation dans le sens inverse des aiguilles d’une montre.

Par exemple, si vous spécifiez **style**= '... rotation : 90 ', vous pouvez faire pivoter la forme de 90 degrés dans le sens des aiguilles d’une montre.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="flip"></a>flip

Vous pouvez utiliser l’attribut **Flip** style pour retourner une forme sur son axe x ou y, conformément au tableau suivant :



| Valeur | Description                                                  |
|-------|--------------------------------------------------------------|
| x     | Retourner la forme pivotée autour de l’axe y (inversement x ordonnés) |
| y     | Retourner la forme pivotée autour de l’axe x (inverser les ordonnées y) |



 

X et y peuvent être spécifiés dans la propriété Flip.

Par exemple, si vous tapez **style**= '... Flip : x y', vous allez retourner la forme sur ses axes x et y.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="summary"></a>Récapitulatif

En fonction de ce que vous avez appris, vous pouvez positionner précisément une forme sur une page Web en procédant comme suit :

1.  Décidez où vous souhaitez que la forme apparaisse sur une page Web et la taille de la forme.
2.  Spécifiez **style**= 'position : relative (ou relative) 'pour déterminer le point de base.
3.  Utilisez **Left** et **Top** pour spécifier le décalage à partir du point de base.
4.  Utilisez la **largeur** et la **hauteur** pour spécifier la taille de la zone conteneur pour la forme.
5.  Utilisez **z-index** pour spécifier l’ordre de plan de la forme.

 

 