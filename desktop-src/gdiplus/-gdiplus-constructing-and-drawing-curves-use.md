---
description: 'GDI+ prend en charge plusieurs types de courbes : ellipses, arcs, splines cardinales et B&\# 233 ;.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Génération et dessin de courbes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f61c1aa12e3152ed65cca2da6911d2d53def81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991377"
---
# <a name="constructing-and-drawing-curves"></a>Génération et dessin de courbes

GDI+ prend en charge plusieurs types de courbes : ellipses, arcs, splines cardinales et splines de Bézier. Une ellipse est définie par son rectangle englobant ; un arc est une partie d’une ellipse définie par un angle de départ et un angle de balayage. Une spline cardinale est définie par un tableau de points et un paramètre de tension. la courbe passe en douceur à chaque point du tableau, et le paramètre de tension influence le mode de courbure de la courbe. Une spline de Bézier est définie par deux points de terminaison et deux points de contrôle : la courbe ne traverse pas les points de contrôle, mais les points de contrôle influencent la direction et le pli à mesure que la courbe passe d’un point de terminaison à l’autre.

Les rubriques suivantes couvrent plus en détail les splines cardinales et les splines de Bézier :

-   [Dessiner des splines cardinales](-gdiplus-drawing-cardinal-splines-use.md)
-   [Dessin de splines de Bézier](-gdiplus-drawing-bezier-splines-use.md)

 

 



