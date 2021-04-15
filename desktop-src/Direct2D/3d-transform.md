---
title: Effet de transformation 3D
description: Utilisez l’effet Transformation 3D pour appliquer une matrice de transformation 4x4 arbitraire à une image.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- transformation 3D, effet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104555569"
---
# <a name="3d-transform-effect"></a><span data-ttu-id="510d2-104">Effet de transformation 3D</span><span class="sxs-lookup"><span data-stu-id="510d2-104">3D transform effect</span></span>

<span data-ttu-id="510d2-105">Utilisez l’effet Transformation 3D pour appliquer une matrice de transformation 4x4 arbitraire à une image.</span><span class="sxs-lookup"><span data-stu-id="510d2-105">Use the 3D transform effect to apply an arbitrary 4x4 transform matrix to an image.</span></span>

<span data-ttu-id="510d2-106">Cet effet applique la matrice (M ?) que vous fournissez aux sommets d’angle de l’image source ( \[ x y z 1 \] ) à l’aide de ce calcul :</span><span class="sxs-lookup"><span data-stu-id="510d2-106">This effect applies the matrix (M?) you provide to the corner vertices of the source image (\[ x y z 1 \]) using this calculation:</span></span>

<span data-ttu-id="510d2-107">\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M ?</span><span class="sxs-lookup"><span data-stu-id="510d2-107">\[ x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \]=\[ x y z 1 \]\*M?</span></span>

<span data-ttu-id="510d2-108">Le CLSID de cet effet est CLSID \_ D2D13DTransform.</span><span class="sxs-lookup"><span data-stu-id="510d2-108">The CLSID for this effect is CLSID\_D2D13DTransform.</span></span>

