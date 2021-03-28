---
description: 'Une spline B&\# 233 ; est définie par quatre points : un point de départ, deux points de contrôle et un point de terminaison.'
ms.assetid: af19e82b-0d13-4fb0-981e-8d5dd1bbfb36
title: Dessin de splines de Bézier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea97d25f482372c387239e8f9083b31e3b2d912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755716"
---
# <a name="drawing-bezier-splines"></a><span data-ttu-id="64230-103">Dessin de splines de Bézier</span><span class="sxs-lookup"><span data-stu-id="64230-103">Drawing Bezier Splines</span></span>

<span data-ttu-id="64230-104">Une spline de Bézier est définie par quatre points : un point de départ, deux points de contrôle et un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="64230-104">A Bézier spline is defined by four points: a start point, two control points, and an end point.</span></span> <span data-ttu-id="64230-105">L’exemple suivant dessine une spline de Bézier avec le point de départ (10, 100) et le point de terminaison (200, 100).</span><span class="sxs-lookup"><span data-stu-id="64230-105">The following example draws a Bézier spline with start point (10, 100) and end point (200, 100).</span></span> <span data-ttu-id="64230-106">Les points de contrôle sont (100, 10) et (150, 150) :</span><span class="sxs-lookup"><span data-stu-id="64230-106">The control points are (100, 10) and (150, 150):</span></span>


```
Point p1(10, 100);   // start point
Point c1(100, 10);   // first control point
Point c2(150, 150);  // second control point
Point p2(200, 100);  // end point
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBezier(&pen, p1, c1, c2, p2);
```



<span data-ttu-id="64230-107">L’illustration suivante montre la spline de Bézier obtenue ainsi que son point de départ, les points de contrôle et le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="64230-107">The following illustration shows the resulting Bézier spline along with its start point, control points, and end point.</span></span> <span data-ttu-id="64230-108">L’illustration montre également la forme convexe de la spline, qui est un polygone formé en reliant les quatre points par des lignes droites.</span><span class="sxs-lookup"><span data-stu-id="64230-108">The illustration also shows the spline's convex hull, which is a polygon formed by connecting the four points with straight lines.</span></span>

![Illustration montrant une spline de Bézier avec deux points de terminaison et deux points de contrôle](images/bezierspline1.png)

<span data-ttu-id="64230-110">Vous pouvez utiliser la méthode [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pour dessiner une séquence de splines de Bézier connectées.</span><span class="sxs-lookup"><span data-stu-id="64230-110">You can use the [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw a sequence of connected Bézier splines.</span></span> <span data-ttu-id="64230-111">L’exemple suivant dessine une courbe composée de deux splines de Bézier connectées.</span><span class="sxs-lookup"><span data-stu-id="64230-111">The following example draws a curve that consists of two connected Bézier splines.</span></span> <span data-ttu-id="64230-112">Le point de terminaison de la première spline de Bézier est le point de départ de la deuxième spline de Bézier.</span><span class="sxs-lookup"><span data-stu-id="64230-112">The end point of the first Bézier spline is the start point of the second Bézier spline.</span></span>


```
Point p[] = {
   Point(10, 100),   // start point of first spline
   Point(75, 10),    // first control point of first spline
   Point(80, 50),    // second control point of first spline
   Point(100, 150),  // end point of first spline and 
                     // start point of second spline
   Point(125, 80),   // first control point of second spline
   Point(175, 200),  // second control point of second spline
   Point(200, 80)};  // end point of second spline
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBeziers(&pen, p, 7);
```



<span data-ttu-id="64230-113">L’illustration suivante montre les splines connectées, ainsi que les sept points.</span><span class="sxs-lookup"><span data-stu-id="64230-113">The following illustration shows the connected splines along with the seven points.</span></span>

![Illustration montrant des points de terminaison et des points de contrôle de deux splines qui partagent l’un des points de terminaison](images/bezierspline2.png)

 

 



