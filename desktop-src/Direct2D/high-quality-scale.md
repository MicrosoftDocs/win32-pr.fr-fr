---
title: Effet d’échelle
description: Utilisez cet effet pour mettre à l’échelle une image. L’effet a six modes de mise à l’échelle, linéaires, linéaires, cubiques, multi-échantillonnage linéaire, anisotrope et de haute qualité.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- effet de mise à l’échelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3af77bc24db387fff0854e0432c270fa2ce6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384495"
---
# <a name="scale-effect"></a><span data-ttu-id="2dc73-105">Effet d’échelle</span><span class="sxs-lookup"><span data-stu-id="2dc73-105">Scale effect</span></span>

<span data-ttu-id="2dc73-106">Utilisez cet effet pour mettre à l’échelle une image.</span><span class="sxs-lookup"><span data-stu-id="2dc73-106">Use this effect to scale an image up or down.</span></span> <span data-ttu-id="2dc73-107">L’effet a six modes de mise à l’échelle : le plus proche voisin, linéaire, cubique, multi-échantillon linéaire, anisotrope et de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="2dc73-107">The effect has six scaling modes: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

<span data-ttu-id="2dc73-108">Le CLSID de cet effet est CLSID \_ D2D1Scale.</span><span class="sxs-lookup"><span data-stu-id="2dc73-108">The CLSID for this effect is CLSID\_D2D1Scale.</span></span>

