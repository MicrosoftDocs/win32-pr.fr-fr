---
description: 'GDI+ prend en charge plusieurs types de courbes : ellipses, arcs, splines cardinales et B&\# 233 ;.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Génération et dessin de courbes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b78ebd7ce81099d5b7f483939c0f4b238d1f124357bf6e1863b25fedb7e22f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015219"
---
# <a name="constructing-and-drawing-curves"></a>Génération et dessin de courbes

GDI+ prend en charge plusieurs types de courbes : ellipses, arcs, splines cardinales et splines de Bézier. Une ellipse est définie par son rectangle englobant ; un arc est une partie d’une ellipse définie par un angle de départ et un angle de balayage. Une spline cardinale est définie par un tableau de points et un paramètre de tension. la courbe passe en douceur à chaque point du tableau, et le paramètre de tension influence le mode de courbure de la courbe. Une spline de Bézier est définie par deux points de terminaison et deux points de contrôle : la courbe ne traverse pas les points de contrôle, mais les points de contrôle influencent la direction et le pli à mesure que la courbe passe d’un point de terminaison à l’autre.

Les rubriques suivantes couvrent plus en détail les splines cardinales et les splines de Bézier :

-   [Dessiner des splines cardinales](-gdiplus-drawing-cardinal-splines-use.md)
-   [Dessin de splines de Bézier](-gdiplus-drawing-bezier-splines-use.md)

 

 