-   [<span data-ttu-id="510d2-109">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="510d2-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="510d2-110">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="510d2-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="510d2-111">Modes d’interpolation</span><span class="sxs-lookup"><span data-stu-id="510d2-111">Interpolation modes</span></span>](#interpolation-modes)
    -   [<span data-ttu-id="510d2-112">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="510d2-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="510d2-113">Classe de matrice de transformation 4x4</span><span class="sxs-lookup"><span data-stu-id="510d2-113">4x4 Transform Matrix Class</span></span>](#4x4-transform-matrix-class)
-   [<span data-ttu-id="510d2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="510d2-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="510d2-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="510d2-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="510d2-116">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="510d2-116">Example image</span></span>



| <span data-ttu-id="510d2-117">Avant</span><span class="sxs-lookup"><span data-stu-id="510d2-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![image avant la transformation.](images/default-before.jpg) |
| <span data-ttu-id="510d2-119">After</span><span class="sxs-lookup"><span data-stu-id="510d2-119">After</span></span>                                                         |
| ![image après la transformation.](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="510d2-121">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="510d2-121">Effect properties</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="510d2-122">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="510d2-122">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="510d2-123">Description</span><span class="sxs-lookup"><span data-stu-id="510d2-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="510d2-124">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="510d2-124">InterpolationMode</span></span><br/> <span data-ttu-id="510d2-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="510d2-125">D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="510d2-126">Mode d’interpolation utilisé par l’effet sur l’image.</span><span class="sxs-lookup"><span data-stu-id="510d2-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="510d2-127">Il existe 5 modes de mise à l’échelle qui vont de la qualité et de la vitesse.</span><span class="sxs-lookup"><span data-stu-id="510d2-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="510d2-128">Le type est D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="510d2-128">Type is D2D1_3DTRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="510d2-129">La valeur par défaut est D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="510d2-129">Default value is D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510d2-130">BorderMode</span><span class="sxs-lookup"><span data-stu-id="510d2-130">BorderMode</span></span><br/> <span data-ttu-id="510d2-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="510d2-131">D2D1_3DTRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="510d2-132">Le mode utilisé pour calculer la bordure de l’image, soft ou Hard.</span><span class="sxs-lookup"><span data-stu-id="510d2-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="510d2-133">Pour plus d’informations, consultez <a href="https://www.bing.com/search?q=Border+modes">modes de bordure</a> .</span><span class="sxs-lookup"><span data-stu-id="510d2-133">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span><br/> <span data-ttu-id="510d2-134">Le type est D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="510d2-134">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="510d2-135">La valeur par défaut est D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="510d2-135">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510d2-136">TransformMatrix</span><span class="sxs-lookup"><span data-stu-id="510d2-136">TransformMatrix</span></span><br/> <span data-ttu-id="510d2-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="510d2-137">D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="510d2-138">Matrice de transformation 4x4 appliquée au plan de projection.</span><span class="sxs-lookup"><span data-stu-id="510d2-138">A 4x4 transform matrix applied to the projection plane.</span></span> <span data-ttu-id="510d2-139">Le calcul de matrice suivant est utilisé pour mapper des points d’un système de coordonnées 3D au système de coordonnées 2D transformé.</span><span class="sxs-lookup"><span data-stu-id="510d2-139">The following matrix calculation is used to map points from one 3D coordinate system to the transformed 2D coordinate system.</span></span> <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" /><span data-ttu-id="510d2-140">Où :</span><span class="sxs-lookup"><span data-stu-id="510d2-140">Where:</span></span><dl> <span data-ttu-id="510d2-141">X, Y, Z = coordonnées du plan de projection d’entrée</span><span class="sxs-lookup"><span data-stu-id="510d2-141">X, Y, Z = Input projection plane coordinates</span></span><br />
<span data-ttu-id="510d2-142">M<sub>x, y</sub> = transformer les éléments de la matrice</span><span class="sxs-lookup"><span data-stu-id="510d2-142">M<sub>x,y</sub> = Transform Matrix elements</span></span><br />
<span data-ttu-id="510d2-143">X, Y, Z = coordonnées du plan de projection de sortie</span><span class="sxs-lookup"><span data-stu-id="510d2-143">X , Y , Z  =Output projection plane coordinates</span></span><br />
</dl> <br/> <span data-ttu-id="510d2-144">Les éléments de matrice individuels ne sont pas limités et sont sans unité.</span><span class="sxs-lookup"><span data-stu-id="510d2-144">The individual matrix elements are not bounded and are unitless.</span></span> <br/> <span data-ttu-id="510d2-145">Le type est D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="510d2-145">Type is D2D1_MATRIX_4X4_F.</span></span><br/> <span data-ttu-id="510d2-146">La valeur par défaut est Matrix4x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="510d2-146">Default value is Matrix4x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a><span data-ttu-id="510d2-147">Modes d’interpolation</span><span class="sxs-lookup"><span data-stu-id="510d2-147">Interpolation modes</span></span>



| <span data-ttu-id="510d2-148">Énumération</span><span class="sxs-lookup"><span data-stu-id="510d2-148">Enumeration</span></span>                                                   | <span data-ttu-id="510d2-149">Description</span><span class="sxs-lookup"><span data-stu-id="510d2-149">Description</span></span>                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="510d2-150">\_Mode d’interpolation d2d1 3DTRANSFORM \_ \_ \_ le plus proche \_ voisin</span><span class="sxs-lookup"><span data-stu-id="510d2-150">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="510d2-151">Échantillonne le point unique le plus proche et l’utilise.</span><span class="sxs-lookup"><span data-stu-id="510d2-151">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="510d2-152">Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.</span><span class="sxs-lookup"><span data-stu-id="510d2-152">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="510d2-153">D2D1 \_ \_ mode d’interpolation \_ 3DTRANSFORM \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="510d2-153">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="510d2-154">Utilise un échantillon à quatre points et une interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="510d2-154">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="510d2-155">Ce mode utilise plus de temps de traitement que le mode voisin le plus proche, mais génère une image de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="510d2-155">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="510d2-156">D2D1 \_ 3DTRANSFORM \_ mode d' \_ interpolation \_ cubique</span><span class="sxs-lookup"><span data-stu-id="510d2-156">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="510d2-157">Utilise un exemple de noyau cubique 16 pour l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="510d2-157">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="510d2-158">Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="510d2-158">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="510d2-159">\_Mode d’interpolation d2d1 3DTRANSFORM multi- \_ \_ \_ \_ exemple \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="510d2-159">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="510d2-160">Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="510d2-160">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="510d2-161">Ce mode est adapté à la réduction de la taille des images avec quelques pixels.</span><span class="sxs-lookup"><span data-stu-id="510d2-161">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="510d2-162">D2D1 \_ \_ mode d’interpolation \_ 3DTRANSFORM \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="510d2-162">D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="510d2-163">Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="510d2-163">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="510d2-164">Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ 3DTRANSFORM \_ interpolation \_ mode \_ Linear.</span><span class="sxs-lookup"><span data-stu-id="510d2-164">If you don't select a mode, the effect defaults to D2D1\_3DTRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="510d2-165">Le mode anisotrope génère des mipmaps lors de la mise à l’échelle. Toutefois, si vous affectez à la propriété **Cached** la valeur true sur les effets entrés dans cet effet, le des mipmaps ne sera pas généré à chaque fois pour des images suffisamment petites.</span><span class="sxs-lookup"><span data-stu-id="510d2-165">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

### <a name="border-modes"></a><span data-ttu-id="510d2-166">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="510d2-166">Border modes</span></span>



| <span data-ttu-id="510d2-167">Nom</span><span class="sxs-lookup"><span data-stu-id="510d2-167">Name</span></span>                     | <span data-ttu-id="510d2-168">Description</span><span class="sxs-lookup"><span data-stu-id="510d2-168">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="510d2-169">\_Mode de bordure d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="510d2-169">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="510d2-170">L’effet remplit l’image avec des pixels noirs transparents au fur et à mesure de l’interpolation, ce qui génère une bordure douce.</span><span class="sxs-lookup"><span data-stu-id="510d2-170">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="510d2-171">D2D1 \_ mode de bordure \_ \_ difficile</span><span class="sxs-lookup"><span data-stu-id="510d2-171">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="510d2-172">L’effet attache la sortie à la taille de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="510d2-172">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a><span data-ttu-id="510d2-173">Classe de matrice de transformation 4x4</span><span class="sxs-lookup"><span data-stu-id="510d2-173">4x4 Transform Matrix Class</span></span>

<span data-ttu-id="510d2-174">Direct2D fournit une classe de matrice 4x4 pour fournir des fonctions d’assistance pour transformer l’image en 3 dimensions.</span><span class="sxs-lookup"><span data-stu-id="510d2-174">Direct2D provides a 4x4 matrix class to provide helper functions for transforming the image in 3 dimensions.</span></span> <span data-ttu-id="510d2-175">Pour plus d’informations et pour obtenir une description de tous les membres de la classe, consultez la rubrique [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) .</span><span class="sxs-lookup"><span data-stu-id="510d2-175">See the [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) topic for more info and a description of all the class members.</span></span>



| <span data-ttu-id="510d2-176">Fonction</span><span class="sxs-lookup"><span data-stu-id="510d2-176">Function</span></span>                                | <span data-ttu-id="510d2-177">Description</span><span class="sxs-lookup"><span data-stu-id="510d2-177">Description</span></span>                                                                                    | <span data-ttu-id="510d2-178">Matrix</span><span class="sxs-lookup"><span data-stu-id="510d2-178">Matrix</span></span>                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="510d2-179">Matrix4x4F :: Scale (X, Y, Z)</span><span class="sxs-lookup"><span data-stu-id="510d2-179">Matrix4x4F::Scale(X, Y, Z)</span></span>              | <span data-ttu-id="510d2-180">Génère une matrice de transformation qui met à l’échelle le plan de projection dans la direction X, Y et/ou Z.</span><span class="sxs-lookup"><span data-stu-id="510d2-180">Generates a transform matrix that scales the projection plane in the X, Y, and/or Z direction.</span></span> | ![matrice scale3d](images/3d-transform-matrix2.png)     |
| <span data-ttu-id="510d2-182">SkewX (X)</span><span class="sxs-lookup"><span data-stu-id="510d2-182">SkewX(X)</span></span>                                | <span data-ttu-id="510d2-183">Génère une matrice de transformation qui incline le plan de projection dans l’axe X.</span><span class="sxs-lookup"><span data-stu-id="510d2-183">Generates a transform matrix that skews the projection plane in the X direction.</span></span>               | ![Affiche une matrice inclinée sur l’axe X.](images/matrix4x4-skewx.png)             |
| <span data-ttu-id="510d2-185">Skew (Y)</span><span class="sxs-lookup"><span data-stu-id="510d2-185">SkewY(Y)</span></span>                                | <span data-ttu-id="510d2-186">Génère une matrice de transformation qui incline le plan de projection sur l’axe Y.</span><span class="sxs-lookup"><span data-stu-id="510d2-186">Generates a transform matrix that skews the projection plane in the Y direction.</span></span>               | ![matrice d’inclinaison](images/matrix4x4-skewy.png)             |
| <span data-ttu-id="510d2-188">Translation (X, Y, Z)</span><span class="sxs-lookup"><span data-stu-id="510d2-188">Translation(X, Y, Z)</span></span>                    | <span data-ttu-id="510d2-189">Génère une matrice de transformation qui convertit le plan de projection dans la direction X, Y ou Z.</span><span class="sxs-lookup"><span data-stu-id="510d2-189">Generates a transform matrix that translates the projection plane in the X, Y, or Z direction.</span></span> | ![translater la matrice](images/3d-transform-matrix4.png)   |
| <span data-ttu-id="510d2-191">RotationX (X)</span><span class="sxs-lookup"><span data-stu-id="510d2-191">RotationX(X)</span></span>                            | <span data-ttu-id="510d2-192">Génère une matrice de transformation qui fait pivoter le plan de projection autour de l’axe X.</span><span class="sxs-lookup"><span data-stu-id="510d2-192">Generates a transform matrix that rotates the projection plane about the X axis.</span></span>               | ![faire pivoter la matrice x](images/3d-transform-matrix5.png)    |
| <span data-ttu-id="510d2-194">RotationY (Y)</span><span class="sxs-lookup"><span data-stu-id="510d2-194">RotationY(Y)</span></span>                            | <span data-ttu-id="510d2-195">Génère une matrice de transformation qui fait pivoter le plan de projection autour de l’axe Y.</span><span class="sxs-lookup"><span data-stu-id="510d2-195">Generates a transform matrix that rotates the projection plane about the Y axis.</span></span>               | ![faire pivoter la matrice y](images/3d-transform-matrix6.png)    |
| <span data-ttu-id="510d2-197">Rotationt (Z)</span><span class="sxs-lookup"><span data-stu-id="510d2-197">RotationZ(Z)</span></span>                            | <span data-ttu-id="510d2-198">Génère une matrice de transformation qui fait pivoter le plan de projection autour de l’axe Z.</span><span class="sxs-lookup"><span data-stu-id="510d2-198">Generates a transform matrix that rotates the projection plane about the Z axis.</span></span>               | ![pivoter la matrice z](images/3d-transform-matrix7.png)    |
| <span data-ttu-id="510d2-200">PerspectiveProjection (D)</span><span class="sxs-lookup"><span data-stu-id="510d2-200">PerspectiveProjection(D)</span></span>                | <span data-ttu-id="510d2-201">Transformation de perspective avec une valeur de profondeur D.</span><span class="sxs-lookup"><span data-stu-id="510d2-201">A perspective transformation with a depth value of D.</span></span>                                          | ![matrice de perspective](images/3d-transform-matrix8.png) |
| <span data-ttu-id="510d2-203">RotationArbitraryAxis (X, Y, Z, degrés)</span><span class="sxs-lookup"><span data-stu-id="510d2-203">RotationArbitraryAxis(X, Y, Z, degrees)</span></span> | <span data-ttu-id="510d2-204">Fait pivoter le plan de projection autour de l’axe que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="510d2-204">Rotates the projection plane about the axis you specify.</span></span>                                       |                                                        |



 

## <a name="requirements"></a><span data-ttu-id="510d2-205">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="510d2-205">Requirements</span></span>



| <span data-ttu-id="510d2-206">Condition requise</span><span class="sxs-lookup"><span data-stu-id="510d2-206">Requirement</span></span> | <span data-ttu-id="510d2-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="510d2-207">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="510d2-208">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="510d2-208">Minimum supported client</span></span> | <span data-ttu-id="510d2-209">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="510d2-209">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="510d2-210">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="510d2-210">Minimum supported server</span></span> | <span data-ttu-id="510d2-211">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="510d2-211">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="510d2-212">En-tête</span><span class="sxs-lookup"><span data-stu-id="510d2-212">Header</span></span>                   | <span data-ttu-id="510d2-213">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="510d2-213">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="510d2-214">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="510d2-214">Library</span></span>                  | <span data-ttu-id="510d2-215">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="510d2-215">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="510d2-216">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="510d2-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="510d2-217">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="510d2-217">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

