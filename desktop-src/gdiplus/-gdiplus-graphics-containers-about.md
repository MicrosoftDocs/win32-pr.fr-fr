---
description: L’État graphique &\# 8212 ; la région de découpage, les transformations et les paramètres de qualité &\# 8212 ; est stocké dans un objet Graphics.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Conteneurs Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8bf6469d0835137be1bb76b7727fd961bba16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551849"
---
# <a name="graphics-containers"></a><span data-ttu-id="0ad72-103">Conteneurs Graphics</span><span class="sxs-lookup"><span data-stu-id="0ad72-103">Graphics Containers</span></span>

<span data-ttu-id="0ad72-104">L’état des graphiques (région de découpage, transformations et paramètres de qualité) est stocké dans un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="0ad72-104">Graphics state — clipping region, transformations, and quality settings — is stored in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="0ad72-105">Windows GDI+ vous permet de remplacer ou d’augmenter temporairement une partie de l’état d’un objet **Graphics** à l’aide d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="0ad72-105">Windows GDI+ allows you to temporarily replace or augment part of the state in a **Graphics** object by using a container.</span></span> <span data-ttu-id="0ad72-106">Vous démarrez un conteneur en appelant la méthode [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) d’un objet **Graphics** , et vous terminez un conteneur en appelant la méthode [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) .</span><span class="sxs-lookup"><span data-stu-id="0ad72-106">You start a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object, and you end a container by calling the [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) method.</span></span> <span data-ttu-id="0ad72-107">Entre **Graphics :: BeginContainer** et **Graphics :: EndContainer**, les modifications d’État que vous apportez à l’objet **Graphics** appartiennent au conteneur et ne remplacent pas l’état existant de l’objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="0ad72-107">In between **Graphics::BeginContainer** and **Graphics::EndContainer**, any state changes you make to the **Graphics** object belong to the container and do not overwrite the existing state of the **Graphics** object.</span></span>

<span data-ttu-id="0ad72-108">L’exemple suivant crée un conteneur dans un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="0ad72-108">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="0ad72-109">La transformation universelle de l’objet **Graphics** est une translation de 200 unités à droite, et la transformation universelle du conteneur est une translation de 100 unités vers le haut.</span><span class="sxs-lookup"><span data-stu-id="0ad72-109">The world transformation of the **Graphics** object is a translation 200 units to the right, and the world transformation of the container is a translation 100 units down.</span></span>


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



<span data-ttu-id="0ad72-110">Notez que dans l’exemple précédent, l’instruction `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` faite entre les appels à [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) et [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produit un rectangle différent de la même instruction que celle effectuée après l’appel à **Graphics :: EndContainer**.</span><span class="sxs-lookup"><span data-stu-id="0ad72-110">Note that in the previous example, the statement `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` made in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produces a different rectangle than the same statement made after the call to **Graphics::EndContainer**.</span></span> <span data-ttu-id="0ad72-111">Seule la traduction horizontale s’applique à l’appel **DrawRectangle** effectué en dehors du conteneur.</span><span class="sxs-lookup"><span data-stu-id="0ad72-111">Only the horizontal translation applies to the **DrawRectangle** call made outside of the container.</span></span> <span data-ttu-id="0ad72-112">Les deux transformations, à savoir la translation horizontale de 200 unités et la translation verticale de 100 unités, s’appliquent aux [**graphiques ::D appel rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) effectué à l’intérieur du conteneur.</span><span class="sxs-lookup"><span data-stu-id="0ad72-112">Both transformations — the horizontal translation of 200 units and the vertical translation of 100 units — apply to the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) call made inside the container.</span></span> <span data-ttu-id="0ad72-113">L’illustration suivante montre les deux rectangles.</span><span class="sxs-lookup"><span data-stu-id="0ad72-113">The following illustration shows the two rectangles.</span></span>

![capture d’écran d’une fenêtre avec deux rectangles dessinés avec un stylet bleu, l’un placé au-dessus de l’autre](images/aboutgdip05-art17.png)

<span data-ttu-id="0ad72-115">Les conteneurs peuvent être imbriqués dans des conteneurs.</span><span class="sxs-lookup"><span data-stu-id="0ad72-115">Containers can be nested within containers.</span></span> <span data-ttu-id="0ad72-116">L’exemple suivant crée un conteneur dans un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et un autre conteneur dans le premier conteneur.</span><span class="sxs-lookup"><span data-stu-id="0ad72-116">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and another container within the first container.</span></span> <span data-ttu-id="0ad72-117">La transformation universelle de l’objet **Graphics** est une translation de 100 unités sur la direction x et de 80 unités sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="0ad72-117">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="0ad72-118">La transformation universelle du premier conteneur est une rotation à 30 degrés.</span><span class="sxs-lookup"><span data-stu-id="0ad72-118">The world transformation of the first container is a 30-degree rotation.</span></span> <span data-ttu-id="0ad72-119">La transformation universelle du deuxième conteneur est une mise à l’échelle par un facteur de 2 dans la direction x.</span><span class="sxs-lookup"><span data-stu-id="0ad72-119">The world transformation of the second container is a scaling by a factor of 2 in the x direction.</span></span> <span data-ttu-id="0ad72-120">Un appel à la méthode [**Graphics ::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) est effectué à l’intérieur du deuxième conteneur.</span><span class="sxs-lookup"><span data-stu-id="0ad72-120">A call to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) method is made inside the second container.</span></span>


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



