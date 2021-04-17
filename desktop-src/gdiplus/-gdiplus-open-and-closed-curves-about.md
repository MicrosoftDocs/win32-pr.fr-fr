---
description: 'L’illustration suivante montre deux courbes : une ouverte et une fermée.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Courbes ouvertes et fermées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7587ec950f8a0abc21f8c9cfb000a7333e87297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557894"
---
# <a name="open-and-closed-curves"></a><span data-ttu-id="b5b3e-103">Courbes ouvertes et fermées</span><span class="sxs-lookup"><span data-stu-id="b5b3e-103">Open and Closed Curves</span></span>

<span data-ttu-id="b5b3e-104">L’illustration suivante montre deux courbes : une ouverte et une fermée.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-104">The following illustration shows two curves: one open and one closed.</span></span>

![illustration d’une courbe ouverte (une ligne courbée) et d’une courbe fermée (le contour d’une forme)](images/aboutgdip02-art24.png)

<span data-ttu-id="b5b3e-106">Les courbes fermées ont un intérieur et peuvent par conséquent être remplies à l’aide d’un pinceau.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-106">Closed curves have an interior and therefore can be filled with a brush.</span></span> <span data-ttu-id="b5b3e-107">La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) dans Windows GDI+ fournit les méthodes suivantes pour remplir les figures fermées et les courbes : [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics :: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)et [**Graphics :: FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span><span class="sxs-lookup"><span data-stu-id="b5b3e-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class in Windows GDI+ provides the following methods for filling closed figures and curves: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath), and [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span></span> <span data-ttu-id="b5b3e-108">Chaque fois que vous appelez l’une de ces méthodes, vous devez passer l’adresse de l’un des types de pinceau spécifiques ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)ou [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) comme argument.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-108">Whenever you call one of these methods, you must pass the address of one of the specific brush types ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), or [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) as an argument.</span></span>

<span data-ttu-id="b5b3e-109">La méthode [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) est associée à la méthode [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) .</span><span class="sxs-lookup"><span data-stu-id="b5b3e-109">The [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) method is a companion to the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method.</span></span> <span data-ttu-id="b5b3e-110">Tout comme la méthode DrawArc dessine une partie du contour d’une ellipse, la méthode FillPie remplit une partie de l’intérieur d’une ellipse.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-110">Just as the DrawArc method draws a portion of the outline of an ellipse, the FillPie method fills a portion of the interior of an ellipse.</span></span> <span data-ttu-id="b5b3e-111">L’exemple suivant dessine un arc et remplit la partie correspondante de l’intérieur de l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-111">The following example draws an arc and fills the corresponding portion of the interior of the ellipse.</span></span>


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



<span data-ttu-id="b5b3e-112">L’illustration suivante montre l’arc et le secteur rempli.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-112">The following illustration shows the arc and the filled pie.</span></span>

![Illustration montrant un segment d’une Ellipse remplie](images/aboutgdip02-art25.png)

<span data-ttu-id="b5b3e-114">La méthode [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) est un complément de la méthode [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="b5b3e-114">The [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) method is a companion to the [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="b5b3e-115">Les deux méthodes ferment automatiquement la courbe en connectant le point de fin au point de départ.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-115">Both methods automatically close the curve by connecting the ending point to the starting point.</span></span> <span data-ttu-id="b5b3e-116">L’exemple suivant dessine une courbe qui passe par (0, 0), (60, 20) et (40, 50).</span><span class="sxs-lookup"><span data-stu-id="b5b3e-116">The following example draws a curve that passes through (0, 0), (60, 20), and (40, 50).</span></span> <span data-ttu-id="b5b3e-117">Ensuite, la courbe est fermée automatiquement en connectant (40, 50) au point de départ (0, 0), et l’intérieur est rempli avec une couleur unie.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-117">Then, the curve is automatically closed by connecting (40, 50) to the starting point (0, 0), and the interior is filled with a solid color.</span></span>


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



<span data-ttu-id="b5b3e-118">Un chemin d’accès peut comprendre plusieurs figures (sous-tracés).</span><span class="sxs-lookup"><span data-stu-id="b5b3e-118">A path can consist of several figures (subpaths).</span></span> <span data-ttu-id="b5b3e-119">La méthode [**Graphics :: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) remplit l’intérieur de chaque figure.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-119">The [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the interior of each figure.</span></span> <span data-ttu-id="b5b3e-120">Si une figure n’est pas fermée, la méthode **Graphics :: FillPath** remplit la zone qui serait placée si la figure était fermée.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-120">If a figure is not closed, the **Graphics::FillPath** method fills the area that would be enclosed if the figure were closed.</span></span> <span data-ttu-id="b5b3e-121">L’exemple suivant dessine et remplit un tracé constitué d’un arc, d’une spline cardinale, d’une chaîne et d’un graphique à secteurs.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-121">The following example draws and fills a path that consists of an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="b5b3e-122">L’illustration suivante montre le chemin d’accès avant et après qu’il a été rempli d’un pinceau plein.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-122">The following illustration shows the path before and after it is filled with a solid brush.</span></span> <span data-ttu-id="b5b3e-123">Notez que le texte de la chaîne est entouré, mais pas rempli, par la méthode [**Graphics ::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) .</span><span class="sxs-lookup"><span data-stu-id="b5b3e-123">Note that the text in the string is outlined, but not filled, by the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method.</span></span> <span data-ttu-id="b5b3e-124">Il s’agit de la méthode [**Graphics :: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) qui peint l’intérieur des caractères de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b5b3e-124">It is the [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method that paints the interiors of the characters in the string.</span></span>

![Illustration montrant deux fois le texte et une courbe ouverte et fermée ; ils sont vides la première fois et remplis la deuxième fois](images/aboutgdip02-art26.png)

 

 



