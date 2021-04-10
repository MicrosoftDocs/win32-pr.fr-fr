---
title: Effet de transformation affine 2D
description: L’effet de transformation affine 2D applique une transformation spatiale à une image basée sur une matrice matrice à l’aide de la transformation de matrice Direct2D et de l’un des six modes d’interpolation.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- Effet de transformation affine 2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3017992d34cd98095f01192ea948684a6b52e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106564"
---
# <a name="2d-affine-transform-effect"></a><span data-ttu-id="31855-104">Effet de transformation affine 2D</span><span class="sxs-lookup"><span data-stu-id="31855-104">2D affine transform effect</span></span>

<span data-ttu-id="31855-105">L’effet de transformation affine 2D applique une transformation spatiale à une image basée sur une matrice matrice à l’aide de la [transformation](direct2d-transforms-overview.md) de matrice Direct2D et de l’un des six modes d’interpolation.</span><span class="sxs-lookup"><span data-stu-id="31855-105">The 2D affine transform effect applies a spatial transform to a image based on a 3X2 matrix using the Direct2D matrix [transform](direct2d-transforms-overview.md) and any of six interpolation modes.</span></span> <span data-ttu-id="31855-106">Vous pouvez utiliser cet effet pour faire pivoter, mettre à l’échelle, incliner ou traduire une image.</span><span class="sxs-lookup"><span data-stu-id="31855-106">You can use this effect to rotate, scale, skew, or translate an image.</span></span> <span data-ttu-id="31855-107">Vous pouvez combiner ces opérations.</span><span class="sxs-lookup"><span data-stu-id="31855-107">Or, you can combine these operations.</span></span> <span data-ttu-id="31855-108">Les transferts affin préservent les lignes parallèles et le ratio des distances entre les trois points d’une image.</span><span class="sxs-lookup"><span data-stu-id="31855-108">Affine transfers preserve parallel lines and the ratio of distances between any three points in an image.</span></span>

<span data-ttu-id="31855-109">Le CLSID de cet effet est CLSID \_ D2D12DAffineTransform.</span><span class="sxs-lookup"><span data-stu-id="31855-109">The CLSID for this effect is CLSID\_D2D12DAffineTransform.</span></span>

