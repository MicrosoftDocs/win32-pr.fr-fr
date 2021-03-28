---
description: Pour créer un chemin d’accès, construisez un objet GraphicsPath, puis appelez des méthodes, telles que AddLine et AddCurve, pour ajouter des primitives au chemin d’accès.
ms.assetid: 66faeb73-16fb-4b7f-a4d5-a90ec2590d8c
title: Création de figures à partir de lignes, de courbes et de formes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c473dfececcaa86347dc02efdfd62131eb9a63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951703"
---
# <a name="creating-figures-from-lines-curves-and-shapes"></a><span data-ttu-id="0482e-103">Création de figures à partir de lignes, de courbes et de formes</span><span class="sxs-lookup"><span data-stu-id="0482e-103">Creating Figures from Lines, Curves, and Shapes</span></span>

<span data-ttu-id="0482e-104">Pour créer un chemin d’accès, construisez un objet [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) , puis appelez des méthodes, telles que [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) et [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), pour ajouter des primitives au chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="0482e-104">To create a path, construct a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object, and then call methods, such as [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) and [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), to add primitives to the path.</span></span>

<span data-ttu-id="0482e-105">L’exemple suivant crée un tracé qui a un seul arc. L’ARC a un angle de balayage de-180 degrés, qui est dans le sens inverse des aiguilles d’une passe dans le système de coordonnées par défaut.</span><span class="sxs-lookup"><span data-stu-id="0482e-105">The following example creates a path that has a single arc. The arc has a sweep angle of –180 degrees, which is counterclockwise in the default coordinate system.</span></span>


```
Pen pen(Color(255, 255, 0, 0));
GraphicsPath path;
path.AddArc(175, 50, 50, 50, 0, -180);
graphics.DrawPath(&pen, &path);
```



<span data-ttu-id="0482e-106">L’exemple suivant crée un tracé qui a deux figures.</span><span class="sxs-lookup"><span data-stu-id="0482e-106">The following example creates a path that has two figures.</span></span> <span data-ttu-id="0482e-107">La première figure est un arc suivi d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="0482e-107">The first figure is an arc followed by a line.</span></span> <span data-ttu-id="0482e-108">La deuxième figure est une ligne suivie d’une courbe, suivie d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="0482e-108">The second figure is a line followed by a curve, followed by a line.</span></span> <span data-ttu-id="0482e-109">La première figure est laissée ouverte et la deuxième figure est fermée.</span><span class="sxs-lookup"><span data-stu-id="0482e-109">The first figure is left open, and the second figure is closed.</span></span>


```
Point points[] = {Point(40, 60), Point(50, 70), Point(30, 90)};

Pen pen(Color(255, 255, 0, 0), 2);
GraphicsPath path;

// The first figure is started automatically, so there is
// no need to call StartFigure here.
path.AddArc(175, 50, 50, 50, 0.0f, -180.0f);
path.AddLine(100, 0, 250, 20);

path.StartFigure();
path.AddLine(50, 20, 5, 90);
path.AddCurve(points, 3);
path.AddLine(50, 150, 150, 180);
path.CloseFigure();

graphics.DrawPath(&pen, &path);
```



<span data-ttu-id="0482e-110">Outre l’ajout de lignes et de courbes aux tracés, vous pouvez ajouter des formes fermées : des rectangles, des ellipses, des secteurs et des polygones.</span><span class="sxs-lookup"><span data-stu-id="0482e-110">In addition to adding lines and curves to paths, you can add closed shapes: rectangles, ellipses, pies, and polygons.</span></span> <span data-ttu-id="0482e-111">L’exemple suivant crée un tracé qui comporte deux lignes, un rectangle et une ellipse.</span><span class="sxs-lookup"><span data-stu-id="0482e-111">The following example creates a path that has two lines, a rectangle, and an ellipse.</span></span> <span data-ttu-id="0482e-112">Le code utilise un stylet pour dessiner le tracé et un pinceau pour remplir le tracé.</span><span class="sxs-lookup"><span data-stu-id="0482e-112">The code uses a pen to draw the path and a brush to fill the path.</span></span>


```
GraphicsPath path;
Pen          pen(Color(255, 255, 0, 0), 2);
SolidBrush   brush(Color(255, 0, 0, 200));

path.AddLine(10, 10, 100, 40);
path.AddLine(100, 60, 30, 60);
path.AddRectangle(Rect(50, 35, 20, 40));
path.AddEllipse(10, 75, 40, 30);

graphics.DrawPath(&pen, &path);
graphics.FillPath(&brush, &path);
```



<span data-ttu-id="0482e-113">Le chemin d’accès dans l’exemple précédent a trois figures.</span><span class="sxs-lookup"><span data-stu-id="0482e-113">The path in the preceding example has three figures.</span></span> <span data-ttu-id="0482e-114">La première figure comprend les deux lignes, la deuxième figure le rectangle et la troisième figure l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="0482e-114">The first figure consists of the two lines, the second figure consists of the rectangle, and the third figure consists of the ellipse.</span></span> <span data-ttu-id="0482e-115">Même s’il n’y a aucun appel à [**GraphicsPath :: CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) ou [**GraphicsPath :: StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), les formes fermées intrinsèquement, telles que les rectangles et les ellipses, sont considérées comme des figures distinctes.</span><span class="sxs-lookup"><span data-stu-id="0482e-115">Even when there are no calls to [**GraphicsPath::CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) or [**GraphicsPath::StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), intrinsically closed shapes, such as rectangles and ellipses, are considered separate figures.</span></span>

 

 



