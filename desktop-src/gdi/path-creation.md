---
description: Pour créer un chemin d’accès et le sélectionner dans un DC, vous devez d’abord définir les points qui le décrivent.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Création du chemin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf2acfeb5c3e31f2f846bff06cf0a0d5b880fc95ed314538036632a83076b8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831549"
---
# <a name="path-creation"></a>Création du chemin

Pour créer un chemin d’accès et le sélectionner dans un DC, vous devez d’abord définir les points qui le décrivent. Pour ce faire, appelez la fonction [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) , en spécifiant les fonctions de dessin appropriées, puis en appelant la fonction [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) . Cette combinaison de fonctions (**BeginPath**, Drawing Functions et **EndPath**) constitue un *crochet de chemin*. La liste suivante répertorie les fonctions de dessin qui peuvent être utilisées.

-   [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [**Es**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [**Secteurs**](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [**Polybézier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [**PolyBezierTo**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [**Polydraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [**Polygone**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [**Polyligne**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [**PolylineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [**Polypolygone**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [**Polyligne**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [**Rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Quand une application appelle [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), le système sélectionne le chemin d’accès associé dans le contrôleur de réseau spécifié. (Si un autre chemin avait déjà été sélectionné dans le contrôleur de réseau, le système supprime ce chemin sans l’enregistrer.) Une fois que le système a sélectionné le chemin d’accès dans le contrôleur de réseau, une application peut fonctionner sur le chemin d’accès de l’une des manières suivantes :

-   Dessine le contour du tracé (à l’aide du stylet actuel).
-   Paint l’intérieur du tracé (à l’aide du pinceau actuel).
-   Dessinez le contour et remplissez l’intérieur du tracé.
-   Modifiez le chemin d’accès (en convertissant les courbes en segments de ligne).
-   Convertit le tracé en tracé de clip.
-   Convertit le tracé en une région.
-   Aplatir le tracé en convertissant chaque courbe du tracé en une série de segments de ligne.
-   Récupérez les coordonnées des lignes et des courbes qui composent un tracé.

 

 



