---
description: Vous pouvez considérer la transformation de projection comme le contrôle des éléments internes de l’appareil photo. Cela revient à choisir une lentille pour l’appareil photo.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Transformation de projection (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b518583dd534bec9784590150233847274ca71
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200765"
---
# <a name="projection-transform-direct3d-9"></a><span data-ttu-id="9f6d0-103">Transformation de projection (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9f6d0-103">Projection Transform (Direct3D 9)</span></span>

<span data-ttu-id="9f6d0-104">Vous pouvez considérer la transformation de projection comme le contrôle des éléments internes de l’appareil photo. Cela revient à choisir une lentille pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-104">You can think of the projection transformation as controlling the camera's internals; it is analogous to choosing a lens for the camera.</span></span> <span data-ttu-id="9f6d0-105">Il s’agit du plus complexe des trois types de transformation.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-105">This is the most complicated of the three transformation types.</span></span> <span data-ttu-id="9f6d0-106">Cette présentation de la transformation de projection est organisée dans les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-106">This discussion of the projection transformation is organized into the following topics.</span></span>

<span data-ttu-id="9f6d0-107">La matrice de projection est généralement une projection d’échelle et de perspective.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-107">The projection matrix is typically a scale and perspective projection.</span></span> <span data-ttu-id="9f6d0-108">La transformation de projection convertit le frustum d’affichage en forme de cuboid.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-108">The projection transformation converts the viewing frustum into a cuboid shape.</span></span> <span data-ttu-id="9f6d0-109">Étant donné que la fin de la frustum d’affichage est inférieure à la fin, cela a pour effet d’étendre les objets qui sont proches de l’appareil photo. C’est ainsi que la perspective est appliquée à la scène.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-109">Because the near end of the viewing frustum is smaller than the far end, this has the effect of expanding objects that are near to the camera; this is how perspective is applied to the scene.</span></span>

<span data-ttu-id="9f6d0-110">Dans [le frustum de visualisation](viewports-and-clipping.md), la distance entre l’appareil photo et l’origine de l’espace de transformation d’affichage est définie arbitrairement comme D, donc la matrice de projection ressemble à l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-110">In [the viewing frustum](viewports-and-clipping.md), the distance between the camera and the origin of the viewing transform space is defined arbitrarily as D, so the projection matrix looks like the following illustration.</span></span>

![illustration de la matrice de projection](images/projmat1.png)

<span data-ttu-id="9f6d0-112">La matrice d’affichage traduit la caméra en l’origine en traduisant dans la direction z par-D. La matrice de translation ressemble à l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-112">The viewing matrix translates the camera to the origin by translating in the z direction by - D. The translation matrix is like the following illustration.</span></span>

![illustration de la matrice de traduction](images/projmat2.png)

<span data-ttu-id="9f6d0-114">La multiplication de la matrice de translation par la matrice de projection (T \* P) donne à la matrice de projection composite, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-114">Multiplying the translation matrix by the projection matrix (T\*P) gives the composite projection matrix, as shown in the following illustration.</span></span>

![illustration de la matrice de projection composite](images/projmat3.png)

<span data-ttu-id="9f6d0-116">La transformation de perspective convertit un frustum d’affichage en un nouvel espace de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-116">The perspective transform converts a viewing frustum into a new coordinate space.</span></span> <span data-ttu-id="9f6d0-117">Notez que le frustum devient cuboid et que l’origine passe de l’angle supérieur droit de la scène au centre, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-117">Notice that the frustum becomes cuboid and also that the origin moves from the upper-right corner of the scene to the center, as shown in the following diagram.</span></span>

![Diagramme illustrant comment la transformation de perspective change le frustum d’affichage en nouvel espace de coordonnées](images/cuboid.png)

<span data-ttu-id="9f6d0-119">Dans la transformation de perspective, les limites des directions x et y sont-1 et 1.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-119">In the perspective transform, the limits of the x- and y-directions are -1 and 1.</span></span> <span data-ttu-id="9f6d0-120">Les limites de l’axe z sont 0 pour le plan avant et 1 pour le plan arrière.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-120">The limits of the z-direction are 0 for the front plane and 1 for the back plane.</span></span>

<span data-ttu-id="9f6d0-121">Cette matrice convertit et met à l’échelle des objets en fonction d’une distance spécifiée entre l’appareil photo et le plan de découpage proche, mais il ne tient pas compte du champ de vue (l’angle de vue) et les valeurs z qu’il produit pour les objets de la distance peuvent être presque identiques, ce qui complique les comparaisons de profondeur.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-121">This matrix translates and scales objects based on a specified distance from the camera to the near clipping plane, but it doesn't consider the field of view (fov), and the z-values that it produces for objects in the distance can be nearly identical, making depth comparisons difficult.</span></span> <span data-ttu-id="9f6d0-122">La matrice suivante résout ces problèmes et ajuste les sommets pour prendre en compte les proportions de la fenêtre d’affichage, ce qui en fait un bon choix pour la projection de perspective.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-122">The following matrix addresses these issues, and it adjusts vertices to account for the aspect ratio of the viewport, making it a good choice for the perspective projection.</span></span>

![illustration d’une matrice pour la projection de perspective](images/prjmatx1.png)

<span data-ttu-id="9f6d0-124">Dans cette matrice, Zn est la valeur z du plan de découpage proche.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-124">In this matrix, Zₙ is the z-value of the near clipping plane.</span></span> <span data-ttu-id="9f6d0-125">Les variables w, h et Q ont les significations suivantes.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-125">The variables w, h, and Q have the following meanings.</span></span> <span data-ttu-id="9f6d0-126">Notez que le point d’affichage et le fovk représentent les champs<sub>horizontal et vertical</sub> de la fenêtre d’affichage, en radians.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-126">Note that fov<sub>w</sub> and fovₖ represent the viewport's horizontal and vertical fields of view, in radians.</span></span>

![équations des significations variables](images/prjmatx2.png)

<span data-ttu-id="9f6d0-128">Pour votre application, l’utilisation d’angles de champ pour définir les coefficients de mise à l’échelle x et y peut ne pas être aussi pratique que l’utilisation des dimensions horizontales et verticales de la fenêtre d’affichage (dans l’espace de l’appareil photo).</span><span class="sxs-lookup"><span data-stu-id="9f6d0-128">For your application, using field-of-view angles to define the x- and y-scaling coefficients might not be as convenient as using the viewport's horizontal and vertical dimensions (in camera space).</span></span> <span data-ttu-id="9f6d0-129">À mesure que les mathématiques fonctionnent, les deux équations suivantes pour w et h utilisent les dimensions de la fenêtre d’affichage, et sont équivalentes aux équations précédentes.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-129">As the math works out, the following two equations for w and h use the viewport's dimensions, and are equivalent to the preceding equations.</span></span>

![équations de la moyenne des variables w et h](images/prjmatx3.png)

<span data-ttu-id="9f6d0-131">Dans ces formules, Zn représente la position du plan de découpage proche, et les variables V<sub>w</sub> et VH représentent la largeur et la hauteur de la fenêtre d’affichage, dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-131">In these formulas, Zₙ represents the position of the near clipping plane, and the V<sub>w</sub> and Vₕ variables represent the width and height of the viewport, in camera space.</span></span>

<span data-ttu-id="9f6d0-132">Pour une application C++, ces deux dimensions correspondent directement aux membres Width et Height de la structure [**D3DVIEWPORT9**](d3dviewport9.md) .</span><span class="sxs-lookup"><span data-stu-id="9f6d0-132">For a C++ application, these two dimensions correspond directly to the Width and Height members of the [**D3DVIEWPORT9**](d3dviewport9.md) structure.</span></span>

<span data-ttu-id="9f6d0-133">Quelle que soit la formule que vous décidez d’utiliser, veillez à définir Zn sur une valeur aussi grande que possible, car les valeurs z les plus proches de l’appareil photo ne varient pas.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-133">Whatever formula you decide to use, be sure to set Zₙ to as large a value as possible, because z-values extremely close to the camera don't vary by much.</span></span> <span data-ttu-id="9f6d0-134">Les comparaisons de profondeur utilisant des tampons z 16 bits sont donc quelque peu compliquées.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-134">This makes depth comparisons using 16-bit z-buffers somewhat complicated.</span></span>

<span data-ttu-id="9f6d0-135">Comme pour le monde et les transformations d’affichage, vous appelez la méthode [**IDirect3DDevice9 :: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) pour définir la transformation de projection.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-135">As with the world and view transformations, you call the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the projection transform.</span></span>

## <a name="setting-up-a-projection-matrix"></a><span data-ttu-id="9f6d0-136">Configuration d’une matrice de projection</span><span class="sxs-lookup"><span data-stu-id="9f6d0-136">Setting Up a Projection Matrix</span></span>

<span data-ttu-id="9f6d0-137">L’exemple de fonction ProjectionMatrix suivant définit les plans de l’avant et de l’arrière-plan, ainsi que le champ horizontal et vertical des angles de vue.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-137">The following ProjectionMatrix sample function sets the front and back clipping planes, as well as the horizontal and vertical field of view angles.</span></span> <span data-ttu-id="9f6d0-138">Les champs de la vue doivent être inférieurs à pi radians.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-138">The fields of view should be less than pi radians.</span></span>


```
D3DXMATRIX 
ProjectionMatrix(const float near_plane, // Distance to near clipping 
                                         // plane
                 const float far_plane,  // Distance to far clipping 
                                         // plane
                 const float fov_horiz,  // Horizontal field of view 
                                         // angle, in radians
                 const float fov_vert)   // Vertical field of view 
                                         // angle, in radians
{
    float    h, w, Q;

    w = (float)1/tan(fov_horiz*0.5);  // 1/tan(x) == cot(x)
    h = (float)1/tan(fov_vert*0.5);   // 1/tan(x) == cot(x)
    Q = far_plane/(far_plane - near_plane);

    D3DXMATRIX ret;
    ZeroMemory(&ret, sizeof(ret));

    ret(0, 0) = w;
    ret(1, 1) = h;
    ret(2, 2) = Q;
    ret(3, 2) = -Q*near_plane;
    ret(2, 3) = 1;
    return ret;
}   // End of ProjectionMatrix
```



<span data-ttu-id="9f6d0-139">Après avoir créé la matrice, définissez-la avec [**IDirect3DDevice9 :: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) en spécifiant la \_ projection D3DTS.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-139">After creating the matrix, set it with [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) specifying D3DTS\_PROJECTION.</span></span>

<span data-ttu-id="9f6d0-140">La bibliothèque de l’utilitaire D3DX fournit les fonctions suivantes pour vous aider à configurer votre matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-140">The D3DX utility library provides the following functions to help you set up your projection matrix.</span></span>

-   [<span data-ttu-id="9f6d0-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="9f6d0-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
-   [<span data-ttu-id="9f6d0-142">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="9f6d0-142">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
-   [<span data-ttu-id="9f6d0-143">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="9f6d0-143">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
-   [<span data-ttu-id="9f6d0-144">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="9f6d0-144">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
-   [<span data-ttu-id="9f6d0-145">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="9f6d0-145">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
-   [<span data-ttu-id="9f6d0-146">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="9f6d0-146">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a><span data-ttu-id="9f6d0-147">Une matrice de projection avec l’e-friendly</span><span class="sxs-lookup"><span data-stu-id="9f6d0-147">A W-Friendly Projection Matrix</span></span>

<span data-ttu-id="9f6d0-148">Direct3D peut utiliser le composant w d’un vertex qui a été transformé par les matrices de projection, de vue et de projection pour effectuer des calculs en fonction de la profondeur dans un tampon de profondeur ou des effets de brouillard.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-148">Direct3D can use the w-component of a vertex that has been transformed by the world, view, and projection matrices to perform depth-based calculations in depth-buffer or fog effects.</span></span> <span data-ttu-id="9f6d0-149">Les calculs tels que ceux-ci requièrent que votre matrice de projection normalise le w pour être équivalente à l’espace universel z.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-149">Computations such as these require that your projection matrix normalize w to be equivalent to world-space z.</span></span> <span data-ttu-id="9f6d0-150">En résumé, si votre matrice de projection comprend un coefficient (3,4) qui n’est pas 1, vous devez mettre à l’échelle tous les coefficients à l’inverse du coefficient (3,4) pour créer une matrice appropriée.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-150">In short, if your projection matrix includes a (3,4) coefficient that is not 1, you must scale all the coefficients by the inverse of the (3,4) coefficient to make a proper matrix.</span></span> <span data-ttu-id="9f6d0-151">Si vous ne fournissez pas de matrice conforme, les effets de brouillard et la mise en mémoire tampon de profondeur ne sont pas appliqués correctement.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-151">If you don't provide a compliant matrix, fog effects and depth buffering are not applied correctly.</span></span>

<span data-ttu-id="9f6d0-152">L’illustration suivante montre une matrice de projection non conforme, et la même matrice mise à l’échelle afin que le brouillard relatif à l’oeil soit activé.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-152">The following illustration shows a noncompliant projection matrix, and the same matrix scaled so that eye-relative fog will be enabled.</span></span>

![illustrations d’une matrice de projection non conforme et d’une matrice avec brouillard relatif à l’oeil](images/eyerlmx.png)

<span data-ttu-id="9f6d0-154">Dans les matrices précédentes, toutes les variables sont supposées être non nulles.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-154">In the preceding matrices, all variables are assumed to be nonzero.</span></span> <span data-ttu-id="9f6d0-155">Pour plus d’informations sur le brouillard relatif à l’oeil, consultez la page relative à l’œil et à la [profondeur Z](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d0-155">For more information about eye-relative fog, see [Eye-Relative vs. Z-Based Depth](pixel-fog.md).</span></span> <span data-ttu-id="9f6d0-156">Pour plus d’informations sur la mise en mémoire tampon de profondeur basée sur w, consultez [mémoires tampons de profondeur (Direct3D 9)](depth-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d0-156">For information about w-based depth buffering, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="9f6d0-157">Direct3D utilise la matrice de projection actuellement définie dans ses calculs de profondeur basés sur w.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-157">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="9f6d0-158">Par conséquent, les applications doivent définir une matrice de projection conforme pour recevoir les fonctionnalités w souhaitées, même si elles n’utilisent pas Direct3D pour les transformations.</span><span class="sxs-lookup"><span data-stu-id="9f6d0-158">As a result, applications must set a compliant projection matrix to receive the desired w-based features, even if they do not use Direct3D for transforms.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f6d0-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9f6d0-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f6d0-160">Transformations</span><span class="sxs-lookup"><span data-stu-id="9f6d0-160">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 
