---
description: Dans Windows GDI+, une couleur est une valeur 32 bits avec 8 bits chacun pour alpha, rouge, vert et bleu.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Fusion alpha de lignes et de remplissages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13fe306dbf31c2a60a0bd38bf71b9e96edb201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864285"
---
# <a name="alpha-blending-lines-and-fills"></a>Fusion alpha de lignes et de remplissages

Dans Windows GDI+, une couleur est une valeur 32 bits avec 8 bits chacun pour alpha, rouge, vert et bleu. La valeur alpha indique la transparence de la couleur, c’est-à-dire l’étendue de la fusion de la couleur avec la couleur d’arrière-plan. Les valeurs alpha sont comprises entre 0 et 255, où 0 représente une couleur entièrement transparente et 255 représente une couleur entièrement opaque.

La fusion alpha est une fusion pixel par pixel des données de couleur d’arrière-plan et de la source. Chacun des trois composants (rouge, vert, bleu) d’une couleur source donnée est fusionné avec le composant correspondant de la couleur d’arrière-plan en fonction de la formule suivante :

displayColor = sourceColor × alpha/255 + backgroundColor × (255 – alpha)/255

Par exemple, supposons que le composant rouge de la couleur source est 150 et que le composant rouge de la couleur d’arrière-plan est 100. Si la valeur alpha est 200, le composant rouge de la couleur résultante est calculé comme suit :

150 × 200 / 255 + 100 × (255 – 200) / 255 = 139

Les rubriques suivantes traitent de la fusion alpha plus en détail :

-   [Dessin de lignes opaques et semi-transparentes](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [Dessiner avec des pinceaux opaques et translucides](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [Utilisation du mode de composition pour contrôler la fusion alpha](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [Utilisation d’une matrice de couleurs pour définir des valeurs alpha dans des images](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [Définition des valeurs alpha de pixels individuels](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