-   [<span data-ttu-id="31855-110">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="31855-110">Example image</span></span>](#example-image)
-   [<span data-ttu-id="31855-111">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="31855-111">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="31855-112">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="31855-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="31855-113">Modes d’interpolation</span><span class="sxs-lookup"><span data-stu-id="31855-113">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="31855-114">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="31855-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="31855-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31855-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="31855-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31855-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="31855-117">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="31855-117">Example image</span></span>



| <span data-ttu-id="31855-118">Avant</span><span class="sxs-lookup"><span data-stu-id="31855-118">Before</span></span>                                                             |
|--------------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)         |
| <span data-ttu-id="31855-120">After</span><span class="sxs-lookup"><span data-stu-id="31855-120">After</span></span>                                                              |
| ![image après la transformation.](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="31855-122">Cet effet effectue cette opération de matrice :</span><span class="sxs-lookup"><span data-stu-id="31855-122">This effect performs this matrix operation:</span></span>

![opération de matrice affine](images/affine-matrix-calculation.png)

<span data-ttu-id="31855-124">Bien que la matrice d’entrée soit définie en tant que matrice matrice, la dernière colonne est remplie avec 0, 0 et 1 pour produire une matrice carrée.</span><span class="sxs-lookup"><span data-stu-id="31855-124">Although the input matrix is defined as a 3x2 matrix, the last column is padded with 0, 0 and 1 to produce a square matrix.</span></span> <span data-ttu-id="31855-125">Cela permet la multiplication de matrice, afin que les transformations puissent être concaténées en une seule matrice.</span><span class="sxs-lookup"><span data-stu-id="31855-125">This allows for matrix multiplication, so that transforms can be concatenated into a single matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="31855-126">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="31855-126">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="31855-127">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="31855-127">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="31855-128">Description</span><span class="sxs-lookup"><span data-stu-id="31855-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31855-129">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="31855-129">InterpolationMode</span></span><br/> <span data-ttu-id="31855-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="31855-130">D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="31855-131">Mode d’interpolation utilisé pour mettre à l’échelle l’image.</span><span class="sxs-lookup"><span data-stu-id="31855-131">The interpolation mode used to scale the image.</span></span> <span data-ttu-id="31855-132">Il existe 6 modes de mise à l’échelle qui vont de la qualité et de la vitesse.</span><span class="sxs-lookup"><span data-stu-id="31855-132">There are 6 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="31855-133">Le type est D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="31855-133">Type is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="31855-134">La valeur par défaut est D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="31855-134">Default value is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31855-135">BorderMode</span><span class="sxs-lookup"><span data-stu-id="31855-135">BorderMode</span></span><br/> <span data-ttu-id="31855-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="31855-136">D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="31855-137">Le mode utilisé pour calculer la bordure de l’image, soft ou Hard.</span><span class="sxs-lookup"><span data-stu-id="31855-137">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="31855-138">Pour plus d’informations, consultez <a href="https://www.bing.com/search?q=Border+modes">modes de bordure</a> .</span><span class="sxs-lookup"><span data-stu-id="31855-138">See <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="31855-139">Le type est D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="31855-139">Type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="31855-140">La valeur par défaut est D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="31855-140">Default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31855-141">TransformMatrix</span><span class="sxs-lookup"><span data-stu-id="31855-141">TransformMatrix</span></span><br/> <span data-ttu-id="31855-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span><span class="sxs-lookup"><span data-stu-id="31855-142">D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX</span></span><br/></td>
<td><span data-ttu-id="31855-143">Matrice matrice pour transformer l’image à l’aide de la <a href="direct2d-transforms-overview.md">transformation</a>de matrice Direct2D.</span><span class="sxs-lookup"><span data-stu-id="31855-143">The 3x2 matrix to transform the image using the Direct2D matrix <a href="direct2d-transforms-overview.md">transform</a>.</span></span> <br/> <span data-ttu-id="31855-144">Le type est D2D1_MATRIX_3X2_F.</span><span class="sxs-lookup"><span data-stu-id="31855-144">Type is D2D1_MATRIX_3X2_F.</span></span><br/> <span data-ttu-id="31855-145">La valeur par défaut est Matrix3x2F :: Identity ().</span><span class="sxs-lookup"><span data-stu-id="31855-145">Default value is Matrix3x2F::Identity().</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31855-146">Netteté</span><span class="sxs-lookup"><span data-stu-id="31855-146">Sharpness</span></span><br/> <span data-ttu-id="31855-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="31855-147">D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="31855-148">Dans le mode d’interpolation cubique de haute qualité, le niveau de netteté du filtre de mise à l’échelle est une valeur float comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="31855-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="31855-149">Les valeurs sont sans unité.</span><span class="sxs-lookup"><span data-stu-id="31855-149">The values are unitless.</span></span> <span data-ttu-id="31855-150">Vous pouvez utiliser la netteté pour ajuster la qualité d’une image lors de la mise à l’échelle de l’image.</span><span class="sxs-lookup"><span data-stu-id="31855-150">You can use sharpness to adjust the quality of an image when you scale the image.</span></span><br/> <span data-ttu-id="31855-151">Le facteur de netteté affecte la forme du noyau.</span><span class="sxs-lookup"><span data-stu-id="31855-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="31855-152">Plus le facteur de netteté est élevé, plus le noyau est petit.</span><span class="sxs-lookup"><span data-stu-id="31855-152">The higher the sharpness factor, the smaller the kernel.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="31855-153">Cette propriété affecte uniquement le mode d’interpolation cubique de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="31855-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="31855-154">Le type est FLOAT.</span><span class="sxs-lookup"><span data-stu-id="31855-154">Type is FLOAT.</span></span><br/> <span data-ttu-id="31855-155">La valeur par défaut est 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="31855-155">Default value is 1.0f.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="border-modes"></a><span data-ttu-id="31855-156">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="31855-156">Border modes</span></span>



| <span data-ttu-id="31855-157">Nom</span><span class="sxs-lookup"><span data-stu-id="31855-157">Name</span></span>                     | <span data-ttu-id="31855-158">Description</span><span class="sxs-lookup"><span data-stu-id="31855-158">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31855-159">\_Mode de bordure d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="31855-159">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="31855-160">L’effet remplit l’image avec des pixels noirs transparents au fur et à mesure de l’interpolation, ce qui génère une bordure douce.</span><span class="sxs-lookup"><span data-stu-id="31855-160">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="31855-161">D2D1 \_ mode de bordure \_ \_ difficile</span><span class="sxs-lookup"><span data-stu-id="31855-161">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="31855-162">L’effet attache la sortie à la taille de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="31855-162">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="31855-163">Modes d’interpolation</span><span class="sxs-lookup"><span data-stu-id="31855-163">Interpolation modes</span></span>



| <span data-ttu-id="31855-164">Énumération</span><span class="sxs-lookup"><span data-stu-id="31855-164">Enumeration</span></span>                                                         | <span data-ttu-id="31855-165">Description</span><span class="sxs-lookup"><span data-stu-id="31855-165">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31855-166">\_Mode d’interpolation d2d1 2DAFFINETRANSFORM \_ \_ \_ le plus proche \_ voisin</span><span class="sxs-lookup"><span data-stu-id="31855-166">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="31855-167">Échantillonne le point unique le plus proche et l’utilise.</span><span class="sxs-lookup"><span data-stu-id="31855-167">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="31855-168">Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.</span><span class="sxs-lookup"><span data-stu-id="31855-168">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="31855-169">D2D1 \_ \_ mode d’interpolation \_ 2DAFFINETRANSFORM \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="31855-169">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="31855-170">Utilise un échantillon à quatre points et une interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="31855-170">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="31855-171">Ce mode utilise plus de temps de traitement que le mode voisin le plus proche, mais génère une image de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="31855-171">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="31855-172">D2D1 \_ 2DAFFINETRANSFORM \_ mode d' \_ interpolation \_ cubique</span><span class="sxs-lookup"><span data-stu-id="31855-172">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="31855-173">Utilise un exemple de noyau cubique 16 pour l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="31855-173">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="31855-174">Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="31855-174">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="31855-175">\_Mode d’interpolation d2d1 2DAFFINETRANSFORM multi- \_ \_ \_ \_ exemple \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="31855-175">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="31855-176">Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="31855-176">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="31855-177">Ce mode est adapté à la réduction de la taille des images avec quelques pixels.</span><span class="sxs-lookup"><span data-stu-id="31855-177">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="31855-178">D2D1 \_ \_ mode d’interpolation \_ 2DAFFINETRANSFORM \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="31855-178">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="31855-179">Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="31855-179">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="31855-180">D2D1 \_ 2DAFFINETRANSFORM \_ mode d’interpolation de \_ \_ haute \_ qualité \_ cubique</span><span class="sxs-lookup"><span data-stu-id="31855-180">D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="31855-181">Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="31855-181">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="31855-182">Utilise ensuite le mode d’interpolation cubique pour la sortie finale.</span><span class="sxs-lookup"><span data-stu-id="31855-182">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="31855-183">Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ 2DAFFINETRANSFORM \_ interpolation \_ mode \_ Linear.</span><span class="sxs-lookup"><span data-stu-id="31855-183">If you don't select a mode, the effect defaults to D2D1\_2DAFFINETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="31855-184">Le mode anisotrope génère des mipmaps lors de la mise à l’échelle. Toutefois, si vous affectez à la propriété **Cached** la valeur true sur les effets entrés dans cet effet, le des mipmaps ne sera pas généré à chaque fois pour des images suffisamment petites.</span><span class="sxs-lookup"><span data-stu-id="31855-184">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="31855-185">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="31855-185">Output bitmap</span></span>

<span data-ttu-id="31855-186">La taille de l’image bitmap de sortie dépend de la matrice de transformation appliquée à l’image.</span><span class="sxs-lookup"><span data-stu-id="31855-186">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="31855-187">L’effet exécute l’opération de transformation, puis applique un cadre englobant autour du résultat.</span><span class="sxs-lookup"><span data-stu-id="31855-187">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="31855-188">La bitmap de sortie correspond à la taille du cadre englobant.</span><span class="sxs-lookup"><span data-stu-id="31855-188">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="31855-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31855-189">Requirements</span></span>



| <span data-ttu-id="31855-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31855-190">Requirement</span></span> | <span data-ttu-id="31855-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="31855-191">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31855-192">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31855-192">Minimum supported client</span></span> | <span data-ttu-id="31855-193">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="31855-193">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="31855-194">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31855-194">Minimum supported server</span></span> | <span data-ttu-id="31855-195">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="31855-195">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="31855-196">En-tête</span><span class="sxs-lookup"><span data-stu-id="31855-196">Header</span></span>                   | <span data-ttu-id="31855-197">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="31855-197">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="31855-198">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="31855-198">Library</span></span>                  | <span data-ttu-id="31855-199">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="31855-199">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="31855-200">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31855-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31855-201">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="31855-201">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

