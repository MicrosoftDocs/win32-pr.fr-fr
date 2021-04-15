---
title: Effet Flou gaussien
description: Utilisez l’effet Flou gaussien pour créer un flou basé sur la fonction Gaussiente sur l’image d’entrée entière.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Flou gaussien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104554224"
---
# <a name="gaussian-blur-effect"></a><span data-ttu-id="65c9a-104">Effet Flou gaussien</span><span class="sxs-lookup"><span data-stu-id="65c9a-104">Gaussian blur effect</span></span>

<span data-ttu-id="65c9a-105">Utilisez l’effet Flou gaussien pour créer un flou basé sur la fonction Gaussiente sur l’image d’entrée entière.</span><span class="sxs-lookup"><span data-stu-id="65c9a-105">Use the Gaussian blur effect to create a blur based on the Gaussian function over the entire input image.</span></span>

<span data-ttu-id="65c9a-106">Vous pouvez utiliser cet effet pour créer des lueurs et des ombres portées et utiliser l’effet [composite](composite.md) pour appliquer le résultat à l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="65c9a-106">You can use this effect to create glows and drop shadows and use the [composite](composite.md) effect to apply the result to the original image.</span></span> <span data-ttu-id="65c9a-107">Il est utile dans le traitement des photos pour les filtres tels que les clairs et les ombres.</span><span class="sxs-lookup"><span data-stu-id="65c9a-107">It is useful in photo processing for filters like highlights and shadows.</span></span> <span data-ttu-id="65c9a-108">Vous pouvez utiliser la sortie de cet effet pour l’entrée dans les effets d’éclairage, comme les effets d’éclairage [spéculaire](specular-lighting.md) ou d' [éclairage diffus](diffuse-lighting.md) , car le canal alpha est flou, et les effets d’éclairage utilisent le canal alpha pour déterminer la géométrie de surface comme une carte de hauteur.</span><span class="sxs-lookup"><span data-stu-id="65c9a-108">You can use the output of this effect for input into lighting effects, like the [Specular Lighting](specular-lighting.md) or [Diffuse Lighting](diffuse-lighting.md) effects, because the alpha channel is blurred, too and lighting effects use the alpha channel to determine surface geometry as a height map.</span></span>

<span data-ttu-id="65c9a-109">Cet effet est utilisé par l’effet d' [ombre](drop-shadow.md) intégré.</span><span class="sxs-lookup"><span data-stu-id="65c9a-109">This effect is used by the built-in [Shadow](drop-shadow.md) effect.</span></span>

<span data-ttu-id="65c9a-110">Le CLSID de cet effet est CLSID \_ D2D1GaussianBlur.</span><span class="sxs-lookup"><span data-stu-id="65c9a-110">The CLSID for this effect is CLSID\_D2D1GaussianBlur.</span></span>

