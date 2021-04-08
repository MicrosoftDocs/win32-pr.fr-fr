---
title: 'Effet de fusion :'
description: Utilisez l’effet de fusion pour combiner 2 images. Cet effet a 26 modes de fusion.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- effet de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e248d1f7f41721d173510b8d10feac9be2e08f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844242"
---
# <a name="blend-effect"></a><span data-ttu-id="09119-105">Effet de fusion :</span><span class="sxs-lookup"><span data-stu-id="09119-105">Blend effect</span></span>

<span data-ttu-id="09119-106">Utilisez l’effet de fusion pour combiner 2 images.</span><span class="sxs-lookup"><span data-stu-id="09119-106">Use the blend effect to combine 2 images.</span></span> <span data-ttu-id="09119-107">Cet effet a 26 modes de fusion.</span><span class="sxs-lookup"><span data-stu-id="09119-107">This effect has 26 blend modes.</span></span>

<span data-ttu-id="09119-108">Le CLSID de cet effet est CLSID \_ D2D1Blend.</span><span class="sxs-lookup"><span data-stu-id="09119-108">The CLSID for this effect is CLSID\_D2D1Blend.</span></span>

-   [<span data-ttu-id="09119-109">Exemples de fusion</span><span class="sxs-lookup"><span data-stu-id="09119-109">Blending examples</span></span>](#blending-examples)
-   [<span data-ttu-id="09119-110">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="09119-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="09119-111">Modes de fusion</span><span class="sxs-lookup"><span data-stu-id="09119-111">Blend modes</span></span>](#blend-modes)
-   [<span data-ttu-id="09119-112">Conversions de l’espace colorimétrique TSL</span><span class="sxs-lookup"><span data-stu-id="09119-112">HSL color space conversions</span></span>](#hsl-color-space-conversions)
    -   [<span data-ttu-id="09119-113">Conversion de RVB en TSL</span><span class="sxs-lookup"><span data-stu-id="09119-113">Converting from RGB to HSL</span></span>](#converting-from-rgb-to-hsl)
    -   [<span data-ttu-id="09119-114">Conversion de TSL en RGB</span><span class="sxs-lookup"><span data-stu-id="09119-114">Converting from HSL to RGB</span></span>](#converting-from-hsl-to-rgb)
-   [<span data-ttu-id="09119-115">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="09119-115">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="09119-116">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="09119-116">Sample code</span></span>](#sample-code)
-   [<span data-ttu-id="09119-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09119-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="09119-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09119-118">Related topics</span></span>](#related-topics)

## <a name="blending-examples"></a><span data-ttu-id="09119-119">Exemples de fusion</span><span class="sxs-lookup"><span data-stu-id="09119-119">Blending examples</span></span>

<span data-ttu-id="09119-120">Voici un exemple d’image de chaque mode de fusion de l’effet de fusion.</span><span class="sxs-lookup"><span data-stu-id="09119-120">Here is an example image of every blend mode of the blend effect.</span></span> <span data-ttu-id="09119-121">La section suivante présente une liste complète des modes de fusion et des propriétés de mode correspondantes.</span><span class="sxs-lookup"><span data-stu-id="09119-121">A full list of the blend modes and the corresponding mode properties are in the next section</span></span>

![exemple de capture d’écran de tous les modes de fusion disponibles.](images/blend-modes.png)

<span data-ttu-id="09119-123">Voici un autre exemple utilisant le mode d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="09119-123">Here is another example using the exclusion mode.</span></span>



| <span data-ttu-id="09119-124">Avant image 1</span><span class="sxs-lookup"><span data-stu-id="09119-124">Before image 1</span></span>                                                             |
|----------------------------------------------------------------------------|
| ![première image source avant l’effet.](images/default-before.jpg)    |
| <span data-ttu-id="09119-126">Avant image 2</span><span class="sxs-lookup"><span data-stu-id="09119-126">Before image 2</span></span>                                                             |
| ![deuxième image avant l’effet.](images/4-arthimetic-composite2.jpg) |
| <span data-ttu-id="09119-128">After</span><span class="sxs-lookup"><span data-stu-id="09119-128">After</span></span>                                                                      |
| ![image après la transformation.](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="09119-130">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="09119-130">Effect properties</span></span>



| <span data-ttu-id="09119-131">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="09119-131">Display name and index enumeration</span></span>                 | <span data-ttu-id="09119-132">Description</span><span class="sxs-lookup"><span data-stu-id="09119-132">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09119-133">Mode</span><span class="sxs-lookup"><span data-stu-id="09119-133">Mode</span></span><br/> <span data-ttu-id="09119-134">\_Mode d2d1 Blend \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="09119-134">D2D1\_BLEND\_PROP\_MODE</span></span><br/> | <span data-ttu-id="09119-135">Mode de fondu utilisé pour l’effet.</span><span class="sxs-lookup"><span data-stu-id="09119-135">The blend mode used for the effect.</span></span> <span data-ttu-id="09119-136">Pour plus d’informations, consultez [modes de fusion](#blend-modes) .</span><span class="sxs-lookup"><span data-stu-id="09119-136">See [Blend modes](#blend-modes) for more info.</span></span> <span data-ttu-id="09119-137">Le type est D2D1 \_ Blend \_ mode.</span><span class="sxs-lookup"><span data-stu-id="09119-137">The type is D2D1\_BLEND\_MODE.</span></span><br/> <span data-ttu-id="09119-138">La valeur par défaut est D2D1 \_ Blend \_ mode \_ Multiply.</span><span class="sxs-lookup"><span data-stu-id="09119-138">The default value is D2D1\_BLEND\_MODE\_MULTIPLY.</span></span><br/> |



 

## <a name="blend-modes"></a><span data-ttu-id="09119-139">Modes de fusion</span><span class="sxs-lookup"><span data-stu-id="09119-139">Blend modes</span></span>

<span data-ttu-id="09119-140">Le tableau ci-dessous montre tous les modes de fusion de cet effet.</span><span class="sxs-lookup"><span data-stu-id="09119-140">The table here shows all the blend modes of this effect.</span></span> <span data-ttu-id="09119-141">Les fonctions d’assistance nécessaires pour calculer la sortie de l’effet se trouvent dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="09119-141">The helper functions necessary to compute the output of the effect are in the next section.</span></span>

<span data-ttu-id="09119-142">Couleur : O <sub>PRGB</sub>  =  *f*(f <sub>RGB</sub>, b <sub>RGB</sub>) \* f <sub>a</sub> \* B <sub></sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>a</sub>) + B <sub>RGB</sub> \* b <sub>a</sub> \* (1-f <sub>a</sub>)</span><span class="sxs-lookup"><span data-stu-id="09119-142">Color: O <sub>PRGB</sub> = *f*(F<sub>RGB</sub>, B<sub>RGB</sub>) \* F<sub>A</sub> \* B<sub>A</sub> + F<sub>RGB</sub> \* F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>RGB</sub> \* B<sub>A</sub> \* (1 - F<sub>A</sub>)</span></span>

<span data-ttu-id="09119-143">Alpha : O<sub>a</sub> = F<sub>a</sub> \* (1-B<sub>a</sub>) + B<sub>a</sub></span><span class="sxs-lookup"><span data-stu-id="09119-143">Alpha: O<sub>A</sub> = F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>A</sub></span></span>

<span data-ttu-id="09119-144">Où :</span><span class="sxs-lookup"><span data-stu-id="09119-144">Where:</span></span>

-   <span data-ttu-id="09119-145">O<sub>PRGB</sub> est la couleur de sortie prémultipliée</span><span class="sxs-lookup"><span data-stu-id="09119-145">O<sub>PRGB</sub> is the pre-multiplied output color</span></span>
-   <span data-ttu-id="09119-146">O<sub>a est une</sub> sortie alpha</span><span class="sxs-lookup"><span data-stu-id="09119-146">O<sub>A</sub> is Output Alpha</span></span>
-   <span data-ttu-id="09119-147">B<sub>RVB</sub> est la couleur de destination non prémultipliée</span><span class="sxs-lookup"><span data-stu-id="09119-147">B<sub>RGB</sub> is the un-pre-multiplied destination color</span></span>
-   <span data-ttu-id="09119-148">B<sub>a est une</sub> destination alpha</span><span class="sxs-lookup"><span data-stu-id="09119-148">B<sub>A</sub> is destination alpha</span></span>
-   <span data-ttu-id="09119-149">F<sub>RGB</sub> est la couleur source non prémultipliée</span><span class="sxs-lookup"><span data-stu-id="09119-149">F<sub>RGB</sub> is the un-pre-multiplied source color</span></span>
-   <span data-ttu-id="09119-150">F<sub>a est une</sub> source alpha</span><span class="sxs-lookup"><span data-stu-id="09119-150">F<sub>A</sub> is source alpha</span></span>
-   <span data-ttu-id="09119-151">*f*(S <sub>RGB</sub>, D <sub>RGB</sub>) est une fonction de fusion qui varie en mode par fusion</span><span class="sxs-lookup"><span data-stu-id="09119-151">*f*(S<sub>RGB</sub>, D<sub>RGB</sub>) is a blend function that varies per-blend-mode</span></span>

<span data-ttu-id="09119-152">Certains modes de fusion nécessitent une conversion vers et à partir de l’espace de couleurs teinte, saturation, luminosité (TSL) sur RVB.</span><span class="sxs-lookup"><span data-stu-id="09119-152">Some of the blend modes require conversion to and from the hue, saturation, luminosity (HSL) color space to RGB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09119-153">Énumération</span><span class="sxs-lookup"><span data-stu-id="09119-153">Enumeration</span></span></th>
<th><span data-ttu-id="09119-154">Sommaire</span><span class="sxs-lookup"><span data-stu-id="09119-154">Equation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09119-155">D2D1_BLEND_MODE_DARKEN</span><span class="sxs-lookup"><span data-stu-id="09119-155">D2D1_BLEND_MODE_DARKEN</span></span></td>
<td><span data-ttu-id="09119-156">Formule de fusion de base pour Alpha uniquement.</span><span class="sxs-lookup"><span data-stu-id="09119-156">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-157">D2D1_BLEND_MODE_MULTIPLY</span><span class="sxs-lookup"><span data-stu-id="09119-157">D2D1_BLEND_MODE_MULTIPLY</span></span></td>
<td><span data-ttu-id="09119-158">Formule de fusion de base pour Alpha uniquement.</span><span class="sxs-lookup"><span data-stu-id="09119-158">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09119-159">D2D1_BLEND_MODE_COLOR_BURN</span><span class="sxs-lookup"><span data-stu-id="09119-159">D2D1_BLEND_MODE_COLOR_BURN</span></span></td>
<td><span data-ttu-id="09119-160">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="09119-160">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-161">D2D1_BLEND_MODE_LINEAR_BURN</span><span class="sxs-lookup"><span data-stu-id="09119-161">D2D1_BLEND_MODE_LINEAR_BURN</span></span></td>
<td><span data-ttu-id="09119-162">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="09119-162">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09119-163">D2D1_BLEND_MODE_DARKER_COLOR</span><span class="sxs-lookup"><span data-stu-id="09119-163">D2D1_BLEND_MODE_DARKER_COLOR</span></span></td>
<td><span data-ttu-id="09119-164">Formule de fusion de base pour Alpha uniquement.</span><span class="sxs-lookup"><span data-stu-id="09119-164">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-165">D2D1_BLEND_MODE_LIGHTEN</span><span class="sxs-lookup"><span data-stu-id="09119-165">D2D1_BLEND_MODE_LIGHTEN</span></span></td>
<td><span data-ttu-id="09119-166">Formule de fusion de base pour Alpha uniquement.</span><span class="sxs-lookup"><span data-stu-id="09119-166">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09119-167">D2D1_BLEND_MODE_SCREEN</span><span class="sxs-lookup"><span data-stu-id="09119-167">D2D1_BLEND_MODE_SCREEN</span></span></td>
<td><span data-ttu-id="09119-168">Formule de fusion de base pour Alpha uniquement.</span><span class="sxs-lookup"><span data-stu-id="09119-168">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-169">D2D1_BLEND_MODE_COLOR_DODGE</span><span class="sxs-lookup"><span data-stu-id="09119-169">D2D1_BLEND_MODE_COLOR_DODGE</span></span></td>
<td><span data-ttu-id="09119-170">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="09119-170">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09119-171">D2D1_BLEND_MODE_LINEAR_DODGE</span><span class="sxs-lookup"><span data-stu-id="09119-171">D2D1_BLEND_MODE_LINEAR_DODGE</span></span></td>
<td><span data-ttu-id="09119-172">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="09119-172">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span><span class="sxs-lookup"><span data-stu-id="09119-173">D2D1_BLEND_MODE_LIGHTER_COLOR</span></span></td>
<td><span data-ttu-id="09119-174">Formule de fusion de base pour Alpha uniquement.</span><span class="sxs-lookup"><span data-stu-id="09119-174">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09119-175">D2D1_BLEND_MODE_OVERLAY</span><span class="sxs-lookup"><span data-stu-id="09119-175">D2D1_BLEND_MODE_OVERLAY</span></span></td>
<td><span data-ttu-id="09119-176">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="09119-176">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-177">D2D1_BLEND_MODE_SOFT_LIGHT</span><span class="sxs-lookup"><span data-stu-id="09119-177">D2D1_BLEND_MODE_SOFT_LIGHT</span></span></td>
<td><span data-ttu-id="09119-178">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="09119-178">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09119-179">D2D1_BLEND_MODE_HARD_LIGHT</span><span class="sxs-lookup"><span data-stu-id="09119-179">D2D1_BLEND_MODE_HARD_LIGHT</span></span></td>
<td><span data-ttu-id="09119-180">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="09119-180">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-181">D2D1_BLEND_MODE_VIVID_LIGHT</span><span class="sxs-lookup"><span data-stu-id="09119-181">D2D1_BLEND_MODE_VIVID_LIGHT</span></span></td>
<td><span data-ttu-id="09119-182">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="09119-182">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09119-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span><span class="sxs-lookup"><span data-stu-id="09119-183">D2D1_BLEND_MODE_LINEAR_LIGHT</span></span></td>
<td><span data-ttu-id="09119-184">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="09119-184">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-185">D2D1_BLEND_MODE_PIN_LIGHT</span><span class="sxs-lookup"><span data-stu-id="09119-185">D2D1_BLEND_MODE_PIN_LIGHT</span></span></td>
<td><span data-ttu-id="09119-186">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="09119-186">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09119-187">D2D1_BLEND_MODE_HARD_MIX</span><span class="sxs-lookup"><span data-stu-id="09119-187">D2D1_BLEND_MODE_HARD_MIX</span></span></td>
<td><span data-ttu-id="09119-188">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) =</span><span class="sxs-lookup"><span data-stu-id="09119-188">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) =</span></span> <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-189">D2D1_BLEND_MODE_DIFFERENCE</span><span class="sxs-lookup"><span data-stu-id="09119-189">D2D1_BLEND_MODE_DIFFERENCE</span></span></td>
<td><span data-ttu-id="09119-190">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = ABS (f<sub>RVB</sub> - b<sub>RGB</sub>)</span><span class="sxs-lookup"><span data-stu-id="09119-190">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = abs(F<sub>RGB</sub> - B<sub>RGB</sub>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09119-191">D2D1_BLEND_MODE_EXCLUSION</span><span class="sxs-lookup"><span data-stu-id="09119-191">D2D1_BLEND_MODE_EXCLUSION</span></span></td>
<td><span data-ttu-id="09119-192">Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + b<sub>RVB</sub> 2 \* f<sub>RVB</sub> \* b<sub></sub> RVB</span><span class="sxs-lookup"><span data-stu-id="09119-192">Basic blend formulas with <em>f</em>(F<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + B<sub>RGB</sub>   2 \* F<sub>RGB</sub> \* B<sub>RGB</sub></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-193">D2D1_BLEND_MODE_HUE</span><span class="sxs-lookup"><span data-stu-id="09119-193">D2D1_BLEND_MODE_HUE</span></span></td>
<td><span data-ttu-id="09119-194">Formule de fusion de base pour Alpha uniquement.</span><span class="sxs-lookup"><span data-stu-id="09119-194">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09119-195">D2D1_BLEND_MODE_SATURATION</span><span class="sxs-lookup"><span data-stu-id="09119-195">D2D1_BLEND_MODE_SATURATION</span></span></td>
<td><span data-ttu-id="09119-196">Formule de fusion de base pour Alpha uniquement.</span><span class="sxs-lookup"><span data-stu-id="09119-196">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-197">D2D1_BLEND_MODE_COLOR</span><span class="sxs-lookup"><span data-stu-id="09119-197">D2D1_BLEND_MODE_COLOR</span></span></td>
<td><span data-ttu-id="09119-198">Formule de fusion de base pour Alpha uniquement.</span><span class="sxs-lookup"><span data-stu-id="09119-198">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09119-199">D2D1_BLEND_MODE_LUMINOSITY</span><span class="sxs-lookup"><span data-stu-id="09119-199">D2D1_BLEND_MODE_LUMINOSITY</span></span></td>
<td><span data-ttu-id="09119-200">Formule de fusion de base pour Alpha uniquement.</span><span class="sxs-lookup"><span data-stu-id="09119-200">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-201">D2D1_BLEND_MODE_DISSOLVE</span><span class="sxs-lookup"><span data-stu-id="09119-201">D2D1_BLEND_MODE_DISSOLVE</span></span></td>
<td><span data-ttu-id="09119-202">Soit :</span><span class="sxs-lookup"><span data-stu-id="09119-202">Given:</span></span>
<ul>
<li><span data-ttu-id="09119-203">Une scène en coordonnées XY pour le pixel actuel</span><span class="sxs-lookup"><span data-stu-id="09119-203">A scene coordinate XY for the current pixel</span></span></li>
<li><span data-ttu-id="09119-204">Un générateur de nombres pseudo-aléatoires déterministe (XY) basé sur la coordonnée de valeur de départ XY, avec une distribution sans biais de valeurs de [0, 1]</span><span class="sxs-lookup"><span data-stu-id="09119-204">A deterministic pseudo-random number generator rand(XY) based on seed coordinate XY, with unbiased distribution of values from [0, 1]</span></span></li>
</ul>
<br/> <img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09119-205">D2D1_BLEND_MODE_SUBTRACT</span><span class="sxs-lookup"><span data-stu-id="09119-205">D2D1_BLEND_MODE_SUBTRACT</span></span></td>
<td><span data-ttu-id="09119-206">Formule de fusion de base pour Alpha uniquement.</span><span class="sxs-lookup"><span data-stu-id="09119-206">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09119-207">D2D1_BLEND_MODE_DIVISION</span><span class="sxs-lookup"><span data-stu-id="09119-207">D2D1_BLEND_MODE_DIVISION</span></span></td>
<td><span data-ttu-id="09119-208">Formule de fusion de base pour Alpha uniquement.</span><span class="sxs-lookup"><span data-stu-id="09119-208">Basic blend formula for alpha only.</span></span> <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="09119-209">Pour tous les modes de fusion, la valeur de sortie est prémultipliée et ancrée à la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="09119-209">For all Blend modes, the output value is premultiplied and clamped to the range \[0, 1\].</span></span>

 

## <a name="hsl-color-space-conversions"></a><span data-ttu-id="09119-210">Conversions de l’espace colorimétrique TSL</span><span class="sxs-lookup"><span data-stu-id="09119-210">HSL color space conversions</span></span>

<span data-ttu-id="09119-211">Le composant luminosité est calculé à l’aide des pondérations RVB ici :</span><span class="sxs-lookup"><span data-stu-id="09119-211">The luminosity component is computed using the RGB weights here:</span></span>

-   <span data-ttu-id="09119-212">*k*<sub>R</sub> = 0,30</span><span class="sxs-lookup"><span data-stu-id="09119-212">*k*<sub>R</sub> = 0.30</span></span>
-   <span data-ttu-id="09119-213">*k*<sub>G</sub> = 0,59</span><span class="sxs-lookup"><span data-stu-id="09119-213">*k*<sub>G</sub> = 0.59</span></span>
-   <span data-ttu-id="09119-214">*k*<sub>B</sub> = 0,11</span><span class="sxs-lookup"><span data-stu-id="09119-214">*k*<sub>B</sub> = 0.11</span></span>

### <a name="converting-from-rgb-to-hsl"></a><span data-ttu-id="09119-215">Conversion de RVB en TSL</span><span class="sxs-lookup"><span data-stu-id="09119-215">Converting from RGB to HSL</span></span>

![formule mathématique décrivant la transformation de la couleur RVB à la couleur TSL.](images/blend-rgb-to-hsl-1.png)

<span data-ttu-id="09119-217">Cela place *S* et *L* dans la plage \[ 0,0, 1,0 \] et *H* dans la plage \[ -1,0, 5,0 \] .</span><span class="sxs-lookup"><span data-stu-id="09119-217">This places *S* and *L* in the range \[0.0, 1.0\] and *H* in the range \[-1.0, 5.0\].</span></span>

### <a name="converting-from-hsl-to-rgb"></a><span data-ttu-id="09119-218">Conversion de TSL en RGB</span><span class="sxs-lookup"><span data-stu-id="09119-218">Converting from HSL to RGB</span></span>

<span data-ttu-id="09119-219">Pour convertir d’une autre façon, nous utilisons l’inverse des calculs précédents.</span><span class="sxs-lookup"><span data-stu-id="09119-219">To convert the other way we use the inverse of the previous calculations.</span></span>

<span data-ttu-id="09119-220">Si *S* = 0, alors *R*  =  *G*  =  *B*  =  *L*</span><span class="sxs-lookup"><span data-stu-id="09119-220">If *S* = 0 then *R* = *G* = *B* = *L*</span></span>

<span data-ttu-id="09119-221">Dans le cas contraire, il existe six cas dépendants de la teinte :</span><span class="sxs-lookup"><span data-stu-id="09119-221">Otherwise there are six hue-dependant cases:</span></span>

<span data-ttu-id="09119-222">Si *H* est supérieur à 0, les valeurs se trouvent dans le secteur rouge/Magenta où *R*  >  *B*  >  *G*.</span><span class="sxs-lookup"><span data-stu-id="09119-222">If *H* is greater than 0, the values are in the red/magenta sector where *R* > *B* > *G*.</span></span>

![equaiton : étape 1 de six convertissant la couleur TSL en RVB.](images/blend-hsl-to-rgb-1rm.png)

<span data-ttu-id="09119-224">Si *H* est supérieur ou égal à 0 et inférieur à 1, les valeurs se trouvent dans le secteur rouge/jaune où *R*  >  *G*  >  *B*.</span><span class="sxs-lookup"><span data-stu-id="09119-224">If *H* is greater than or equal to 0 and less than 1, the values are in the red/yellow sector where *R* > *G* > *B*.</span></span>

![mathématiques equaiton étape deux de six convertissant la couleur TSL en RVB.](images/blend-hsl-to-rgb-1ry.png)

<span data-ttu-id="09119-226">Si *H* est supérieur ou égal à 1 et inférieur à 2, les valeurs se trouvent dans le secteur jaune/vert où *G*  >  *R*  >  *B*.</span><span class="sxs-lookup"><span data-stu-id="09119-226">If *H* is greater than or equal to 1 and less than 2, the values are in the yellow/green sector where *G* > *R* > *B*.</span></span>

![mathématiques equaiton étape trois de six convertissant la couleur TSL en RVB.](images/blend-hsl-to-rgb-1yg.png)

<span data-ttu-id="09119-228">Si *H* est supérieur ou égal à 2 et inférieur à 3, les valeurs se trouvent dans le secteur vert/cyan où *G*  >  *B*  >  *R*.</span><span class="sxs-lookup"><span data-stu-id="09119-228">If *H* is greater than or equal to 2 and less than 3, the values are in the green/cyan sector where *G* > *B* > *R*.</span></span>

![mathématiques equaiton étape quatre de six convertissant la couleur TSL en RVB.](images/blend-hsl-to-rgb-1gc.png)

<span data-ttu-id="09119-230">Si *H* est supérieur ou égal à 3 et inférieur à 4, les valeurs se trouvent dans le secteur cyan/bleu, où *B*  >  *G*  >  *R*.</span><span class="sxs-lookup"><span data-stu-id="09119-230">If *H* is greater than or equal to 3 and less than 4, the values are in the cyan/blue sector where *B* > *G* > *R*.</span></span>

![mathématiques equaiton étape 5 de six convertissant la couleur TSL en RVB.](images/blend-hsl-to-rgb-1cb.png)

<span data-ttu-id="09119-232">Si *H* est supérieur ou égal à 4, les valeurs se trouvent dans le secteur bleu/magenta où *B*  >  *R*  >  *G*.</span><span class="sxs-lookup"><span data-stu-id="09119-232">If *H* is greater than or equal to 4, the values are in the blue/magenta sector where *B* > *R* > *G*.</span></span>

![mathématiques equaiton étape six de six convertissant la couleur TSL en RVB.](images/blend-hsl-to-rgb-1bm.png)

<span data-ttu-id="09119-234">Étant donné que les modes de fusion apportent des combinaisons arbitraires de composants TSL à partir de deux couleurs différentes, il est courant que la valeur RVB convertie soit hors de la gamme, c’est-à-dire qu’un ou plusieurs composants de canal soient en dehors de la plage légale \[ 0,0, 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="09119-234">Because the blending modes make arbitrary combinations of HSL components from two different colors, it is common for the converted RGB value to be out-of-gamut, that is, one or more channel components may be outside the legal range of \[0.0, 1.0\].</span></span> <span data-ttu-id="09119-235">Ces couleurs sont remises en gamme en réduisant au minimum la saturation, tout en préservant la teinte et la luminosité :</span><span class="sxs-lookup"><span data-stu-id="09119-235">These colors are brought back into gamut by minimally reducing the saturation, while preserving both hue and luminosity:</span></span>

![formule mathématique décrivant les corrections requises pour les instances de non-gamme.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a><span data-ttu-id="09119-237">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="09119-237">Output bitmap</span></span>

<span data-ttu-id="09119-238">Le bitmap de sortie de cet effet est toujours la taille de l’Union des deux images d’entrée.</span><span class="sxs-lookup"><span data-stu-id="09119-238">The output bitmap for this effect is always the size of the union of the two input images.</span></span>

## <a name="sample-code"></a><span data-ttu-id="09119-239">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="09119-239">Sample code</span></span>

<span data-ttu-id="09119-240">Pour obtenir un exemple de cet effet, téléchargez l' [exemple de modes d’effet composite de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span><span class="sxs-lookup"><span data-stu-id="09119-240">For an example of this effect, download the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).</span></span>

## <a name="requirements"></a><span data-ttu-id="09119-241">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09119-241">Requirements</span></span>



| <span data-ttu-id="09119-242">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09119-242">Requirement</span></span> | <span data-ttu-id="09119-243">Valeur</span><span class="sxs-lookup"><span data-stu-id="09119-243">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09119-244">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09119-244">Minimum supported client</span></span> | <span data-ttu-id="09119-245">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="09119-245">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="09119-246">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09119-246">Minimum supported server</span></span> | <span data-ttu-id="09119-247">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="09119-247">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="09119-248">En-tête</span><span class="sxs-lookup"><span data-stu-id="09119-248">Header</span></span>                   | <span data-ttu-id="09119-249">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="09119-249">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="09119-250">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09119-250">Library</span></span>                  | <span data-ttu-id="09119-251">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="09119-251">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="09119-252">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09119-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09119-253">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="09119-253">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

