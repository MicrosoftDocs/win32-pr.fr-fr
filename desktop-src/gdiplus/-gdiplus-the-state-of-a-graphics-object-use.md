---
description: La classe Graphics est au cœur de Windows GDI+. Pour dessiner tout, vous créez un objet Graphics, définissez ses propriétés et appelez ses méthodes (DrawLine, DrawImage, DrawString et like).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: État d’un objet Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661733f944b08633b5df84eed3ac488e612d9e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569792"
---
# <a name="the-state-of-a-graphics-object"></a><span data-ttu-id="97f9c-104">État d’un objet Graphics</span><span class="sxs-lookup"><span data-stu-id="97f9c-104">The State of a Graphics Object</span></span>

<span data-ttu-id="97f9c-105">La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) est au cœur de Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="97f9c-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is at the heart of Windows GDI+.</span></span> <span data-ttu-id="97f9c-106">Pour dessiner tout, vous créez un objet **Graphics** , définissez ses propriétés et appelez ses méthodes ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))et like).</span><span class="sxs-lookup"><span data-stu-id="97f9c-106">To draw anything, you create a **Graphics** object, set its properties, and call its methods ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)), and the like).</span></span>

<span data-ttu-id="97f9c-107">L’exemple suivant construit un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , puis appelle la méthode [**Graphics ::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) de l’objet **Graphics** :</span><span class="sxs-lookup"><span data-stu-id="97f9c-107">The following example constructs a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and then calls the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object:</span></span>


```
HDC          hdc;
PAINTSTRUCT  ps;

hdc = BeginPaint(hWnd, &ps);
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));  // opaque blue
   graphics.DrawRectangle(&pen, 10, 10, 200, 100);
}
EndPaint(hWnd, &ps);
```



<span data-ttu-id="97f9c-108">Dans le code précédent, la méthode [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) retourne un handle vers un contexte de périphérique (Device Context) et ce handle est passé au constructeur [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="97f9c-108">In the preceding code, the [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) method returns a handle to a device context, and that handle is passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="97f9c-109">Un contexte de périphérique est une structure (gérée par Windows) qui contient des informations sur le périphérique d’affichage en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="97f9c-109">A device context is a structure (maintained by Windows) that holds information about the particular display device being used.</span></span>

## <a name="graphics-state"></a><span data-ttu-id="97f9c-110">État graphique</span><span class="sxs-lookup"><span data-stu-id="97f9c-110">Graphics State</span></span>

<span data-ttu-id="97f9c-111">Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fait plus que fournir des méthodes de dessin, telles que [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) et [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span><span class="sxs-lookup"><span data-stu-id="97f9c-111">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object does more than provide drawing methods, such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) and [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)).</span></span> <span data-ttu-id="97f9c-112">Un objet **Graphics** conserve également l’État Graphics, qui peut être divisé selon les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="97f9c-112">A **Graphics** object also maintains graphics state, which can be divided into the following categories:</span></span>

-   <span data-ttu-id="97f9c-113">Lien vers un contexte de périphérique (Device Context)</span><span class="sxs-lookup"><span data-stu-id="97f9c-113">A link to a device context</span></span>
-   <span data-ttu-id="97f9c-114">Paramètres de qualité</span><span class="sxs-lookup"><span data-stu-id="97f9c-114">Quality settings</span></span>
-   <span data-ttu-id="97f9c-115">Transformations</span><span class="sxs-lookup"><span data-stu-id="97f9c-115">Transformations</span></span>
-   <span data-ttu-id="97f9c-116">Une zone de découpage</span><span class="sxs-lookup"><span data-stu-id="97f9c-116">A clipping region</span></span>

### <a name="device-context"></a><span data-ttu-id="97f9c-117">Contexte de périphérique</span><span class="sxs-lookup"><span data-stu-id="97f9c-117">Device Context</span></span>

<span data-ttu-id="97f9c-118">En tant que programmeur d’applications, vous n’êtes pas obligé de réfléchir à l’interaction entre un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et son contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="97f9c-118">As an application programmer, you don't have to think about the interaction between a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and its device context.</span></span> <span data-ttu-id="97f9c-119">Cette interaction est gérée par GDI+ en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="97f9c-119">This interaction is handled by GDI+ behind the scenes.</span></span>

