---
description: Une courbe régulière est un ensemble de pixels en surbrillance sur un affichage raster (ou des points sur une page imprimée) qui définissent le périmètre (ou une partie du périmètre) d’une section conique.
ms.assetid: b7a1b544-8b50-45ba-918c-17472c46c8b8
title: Courbes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e694edeb535dbc7dbd4191a5a2b0b44556b810e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863673"
---
# <a name="curves"></a>Courbes

Une courbe régulière est un ensemble de pixels en surbrillance sur un affichage raster (ou des points sur une page imprimée) qui définissent le périmètre (ou une partie du périmètre) d’une section conique. Une courbe irrégulière est un ensemble de pixels qui définissent une courbe qui ne correspond pas au périmètre d’une section conique. Le point de fin est exclu d’une courbe de la même façon qu’elle est exclue d’une ligne.

Quand une application appelle l’une des fonctions de dessin courbé, GDI divise la courbe en plusieurs segments de ligne discrets très petits. Après avoir déterminé les points de terminaison (point de départ et point de fin) pour chacun de ces segments de ligne, GDI détermine les pixels (ou points) qui définissent chaque ligne en appliquant son DDA.

Une application peut dessiner une ellipse ou une partie d’une ellipse en appelant la fonction [**arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) . Cette fonction dessine la courbe dans le périmètre d’un rectangle invisible appelé un rectangle englobant. La taille de l’ellipse est spécifiée par deux rayons invisibles qui s’étendent du centre du rectangle aux côtés du rectangle. L’illustration suivante montre un arc (une partie d’une ellipse) dessiné à l’aide de la fonction **arc** .

![Diagramme montrant un arc représentant trois quarts d’un cercle entier](images/cslcv-03.png)

Lors de l’appel de la fonction [**arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) , une application spécifie les coordonnées du rectangle englobant et des radiales. L’illustration précédente montre le rectangle et les rayons avec des lignes en pointillés tandis que l’arc réel a été dessiné à l’aide d’une ligne pleine.

Lors du dessin de l’arc d’un autre objet, l’application peut appeler les fonctions [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) et [**GetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) pour contrôler la direction (dans le sens inverse des aiguilles d’une montre) dans laquelle l’objet est dessiné. La direction par défaut pour dessiner des arcs et d’autres objets est dans le sens inverse des aiguilles d’une autre.

En plus de dessiner des ellipses ou des parties de ellipses, les applications peuvent dessiner des courbes irrégulières appelées courbes de Bézier. Une *courbe de Bézier* est une courbe irrégulière dont la courbure est définie par quatre points de contrôle (P1, P2, P3 et P4). Les points de contrôle P1 et P4 définissent les points de départ et de fin de la courbe, tandis que les points de contrôle P2 et P3 définissent la forme de la courbe en marquant les points où la courbe inverse l’orientation, comme indiqué dans le diagramme suivant.

![Illustration montrant deux courbes de Bézier, chacune comprise entre un point de départ et un point de fin, et chacune avec deux points de contrôle](images/cslcv-04.png)

Une application peut dessiner des courbes irrégulières en appelant la fonction [**Polybézier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) , en fournissant les points de contrôle appropriés.

 

 



