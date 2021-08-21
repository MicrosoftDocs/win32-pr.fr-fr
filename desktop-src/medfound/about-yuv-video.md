---
description: À propos de la vidéo YUV
ms.assetid: 089f42f2-1e5b-4d4b-98a4-9ef0ca2823c1
title: À propos de la vidéo YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499a8adfe1a43a22fe9bdd9ff4e576b7a14c398a9dafc0b945647d7225ad581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744241"
---
# <a name="about-yuv-video"></a>À propos de la vidéo YUV

La vidéo numérique est souvent encodée au format *YUV* . Cet article explique les concepts généraux de la vidéo YUV, ainsi que certains termes, sans passer par la mathématique du traitement vidéo YUV.

Si vous avez travaillé avec des graphiques informatiques, vous êtes probablement familiarisé avec la couleur RVB. Une couleur RVB est encodée à l’aide de trois valeurs : rouge, vert et bleu. Ces valeurs correspondent directement aux portions du spectre visible. Les trois valeurs RVB forment un système de coordonnées mathématique, appelé *espace colorimétrique*. Le composant Red définit un axe de ce système de coordonnées, Blue définit le deuxième et Green définit le troisième, comme indiqué dans l’illustration suivante. Toute couleur RVB valide se trouve quelque part dans cet espace de couleurs. Par exemple, le magenta pur est 100% Blue, 100% Red et 0% Green.

![Diagramme montrant l’espace colorimétrique RVB](images/8ec60365-ed5c-41f7-9da9-be46aa82896a.gif)