### <a name="quality-settings"></a><span data-ttu-id="97f9c-120">Paramètres de qualité</span><span class="sxs-lookup"><span data-stu-id="97f9c-120">Quality Settings</span></span>

<span data-ttu-id="97f9c-121">Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a plusieurs propriétés qui influencent la qualité des éléments qui sont dessinés à l’écran.</span><span class="sxs-lookup"><span data-stu-id="97f9c-121">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object has several properties that influence the quality of the items that are drawn on the screen.</span></span> <span data-ttu-id="97f9c-122">Vous pouvez afficher et manipuler ces propriétés en appelant les méthodes obtenir et définir.</span><span class="sxs-lookup"><span data-stu-id="97f9c-122">You can view and manipulate these properties by calling get and set methods.</span></span> <span data-ttu-id="97f9c-123">Par exemple, vous pouvez appeler la méthode [**Graphics :: SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) pour spécifier le type d’anticrénelage (le cas échéant) appliqué au texte.</span><span class="sxs-lookup"><span data-stu-id="97f9c-123">For example, you can call the [**Graphics::SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method to specify the type of antialiasing (if any) applied to text.</span></span> <span data-ttu-id="97f9c-124">Les autres méthodes Set qui influencent la qualité sont [**Graphics :: SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics :: SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics :: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)et [**Graphics :: SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span><span class="sxs-lookup"><span data-stu-id="97f9c-124">Other set methods that influence quality are [**Graphics::SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics::SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality), and [**Graphics::SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).</span></span>

<span data-ttu-id="97f9c-125">L’exemple suivant dessine deux ellipses, l’une avec le mode de lissage défini sur [\* \* \* \* SmoothingModeAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) \* \* et l’autre avec le mode de lissage défini sur [\* \* \* \* SmoothingModeHighSpeed \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)\* \* :</span><span class="sxs-lookup"><span data-stu-id="97f9c-125">The following example draws two ellipses, one with the smoothing mode set to [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) and one with the smoothing mode set to [\*\*\*\*SmoothingModeHighSpeed\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode):</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a><span data-ttu-id="97f9c-126">Transformations</span><span class="sxs-lookup"><span data-stu-id="97f9c-126">Transformations</span></span>

<span data-ttu-id="97f9c-127">Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) gère deux transformations (World et page) qui sont appliquées à tous les éléments dessinés par cet objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="97f9c-127">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains two transformations (world and page) that are applied to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="97f9c-128">Toute transformation affine peut être stockée dans la transformation universelle.</span><span class="sxs-lookup"><span data-stu-id="97f9c-128">Any affine transformation can be stored in the world transformation.</span></span> <span data-ttu-id="97f9c-129">Les transformations affines incluent la mise à l’échelle, la rotation, la réflexion, l’inclinaison et la translation.</span><span class="sxs-lookup"><span data-stu-id="97f9c-129">Affine transformations include scaling, rotating, reflecting, skewing, and translating.</span></span> <span data-ttu-id="97f9c-130">La transformation de page peut être utilisée pour la mise à l’échelle et pour changer d’unités (par exemple, les pixels en pouces).</span><span class="sxs-lookup"><span data-stu-id="97f9c-130">The page transformation can be used for scaling and for changing units (for example, pixels to inches).</span></span> <span data-ttu-id="97f9c-131">Pour plus d’informations sur les transformations, consultez [systèmes de coordonnées et transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span><span class="sxs-lookup"><span data-stu-id="97f9c-131">For more information on transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="97f9c-132">L’exemple suivant définit les transformations universelles et de page d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="97f9c-132">The following example sets the world and page transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="97f9c-133">La transformation universelle est définie sur une rotation de 30 degrés.</span><span class="sxs-lookup"><span data-stu-id="97f9c-133">The world transformation is set to a 30-degree rotation.</span></span> <span data-ttu-id="97f9c-134">La transformation de page est définie de façon à ce que les coordonnées passées au deuxième [**graphique ::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) soient considérées comme des millimètres au lieu de pixels.</span><span class="sxs-lookup"><span data-stu-id="97f9c-134">The page transformation is set so that the coordinates passed to the second [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) will be treated as millimeters instead of pixels.</span></span> <span data-ttu-id="97f9c-135">Le code effectue deux appels identiques à la méthode **Graphics ::D rawellipse** .</span><span class="sxs-lookup"><span data-stu-id="97f9c-135">The code makes two identical calls to the **Graphics::DrawEllipse** method.</span></span> <span data-ttu-id="97f9c-136">La transformation universelle est appliquée au premier **graphique ::D appel rawellipse** , et les deux transformations (World et page) sont appliquées au second **graphics ::D appel rawellipse** .</span><span class="sxs-lookup"><span data-stu-id="97f9c-136">The world transformation is applied to the first **Graphics::DrawEllipse** call, and both transformations (world and page) are applied to the second **Graphics::DrawEllipse** call.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



<span data-ttu-id="97f9c-137">L’illustration suivante montre les deux points de suspension.</span><span class="sxs-lookup"><span data-stu-id="97f9c-137">The following illustration shows the two ellipses.</span></span> <span data-ttu-id="97f9c-138">Notez que la rotation à 30 degrés concerne l’origine du système de coordonnées (l’angle supérieur gauche de la zone cliente), pas les centres des points de suspension.</span><span class="sxs-lookup"><span data-stu-id="97f9c-138">Note that the 30-degree rotation is about the origin of the coordinate system (upper-left corner of the client area), not about the centers of the ellipses.</span></span> <span data-ttu-id="97f9c-139">Notez également que la largeur du stylet 1 signifie 1 pixel pour la première ellipse et 1 millimètre pour la deuxième ellipse.</span><span class="sxs-lookup"><span data-stu-id="97f9c-139">Also note that the pen width of 1 means 1 pixel for the first ellipse and 1 millimeter for the second ellipse.</span></span>

![capture d’écran d’une fenêtre contenant une ellipse petite, fine et épaisse](images/graphicsascon1.png)

 

### <a name="clipping-region"></a><span data-ttu-id="97f9c-141">Zone de découpage</span><span class="sxs-lookup"><span data-stu-id="97f9c-141">Clipping Region</span></span>

<span data-ttu-id="97f9c-142">Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) gère une zone de découpage qui s’applique à tous les éléments dessinés par cet objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="97f9c-142">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object maintains a clipping region that applies to all items drawn by that **Graphics** object.</span></span> <span data-ttu-id="97f9c-143">Vous pouvez définir la région de découpage en appelant la méthode [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) .</span><span class="sxs-lookup"><span data-stu-id="97f9c-143">You can set the clipping region by calling the [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) method.</span></span>

<span data-ttu-id="97f9c-144">L’exemple suivant crée une région en forme de plus en formant l’Union de deux rectangles.</span><span class="sxs-lookup"><span data-stu-id="97f9c-144">The following example creates a plus-shaped region by forming the union of two rectangles.</span></span> <span data-ttu-id="97f9c-145">Cette région est désignée comme zone de découpage d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="97f9c-145">That region is designated as the clipping region of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="97f9c-146">Ensuite, le code dessine deux lignes qui sont limitées à l’intérieur de la zone de découpage.</span><span class="sxs-lookup"><span data-stu-id="97f9c-146">Then the code draws two lines that are restricted to the interior of the clipping region.</span></span>


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0), 5);  // opaque red, width 5
SolidBrush brush(Color(255, 180, 255, 255));  // opaque aqua

// Create a plus-shaped region by forming the union of two rectangles.
Region region(Rect(50, 0, 50, 150));
region.Union(Rect(0, 50, 150, 50));
graphics.FillRegion(&brush, &region);

// Set the clipping region.
graphics.SetClip(&region);

// Draw two clipped lines.
graphics.DrawLine(&pen, 0, 30, 150, 160);
graphics.DrawLine(&pen, 40, 20, 190, 150);
```



<span data-ttu-id="97f9c-147">L’illustration suivante montre les lignes écrêtées.</span><span class="sxs-lookup"><span data-stu-id="97f9c-147">The following illustration shows the clipped lines.</span></span>

![Illustration montrant une forme de couleur franchie de deux lignes rouges diagonales](images/graphicsascon2.png)

 

 
