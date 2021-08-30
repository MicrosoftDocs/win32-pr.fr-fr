---
description: 'La position, la vélocité et l’orientation des sources et écouteurs du son dans l’espace 3D sont représentées par des coordonnées cartésiennes, qui sont des valeurs sur trois axes : l’axe des abscisses, l’axe des y et l’axe des z.'
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: Coordonnées de l’espace 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b80cee9888d5dff446939e7b923626e01700405577bbe5ef1ddbbda2cb1bb085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926679"
---
# <a name="coordinates-of-3d-space"></a>Coordonnées de l’espace 3D

La position, la vélocité et l’orientation des sources et écouteurs du son dans l’espace 3D sont représentées par des coordonnées cartésiennes, qui sont des valeurs sur trois axes : l’axe des abscisses, l’axe des y et l’axe des z.

Les axes sont relatifs à un point de vue établi par l’application. Les valeurs sur l’axe des x s’étendent de gauche à droite, sur l’axe des y de bas en haut et sur l’axe z de près à Far.

La **structure \_ vectorielle X3DAUDIO** contient des valeurs décrivant la position, la vélocité ou l’orientation sur les trois axes.

D’un point de vue conventionnel, les vecteurs sont exprimés sous la forme de trois valeurs entre parenthèses et séparées par des virgules, dans l’ordre (x, y, z).

Pour la position, les valeurs sont en unités universelles définies par l’utilisateur.

Pour la vélocité, le vecteur décrit le taux de mouvement le long de chaque axe en unités universelles par seconde.

Pour l’orientation, les valeurs sont exprimées en unités arbitraires et sont relatives les unes aux autres. Par exemple, si la vue de base du monde 3D est dirigée vers le nord vers l’horizon et que l’orientation de l’écouteur est (-1, 0, 1), l’écouteur est orienté nord-ouest. Étant donné que les valeurs d’un vecteur ne sont pas en unités absolues, le vecteur peut être également exprimé sous la forme (-5, 0, 5) ou (-0,25, 0, 0,25).

les vecteurs 3D fonctionnent de la même façon que les vecteurs 2D, mais avec un axe supplémentaire dans le sens inverse. Vous pouvez voir comment les vecteurs fonctionnent dans l’espace 2D en les dessinant sur une feuille de papier de graphique. Laissez les valeurs augmenter du bas vers le haut du papier, et de gauche à droite. Une ligne dessinée de (0,0) à (1,1) a la même orientation, ou direction, qu’une ligne tirée de (0,0) à (5, 5). Toutefois, la deuxième ligne indique une distance ou une vélocité supérieure.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts audio courants](common-audio-concepts.md)
</dt> <dt>

[Présentation de X3DAudio](x3daudio-overview.md)
</dt> </dl>

 

 



