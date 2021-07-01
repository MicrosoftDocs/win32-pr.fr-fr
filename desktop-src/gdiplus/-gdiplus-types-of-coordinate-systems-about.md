---
description: 'Windows GDI+ utilise trois espaces de coordonnées : World, page et Device.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Types de systèmes de coordonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e259f43d4fc0d6a74021f3a6125f85652f51ac95
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120624"
---
# <a name="types-of-coordinate-systems"></a><span data-ttu-id="f692c-103">Types de systèmes de coordonnées</span><span class="sxs-lookup"><span data-stu-id="f692c-103">Types of Coordinate Systems</span></span>

<span data-ttu-id="f692c-104">Windows GDI+ utilise trois espaces de coordonnées : World, page et Device.</span><span class="sxs-lookup"><span data-stu-id="f692c-104">Windows GDI+ uses three coordinate spaces: world, page, and device.</span></span> <span data-ttu-id="f692c-105">Lorsque vous effectuez l’appel `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , les points que vous transmettez à la méthode [**Graphics ::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) , (0,0) et (160, 80), se trouvent dans l’espace de coordonnées universel.</span><span class="sxs-lookup"><span data-stu-id="f692c-105">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, the points that you pass to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) method — (0, 0) and (160, 80) — are in the world coordinate space.</span></span> <span data-ttu-id="f692c-106">Avant que GDI+ puisse dessiner la ligne sur l’écran, les coordonnées passent par une séquence de transformations.</span><span class="sxs-lookup"><span data-stu-id="f692c-106">Before GDI+ can draw the line on the screen, the coordinates pass through a sequence of transformations.</span></span> <span data-ttu-id="f692c-107">Une transformation convertit les coordonnées universelles en coordonnées de page et une autre transformation convertit les coordonnées de page en coordonnées de périphérique.</span><span class="sxs-lookup"><span data-stu-id="f692c-107">One transformation converts world coordinates to page coordinates, and another transformation converts page coordinates to device coordinates.</span></span>

<span data-ttu-id="f692c-108">Supposons que vous souhaitiez utiliser un système de coordonnées dont l’origine se trouve dans le corps de la zone cliente plutôt que dans le coin supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="f692c-108">Suppose you want to work with a coordinate system that has its origin in the body of the client area rather than the upper-left corner.</span></span> <span data-ttu-id="f692c-109">Par exemple, imaginons que vous souhaitiez que l’origine soit de 100 pixels du bord gauche de la zone cliente et de 50 pixels en haut de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="f692c-109">Say, for example, that you want the origin to be 100 pixels from the left edge of the client area and 50 pixels from the top of the client area.</span></span> <span data-ttu-id="f692c-110">L’illustration suivante montre un tel système de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="f692c-110">The following illustration shows such a coordinate system.</span></span>

![capture d’écran d’une fenêtre contenant des axes de coordonnées étiquetés](images/aboutgdip05-art01.png)

<span data-ttu-id="f692c-112">Lorsque vous effectuez l’appel `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , vous recevez la ligne indiquée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="f692c-112">When you make the call `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)`, you get the line shown in the following illustration.</span></span>

![capture d’écran de la fenêtre précédente, mais avec une ligne bleue qui s’étend en diagonale à partir de l’origine](images/aboutgdip05-art02.png)

<span data-ttu-id="f692c-114">Les coordonnées des points de terminaison de votre ligne dans les trois espaces de coordonnées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f692c-114">The coordinates of the endpoints of your line in the three coordinate spaces are as follows:</span></span>



| <span data-ttu-id="f692c-115">Espace</span><span class="sxs-lookup"><span data-stu-id="f692c-115">Space</span></span>       |  <span data-ttu-id="f692c-116">Coordonnées du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f692c-116">Endpoint coordinates</span></span>                       |
|--------|-------------------------|
| <span data-ttu-id="f692c-117">World (Monde)</span><span class="sxs-lookup"><span data-stu-id="f692c-117">World</span></span>  | <span data-ttu-id="f692c-118">(0, 0) à (160, 80)</span><span class="sxs-lookup"><span data-stu-id="f692c-118">(0, 0) to (160, 80)</span></span>     |
| <span data-ttu-id="f692c-119">Page</span><span class="sxs-lookup"><span data-stu-id="f692c-119">Page</span></span>   | <span data-ttu-id="f692c-120">(100, 50) vers (260, 130)</span><span class="sxs-lookup"><span data-stu-id="f692c-120">(100, 50) to (260, 130)</span></span> |
| <span data-ttu-id="f692c-121">Périphérique</span><span class="sxs-lookup"><span data-stu-id="f692c-121">Device</span></span> | <span data-ttu-id="f692c-122">(100, 50) vers (260, 130)</span><span class="sxs-lookup"><span data-stu-id="f692c-122">(100, 50) to (260, 130)</span></span> |



 

