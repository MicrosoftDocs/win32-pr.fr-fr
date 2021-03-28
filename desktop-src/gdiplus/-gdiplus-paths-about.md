---
description: Les tracés sont formés en combinant des lignes, des rectangles et des courbes simples. Rappelez-vous à partir de la vue d’ensemble des graphiques vectoriels que les blocs de construction de base suivants se sont avérés les plus utiles pour dessiner des images.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Chemins (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768d01d2d945c8252125a43ee2dc79f985703da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568043"
---
# <a name="paths-gdi"></a><span data-ttu-id="4c649-104">Chemins (GDI+)</span><span class="sxs-lookup"><span data-stu-id="4c649-104">Paths (GDI+)</span></span>

<span data-ttu-id="4c649-105">Les tracés sont formés en combinant des lignes, des rectangles et des courbes simples.</span><span class="sxs-lookup"><span data-stu-id="4c649-105">Paths are formed by combining lines, rectangles, and simple curves.</span></span> <span data-ttu-id="4c649-106">Rappelez-vous à partir de la [vue d’ensemble des graphiques vectoriels](-gdiplus-overview-of-vector-graphics-about.md) que les blocs de construction de base suivants se sont avérés les plus utiles pour dessiner des images.</span><span class="sxs-lookup"><span data-stu-id="4c649-106">Recall from the [Overview of Vector Graphics](-gdiplus-overview-of-vector-graphics-about.md) that the following basic building blocks have proven to be the most useful for drawing pictures.</span></span>

-   <span data-ttu-id="4c649-107">Lignes</span><span class="sxs-lookup"><span data-stu-id="4c649-107">Lines</span></span>
-   <span data-ttu-id="4c649-108">Rectangles</span><span class="sxs-lookup"><span data-stu-id="4c649-108">Rectangles</span></span>
-   <span data-ttu-id="4c649-109">Suspension</span><span class="sxs-lookup"><span data-stu-id="4c649-109">Ellipses</span></span>
-   <span data-ttu-id="4c649-110">Arcs</span><span class="sxs-lookup"><span data-stu-id="4c649-110">Arcs</span></span>
-   <span data-ttu-id="4c649-111">Polygones</span><span class="sxs-lookup"><span data-stu-id="4c649-111">Polygons</span></span>
-   <span data-ttu-id="4c649-112">Splines cardinales</span><span class="sxs-lookup"><span data-stu-id="4c649-112">Cardinal splines</span></span>
-   <span data-ttu-id="4c649-113">Splines de Bézier</span><span class="sxs-lookup"><span data-stu-id="4c649-113">Bézier splines</span></span>

<span data-ttu-id="4c649-114">Dans Windows GDI+, l’objet [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) vous permet de collecter une séquence de ces blocs de construction en une seule unité.</span><span class="sxs-lookup"><span data-stu-id="4c649-114">In Windows GDI+, the [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object allows you to collect a sequence of these building blocks into a single unit.</span></span> <span data-ttu-id="4c649-115">L’intégralité de la séquence de lignes, de rectangles, de polygones et de courbes peut ensuite être dessinée à l’aide d’un appel à la méthode [**Graphics ::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="4c649-115">The entire sequence of lines, rectangles, polygons, and curves can then be drawn with one call to the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="4c649-116">L’illustration suivante montre un tracé créé en combinant une ligne, un arc, une spline de Bézier et une spline cardinale.</span><span class="sxs-lookup"><span data-stu-id="4c649-116">The following illustration shows a path created by combining a line, an arc, a Bézier spline, and a cardinal spline.</span></span>

![illustration d’un tracé qui combine une ligne, un arc, une spline de Bézier et une spline cardinale](images/aboutgdip02-art14.png)

<span data-ttu-id="4c649-118">La classe [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) fournit les méthodes suivantes pour créer une séquence d’éléments à dessiner : [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (pour les splines cardinales) et [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span><span class="sxs-lookup"><span data-stu-id="4c649-118">The [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) class provides the following methods for creating a sequence of items to be drawn: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (for cardinal splines), and [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span></span> <span data-ttu-id="4c649-119">Chacune de ces méthodes est surchargée ; autrement dit, chaque méthode est proposée en plusieurs variations avec différentes listes de paramètres.</span><span class="sxs-lookup"><span data-stu-id="4c649-119">Each of these methods is overloaded; that is, each method comes in several variations with different parameter lists.</span></span> <span data-ttu-id="4c649-120">Par exemple, une variante de la méthode AddLine reçoit quatre entiers et une autre variante de la méthode AddLine reçoit deux objets [**point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="4c649-120">For example, one variation of the AddLine method receives four integers, and another variation of the AddLine method receives two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span>

<span data-ttu-id="4c649-121">Les méthodes permettant d’ajouter des lignes, des rectangles et des splines de Bézier à un chemin d’accès ont des méthodes auxiliaires qui ajoutent plusieurs éléments au chemin d’accès en un seul appel : [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))et [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span><span class="sxs-lookup"><span data-stu-id="4c649-121">The methods for adding lines, rectangles, and Bézier splines to a path have plural companion methods that add several items to the path in a single call: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint)), and [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span></span> <span data-ttu-id="4c649-122">En outre, la méthode [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) a une méthode auxiliaire, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), qui ajoute une courbe fermée au tracé.</span><span class="sxs-lookup"><span data-stu-id="4c649-122">Also, the [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) method has a companion method, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), that adds a closed curve to the path.</span></span>

<span data-ttu-id="4c649-123">Pour dessiner un tracé, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) et d’un objet [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="4c649-123">To draw a path, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="4c649-124">L’objet **Graphics** fournit la méthode [**graphics ::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) , et l’objet **Pen** stocke les attributs du chemin d’accès, tels que la largeur et la couleur de ligne.</span><span class="sxs-lookup"><span data-stu-id="4c649-124">The **Graphics** object provides the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method, and the **Pen** object stores attributes of the path, such as line width and color.</span></span> <span data-ttu-id="4c649-125">L’objet **GraphicsPath** stocke la séquence de lignes, de rectangles et de courbes qui composent le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="4c649-125">The **GraphicsPath** object stores the sequence of lines, rectangles, and curves that make up the path.</span></span> <span data-ttu-id="4c649-126">Les adresses de l’objet **Pen** et de l’objet **GraphicsPath** sont passées comme arguments à la méthode **Graphics ::D rawpath** .</span><span class="sxs-lookup"><span data-stu-id="4c649-126">The addresses of the **Pen** object and the **GraphicsPath** object are passed as arguments to the **Graphics::DrawPath** method.</span></span> <span data-ttu-id="4c649-127">L’exemple suivant dessine un tracé qui se compose d’une ligne, d’une ellipse et d’une spline de Bézier.</span><span class="sxs-lookup"><span data-stu-id="4c649-127">The following example draws a path that consists of a line, an ellipse, and a Bézier spline.</span></span>


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="4c649-128">L’illustration suivante montre le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="4c649-128">The following illustration shows the path.</span></span>

![illustration d’un tracé composé d’une ligne, d’une ellipse et d’une spline de Bézier](images/aboutgdip02-art15.png)

<span data-ttu-id="4c649-130">En plus d’ajouter des lignes, des rectangles et des courbes à un tracé, vous pouvez ajouter des tracés à un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="4c649-130">In addition to adding lines, rectangles, and curves to a path, you can add paths to a path.</span></span> <span data-ttu-id="4c649-131">Cela vous permet de combiner des chemins existants pour former des chemins d’accès volumineux et complexes.</span><span class="sxs-lookup"><span data-stu-id="4c649-131">This allows you to combine existing paths to form large, complex paths.</span></span> <span data-ttu-id="4c649-132">Le code suivant ajoute **graphicsPath1** et **graphicsPath2** à **myGraphicsPath**.</span><span class="sxs-lookup"><span data-stu-id="4c649-132">The following code adds **graphicsPath1** and **graphicsPath2** to **myGraphicsPath**.</span></span> <span data-ttu-id="4c649-133">Le deuxième paramètre de la méthode [**GraphicsPath :: AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) spécifie si le chemin d’accès ajouté est connecté au chemin d’accès existant.</span><span class="sxs-lookup"><span data-stu-id="4c649-133">The second parameter of the [**GraphicsPath::AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) method specifies whether the added path is connected to the existing path.</span></span>


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



<span data-ttu-id="4c649-134">Il existe deux autres éléments que vous pouvez ajouter à un chemin d’accès : des chaînes et des secteurs.</span><span class="sxs-lookup"><span data-stu-id="4c649-134">There are two other items you can add to a path: strings and pies.</span></span> <span data-ttu-id="4c649-135">Un secteur est une partie de l’intérieur d’une ellipse.</span><span class="sxs-lookup"><span data-stu-id="4c649-135">A pie is a portion of the interior of an ellipse.</span></span> <span data-ttu-id="4c649-136">L’exemple suivant crée un tracé à partir d’un arc, d’une spline cardinale, d’une chaîne et d’un graphique à secteurs.</span><span class="sxs-lookup"><span data-stu-id="4c649-136">The following example creates a path from an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="4c649-137">L’illustration suivante montre le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="4c649-137">The following illustration shows the path.</span></span> <span data-ttu-id="4c649-138">Notez qu’il n’est pas nécessaire de connecter un chemin d’accès ; l’arc, la spline cardinale, la chaîne et le secteur sont séparés.</span><span class="sxs-lookup"><span data-stu-id="4c649-138">Note that a path does not have to be connected; the arc, cardinal spline, string, and pie are separated.</span></span>

![illustration d’un tracé constitué de lignes déconnectées : un arc, une spline cardinale, une chaîne et un graphique à secteurs](images/aboutgdip02-art16.png)

 

 