-   [<span data-ttu-id="2dc73-109">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="2dc73-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="2dc73-110">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="2dc73-110">Effect properties</span></span>](#effect-properties)
    -   [<span data-ttu-id="2dc73-111">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="2dc73-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="2dc73-112">Modes d’interpolation</span><span class="sxs-lookup"><span data-stu-id="2dc73-112">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="2dc73-113">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="2dc73-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="2dc73-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2dc73-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="2dc73-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2dc73-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="2dc73-116">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="2dc73-116">Example image</span></span>

<span data-ttu-id="2dc73-117">Cet exemple montre l’effet de mise à l’échelle dans 2 fois l’entrée et le rognage à la taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="2dc73-117">This example shows the scale effect zooming in 2 times the input and cropping to the original size.</span></span>



| <span data-ttu-id="2dc73-118">Avant</span><span class="sxs-lookup"><span data-stu-id="2dc73-118">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg) |
| <span data-ttu-id="2dc73-120">After</span><span class="sxs-lookup"><span data-stu-id="2dc73-120">After</span></span>                                                      |
| ![image après la transformation.](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="2dc73-122">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="2dc73-122">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2dc73-123">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="2dc73-123">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="2dc73-124">Description</span><span class="sxs-lookup"><span data-stu-id="2dc73-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2dc73-125">Scale</span><span class="sxs-lookup"><span data-stu-id="2dc73-125">Scale</span></span><br/> <span data-ttu-id="2dc73-126">D2D1_SCALE_PROP_SCALE</span><span class="sxs-lookup"><span data-stu-id="2dc73-126">D2D1_SCALE_PROP_SCALE</span></span><br/></td>
<td><span data-ttu-id="2dc73-127">Le montant de l’échelle de la direction X et Y en tant que rapport entre la taille de sortie et la taille d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2dc73-127">The scale amount in the X and Y direction as a ratio of the output size to the input size.</span></span> <span data-ttu-id="2dc73-128">Cette propriété a D2D1_VECTOR_2Fdefined en tant que : (X Scale, échelle Y).</span><span class="sxs-lookup"><span data-stu-id="2dc73-128">This property a D2D1_VECTOR_2Fdefined as: (X scale, Y scale).</span></span> <span data-ttu-id="2dc73-129">Les valeurs de mise à l’échelle sont FLOAT, sans unité, et doivent être positives ou égales à 0.</span><span class="sxs-lookup"><span data-stu-id="2dc73-129">The scale amounts are FLOAT, unitless, and must be positive or 0.</span></span><br/> <span data-ttu-id="2dc73-130">Le type est D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="2dc73-130">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="2dc73-131">La valeur par défaut est {1.0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="2dc73-131">The default value is {1.0f, 1.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2dc73-132">CenterPoint</span><span class="sxs-lookup"><span data-stu-id="2dc73-132">CenterPoint</span></span><br/> <span data-ttu-id="2dc73-133">D2D1_SCALE_PROP_CENTER_POINT</span><span class="sxs-lookup"><span data-stu-id="2dc73-133">D2D1_SCALE_PROP_CENTER_POINT</span></span><br/></td>
<td><span data-ttu-id="2dc73-134">Point central de mise à l’échelle de l’image.</span><span class="sxs-lookup"><span data-stu-id="2dc73-134">The image scaling center point.</span></span> <span data-ttu-id="2dc73-135">Cette propriété est une D2D1_VECTOR_2F définie comme suit : (point X, point Y).</span><span class="sxs-lookup"><span data-stu-id="2dc73-135">This property is a D2D1_VECTOR_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="2dc73-136">Les unités sont en DIP.</span><span class="sxs-lookup"><span data-stu-id="2dc73-136">The units are in DIPs.</span></span><br/> <span data-ttu-id="2dc73-137">Utilisez la propriété point central pour mettre à l’échelle un point autre que l’angle supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="2dc73-137">Use the center point property to scale around a point other than the upper-left corner.</span></span><br/> <span data-ttu-id="2dc73-138">Le type est D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="2dc73-138">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="2dc73-139">La valeur par défaut est {0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="2dc73-139">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2dc73-140">BorderMode</span><span class="sxs-lookup"><span data-stu-id="2dc73-140">BorderMode</span></span><br/> <span data-ttu-id="2dc73-141">D2D1_SCALE_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="2dc73-141">D2D1_SCALE_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="2dc73-142">Le mode utilisé pour calculer la bordure de l’image, soft ou Hard.</span><span class="sxs-lookup"><span data-stu-id="2dc73-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="2dc73-143">Pour plus d’informations, consultez <a href="#border-modes">modes de bordure</a> .</span><span class="sxs-lookup"><span data-stu-id="2dc73-143">See <a href="#border-modes">Border modes</a> for more info.</span></span> <br/> <span data-ttu-id="2dc73-144">Le type est D2D1_BORDER_MODE.</span><span class="sxs-lookup"><span data-stu-id="2dc73-144">The type is D2D1_BORDER_MODE.</span></span><br/> <span data-ttu-id="2dc73-145">La valeur par défaut est D2D1_BORDER_MODE_SOFT.</span><span class="sxs-lookup"><span data-stu-id="2dc73-145">The default value is D2D1_BORDER_MODE_SOFT.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2dc73-146">Netteté</span><span class="sxs-lookup"><span data-stu-id="2dc73-146">Sharpness</span></span><br/> <span data-ttu-id="2dc73-147">D2D1_SCALE_PROP_SHARPNESS</span><span class="sxs-lookup"><span data-stu-id="2dc73-147">D2D1_SCALE_PROP_SHARPNESS</span></span><br/></td>
<td><span data-ttu-id="2dc73-148">Dans le mode d’interpolation cubique de haute qualité, le niveau de netteté du filtre de mise à l’échelle est une valeur float comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="2dc73-148">In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1.</span></span> <span data-ttu-id="2dc73-149">Les valeurs sont sans unité.</span><span class="sxs-lookup"><span data-stu-id="2dc73-149">The values are unitless.</span></span> <span data-ttu-id="2dc73-150">Vous pouvez utiliser la netteté pour ajuster la qualité d’une image lors de la mise à l’échelle de l’image.</span><span class="sxs-lookup"><span data-stu-id="2dc73-150">You can use sharpness to adjust the quality of an image when you scale the image down.</span></span><br/> <span data-ttu-id="2dc73-151">Le facteur de netteté affecte la forme du noyau.</span><span class="sxs-lookup"><span data-stu-id="2dc73-151">The sharpness factor affects the shape of the kernel.</span></span> <span data-ttu-id="2dc73-152">Plus le facteur de netteté est élevé, plus le noyau est petit.</span><span class="sxs-lookup"><span data-stu-id="2dc73-152">The higher the sharpness factor, the smaller the kernel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2dc73-153">Cette propriété affecte uniquement le mode d’interpolation cubique de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="2dc73-153">This property affects only the high quality cubic interpolation mode.</span></span>
</blockquote>
<br/> <span data-ttu-id="2dc73-154">Le type est FLOAT.</span><span class="sxs-lookup"><span data-stu-id="2dc73-154">The type is FLOAT.</span></span><br/> <span data-ttu-id="2dc73-155">La valeur par défaut est 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="2dc73-155">The default value is 0.0f.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2dc73-156">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="2dc73-156">InterpolationMode</span></span><br/> <span data-ttu-id="2dc73-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span><span class="sxs-lookup"><span data-stu-id="2dc73-157">D2D1_SCALE_PROP_INTERPOLATION_MODE</span></span><br/></td>
<td><span data-ttu-id="2dc73-158">Mode d’interpolation utilisé par l’effet pour mettre l’image à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="2dc73-158">The interpolation mode the effect uses to scale the image.</span></span> <span data-ttu-id="2dc73-159">Il existe 6 modes de mise à l’échelle qui vont de la qualité et de la vitesse.</span><span class="sxs-lookup"><span data-stu-id="2dc73-159">There are 6 scale modes that range in quality and speed.</span></span> <span data-ttu-id="2dc73-160">Pour plus d’informations, consultez <a href="#interpolation-modes">modes d’interpolation</a> .</span><span class="sxs-lookup"><span data-stu-id="2dc73-160">See <a href="#interpolation-modes">Interpolation modes</a> for more info.</span></span> <br/> <span data-ttu-id="2dc73-161">Le type est D2D1_SCALE_INTERPOLATION_MODE.</span><span class="sxs-lookup"><span data-stu-id="2dc73-161">The type is D2D1_SCALE_INTERPOLATION_MODE.</span></span><br/> <span data-ttu-id="2dc73-162">La valeur par défaut est D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span><span class="sxs-lookup"><span data-stu-id="2dc73-162">The default value is D2D1_SCALE_INTERPOLATION_MODE_LINEAR.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a><span data-ttu-id="2dc73-163">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="2dc73-163">Border modes</span></span>



| <span data-ttu-id="2dc73-164">Nom</span><span class="sxs-lookup"><span data-stu-id="2dc73-164">Name</span></span>                     | <span data-ttu-id="2dc73-165">Description</span><span class="sxs-lookup"><span data-stu-id="2dc73-165">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc73-166">\_Mode de bordure d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="2dc73-166">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="2dc73-167">L’effet remplit l’image d’entrée avec des pixels noirs transparents pour les échantillons en dehors des limites d’entrée lorsqu’elle applique le noyau de convolution.</span><span class="sxs-lookup"><span data-stu-id="2dc73-167">The effect pads the input image with transparent black pixels for samples outside of the input bounds when it applies the convolution kernel.</span></span> <span data-ttu-id="2dc73-168">Cela crée une bordure douce pour l’image et, dans le processus, développe la bitmap de sortie de la taille du noyau.</span><span class="sxs-lookup"><span data-stu-id="2dc73-168">This creates a soft edge for the image, and in the process expands the output bitmap by the size of the kernel.</span></span><br/> |
| <span data-ttu-id="2dc73-169">D2D1 \_ mode de bordure \_ \_ difficile</span><span class="sxs-lookup"><span data-stu-id="2dc73-169">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="2dc73-170">L’effet étend l’image d’entrée avec une transformation de bordure de type miroir pour les exemples en dehors des limites d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2dc73-170">The effect extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span> <span data-ttu-id="2dc73-171">La taille de l’image bitmap de sortie est égale à la taille de l’image bitmap d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2dc73-171">The size of the output bitmap is equal to the size of the input bitmap.</span></span><br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a><span data-ttu-id="2dc73-172">Modes d’interpolation</span><span class="sxs-lookup"><span data-stu-id="2dc73-172">Interpolation modes</span></span>



| <span data-ttu-id="2dc73-173">Énumération</span><span class="sxs-lookup"><span data-stu-id="2dc73-173">Enumeration</span></span>                                             | <span data-ttu-id="2dc73-174">Description</span><span class="sxs-lookup"><span data-stu-id="2dc73-174">Description</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc73-175">D2D1 \_ \_ mode d’interpolation \_ \_ le plus proche \_ voisin</span><span class="sxs-lookup"><span data-stu-id="2dc73-175">D2D1\_SCALE\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="2dc73-176">Échantillonne le point unique le plus proche et l’utilise.</span><span class="sxs-lookup"><span data-stu-id="2dc73-176">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="2dc73-177">Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.</span><span class="sxs-lookup"><span data-stu-id="2dc73-177">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="2dc73-178">D2D1 \_ \_ \_ mode interpolation \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="2dc73-178">D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="2dc73-179">Utilise un échantillon à quatre points et une interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="2dc73-179">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="2dc73-180">Ce mode utilise plus de temps de traitement que le mode voisin le plus proche, mais génère une image de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="2dc73-180">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="2dc73-181">D2D1 \_ \_ \_ mode interpolation \_ cubique</span><span class="sxs-lookup"><span data-stu-id="2dc73-181">D2D1\_SCALE\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="2dc73-182">Utilise un exemple de noyau cubique 16 pour l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="2dc73-182">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="2dc73-183">Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="2dc73-183">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="2dc73-184">\_Mode interpolation à l’échelle d2d1 multi- \_ \_ \_ \_ exemple \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="2dc73-184">D2D1\_SCALE\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="2dc73-185">Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="2dc73-185">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="2dc73-186">Ce mode est adapté à la réduction de la taille des images avec quelques pixels.</span><span class="sxs-lookup"><span data-stu-id="2dc73-186">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="2dc73-187">D2D1 \_ \_ mode d’interpolation \_ \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="2dc73-187">D2D1\_SCALE\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="2dc73-188">Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="2dc73-188">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="2dc73-189">D2D1 mise à l' \_ échelle \_ \_ en mode interpolation de \_ haute \_ qualité \_ cubique</span><span class="sxs-lookup"><span data-stu-id="2dc73-189">D2D1\_SCALE\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="2dc73-190">Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation.</span><span class="sxs-lookup"><span data-stu-id="2dc73-190">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="2dc73-191">Utilise ensuite le mode d’interpolation cubique pour la sortie finale.</span><span class="sxs-lookup"><span data-stu-id="2dc73-191">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="2dc73-192">Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 mettre à l' \_ échelle le \_ \_ mode interpolation \_ linéaire.</span><span class="sxs-lookup"><span data-stu-id="2dc73-192">If you don't select a mode, the effect defaults to D2D1\_SCALE\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="2dc73-193">Le mode anisotrope génère des mipmaps lors de la mise à l’échelle. Toutefois, si vous affectez à la propriété **Cached** la valeur true sur les effets entrés dans cet effet, le des mipmaps ne sera pas généré à chaque fois pour des images suffisamment petites.</span><span class="sxs-lookup"><span data-stu-id="2dc73-193">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="2dc73-194">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="2dc73-194">Output bitmap</span></span>

<span data-ttu-id="2dc73-195">L’emplacement et la taille de l’image bitmap de sortie dépendent du facteur d’échelle et du point central spécifiés.</span><span class="sxs-lookup"><span data-stu-id="2dc73-195">The location and size of the output bitmap depends on the specified scale factor and the center point.</span></span>

<span data-ttu-id="2dc73-196">Vous pouvez calculer la taille de l’image bitmap de sortie à l’aide de cette équation :</span><span class="sxs-lookup"><span data-stu-id="2dc73-196">You can calculate the size of the output bitmap using this equation:</span></span><dl> <span data-ttu-id="2dc73-197">BitmapSize? (Pixels) = mettre à l’échelle ? \* Taille de la bitmap d’origine ?</span><span class="sxs-lookup"><span data-stu-id="2dc73-197">BitmapSize?(Pixels)=Scale?\*Original Bitmap Size?</span></span> <span data-ttu-id="2dc73-198">(DIP) \* (UserDPI/96)</span><span class="sxs-lookup"><span data-stu-id="2dc73-198">(DIPs)\*(UserDPI/96)</span></span>  
<span data-ttu-id="2dc73-199">BitmapSize<sub>y</sub>(pixels) = mettre à l’échelle<sub>y</sub> \* taille de bitmap d’origine<sub>y</sub> (DIP) \* (UserDPI/96)</span><span class="sxs-lookup"><span data-stu-id="2dc73-199">BitmapSize<sub>y</sub>(Pixels)=Scale<sub>y</sub>\*Original Bitmap Size<sub>y</sub> (DIPs)\*(UserDPI/96)</span></span>  
</dl>

<span data-ttu-id="2dc73-200">L’effet arrondit les fractions de pixels au pixel entier le plus proche.</span><span class="sxs-lookup"><span data-stu-id="2dc73-200">The effect rounds fractions of pixels up to the nearest whole pixel.</span></span>

<span data-ttu-id="2dc73-201">L’emplacement de la bitmap est (0,0) ou la valeur de la propriété du point central.</span><span class="sxs-lookup"><span data-stu-id="2dc73-201">The location of the bitmap is (0, 0) or the value of the center point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc73-202">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2dc73-202">Requirements</span></span>



| <span data-ttu-id="2dc73-203">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2dc73-203">Requirement</span></span> | <span data-ttu-id="2dc73-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="2dc73-204">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc73-205">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2dc73-205">Minimum supported client</span></span> | <span data-ttu-id="2dc73-206">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="2dc73-206">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2dc73-207">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2dc73-207">Minimum supported server</span></span> | <span data-ttu-id="2dc73-208">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="2dc73-208">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2dc73-209">En-tête</span><span class="sxs-lookup"><span data-stu-id="2dc73-209">Header</span></span>                   | <span data-ttu-id="2dc73-210">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="2dc73-210">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="2dc73-211">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2dc73-211">Library</span></span>                  | <span data-ttu-id="2dc73-212">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="2dc73-212">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="2dc73-213">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2dc73-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dc73-214">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="2dc73-214">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