<span data-ttu-id="f692c-123">Notez que l’espace de coordonnées de la page a son origine dans l’angle supérieur gauche de la zone cliente. ce sera toujours le cas.</span><span class="sxs-lookup"><span data-stu-id="f692c-123">Note that the page coordinate space has its origin at the upper-left corner of the client area; this will always be the case.</span></span> <span data-ttu-id="f692c-124">Notez également que, étant donné que l’unité de mesure est le pixel, les coordonnées de l’appareil sont les mêmes que les coordonnées de la page.</span><span class="sxs-lookup"><span data-stu-id="f692c-124">Also note that because the unit of measure is the pixel, the device coordinates are the same as the page coordinates.</span></span> <span data-ttu-id="f692c-125">Si vous définissez l’unité de mesure sur une valeur autre que les pixels (par exemple, pouces), les coordonnées de l’appareil seront différentes des coordonnées de la page.</span><span class="sxs-lookup"><span data-stu-id="f692c-125">If you set the unit of measure to something other than pixels (for example, inches), then the device coordinates will be different from the page coordinates.</span></span>

<span data-ttu-id="f692c-126">La transformation qui mappe les coordonnées universelles aux coordonnées de la page est appelée *transformation universelle* et est conservée par un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="f692c-126">The transformation that maps world coordinates to page coordinates is called the *world transformation* and is maintained by a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="f692c-127">Dans l’exemple précédent, la transformation universelle est une translation de 100 unités sur la direction x et de 50 unités sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="f692c-127">In the previous example, the world transformation is a translation 100 units in the x direction and 50 units in the y direction.</span></span> <span data-ttu-id="f692c-128">L’exemple suivant définit la transformation universelle d’un objet **Graphics** , puis utilise cet objet **Graphics** pour dessiner la ligne indiquée dans la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="f692c-128">The following example sets the world transformation of a **Graphics** object and then uses that **Graphics** object to draw the line shown in the previous figure.</span></span>


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



<span data-ttu-id="f692c-129">La transformation qui mappe les coordonnées de page aux coordonnées de l’appareil est appelée *transformation de page*.</span><span class="sxs-lookup"><span data-stu-id="f692c-129">The transformation that maps page coordinates to device coordinates is called the *page transformation*.</span></span> <span data-ttu-id="f692c-130">La classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fournit quatre méthodes pour la manipulation et l’inspection de la transformation de page : [**Graphics :: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics :: GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics :: SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)et [**Graphics :: GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span><span class="sxs-lookup"><span data-stu-id="f692c-130">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides four methods for manipulating and inspecting the page transformation: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale), and [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale).</span></span> <span data-ttu-id="f692c-131">La classe **Graphics** fournit également deux méthodes, [**Graphics :: GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) et [**Graphics :: GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), pour l’examen des points horizontaux et verticaux par pouce du périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f692c-131">The **Graphics** class also provides two methods, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) and [**Graphics::GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), for examining the horizontal and vertical dots per inch of the display device.</span></span>

