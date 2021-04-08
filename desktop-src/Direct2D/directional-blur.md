---
title: Effet flou directionnel
description: L’effet de flou directionnel est semblable au flou gaussien, sauf que vous pouvez incliner le flou dans une direction particulière.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- flou directionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739853"
---
# <a name="directional-blur-effect"></a><span data-ttu-id="9fab7-104">Effet flou directionnel</span><span class="sxs-lookup"><span data-stu-id="9fab7-104">Directional blur effect</span></span>

<span data-ttu-id="9fab7-105">L’effet de flou directionnel est semblable au [flou gaussien](gaussian-blur.md), sauf que vous pouvez incliner le flou dans une direction particulière.</span><span class="sxs-lookup"><span data-stu-id="9fab7-105">The directional blur effect is similar to [Gaussian blur](gaussian-blur.md), except you can skew the blur in a particular direction.</span></span> <span data-ttu-id="9fab7-106">Vous pouvez utiliser cet effet pour donner à une image l’apparence si elle est en mouvement ou pour mettre en évidence une image animée.</span><span class="sxs-lookup"><span data-stu-id="9fab7-106">You can use this effect to make an image look as if it is in motion or to emphasize an animated image.</span></span>

<span data-ttu-id="9fab7-107">Le CLSID de cet effet est CLSID \_ D2D1DirectionalBlur.</span><span class="sxs-lookup"><span data-stu-id="9fab7-107">The CLSID for this effect is CLSID\_D2D1DirectionalBlur.</span></span>