Bien que RVB soit un moyen courant de représenter des couleurs, d’autres systèmes de coordonnées sont possibles. Le terme *YUV* fait référence à une famille d’espaces de couleurs, qui encodent tous les informations de luminosité séparément des informations de couleur. Comme RVB, YUV utilise trois valeurs pour représenter n’importe quelle couleur. Ces valeurs sont les suivantes : Y, U et V. (en fait, cette utilisation du terme « YUV » est techniquement inexacte. Dans la vidéo de l’ordinateur, le terme YUV fait presque toujours référence à un espace de couleurs particulier nommé Y’CbCr, présenté plus loin. Toutefois, YUV est souvent utilisé comme un terme général pour tout espace de couleurs qui fonctionne selon les mêmes principes que Y’CbCr.

Le composant Y, également appelé *luminance*, représente la valeur de luminosité de la couleur. Le symbole prime (') est utilisé pour différencier la luminance d’une valeur étroitement liée, *luminance*, qui est désignée Y. la luminance est dérivée des valeurs RVB *linéaires* , tandis que la luminance est dérivée des valeurs RVB *non linéaires* (corrigées par gamma). La luminance est une mesure plus proche de la luminosité réelle, mais la luminance est plus pratique pour des raisons techniques. Le symbole prime est souvent omis, mais les espaces de couleurs YUV utilisent toujours la luminance, pas la luminance.

La luminance est dérivée d’une couleur RVB en utilisant une moyenne pondérée des composants rouge, vert et bleu. Pour la télévision de définition standard, la formule suivante est utilisée :

`Y' = 0.299R + 0.587G + 0.114B`

Cette formule reflète le fait que l’oeil humain est plus sensible à certaines longueurs d’onde de lumière que d’autres, ce qui affecte la luminosité perçue d’une couleur. Bleu clair apparaît en DIMM, le vert apparaît plus clair et le rouge sur un autre emplacement. Cette formule reflète également les caractéristiques physiques des phosphores utilisées dans les premières télévisions. Une formule plus récente, en tenant compte de la technologie de télévision moderne, est utilisée pour la télévision haute définition :

`Y' = 0.2125R + 0.7154G + 0.0721B`

L’équation de luminance pour la télévision de définition standard est définie dans une spécification nommée ITU-R BT. 601. Pour la télévision haute définition, la spécification pertinente est ITU-R BT. 709.

Les composants que vous et V, également appelés valeurs de *chrominance* ou valeurs de *différence de couleur* , sont dérivés en soustrayant la valeur Y des composants rouge et bleu de la couleur RVB d’origine :

`U = B - Y'`

`V = R - Y'`

Ensemble, ces valeurs contiennent suffisamment d’informations pour récupérer la valeur RVB d’origine.

## <a name="benefits-of-yuv"></a>Avantages des YUV

La télévision analogique utilise des YUV en partie pour des raisons historiques. Les signaux TV couleur analogiques ont été conçus pour assurer une compatibilité descendante avec les télévisions en noir et blanc. Le signal de couleur de la télévision contient les informations chromatiques (vous et V) superposées sur le signal de luminance. Les télévisions en noir et blanc ignorent la chrominance et affichent le signal combiné sous la forme d’une image en nuances de gris. (Le signal est conçu de sorte que la chrominance n’interfère pas de manière significative avec le signal de luminance.) Les télévisions en couleurs peuvent extraire la chrominance et reconvertir le signal en RVB.

YUV présente un autre avantage qui est plus pertinent aujourd’hui. L’oeil humain est moins sensible aux modifications de teintes que les changements de luminosité. Par conséquent, une image peut avoir moins d’informations chromatiques que les informations de luminance sans sacrifier la qualité perçue de l’image. Par exemple, il est courant d’échantillonner les valeurs de chrominance à la moitié de la résolution horizontale des échantillons de luminance. En d’autres termes, pour chaque échantillon de luminance dans une ligne de pixels, il existe un échantillon U et un exemple V. En supposant que 8 bits sont utilisés pour encoder chaque valeur, un total de 4 octets sont nécessaires pour tous les deux pixels (deux Y', un U et un V), pour une moyenne de 16 bits par pixel, ou 30% inférieur à l’encodage RVB 24 bits équivalent.

YUV n’est pas, par nature, plus compact que le format RVB. À moins que le Chroma ne soit sous-échantillonné, un pixel YUV a la même taille qu’un pixel RVB. En outre, la conversion de RVB en YUV n’est pas perdue. S’il n’existe aucun sous-échantillonnage, un pixel YUV peut être reconverti en RVB sans perte d’informations. Le sous-échantillonnage rend une image YUV plus petite et perd également certaines informations de couleur. En cas de réalisation correcte, toutefois, la perte n’est pas significative.

## <a name="yuv-in-computer-video"></a>Vidéo YUV dans l’ordinateur

Les formules répertoriées précédemment pour YUV ne sont pas les conversions exactes utilisées dans la vidéo numérique. La vidéo numérique utilise généralement une forme de YUV appelée Y’CbCr. Fondamentalement, Y’CbCr fonctionne en mettant à l’échelle les composants YUV sur les plages suivantes :



| Composant | Plage                              |
|-----------|------------------------------------|
| Y        | 16 – 235                             |
| CB/CR     | 16 – 240, avec 128 représentant zéro |



 

Ces plages supposent une précision de 8 bits pour les composants Y’CbCr. Voici la dérivation exacte de Y’CbCr, à l’aide de la définition de la luminance BT. 601 :

1.  Commencez par les valeurs RVB dans la plage \[ 0... \] 1. En d’autres termes, le noir pur est 0 et le blanc pur est 1. Important, il s’agit de valeurs RVB non linéaires (corrigées gamma).
2.  Calculez la luminance. Pour BT. 601, Y' = 0.299 R + 0.587 G + 0.114 B, comme décrit précédemment.
3.  Calcule les valeurs de différence de chrominance intermédiaires (B-Y') et (R-Y'). Ces valeurs sont comprises entre +/-0,886 pour (B-Y) et +/-0,701 pour (R-Y').
4.  Mettez à l’échelle les valeurs de différence Chroma comme suit :

    PB = (0,5/(1-0,114)) × (B-Y)

    PR = (0,5/(1-0,299)) × (R-Y')

    Ces facteurs de mise à l’échelle sont conçus pour fournir les deux valeurs de la même plage numérique, +/-0,5. Ensemble, ils définissent un espace de couleurs YUV nommé Y’PbPr. Cet espace colorimétrique est utilisé dans la vidéo du composant analogique.

5.  Mettez à l’échelle les valeurs Y’PbPr pour récupérer les valeurs Y’CbCr finales :

    Y' = 16 + 219 × Y'

    CB = 128 + 224 × PB

    CR = 128 + 224 × PR

Ces derniers facteurs de mise à l’échelle produisent la plage des valeurs répertoriées dans le tableau précédent. Bien entendu, vous pouvez convertir RGB directement en Y’CbCr sans stocker les résultats intermédiaires. Les étapes sont répertoriées séparément ici pour montrer comment Y’CbCr dérive des équations YUV d’origine indiquées au début de cet article.

Le tableau suivant montre les valeurs RVB et YCbCr pour différentes couleurs, à nouveau à l’aide de la définition de la luminance BT. 601.



| Couleur   | R   | G   | B   | Y  | Libéré  | Cr  |
|---------|-----|-----|-----|-----|-----|-----|
| Noir   | 0   | 0   | 0   | 16  | 128 | 128 |
| Rouge     | 255 | 0   | 0   | 81  | 90  | 240 |
| Vert   | 0   | 255 | 0   | 145 | 54  | 34  |
| Bleu    | 0   | 0   | 255 | 41  | 240 | 110 |
| Cyan    | 0   | 255 | 255 | 170 | 166 | 16  |
| Magenta | 255 | 0   | 255 | 106 | 202 | 222 |
| Jaune  | 255 | 255 | 0   | 210 | 16  | 146 |
| Blancs   | 255 | 255 | 255 | 235 | 128 | 128 |



 

Comme le montre ce tableau, CB et CR ne correspondent pas à des idées intuitives sur la couleur. Par exemple, le blanc pur et le noir pur contiennent tous les deux des niveaux neutres de CB et CR (128). Les valeurs les plus élevées et les plus basses pour CB sont Blue et Yellow, respectivement. Pour CR, les valeurs les plus élevées et les plus basses sont rouge et cyan.

## <a name="for-more-information"></a>Pour plus d'informations

-   [Formats YUV 8 bits recommandés pour le rendu vidéo](recommended-8-bit-yuv-formats-for-video-rendering.md)
-   Keith Jack. Vidéo démystifié, cinquième édition. Newnes, 2007.
-   Charles A. Poynton. Présentation technique de la vidéo numérique. Wiley, 1996.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de média vidéo](video-media-types.md)
</dt> <dt>

[Types de médias](media-types.md)
</dt> </dl>

 

 



