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
# <a name="constructing-and-drawing-curves"></a><span data-ttu-id="580e5-103">Génération et dessin de courbes</span><span class="sxs-lookup"><span data-stu-id="580e5-103">Constructing and Drawing Curves</span></span>

<span data-ttu-id="580e5-104">GDI+ prend en charge plusieurs types de courbes : ellipses, arcs, splines cardinales et splines de Bézier.</span><span class="sxs-lookup"><span data-stu-id="580e5-104">GDI+ supports several types of curves: ellipses, arcs, cardinal splines, and Bézier splines.</span></span> <span data-ttu-id="580e5-105">Une ellipse est définie par son rectangle englobant ; un arc est une partie d’une ellipse définie par un angle de départ et un angle de balayage.</span><span class="sxs-lookup"><span data-stu-id="580e5-105">An ellipse is defined by its bounding rectangle; an arc is a portion of an ellipse defined by a starting angle and a sweep angle.</span></span> <span data-ttu-id="580e5-106">Une spline cardinale est définie par un tableau de points et un paramètre de tension. la courbe passe en douceur à chaque point du tableau, et le paramètre de tension influence le mode de courbure de la courbe.</span><span class="sxs-lookup"><span data-stu-id="580e5-106">A cardinal spline is defined by an array of points and a tension parameter — the curve passes smoothly through each point in the array, and the tension parameter influences the way the curve bends.</span></span> <span data-ttu-id="580e5-107">Une spline de Bézier est définie par deux points de terminaison et deux points de contrôle : la courbe ne traverse pas les points de contrôle, mais les points de contrôle influencent la direction et le pli à mesure que la courbe passe d’un point de terminaison à l’autre.</span><span class="sxs-lookup"><span data-stu-id="580e5-107">A Bézier spline is defined by two end points and two control points — the curve does not pass through the control points, but the control points influence the direction and bend as the curve goes from one end point to the other.</span></span>

<span data-ttu-id="580e5-108">Les rubriques suivantes couvrent plus en détail les splines cardinales et les splines de Bézier :</span><span class="sxs-lookup"><span data-stu-id="580e5-108">The following topics cover cardinal splines and Bézier splines in more detail:</span></span>

-   [<span data-ttu-id="580e5-109">Dessiner des splines cardinales</span><span class="sxs-lookup"><span data-stu-id="580e5-109">Drawing Cardinal Splines</span></span>](-gdiplus-drawing-cardinal-splines-use.md)
-   [<span data-ttu-id="580e5-110">Dessin de splines de Bézier</span><span class="sxs-lookup"><span data-stu-id="580e5-110">Drawing Bézier Splines</span></span>](-gdiplus-drawing-bezier-splines-use.md)

 

 