-   [<span data-ttu-id="65c9a-111">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="65c9a-111">Example image</span></span>](#example-image)
-   [<span data-ttu-id="65c9a-112">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="65c9a-112">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="65c9a-113">Modes d’optimisation</span><span class="sxs-lookup"><span data-stu-id="65c9a-113">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="65c9a-114">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="65c9a-114">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="65c9a-115">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="65c9a-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="65c9a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65c9a-116">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="65c9a-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65c9a-117">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="65c9a-118">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="65c9a-118">Example image</span></span>



| <span data-ttu-id="65c9a-119">Avant</span><span class="sxs-lookup"><span data-stu-id="65c9a-119">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)   |
| <span data-ttu-id="65c9a-121">After</span><span class="sxs-lookup"><span data-stu-id="65c9a-121">After</span></span>                                                        |
| ![image après la transformation.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="65c9a-123">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="65c9a-123">Effect properties</span></span>



| <span data-ttu-id="65c9a-124">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="65c9a-124">Display name and index enumeration</span></span>                                                    | <span data-ttu-id="65c9a-125">Description</span><span class="sxs-lookup"><span data-stu-id="65c9a-125">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65c9a-126">StandardDeviation</span><span class="sxs-lookup"><span data-stu-id="65c9a-126">StandardDeviation</span></span><br/> <span data-ttu-id="65c9a-127">ÉCART type de D2D1 \_ GAUSSIANBLUR \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="65c9a-127">D2D1\_GAUSSIANBLUR\_PROP\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="65c9a-128">Quantité de flou à appliquer à l’image.</span><span class="sxs-lookup"><span data-stu-id="65c9a-128">The amount of blur to be applied to the image.</span></span> <span data-ttu-id="65c9a-129">Vous pouvez calculer le rayon de flou du noyau en multipliant l’écart type par 3.</span><span class="sxs-lookup"><span data-stu-id="65c9a-129">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="65c9a-130">Les unités de l’écart type et du rayon de flou sont des DIP.</span><span class="sxs-lookup"><span data-stu-id="65c9a-130">The units of both the standard deviation and blur radius are DIPs.</span></span> <span data-ttu-id="65c9a-131">Une valeur de zéro DIP désactive entièrement cet effet.</span><span class="sxs-lookup"><span data-stu-id="65c9a-131">A value of zero DIPs disables this effect entirely.</span></span> <span data-ttu-id="65c9a-132">Le type est FLOAT.</span><span class="sxs-lookup"><span data-stu-id="65c9a-132">The type is FLOAT.</span></span><br/> <span data-ttu-id="65c9a-133">La valeur par défaut est 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="65c9a-133">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="65c9a-134">Optimization</span><span class="sxs-lookup"><span data-stu-id="65c9a-134">Optimization</span></span><br/> <span data-ttu-id="65c9a-135">Optimisation de D2D1 \_ GAUSSIANBLUR \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="65c9a-135">D2D1\_GAUSSIANBLUR\_PROP\_OPTIMIZATION</span></span><br/>             | <span data-ttu-id="65c9a-136">Mode d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="65c9a-136">The optimization mode.</span></span> <span data-ttu-id="65c9a-137">Pour plus d’informations, consultez [modes d’optimisation](#optimization-modes) .</span><span class="sxs-lookup"><span data-stu-id="65c9a-137">See [Optimization modes](#optimization-modes) for more info.</span></span> <span data-ttu-id="65c9a-138">Le type est D2D1 \_ GAUSSIANBLUR \_ Optimization.</span><span class="sxs-lookup"><span data-stu-id="65c9a-138">The type is D2D1\_GAUSSIANBLUR\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="65c9a-139">La valeur par défaut est D2D1 \_ GAUSSIANBLUR \_ Optimization \_ Balanced.</span><span class="sxs-lookup"><span data-stu-id="65c9a-139">The default value is D2D1\_GAUSSIANBLUR\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                            |
| <span data-ttu-id="65c9a-140">BorderMode</span><span class="sxs-lookup"><span data-stu-id="65c9a-140">BorderMode</span></span><br/> <span data-ttu-id="65c9a-141">\_Mode de bordure d2d1 GAUSSIANBLUR \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="65c9a-141">D2D1\_GAUSSIANBLUR\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="65c9a-142">Le mode utilisé pour calculer la bordure de l’image, soft ou Hard.</span><span class="sxs-lookup"><span data-stu-id="65c9a-142">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="65c9a-143">Pour plus d’informations, consultez [modes de bordure](#border-modes) .</span><span class="sxs-lookup"><span data-stu-id="65c9a-143">See [Border modes](#border-modes) for more info.</span></span> <br/> <span data-ttu-id="65c9a-144">Le type est D2D1 \_ GAUSSIANBLUR \_ Border \_ mode.</span><span class="sxs-lookup"><span data-stu-id="65c9a-144">The type is D2D1\_GAUSSIANBLUR\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="65c9a-145">La valeur par défaut est \_ d2d1 \_ en mode bordure \_ souple.</span><span class="sxs-lookup"><span data-stu-id="65c9a-145">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="65c9a-146">Modes d’optimisation</span><span class="sxs-lookup"><span data-stu-id="65c9a-146">Optimization modes</span></span>



| <span data-ttu-id="65c9a-147">Nom</span><span class="sxs-lookup"><span data-stu-id="65c9a-147">Name</span></span>                                          | <span data-ttu-id="65c9a-148">Description</span><span class="sxs-lookup"><span data-stu-id="65c9a-148">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65c9a-149">Vitesse d’optimisation de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="65c9a-149">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="65c9a-150">Applique des optimisations internes telles que la pré-mise à l’échelle à des rayons relativement petits.</span><span class="sxs-lookup"><span data-stu-id="65c9a-150">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="65c9a-151">Utilise le filtrage linéaire.</span><span class="sxs-lookup"><span data-stu-id="65c9a-151">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="65c9a-152">D2D1 \_ DIRECTIONALBLUR \_ Optimization \_ Balanced</span><span class="sxs-lookup"><span data-stu-id="65c9a-152">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="65c9a-153">Utilise les mêmes seuils d’optimisation que le mode vitesse, mais utilise le filtrage trilinéaire.</span><span class="sxs-lookup"><span data-stu-id="65c9a-153">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="65c9a-154">Qualité de l’optimisation de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="65c9a-154">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="65c9a-155">Utilise uniquement des optimisations internes avec de grands rayons de flou, où les approximations sont moins susceptibles d’être visibles.</span><span class="sxs-lookup"><span data-stu-id="65c9a-155">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="65c9a-156">Utilise le filtrage trilinéaire.</span><span class="sxs-lookup"><span data-stu-id="65c9a-156">Uses trilinear filtering.</span></span> |



 

## <a name="border-modes"></a><span data-ttu-id="65c9a-157">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="65c9a-157">Border modes</span></span>



| <span data-ttu-id="65c9a-158">Nom</span><span class="sxs-lookup"><span data-stu-id="65c9a-158">Name</span></span>                     | <span data-ttu-id="65c9a-159">Description</span><span class="sxs-lookup"><span data-stu-id="65c9a-159">Description</span></span>                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65c9a-160">\_Mode de bordure d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="65c9a-160">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="65c9a-161">L’effet remplit l’image avec des pixels noirs transparents au fur et à mesure qu’elle applique le noyau de flou, entraînant ainsi un contour adouci.</span><span class="sxs-lookup"><span data-stu-id="65c9a-161">The effect pads the image with transparent black pixels as it applies the blur kernel, resulting in a soft edge.</span></span> <br/>                                                                                             |
| <span data-ttu-id="65c9a-162">D2D1 \_ mode de bordure \_ \_ difficile</span><span class="sxs-lookup"><span data-stu-id="65c9a-162">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="65c9a-163">L’effet attache la sortie à la taille de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="65c9a-163">The effect clamps the output to the size of the input image.</span></span> <span data-ttu-id="65c9a-164">Lorsque l’effet applique le noyau de flou, il étend l’image d’entrée avec une transformation de bordure de type miroir pour les exemples en dehors des limites d’entrée.</span><span class="sxs-lookup"><span data-stu-id="65c9a-164">When the effect applies the blur kernel, it extends the input image with a mirror-type border transform for samples outside of the input bounds.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="65c9a-165">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="65c9a-165">Output bitmap</span></span>

<span data-ttu-id="65c9a-166">La sortie de cet effet peut être supérieure à la bitmap d’entrée en fonction du rayon de flou et du mode de bordure.</span><span class="sxs-lookup"><span data-stu-id="65c9a-166">The output of this effect can be larger than the input bitmap based on the blur radius and the border mode.</span></span> <span data-ttu-id="65c9a-167">Si le mode de bordure est défini sur \_ d2d1 \_ en mode bordure \_ , les Ille de la sortie bitmap augmentent de la taille du noyau de flou, représentée en pixels.</span><span class="sxs-lookup"><span data-stu-id="65c9a-167">If the border mode is set to D2D1\_BORDER\_MODE\_SOFT the s ize of the output bitmap increases by the size of the blur kernel, represented in pixels.</span></span> <span data-ttu-id="65c9a-168">Ce tableau fournit une équation que vous pouvez utiliser pour calculer la bitmap de sortie.</span><span class="sxs-lookup"><span data-stu-id="65c9a-168">This table provides an equation that you can use to compute the output bitmap.</span></span>

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

<span data-ttu-id="65c9a-169">Par conséquent, si la taille de l’image augmente de 10 pixels dans chaque direction, l’angle supérieur gauche de l’image sera situé à (-5,-5), tandis que le coin inférieur droit sera (105, 105).</span><span class="sxs-lookup"><span data-stu-id="65c9a-169">So, if the image size increases by 10 pixels in each direction the upper left corner of the image will be located at (-5, -5) while the lower right will be at (105, 105).</span></span>

## <a name="requirements"></a><span data-ttu-id="65c9a-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65c9a-170">Requirements</span></span>



| <span data-ttu-id="65c9a-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65c9a-171">Requirement</span></span> | <span data-ttu-id="65c9a-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="65c9a-172">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65c9a-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65c9a-173">Minimum supported client</span></span> | <span data-ttu-id="65c9a-174">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="65c9a-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="65c9a-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65c9a-175">Minimum supported server</span></span> | <span data-ttu-id="65c9a-176">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="65c9a-176">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="65c9a-177">En-tête</span><span class="sxs-lookup"><span data-stu-id="65c9a-177">Header</span></span>                   | <span data-ttu-id="65c9a-178">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="65c9a-178">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="65c9a-179">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65c9a-179">Library</span></span>                  | <span data-ttu-id="65c9a-180">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="65c9a-180">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="65c9a-181">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65c9a-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65c9a-182">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="65c9a-182">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