<span data-ttu-id="0ad72-121">L’illustration suivante montre l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="0ad72-121">The following illustration shows the ellipse.</span></span>

![capture d’écran d’une fenêtre qui contient une ellipse bleue pivotée avec son centre étiqueté comme (100, 80)](images/aboutgdip05-art18.png)

<span data-ttu-id="0ad72-123">Notez que les trois transformations s’appliquent aux [**graphiques ::D appel rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) effectué dans le deuxième conteneur (le plus à l’intérieur).</span><span class="sxs-lookup"><span data-stu-id="0ad72-123">Note that all three transformations apply to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) call made in the second (innermost) container.</span></span> <span data-ttu-id="0ad72-124">Notez également l’ordre des transformations : première échelle, faire pivoter, puis traduire.</span><span class="sxs-lookup"><span data-stu-id="0ad72-124">Also note the order of the transformations: first scale, then rotate, then translate.</span></span> <span data-ttu-id="0ad72-125">La transformation la plus profonde est appliquée en premier, et la transformation la plus à l’extérieur est appliquée en dernier.</span><span class="sxs-lookup"><span data-stu-id="0ad72-125">The innermost transformation is applied first, and the outermost transformation is applied last.</span></span>

<span data-ttu-id="0ad72-126">Toute propriété d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) peut être définie à l’intérieur d’un conteneur (entre les appels à [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) et [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span><span class="sxs-lookup"><span data-stu-id="0ad72-126">Any property of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be set inside a container (in between calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="0ad72-127">Par exemple, une zone de découpage peut être définie à l’intérieur d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="0ad72-127">For example, a clipping region can be set inside a container.</span></span> <span data-ttu-id="0ad72-128">Tout dessin effectué à l’intérieur du conteneur sera limité à la zone de découpage de ce conteneur et sera également limité aux régions de découpage de tous les conteneurs externes et à la zone de découpage de l’objet **Graphics** lui-même.</span><span class="sxs-lookup"><span data-stu-id="0ad72-128">Any drawing done inside the container will be restricted to the clipping region of that container and will also be restricted to the clipping regions of any outer containers and the clipping region of the **Graphics** object itself.</span></span>

<span data-ttu-id="0ad72-129">Les propriétés abordées jusqu’à présent (la transformation universelle et la région de découpage) sont combinées par des conteneurs imbriqués.</span><span class="sxs-lookup"><span data-stu-id="0ad72-129">The properties discussed so far — the world transformation and the clipping region — are combined by nested containers.</span></span> <span data-ttu-id="0ad72-130">D’autres propriétés sont remplacées temporairement par un conteneur imbriqué.</span><span class="sxs-lookup"><span data-stu-id="0ad72-130">Other properties are temporarily replaced by a nested container.</span></span> <span data-ttu-id="0ad72-131">Par exemple, si vous définissez le mode de lissage sur SmoothingModeAntiAlias dans un conteneur, toutes les méthodes de dessin appelées à l’intérieur de ce conteneur utilisent le mode de lissage anticrénelage, mais les méthodes de dessin appelées après [**Graphics :: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) utilisent le mode de lissage qui était en place avant l’appel à [**Graphics :: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span><span class="sxs-lookup"><span data-stu-id="0ad72-131">For example, if you set the smoothing mode to SmoothingModeAntiAlias within a container, any drawing methods called inside that container will use the antialias smoothing mode, but drawing methods called after [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will use the smoothing mode that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

<span data-ttu-id="0ad72-132">Pour obtenir un autre exemple de la combinaison des transformations universelles d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un conteneur, supposons que vous souhaitiez dessiner un œil et le placer à différents emplacements sur une séquence de visages.</span><span class="sxs-lookup"><span data-stu-id="0ad72-132">For another example of combining the world transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container, suppose you want to draw an eye and place it at various locations on a sequence of faces.</span></span> <span data-ttu-id="0ad72-133">L’exemple suivant dessine un œil centré sur l’origine du système de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="0ad72-133">The following example draws an eye centered at the origin of the coordinate system.</span></span>


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



<span data-ttu-id="0ad72-134">L’illustration suivante montre l’œil et les axes de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="0ad72-134">The following illustration shows the eye and the coordinate axes.</span></span>

![Illustration montrant un œil composé de trois ellipses : une pour le plan, un iris et un élève](images/aboutgdip05-art19.png)

<span data-ttu-id="0ad72-136">La fonction DrawEye, définie dans l’exemple précédent, reçoit l’adresse d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et crée immédiatement un conteneur dans cet objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="0ad72-136">The DrawEye function, defined in the previous example receives the address of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and immediately creates a container within that **Graphics** object.</span></span> <span data-ttu-id="0ad72-137">Ce conteneur isole tout code qui appelle la fonction DrawEye des paramètres de propriété effectués lors de l’exécution de la fonction DrawEye.</span><span class="sxs-lookup"><span data-stu-id="0ad72-137">This container insulates any code that calls the DrawEye function from property settings made during the execution of the DrawEye function.</span></span> <span data-ttu-id="0ad72-138">Par exemple, le code de la fonction DrawEye définit la zone de découpage de l’objet **Graphics** , mais lorsque DrawEye retourne le contrôle à la routine appelante, la zone de découpage est telle qu’elle était avant l’appel à DrawEye.</span><span class="sxs-lookup"><span data-stu-id="0ad72-138">For example, code in the DrawEye function sets the clipping region of the **Graphics** object, but when DrawEye returns control to the calling routine, the clipping region will be as it was before the call to DrawEye.</span></span>

<span data-ttu-id="0ad72-139">L’exemple suivant dessine trois ellipses (faces), chacune avec un œil à l’intérieur.</span><span class="sxs-lookup"><span data-stu-id="0ad72-139">The following example draws three ellipses (faces), each with an eye inside.</span></span>


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



<span data-ttu-id="0ad72-140">L’illustration suivante montre les trois ellipses.</span><span class="sxs-lookup"><span data-stu-id="0ad72-140">The following illustration shows the three ellipses.</span></span>

![capture d’écran d’une fenêtre avec trois ellipses, chacune contenant un œil à une taille et une rotation différentes](images/aboutgdip05-art20.png)

<span data-ttu-id="0ad72-142">Dans l’exemple précédent, toutes les ellipses sont dessinées avec l’appel `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` , qui dessine une ellipse centrée sur l’origine du système de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="0ad72-142">In the previous example, all ellipses are drawn with the call `DrawEllipse(&myBlackPen, -40, -60, 80, 120)`, which draws an ellipse centered at the origin of the coordinate system.</span></span> <span data-ttu-id="0ad72-143">Les ellipses sont déplacées hors de l’angle supérieur gauche de la zone cliente en définissant la transformation universelle de l’objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="0ad72-143">The ellipses are moved away from the upper-left corner of the client area by setting the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="0ad72-144">L’instruction fait en sorte que la première ellipse soit centrée sur (100, 100).</span><span class="sxs-lookup"><span data-stu-id="0ad72-144">The statement causes the first ellipse to be centered at (100, 100).</span></span> <span data-ttu-id="0ad72-145">L’instruction amène le centre de la deuxième ellipse à 100 unités à droite du centre de la première ellipse.</span><span class="sxs-lookup"><span data-stu-id="0ad72-145">The statement causes the center of the second ellipse to be 100 units to the right of the center of the first ellipse.</span></span> <span data-ttu-id="0ad72-146">De même, le centre de la troisième ellipse est 100 unités à droite du centre de la deuxième ellipse.</span><span class="sxs-lookup"><span data-stu-id="0ad72-146">Likewise, the center of the third ellipse is 100 units to the right of the center of the second ellipse.</span></span>

<span data-ttu-id="0ad72-147">Les conteneurs de l’exemple précédent sont utilisés pour transformer l’œil par rapport au centre d’une ellipse donnée.</span><span class="sxs-lookup"><span data-stu-id="0ad72-147">The containers in the previous example are used to transform the eye relative to the center of a given ellipse.</span></span> <span data-ttu-id="0ad72-148">Le premier œil est dessiné au centre de l’ellipse sans transformation, de sorte que l’appel DrawEye n’est pas à l’intérieur d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="0ad72-148">The first eye is drawn at the center of the ellipse with no transformation, so the DrawEye call is not inside a container.</span></span> <span data-ttu-id="0ad72-149">Le deuxième œil fait pivoter 40 degrés et a dessiné 30 unités au-dessus du centre de l’ellipse, de sorte que la fonction DrawEye et les méthodes qui définissent la transformation sont appelées à l’intérieur d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="0ad72-149">The second eye is rotated 40 degrees and drawn 30 units above the center of the ellipse, so the DrawEye function and the methods that set the transformation are called inside a container.</span></span> <span data-ttu-id="0ad72-150">Le troisième œil est étiré et pivoté et dessiné au centre de l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="0ad72-150">The third eye is stretched and rotated and drawn at the center of the ellipse.</span></span> <span data-ttu-id="0ad72-151">Comme pour le deuxième œil, la fonction DrawEye et les méthodes qui définissent la transformation sont appelées à l’intérieur d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="0ad72-151">As with the second eye, the DrawEye function and the methods that set the transformation are called inside a container.</span></span>

 

 
