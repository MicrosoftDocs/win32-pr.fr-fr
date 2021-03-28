---
description: Windows GDI+ fournit des conteneurs que vous pouvez utiliser pour remplacer ou augmenter temporairement une partie de l’État dans un objet Graphics.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Conteneurs Graphics imbriqués
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f9d9feac3494b423d844cb1e3da359af33eaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951698"
---
# <a name="nested-graphics-containers"></a><span data-ttu-id="c288f-103">Conteneurs Graphics imbriqués</span><span class="sxs-lookup"><span data-stu-id="c288f-103">Nested Graphics Containers</span></span>

<span data-ttu-id="c288f-104">Windows GDI+ fournit des conteneurs que vous pouvez utiliser pour remplacer ou augmenter temporairement une partie de l’État dans un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="c288f-104">Windows GDI+ provides containers that you can use to temporarily replace or augment part of the state in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="c288f-105">Pour créer un conteneur, appelez la méthode [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) d’un objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="c288f-105">You create a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object.</span></span> <span data-ttu-id="c288f-106">Vous pouvez appeler **Graphics :: BeginContainer** à plusieurs reprises pour former des conteneurs imbriqués.</span><span class="sxs-lookup"><span data-stu-id="c288f-106">You can call **Graphics::BeginContainer** repeatedly to form nested containers.</span></span>

## <a name="transformations-in-nested-containers"></a><span data-ttu-id="c288f-107">Transformations dans les conteneurs imbriqués</span><span class="sxs-lookup"><span data-stu-id="c288f-107">Transformations in Nested Containers</span></span>

<span data-ttu-id="c288f-108">L’exemple suivant crée un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et un conteneur dans cet objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="c288f-108">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="c288f-109">La transformation universelle de l’objet **Graphics** est une translation de 100 unités sur la direction x et de 80 unités sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="c288f-109">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="c288f-110">La transformation universelle du conteneur est une rotation à 30 degrés.</span><span class="sxs-lookup"><span data-stu-id="c288f-110">The world transformation of the container is a 30-degree rotation.</span></span> <span data-ttu-id="c288f-111">Le code effectue l’appel</span><span class="sxs-lookup"><span data-stu-id="c288f-111">The code makes the call</span></span>


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



