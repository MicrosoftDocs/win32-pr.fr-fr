---
title: Application de transformations dans Direct2D
description: Application de transformations dans Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8edddbb3150f16428c56bd4c6da828c9b2ce594e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727340"
---
# <a name="applying-transforms-in-direct2d"></a><span data-ttu-id="8e302-103">Application de transformations dans Direct2D</span><span class="sxs-lookup"><span data-stu-id="8e302-103">Applying Transforms in Direct2D</span></span>

<span data-ttu-id="8e302-104">En [dessin avec Direct2D](drawing-with-direct2d.md), nous avons vu que la méthode [**ID2D1RenderTarget :: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) dessine une ellipse alignée sur les axes x et y.</span><span class="sxs-lookup"><span data-stu-id="8e302-104">In [Drawing with Direct2D](drawing-with-direct2d.md), we saw that the [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws an ellipse that is aligned to the x- and y-axes.</span></span> <span data-ttu-id="8e302-105">Mais supposons que vous souhaitiez dessiner une ellipse inclinée à un angle ?</span><span class="sxs-lookup"><span data-stu-id="8e302-105">But suppose that you want to draw an ellipse tilted at an angle?</span></span>

![image qui affiche une ellipse inclinée.](images/graphics16.png)

<span data-ttu-id="8e302-107">À l’aide de transformations, vous pouvez modifier une forme des manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e302-107">By using transforms, you can alter a shape in the following ways.</span></span>

-   <span data-ttu-id="8e302-108">Rotation autour d’un point.</span><span class="sxs-lookup"><span data-stu-id="8e302-108">Rotation around a point.</span></span>
-   <span data-ttu-id="8e302-109">Mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="8e302-109">Scaling.</span></span>
-   <span data-ttu-id="8e302-110">Translation (déplacement dans la direction X ou Y).</span><span class="sxs-lookup"><span data-stu-id="8e302-110">Translation (displacement in the X or Y direction).</span></span>
-   <span data-ttu-id="8e302-111">Skew (également appelé *cisaillement*).</span><span class="sxs-lookup"><span data-stu-id="8e302-111">Skew (also known as *shear*).</span></span>

<span data-ttu-id="8e302-112">Une transformation est une opération mathématique qui mappe un ensemble de points à un nouvel ensemble de points.</span><span class="sxs-lookup"><span data-stu-id="8e302-112">A transform is a mathematical operation that maps a set of points to a new set of points.</span></span> <span data-ttu-id="8e302-113">Par exemple, le diagramme suivant montre un triangle pivoté autour du point P3.</span><span class="sxs-lookup"><span data-stu-id="8e302-113">For example, the following diagram shows a triangle rotated around the point P3.</span></span> <span data-ttu-id="8e302-114">Une fois la rotation appliquée, le point P1 est mappé à P1 ', le point P2 est mappé à P2 'et le point P3 est mappé à lui-même.</span><span class="sxs-lookup"><span data-stu-id="8e302-114">After the rotation is applied, the point P1 is mapped to P1', the point P2 is mapped to P2', and the point P3 maps to itself.</span></span>

![diagramme qui montre une rotation autour d’un point.](images/graphics17.png)

<span data-ttu-id="8e302-116">Les transformations sont implémentées à l’aide de matrices.</span><span class="sxs-lookup"><span data-stu-id="8e302-116">Transforms are implemented by using matrices.</span></span> <span data-ttu-id="8e302-117">Toutefois, vous n’avez pas besoin de comprendre les mathématiques des matrices pour pouvoir les utiliser.</span><span class="sxs-lookup"><span data-stu-id="8e302-117">However, you do not have to understand the mathematics of matrices in order to use them.</span></span> <span data-ttu-id="8e302-118">Si vous souhaitez en savoir plus sur les mathématiques, consultez [annexe : matrice transformations](appendix--matrix-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="8e302-118">If you want to learn more about the math, see [Appendix: Matrix Transforms](appendix--matrix-transforms.md).</span></span>

<span data-ttu-id="8e302-119">Pour appliquer une transformation dans Direct2D, appelez la méthode [**ID2D1RenderTarget :: setTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) .</span><span class="sxs-lookup"><span data-stu-id="8e302-119">To apply a transform in Direct2D, call the [**ID2D1RenderTarget::SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) method.</span></span> <span data-ttu-id="8e302-120">Cette méthode prend une structure [**d2d1 \_ Matrix \_ matrice \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) qui définit la transformation.</span><span class="sxs-lookup"><span data-stu-id="8e302-120">This method takes a [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure that defines the transformation.</span></span> <span data-ttu-id="8e302-121">Vous pouvez initialiser cette structure en appelant des méthodes sur la classe [**d2d1 :: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="8e302-121">You can initialize this structure by calling methods on the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="8e302-122">Cette classe contient des méthodes statiques qui retournent une matrice pour chaque type de transformation :</span><span class="sxs-lookup"><span data-stu-id="8e302-122">This class contains static methods that return a matrix for each kind of transform:</span></span>

-   [<span data-ttu-id="8e302-123">**Matrix3x2F :: rotation**</span><span class="sxs-lookup"><span data-stu-id="8e302-123">**Matrix3x2F::Rotation**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   <span data-ttu-id="8e302-124">[**Matrix3x2F :: Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span><span class="sxs-lookup"><span data-stu-id="8e302-124">[**Matrix3x2F::Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span></span>
-   <span data-ttu-id="8e302-125">[**Matrix3x2F :: translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span><span class="sxs-lookup"><span data-stu-id="8e302-125">[**Matrix3x2F::Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span></span>
-   [<span data-ttu-id="8e302-126">**Matrix3x2F :: Skew**</span><span class="sxs-lookup"><span data-stu-id="8e302-126">**Matrix3x2F::Skew**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

<span data-ttu-id="8e302-127">Par exemple, le code suivant applique une rotation à 20 degrés autour du point (100, 100).</span><span class="sxs-lookup"><span data-stu-id="8e302-127">For example, the following code applies a 20-degree rotation around the point (100, 100).</span></span>


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

<span data-ttu-id="8e302-128">La transformation est appliquée à toutes les opérations de dessin ultérieures jusqu’à ce que vous rappeliez [**setTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) .</span><span class="sxs-lookup"><span data-stu-id="8e302-128">The transform is applied to all later drawing operations until you call [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) again.</span></span> <span data-ttu-id="8e302-129">Pour supprimer la transformation actuelle, appelez **setTransform** avec la matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="8e302-129">To remove the current transform, call **SetTransform** with the identity matrix.</span></span> <span data-ttu-id="8e302-130">Pour créer la matrice d’identité, appelez la fonction [**Matrix3x2F :: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) .</span><span class="sxs-lookup"><span data-stu-id="8e302-130">To create the identity matrix, call the [**Matrix3x2F::Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) function.</span></span>


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a><span data-ttu-id="8e302-131">Dessin des aiguilles de l’horloge</span><span class="sxs-lookup"><span data-stu-id="8e302-131">Drawing Clock Hands</span></span>

<span data-ttu-id="8e302-132">Nous allons mettre en place des transformations en convertissant notre programme Circle en horloge analogique.</span><span class="sxs-lookup"><span data-stu-id="8e302-132">Let's put transforms to use by converting our Circle program into an analog clock.</span></span> <span data-ttu-id="8e302-133">Nous pouvons faire cela en ajoutant des lignes pour les mains.</span><span class="sxs-lookup"><span data-stu-id="8e302-133">We can do this by adding lines for the hands.</span></span>

![capture d’écran du programme d’horloge analogique.](images/graphics18.png)

<span data-ttu-id="8e302-135">Au lieu de calculer les coordonnées des lignes, nous pouvons calculer l’angle, puis appliquer une transformation de rotation.</span><span class="sxs-lookup"><span data-stu-id="8e302-135">Instead of calculating the coordinates for the lines, we can calculate the angle and then apply a rotation transform.</span></span> <span data-ttu-id="8e302-136">Le code suivant illustre une fonction qui dessine une main.</span><span class="sxs-lookup"><span data-stu-id="8e302-136">The following code shows a function that draws one clock hand.</span></span> <span data-ttu-id="8e302-137">Le paramètre *fAngle* donne l’angle de la main, en degrés.</span><span class="sxs-lookup"><span data-stu-id="8e302-137">The *fAngle* parameter gives the angle of the hand, in degrees.</span></span>

```C++
void Scene::DrawClockHand(float fHandLength, float fAngle, float fStrokeWidth)
{
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(fAngle, m_ellipse.point)
            );

    // endPoint defines one end of the hand.
    D2D_POINT_2F endPoint = D2D1::Point2F(
        m_ellipse.point.x,
        m_ellipse.point.y - (m_ellipse.radiusY * fHandLength)
        );

    // Draw a line from the center of the ellipse to endPoint.
    m_pRenderTarget->DrawLine(
        m_ellipse.point, endPoint, m_pStroke, fStrokeWidth);
}
```

<span data-ttu-id="8e302-138">Ce code dessine une ligne verticale, en commençant par le centre de l’horloge et en se terminant au point de *terminaison* du point.</span><span class="sxs-lookup"><span data-stu-id="8e302-138">This code draws a vertical line, starting from the center of the clock face and ending at the point *endPoint*.</span></span> <span data-ttu-id="8e302-139">La ligne pivote autour du centre de l’ellipse en appliquant une transformation de rotation.</span><span class="sxs-lookup"><span data-stu-id="8e302-139">The line is rotated around the center of the ellipse by applying a rotation transform.</span></span> <span data-ttu-id="8e302-140">Le point central de la rotation est le centre de l’ellipse qui forme la face de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="8e302-140">The center point for the rotation is the center of ellipse that forms the clock face.</span></span>

![diagramme qui affiche la rotation de la main d’horloge.](images/graphics19.png)

<span data-ttu-id="8e302-142">Le code suivant montre comment le cadran entier est dessiné.</span><span class="sxs-lookup"><span data-stu-id="8e302-142">The following code shows how the whole clock face is drawn.</span></span>

```C++
void Scene::RenderScene()
{
    m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::SkyBlue));

    m_pRenderTarget->FillEllipse(m_ellipse, m_pFill);
    m_pRenderTarget->DrawEllipse(m_ellipse, m_pStroke);

    // Draw hands
    SYSTEMTIME time;
    GetLocalTime(&time);

    // 60 minutes = 30 degrees, 1 minute = 0.5 degree
    const float fHourAngle = (360.0f / 12) * (time.wHour) + (time.wMinute * 0.5f);
    const float fMinuteAngle =(360.0f / 60) * (time.wMinute);

    DrawClockHand(0.6f,  fHourAngle,   6);
    DrawClockHand(0.85f, fMinuteAngle, 4);

    // Restore the identity transformation.
    m_pRenderTarget->SetTransform( D2D1::Matrix3x2F::Identity() );
}
```

<span data-ttu-id="8e302-143">Vous pouvez télécharger le projet Visual Studio complet à partir de l' [exemple d’horloge Direct2D](direct2d-clock-sample.md).</span><span class="sxs-lookup"><span data-stu-id="8e302-143">You can download the complete Visual Studio project from [Direct2D Clock Sample](direct2d-clock-sample.md).</span></span> <span data-ttu-id="8e302-144">(Juste pour le plaisir, la version de téléchargement ajoute un gradiant radial à la face de l’horloge.)</span><span class="sxs-lookup"><span data-stu-id="8e302-144">(Just for fun, the download version adds a radial gradiant to the clock face.)</span></span>

## <a name="combining-transforms"></a><span data-ttu-id="8e302-145">Combinaison de transformations</span><span class="sxs-lookup"><span data-stu-id="8e302-145">Combining Transforms</span></span>

<span data-ttu-id="8e302-146">Les quatre transformations de base peuvent être combinées en multipliant au moins deux matrices.</span><span class="sxs-lookup"><span data-stu-id="8e302-146">The four basic transforms can be combined by multiplying two or more matrices.</span></span> <span data-ttu-id="8e302-147">Par exemple, le code suivant combine une rotation et une translation.</span><span class="sxs-lookup"><span data-stu-id="8e302-147">For example, the following code combines a rotation with a translation.</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="8e302-148">La classe [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) fournit l' [**opérateur \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) pour la multiplication de matrice.</span><span class="sxs-lookup"><span data-stu-id="8e302-148">The [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class provides [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for matrix multiplication.</span></span> <span data-ttu-id="8e302-149">L’ordre dans lequel vous multipliez les matrices est important.</span><span class="sxs-lookup"><span data-stu-id="8e302-149">The order in which you multiply the matrices is important.</span></span> <span data-ttu-id="8e302-150">La définition d’une transformation (M × N) signifie « Apply M First, suivi de N ».</span><span class="sxs-lookup"><span data-stu-id="8e302-150">Setting a transform (M × N) means "Apply M first, followed by N."</span></span> <span data-ttu-id="8e302-151">Par exemple, voici la rotation suivie d’une traduction :</span><span class="sxs-lookup"><span data-stu-id="8e302-151">For example, here is rotation followed by translation:</span></span>

![diagramme qui affiche la rotation suivie d’une traduction.](images/graphics20.png)

<span data-ttu-id="8e302-153">Voici le code de cette transformation :</span><span class="sxs-lookup"><span data-stu-id="8e302-153">Here is the code for this transform:</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="8e302-154">Comparez maintenant cette transformation à une transformation dans l’ordre inverse, à la translation suivie de la rotation.</span><span class="sxs-lookup"><span data-stu-id="8e302-154">Now compare that transform with a transform in the reverse order, translation followed by rotation.</span></span>

![diagramme qui affiche la translation suivie d’une rotation.](images/graphics21.png)

<span data-ttu-id="8e302-156">La rotation est effectuée autour du centre du rectangle d’origine.</span><span class="sxs-lookup"><span data-stu-id="8e302-156">The rotation is performed around the center of the original rectangle.</span></span> <span data-ttu-id="8e302-157">Voici le code de cette transformation.</span><span class="sxs-lookup"><span data-stu-id="8e302-157">Here is the code for this transform.</span></span>

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

<span data-ttu-id="8e302-158">Comme vous pouvez le voir, les matrices sont identiques, mais l’ordre des opérations a changé.</span><span class="sxs-lookup"><span data-stu-id="8e302-158">As you can see, the matrices are the same, but the order of operations has changed.</span></span> <span data-ttu-id="8e302-159">Cela se produit parce que la multiplication de matrice n’est pas commutative : M × N ≠ N × M.</span><span class="sxs-lookup"><span data-stu-id="8e302-159">This happens because matrix multiplication is not commutative: M × N ≠ N × M.</span></span>

## <a name="next"></a><span data-ttu-id="8e302-160">Suivant</span><span class="sxs-lookup"><span data-stu-id="8e302-160">Next</span></span>

[<span data-ttu-id="8e302-161">Annexe : transformations de matrice</span><span class="sxs-lookup"><span data-stu-id="8e302-161">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)