<span data-ttu-id="f692c-132">Vous pouvez utiliser la méthode [**Graphics :: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pour spécifier une unité de mesure.</span><span class="sxs-lookup"><span data-stu-id="f692c-132">You can use the [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to specify a unit of measure.</span></span> <span data-ttu-id="f692c-133">L’exemple suivant dessine une ligne de (0,0) à (2,3) où le point (2, 1) est de 2 pouces à droite et de 1 pouce en dessous du point (0, 0).</span><span class="sxs-lookup"><span data-stu-id="f692c-133">The following example draws a line from (0, 0) to (2, 1) where the point (2, 1) is 2 inches to the right and 1 inch down from the point (0, 0).</span></span>


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> <span data-ttu-id="f692c-134">Si vous ne spécifiez pas de largeur du stylet lorsque vous construisez votre stylet, l’exemple précédent dessine une ligne d’une largeur d’un pouce.</span><span class="sxs-lookup"><span data-stu-id="f692c-134">If you don't specify a pen width when you construct your pen, the previous example will draw a line that is one inch wide.</span></span> <span data-ttu-id="f692c-135">Vous pouvez spécifier la largeur du stylet dans le deuxième argument du constructeur [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) :</span><span class="sxs-lookup"><span data-stu-id="f692c-135">You can specify the pen width in the second argument to the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor:</span></span>
> <br/><br/>
> <span data-ttu-id="f692c-136">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span><span class="sxs-lookup"><span data-stu-id="f692c-136">`Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.</span></span>

 

<span data-ttu-id="f692c-137">Si nous supposons que le périphérique d’affichage a 96 points par pouce dans la direction horizontale et 96 points par pouce dans la direction verticale, les points de terminaison de la ligne de l’exemple précédent ont les coordonnées suivantes dans les trois espaces de coordonnées :</span><span class="sxs-lookup"><span data-stu-id="f692c-137">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



| <span data-ttu-id="f692c-138">Espace</span><span class="sxs-lookup"><span data-stu-id="f692c-138">Space</span></span>       | <span data-ttu-id="f692c-139">Coordonnées du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f692c-139">Endpoint coordinates</span></span>                    |
|--------|---------------------|
| <span data-ttu-id="f692c-140">World (Monde)</span><span class="sxs-lookup"><span data-stu-id="f692c-140">World</span></span>  | <span data-ttu-id="f692c-141">(0, 0) à (2, 1)</span><span class="sxs-lookup"><span data-stu-id="f692c-141">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="f692c-142">Page</span><span class="sxs-lookup"><span data-stu-id="f692c-142">Page</span></span>   | <span data-ttu-id="f692c-143">(0, 0) à (2, 1)</span><span class="sxs-lookup"><span data-stu-id="f692c-143">(0, 0) to (2, 1)</span></span>    |
| <span data-ttu-id="f692c-144">Périphérique</span><span class="sxs-lookup"><span data-stu-id="f692c-144">Device</span></span> | <span data-ttu-id="f692c-145">(0,0, to (192, 96)</span><span class="sxs-lookup"><span data-stu-id="f692c-145">(0, 0, to (192, 96)</span></span> |



 

<span data-ttu-id="f692c-146">Vous pouvez combiner les transformations universelles et de page pour obtenir un grand nombre d’effets.</span><span class="sxs-lookup"><span data-stu-id="f692c-146">You can combine the world and page transformations to achieve a variety of effects.</span></span> <span data-ttu-id="f692c-147">Par exemple, supposons que vous souhaitiez utiliser des pouces comme unité de mesure et que vous souhaitez que l’origine de votre système de coordonnées soit de 2 pouces à partir du bord gauche de la zone cliente et de 1/2 centimètres à partir du haut de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="f692c-147">For example, suppose you want to use inches as the unit of measure and you want the origin of your coordinate system to be 2 inches from the left edge of the client area and 1/2 inch from the top of the client area.</span></span> <span data-ttu-id="f692c-148">L’exemple suivant définit les transformations universelles et de page d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , puis dessine une ligne comprise entre (0,0) et (2, 1).</span><span class="sxs-lookup"><span data-stu-id="f692c-148">The following example sets the world and page transformations of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and then draws a line from (0, 0) to (2, 1).</span></span>


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



<span data-ttu-id="f692c-149">L’illustration suivante montre la ligne et le système de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="f692c-149">The following illustration shows the line and coordinate system.</span></span>

![capture d’écran de la fenêtre précédente, mais plus grande, avec les axes positionnés à gauche et libellés différemment](images/aboutgdip05-art03.png)

<span data-ttu-id="f692c-151">Si nous supposons que le périphérique d’affichage a 96 points par pouce dans la direction horizontale et 96 points par pouce dans la direction verticale, les points de terminaison de la ligne de l’exemple précédent ont les coordonnées suivantes dans les trois espaces de coordonnées :</span><span class="sxs-lookup"><span data-stu-id="f692c-151">If we assume that the display device has 96 dots per inch in the horizontal direction and 96 dots per inch in the vertical direction, the endpoints of the line in the previous example have the following coordinates in the three coordinate spaces:</span></span>



| <span data-ttu-id="f692c-152">Espace</span><span class="sxs-lookup"><span data-stu-id="f692c-152">Space</span></span>       | <span data-ttu-id="f692c-153">Coordonnées du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f692c-153">Endpoint coordinates</span></span>                        |
|--------|-------------------------|
| <span data-ttu-id="f692c-154">World (Monde)</span><span class="sxs-lookup"><span data-stu-id="f692c-154">World</span></span>  | <span data-ttu-id="f692c-155">(0, 0) à (2, 1)</span><span class="sxs-lookup"><span data-stu-id="f692c-155">(0, 0) to (2, 1)</span></span>        |
| <span data-ttu-id="f692c-156">Page</span><span class="sxs-lookup"><span data-stu-id="f692c-156">Page</span></span>   | <span data-ttu-id="f692c-157">(2, 0,5) à (4, 1,5)</span><span class="sxs-lookup"><span data-stu-id="f692c-157">(2, 0.5) to (4, 1.5)</span></span>    |
| <span data-ttu-id="f692c-158">Périphérique</span><span class="sxs-lookup"><span data-stu-id="f692c-158">Device</span></span> | <span data-ttu-id="f692c-159">(192, 48) vers (384, 144)</span><span class="sxs-lookup"><span data-stu-id="f692c-159">(192, 48) to (384, 144)</span></span> |



 

 

 