<span data-ttu-id="c288f-112">deux fois.</span><span class="sxs-lookup"><span data-stu-id="c288f-112">twice.</span></span> <span data-ttu-id="c288f-113">Le premier appel à [**Graphics ::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) est *à l’intérieur du conteneur*; autrement dit, l’appel se trouve entre les appels à [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) et [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span><span class="sxs-lookup"><span data-stu-id="c288f-113">The first call to [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is *inside the container*; that is, the call is in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span></span> <span data-ttu-id="c288f-114">Le deuxième appel à **Graphics ::D rawrectangle** est après l’appel à **Graphics :: EndContainer**.</span><span class="sxs-lookup"><span data-stu-id="c288f-114">The second call to **Graphics::DrawRectangle** is after the call to **Graphics::EndContainer**.</span></span>


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



<span data-ttu-id="c288f-115">Dans le code précédent, le Rectangle dessiné à partir de l’intérieur du conteneur est transformé en premier par la transformation universelle du conteneur (rotation), puis par la transformation universelle de l’objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) (translation).</span><span class="sxs-lookup"><span data-stu-id="c288f-115">In the preceding code, the rectangle drawn from inside the container is transformed first by the world transformation of the container (rotation) and then by the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object (translation).</span></span> <span data-ttu-id="c288f-116">Le Rectangle dessiné à l’extérieur du conteneur est transformé uniquement par la transformation universelle de l’objet **Graphics** (translation).</span><span class="sxs-lookup"><span data-stu-id="c288f-116">The rectangle drawn from outside the container is transformed only by the world transformation of the **Graphics** object (translation).</span></span> <span data-ttu-id="c288f-117">L’illustration suivante montre les deux rectangles.</span><span class="sxs-lookup"><span data-stu-id="c288f-117">The following illustration shows the two rectangles.</span></span>

![capture d’écran d’une fenêtre avec deux rectangles rouges centrés sur le même point, mais avec des rotations différentes](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a><span data-ttu-id="c288f-119">Découpage dans les conteneurs imbriqués</span><span class="sxs-lookup"><span data-stu-id="c288f-119">Clipping in Nested Containers</span></span>

<span data-ttu-id="c288f-120">L’exemple suivant illustre la façon dont les conteneurs imbriqués gèrent les régions de découpage.</span><span class="sxs-lookup"><span data-stu-id="c288f-120">The following example illustrates how nested containers handle clipping regions.</span></span> <span data-ttu-id="c288f-121">Le code crée un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et un conteneur dans cet objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="c288f-121">The code creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="c288f-122">La zone de découpage de l’objet **Graphics** est un rectangle et la zone de découpage du conteneur est une ellipse.</span><span class="sxs-lookup"><span data-stu-id="c288f-122">The clipping region of the **Graphics** object is a rectangle, and the clipping region of the container is an ellipse.</span></span> <span data-ttu-id="c288f-123">Le code effectue deux appels à la méthode [**Graphics ::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="c288f-123">The code makes two calls to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method.</span></span> <span data-ttu-id="c288f-124">Le premier appel à **Graphics ::D rawline** est à l’intérieur du conteneur, et le deuxième appel à **graphics ::D rawline** se trouve en dehors du conteneur (après l’appel à [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span><span class="sxs-lookup"><span data-stu-id="c288f-124">The first call to **Graphics::DrawLine** is inside the container, and the second call to **Graphics::DrawLine** is outside the container (after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="c288f-125">La première ligne est découpée en fonction de l’intersection des deux régions de découpage.</span><span class="sxs-lookup"><span data-stu-id="c288f-125">The first line is clipped by the intersection of the two clipping regions.</span></span> <span data-ttu-id="c288f-126">La deuxième ligne est découpée uniquement par la zone de découpage rectangulaire de l’objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="c288f-126">The second line is clipped only by the rectangular clipping region of the **Graphics** object.</span></span>


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



<span data-ttu-id="c288f-127">L’illustration suivante montre les deux lignes écrêtées.</span><span class="sxs-lookup"><span data-stu-id="c288f-127">The following illustration shows the two clipped lines.</span></span>

![illustration d’une ellipse à l’intérieur d’un rectangle, avec une ligne coupée par l’ellipse et l’autre par le rectangle](images/nestedcontainers2.png)

<span data-ttu-id="c288f-129">Comme le montrent les deux exemples précédents, les transformations et les régions de découpage sont cumulatives dans les conteneurs imbriqués.</span><span class="sxs-lookup"><span data-stu-id="c288f-129">As the two preceding examples show, transformations and clipping regions are cumulative in nested containers.</span></span> <span data-ttu-id="c288f-130">Si vous définissez les transformations universelles du conteneur et de l’objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , les deux transformations s’appliqueront aux éléments dessinés à partir de l’intérieur du conteneur.</span><span class="sxs-lookup"><span data-stu-id="c288f-130">If you set the world transformations of the container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, both transformations will apply to items drawn from inside the container.</span></span> <span data-ttu-id="c288f-131">La transformation du conteneur est appliquée en premier, et la transformation de l’objet **Graphics** est appliquée en second.</span><span class="sxs-lookup"><span data-stu-id="c288f-131">The transformation of the container will be applied first, and the transformation of the **Graphics** object will be applied second.</span></span> <span data-ttu-id="c288f-132">Si vous définissez les régions de découpage du conteneur et de l’objet **Graphics** , les éléments dessinés à l’intérieur du conteneur sont découpés par l’intersection des deux régions de découpage.</span><span class="sxs-lookup"><span data-stu-id="c288f-132">If you set the clipping regions of the container and the **Graphics** object, items drawn from inside the container will be clipped by the intersection of the two clipping regions.</span></span>

## <a name="quality-settings-in-nested-containers"></a><span data-ttu-id="c288f-133">Paramètres de qualité dans les conteneurs imbriqués</span><span class="sxs-lookup"><span data-stu-id="c288f-133">Quality Settings in Nested Containers</span></span>

<span data-ttu-id="c288f-134">Les paramètres de qualité ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)et like) dans les conteneurs imbriqués ne sont pas cumulatifs ; au lieu de cela, les paramètres de qualité du conteneur remplacent temporairement les paramètres de qualité d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="c288f-134">Quality settings ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the like) in nested containers are not cumulative; rather, the quality settings of the container temporarily replace the quality settings of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="c288f-135">Lorsque vous créez un conteneur, les paramètres de qualité de ce conteneur sont définis sur les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="c288f-135">When you create a new container, the quality settings for that container are set to default values.</span></span> <span data-ttu-id="c288f-136">Par exemple, supposons que vous ayez un objet **Graphics** avec un mode de lissage [\* \* \* \* SmoothingModeAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)\* \*.</span><span class="sxs-lookup"><span data-stu-id="c288f-136">For example, suppose you have a **Graphics** object with a smoothing mode of [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode).</span></span> <span data-ttu-id="c288f-137">Lorsque vous créez un conteneur, le mode de lissage à l’intérieur du conteneur est le mode de lissage par défaut.</span><span class="sxs-lookup"><span data-stu-id="c288f-137">When you create a container, the smoothing mode inside the container is the default smoothing mode.</span></span> <span data-ttu-id="c288f-138">Vous êtes libre de définir le mode de lissage du conteneur, et tous les éléments dessinés à l’intérieur du conteneur sont dessinés en fonction du mode que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="c288f-138">You are free to set the smoothing mode of the container, and any items drawn from inside the container will be drawn according to the mode you set.</span></span> <span data-ttu-id="c288f-139">Les éléments dessinés après l’appel à [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) sont dessinés en fonction du mode de lissage ([\* \* \* \* SmoothingModeAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)\* \*) qui était en place avant l’appel à [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span><span class="sxs-lookup"><span data-stu-id="c288f-139">Items drawn after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will be drawn according to the smoothing mode ([\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)) that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

## <a name="several-layers-of-nested-containers"></a><span data-ttu-id="c288f-140">Plusieurs couches de conteneurs imbriqués</span><span class="sxs-lookup"><span data-stu-id="c288f-140">Several Layers of Nested Containers</span></span>

<span data-ttu-id="c288f-141">Vous n’êtes pas limité à un conteneur dans un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="c288f-141">You are not limited to one container in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="c288f-142">Vous pouvez créer une séquence de conteneurs, chacun imbriqué dans le précédent, et vous pouvez spécifier la transformation universelle, la région de découpage et les paramètres de qualité de chacun de ces conteneurs imbriqués.</span><span class="sxs-lookup"><span data-stu-id="c288f-142">You can create a sequence of containers, each nested in the preceding, and you can specify the world transformation, clipping region, and quality settings of each of those nested containers.</span></span> <span data-ttu-id="c288f-143">Si vous appelez une méthode de dessin à partir de l’intérieur du conteneur le plus profond, les transformations sont appliquées dans l’ordre, en commençant par le conteneur le plus profond et en terminant par le conteneur le plus à l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="c288f-143">If you call a drawing method from inside the innermost container, the transformations will be applied in order, starting with the innermost container and ending with the outermost container.</span></span> <span data-ttu-id="c288f-144">Les éléments dessinés à l’intérieur du conteneur le plus profond sont découpés par l’intersection de toutes les régions de découpage.</span><span class="sxs-lookup"><span data-stu-id="c288f-144">Items drawn from inside the innermost container will be clipped by the intersection of all the clipping regions.</span></span>

<span data-ttu-id="c288f-145">L’exemple suivant crée un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et définit son indicateur de rendu de texte sur [\* \* \* \* TextRenderingHintAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* \*.</span><span class="sxs-lookup"><span data-stu-id="c288f-145">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and sets its text rendering hint to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="c288f-146">Le code crée deux conteneurs, l’un imbriqué dans l’autre.</span><span class="sxs-lookup"><span data-stu-id="c288f-146">The code creates two containers, one nested within the other.</span></span> <span data-ttu-id="c288f-147">L’indicateur de rendu de texte du conteneur externe est défini sur [\* \* \* \* TextRenderingHintSingleBitPerPixel \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* *, et l’indicateur de rendu de texte du conteneur interne est défini sur [\* \* \* \* TextRenderingHintAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* \*.</span><span class="sxs-lookup"><span data-stu-id="c288f-147">The text rendering hint of the outer container is set to [\*\*\*\*TextRenderingHintSingleBitPerPixel\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the text rendering hint of the inner container is set to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="c288f-148">Le code dessine trois chaînes : une à partir du conteneur interne, une à partir du conteneur externe et une à partir de l’objet **Graphics** lui-même.</span><span class="sxs-lookup"><span data-stu-id="c288f-148">The code draws three strings: one from the inner container, one from the outer container, and one from the **Graphics** object itself.</span></span>


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



<span data-ttu-id="c288f-149">L’illustration suivante montre les trois chaînes.</span><span class="sxs-lookup"><span data-stu-id="c288f-149">The following illustration shows the three strings.</span></span> <span data-ttu-id="c288f-150">Les chaînes dessinées à partir du conteneur interne et de l’objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) sont lissées par l’anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="c288f-150">The strings drawn from the inner container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object are smoothed by antialiasing.</span></span> <span data-ttu-id="c288f-151">La chaîne dessinée à partir du conteneur externe n’est pas lissée par l’anticrénelage en raison du paramètre TextRenderingHintSingleBitPerPixel.</span><span class="sxs-lookup"><span data-stu-id="c288f-151">The string drawn from the outer container is not smoothed by antialiasing because of the TextRenderingHintSingleBitPerPixel setting.</span></span>

![illustration d’un rectangle contenant la même chaîne à l’heure ; Seuls les caractères de la première et de la dernière lignes sont lisses](images/nestedcontainers3.png)

 

 