-   [<span data-ttu-id="9fab7-108">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="9fab7-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="9fab7-109">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="9fab7-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="9fab7-110">Modes d’optimisation</span><span class="sxs-lookup"><span data-stu-id="9fab7-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="9fab7-111">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="9fab7-111">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="9fab7-112">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="9fab7-112">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="9fab7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fab7-113">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9fab7-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9fab7-114">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="9fab7-115">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="9fab7-115">Example image</span></span>



| <span data-ttu-id="9fab7-116">Avant</span><span class="sxs-lookup"><span data-stu-id="9fab7-116">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)      |
| <span data-ttu-id="9fab7-118">After</span><span class="sxs-lookup"><span data-stu-id="9fab7-118">After</span></span>                                                           |
| ![image après la transformation.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="9fab7-120">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="9fab7-120">Effect properties</span></span>



| <span data-ttu-id="9fab7-121">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="9fab7-121">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="9fab7-122">Description</span><span class="sxs-lookup"><span data-stu-id="9fab7-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fab7-123">StandardDeviation</span><span class="sxs-lookup"><span data-stu-id="9fab7-123">StandardDeviation</span></span><br/> <span data-ttu-id="9fab7-124">ÉCART type de D2D1 \_ DIRECTIONALBLUR \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="9fab7-124">D2D1\_DIRECTIONALBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="9fab7-125">Quantité de flou à appliquer à l’image.</span><span class="sxs-lookup"><span data-stu-id="9fab7-125">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="9fab7-126">Vous pouvez calculer le rayon de flou du noyau en multipliant l’écart type par 3.</span><span class="sxs-lookup"><span data-stu-id="9fab7-126">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="9fab7-127">Les unités de l’écart type et du rayon de flou sont des DIP.</span><span class="sxs-lookup"><span data-stu-id="9fab7-127">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="9fab7-128">La valeur 0 DIP désactive cet effet.</span><span class="sxs-lookup"><span data-stu-id="9fab7-128">A value of 0 DIPs disables this effect.</span></span> <span data-ttu-id="9fab7-129">Le type est FLOAT.</span><span class="sxs-lookup"><span data-stu-id="9fab7-129">The type is FLOAT.</span></span><br/> <span data-ttu-id="9fab7-130">La valeur par défaut est 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="9fab7-130">The default value is 3.0f.</span></span><br/>                                                                            |
| <span data-ttu-id="9fab7-131">Angle</span><span class="sxs-lookup"><span data-stu-id="9fab7-131">Angle</span></span><br/> <span data-ttu-id="9fab7-132">\_Angle d2d1 DIRECTIONALBLUR \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="9fab7-132">D2D1\_DIRECTIONALBLUR\_PROP\_ANGLE</span></span><br/>                           | <span data-ttu-id="9fab7-133">Angle du flou par rapport à l’axe x, dans le sens inverse des aiguilles d’une passe.</span><span class="sxs-lookup"><span data-stu-id="9fab7-133">The angle of the blur relative to the x-axis, in the counterclockwise direction.</span></span> <span data-ttu-id="9fab7-134">Les unités sont spécifiées en degrés.</span><span class="sxs-lookup"><span data-stu-id="9fab7-134">The units are specified in degrees.</span></span><br/> <span data-ttu-id="9fab7-135">Le noyau de flou est d’abord généré à l’aide du même processus que pour l’effet [flou gaussien](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="9fab7-135">The blur kernel is first generated using the same process as for the [Gaussian blur](gaussian-blur.md) effect.</span></span> <span data-ttu-id="9fab7-136">Les valeurs de noyau sont ensuite transformées en fonction de l’angle de flou.</span><span class="sxs-lookup"><span data-stu-id="9fab7-136">The kernel values are then transformed according to the blur angle.</span></span><br/> <span data-ttu-id="9fab7-137">Le type est FLOAT.</span><span class="sxs-lookup"><span data-stu-id="9fab7-137">The type is FLOAT.</span></span><br/> <span data-ttu-id="9fab7-138">La valeur par défaut est 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="9fab7-138">The default value is 0.0f.</span></span><br/> |
| <span data-ttu-id="9fab7-139">Optimization</span><span class="sxs-lookup"><span data-stu-id="9fab7-139">Optimization</span></span><br/> <span data-ttu-id="9fab7-140">Optimisation de D2D1 \_ DIRECTIONALBLUR \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="9fab7-140">D2D1\_DIRECTIONALBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="9fab7-141">Mode d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="9fab7-141">The optimization mode.</span></span> <span data-ttu-id="9fab7-142">Pour plus d’informations, consultez [modes d’optimisation](#optimization-modes) .</span><span class="sxs-lookup"><span data-stu-id="9fab7-142">See [Optimization modes](#optimization-modes) for more info.</span></span><br/> <span data-ttu-id="9fab7-143">Le type est D2D1 \_ DIRECTIONALBLUR \_ Optimization.</span><span class="sxs-lookup"><span data-stu-id="9fab7-143">The type is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="9fab7-144">La valeur par défaut est D2D1 \_ DIRECTIONALBLUR \_ Optimization \_ Balanced.</span><span class="sxs-lookup"><span data-stu-id="9fab7-144">The default value is D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED.</span></span> <br/>                                                                                                                                                         |
| <span data-ttu-id="9fab7-145">BorderMode</span><span class="sxs-lookup"><span data-stu-id="9fab7-145">BorderMode</span></span><br/> <span data-ttu-id="9fab7-146">\_Mode de bordure d2d1 DIRECTIONALBLUR \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="9fab7-146">D2D1\_DIRECTIONALBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="9fab7-147">Le mode utilisé pour calculer la bordure de l’image, soft ou Hard.</span><span class="sxs-lookup"><span data-stu-id="9fab7-147">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="9fab7-148">Pour plus d’informations, consultez [modes de bordure](#border-modes) .</span><span class="sxs-lookup"><span data-stu-id="9fab7-148">See [Border modes](#border-modes) for more info.</span></span><br/> <span data-ttu-id="9fab7-149">Le type est D2D1 \_ Border \_ mode.</span><span class="sxs-lookup"><span data-stu-id="9fab7-149">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="9fab7-150">La valeur par défaut est \_ d2d1 \_ en mode bordure \_ souple.</span><span class="sxs-lookup"><span data-stu-id="9fab7-150">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a><span data-ttu-id="9fab7-151">Modes d’optimisation</span><span class="sxs-lookup"><span data-stu-id="9fab7-151">Optimization modes</span></span>



| <span data-ttu-id="9fab7-152">Nom</span><span class="sxs-lookup"><span data-stu-id="9fab7-152">Name</span></span>                                          | <span data-ttu-id="9fab7-153">Description</span><span class="sxs-lookup"><span data-stu-id="9fab7-153">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fab7-154">Vitesse d’optimisation de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="9fab7-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="9fab7-155">Applique des optimisations internes telles que la pré-mise à l’échelle à des rayons relativement petits.</span><span class="sxs-lookup"><span data-stu-id="9fab7-155">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="9fab7-156">Utilise le filtrage linéaire.</span><span class="sxs-lookup"><span data-stu-id="9fab7-156">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="9fab7-157">D2D1 \_ DIRECTIONALBLUR \_ Optimization \_ Balanced</span><span class="sxs-lookup"><span data-stu-id="9fab7-157">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="9fab7-158">Utilise les mêmes seuils d’optimisation que le mode vitesse, mais utilise le filtrage trilinéaire.</span><span class="sxs-lookup"><span data-stu-id="9fab7-158">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="9fab7-159">Qualité de l’optimisation de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="9fab7-159">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="9fab7-160">Utilise uniquement des optimisations internes avec de grands rayons de flou, où les approximations sont moins susceptibles d’être visibles.</span><span class="sxs-lookup"><span data-stu-id="9fab7-160">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="9fab7-161">Utilise le filtrage trilinéaire.</span><span class="sxs-lookup"><span data-stu-id="9fab7-161">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="9fab7-162">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="9fab7-162">Border modes</span></span>



| <span data-ttu-id="9fab7-163">Nom</span><span class="sxs-lookup"><span data-stu-id="9fab7-163">Name</span></span>                     | <span data-ttu-id="9fab7-164">Description</span><span class="sxs-lookup"><span data-stu-id="9fab7-164">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fab7-165">\_Mode de bordure d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="9fab7-165">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="9fab7-166">L’effet remplit l’image avec des pixels noirs transparents au fur et à mesure qu’elle applique le noyau de flou, entraînant ainsi un contour adouci.</span><span class="sxs-lookup"><span data-stu-id="9fab7-166">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="9fab7-167">D2D1 \_ mode de bordure \_ \_ difficile</span><span class="sxs-lookup"><span data-stu-id="9fab7-167">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="9fab7-168">L’effet attache la sortie à la taille de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9fab7-168">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="9fab7-169">Lorsque l’effet applique le noyau de flou, il étend l’image d’entrée avec une transformation de bordure de type miroir pour les exemples en dehors des limites d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9fab7-169">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="9fab7-170">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="9fab7-170">Output bitmap</span></span>

<span data-ttu-id="9fab7-171">La taille de la bitmap de sortie augmente en fonction de l’écart type, de l’angle de l’effet et du mode de bordure.</span><span class="sxs-lookup"><span data-stu-id="9fab7-171">The size of the output bitmap increases based on the standard deviation, the angle of the effect, and the border mode.</span></span> <span data-ttu-id="9fab7-172">Si le mode de bordure est défini sur le \_ mode de bordure d2d1 \_ \_ , la taille de la bitmap de sortie augmente de la taille du noyau de flou, représentée en pixels.</span><span class="sxs-lookup"><span data-stu-id="9fab7-172">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the size of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="9fab7-173">Ces équations peuvent être utilisées pour calculer la taille de l’image bitmap de sortie.</span><span class="sxs-lookup"><span data-stu-id="9fab7-173">These equations can be used to calculate the size of the output bitmap.</span></span>



| <span data-ttu-id="9fab7-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fab7-174">Requirement</span></span> | <span data-ttu-id="9fab7-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fab7-175">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9fab7-176">Croissance bitmap en sortie X</span><span class="sxs-lookup"><span data-stu-id="9fab7-176">Output Bitmap Growth X</span></span> | <span data-ttu-id="9fab7-177">StandardDeviation (DIP) \* 6 \* ((PPP utilisateur)/96) \* cos (angle))</span><span class="sxs-lookup"><span data-stu-id="9fab7-177">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* cos(Angle))</span></span> |
| <span data-ttu-id="9fab7-178">Croissance des bitmaps en sortie Y</span><span class="sxs-lookup"><span data-stu-id="9fab7-178">Output Bitmap Growth Y</span></span> | <span data-ttu-id="9fab7-179">StandardDeviation (DIP) \* 6 \* ((PPP utilisateur)/96) \* Sin (angle))</span><span class="sxs-lookup"><span data-stu-id="9fab7-179">StandardDeviation (DIPs) \* 6 \* ((User DPI) / 96) \* sin(Angle))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9fab7-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fab7-180">Requirements</span></span>



| <span data-ttu-id="9fab7-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fab7-181">Requirement</span></span> | <span data-ttu-id="9fab7-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fab7-182">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9fab7-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fab7-183">Minimum supported client</span></span> | <span data-ttu-id="9fab7-184">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="9fab7-184">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9fab7-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fab7-185">Minimum supported server</span></span> | <span data-ttu-id="9fab7-186">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="9fab7-186">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9fab7-187">En-tête</span><span class="sxs-lookup"><span data-stu-id="9fab7-187">Header</span></span>                   | <span data-ttu-id="9fab7-188">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="9fab7-188">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="9fab7-189">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9fab7-189">Library</span></span>                  | <span data-ttu-id="9fab7-190">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="9fab7-190">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="9fab7-191">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9fab7-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fab7-192">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="9fab7-192">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

