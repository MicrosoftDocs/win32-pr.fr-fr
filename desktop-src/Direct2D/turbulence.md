---
title: Effet turbulence
description: Utilisez l’effet turbulence pour générer une image bitmap basée sur la fonction de bruit perl.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- effet turbulence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f67f615ec5b68ca285a048b68bc7bc8eab6e24
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104565102"
---
# <a name="turbulence-effect"></a><span data-ttu-id="ec2f4-104">Effet turbulence</span><span class="sxs-lookup"><span data-stu-id="ec2f4-104">Turbulence effect</span></span>

<span data-ttu-id="ec2f4-105">Utilisez l’effet turbulence pour générer une image bitmap basée sur la fonction de bruit perl.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-105">Use the turbulence effect to generate a bitmap based on the Perlin noise function.</span></span>

<span data-ttu-id="ec2f4-106">L’effet turbulence n’a aucune image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-106">The turbulence effect has no input image.</span></span>

<span data-ttu-id="ec2f4-107">Le CLSID de cet effet est CLSID \_ D2D1Turbulence.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-107">The CLSID for this effect is CLSID\_D2D1Turbulence.</span></span>

-   [<span data-ttu-id="ec2f4-108">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="ec2f4-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="ec2f4-109">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="ec2f4-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="ec2f4-110">Modes de bruit</span><span class="sxs-lookup"><span data-stu-id="ec2f4-110">Noise modes</span></span>](#noise-modes)
-   [<span data-ttu-id="ec2f4-111">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="ec2f4-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="ec2f4-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec2f4-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ec2f4-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ec2f4-113">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ec2f4-114">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="ec2f4-114">Example image</span></span>

![exemple de capture d’écran montrant la sortie de l’effet turbulence.](images/32-turbulence.png)

<span data-ttu-id="ec2f4-116">L’effet turbulence calcule la somme d’une ou de plusieurs octaves de la fonction de bruit perl.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-116">The Turbulence effect computes the sum of one or more octaves of the Perlin noise function.</span></span> <span data-ttu-id="ec2f4-117">Le bruit perl est une fonction Pseudo-aléatoire dont la valeur dépend de la valeur de la fréquence, de la position et de la valeur initiale.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-117">Perlin noise is a pseudo-random function whose value depends on the frequency, position, and seed value.</span></span> <span data-ttu-id="ec2f4-118">L’effet génère les valeurs RVBA à l’aide de l’une de ces équations.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-118">The effect generates the RGBA values using one of these equations.</span></span>

<span data-ttu-id="ec2f4-119">Si vous sélectionnez le mode de bruit de la \_ \_ \_ somme fractale d2d1 turbulence bruit \_ , l’effet utilise cette équation.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-119">If you select the D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM noise mode the effect uses this equation.</span></span>

![Capture d’écran montrant la fonction turbulence utilisée pour générer une image bitmap.](images/turbulence-equation1.png)

<span data-ttu-id="ec2f4-121">Si vous sélectionnez le \_ mode de turbulence du bruit d2d1 turbulence \_ \_ , l’effet utilise cette équation.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-121">If you select the D2D1\_TURBULENCE\_NOISE\_TURBULENCE noise mode the effect uses this equation.</span></span>

![fonction turbulence utilisée pour générer une image bitmap.](images/turbulence-equation2.png)

> [!Note]  
> <span data-ttu-id="ec2f4-123">La `PerlinNoise` fonction est comprise entre \[ -1 et 1 \] .</span><span class="sxs-lookup"><span data-stu-id="ec2f4-123">The `PerlinNoise` function has a range of \[-1, 1\].</span></span>

 

<span data-ttu-id="ec2f4-124">Cet effet génère des valeurs en pixels dans des valeurs alpha prémultipliées.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-124">This effect outputs pixel values in premultiplied alpha.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="ec2f4-125">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="ec2f4-125">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec2f4-126">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="ec2f4-126">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="ec2f4-127">Description</span><span class="sxs-lookup"><span data-stu-id="ec2f4-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec2f4-128">Offset</span><span class="sxs-lookup"><span data-stu-id="ec2f4-128">Offset</span></span><br/> <span data-ttu-id="ec2f4-129">D2D1_TURBULENCE_PROP_OFFSET</span><span class="sxs-lookup"><span data-stu-id="ec2f4-129">D2D1_TURBULENCE_PROP_OFFSET</span></span><br/></td>
<td><span data-ttu-id="ec2f4-130">Coordonnées où la sortie de turbulence est générée.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-130">The coordinates where the turbulence output is generated.</span></span><br/> <span data-ttu-id="ec2f4-131">L’algorithme utilisé pour générer le bruit perl est dépendant de la position, donc un décalage différent produit une sortie différente.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-131">The algorithm used to generate the Perlin noise is position dependent, so a different offset results in a different output.</span></span> <span data-ttu-id="ec2f4-132">Cette propriété n’est pas limitée et les unités sont spécifiées dans des DIP</span><span class="sxs-lookup"><span data-stu-id="ec2f4-132">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ec2f4-133">Le décalage n’a pas le même effet qu’une translation, car la sortie de la fonction Noise est infinie et la fonction est encapsulée dans la vignette.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-133">The offset does not have the same effect as a translation because the noise function output is infinite and the function will wrap around the tile.</span></span>
</blockquote>
<br/> <span data-ttu-id="ec2f4-134">Le type est D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-134">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="ec2f4-135">La valeur par défaut est {0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-135">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec2f4-136">Taille</span><span class="sxs-lookup"><span data-stu-id="ec2f4-136">Size</span></span><br/> <span data-ttu-id="ec2f4-137">D2D1_TURBULENCE_PROP_SIZE</span><span class="sxs-lookup"><span data-stu-id="ec2f4-137">D2D1_TURBULENCE_PROP_SIZE</span></span><br/></td>
<td><span data-ttu-id="ec2f4-138">Taille de la sortie de turbulence.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-138">The size of the turbulence output.</span></span><br/> <span data-ttu-id="ec2f4-139">Cette propriété n’est pas limitée et les unités sont spécifiées dans des DIP</span><span class="sxs-lookup"><span data-stu-id="ec2f4-139">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<br/> <span data-ttu-id="ec2f4-140">Le type est D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-140">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="ec2f4-141">La valeur par défaut est {0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-141">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec2f4-142">BaseFrequency</span><span class="sxs-lookup"><span data-stu-id="ec2f4-142">BaseFrequency</span></span><br/> <span data-ttu-id="ec2f4-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span><span class="sxs-lookup"><span data-stu-id="ec2f4-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span></span><br/></td>
<td><span data-ttu-id="ec2f4-144">Les fréquences de base dans les directions X et Y.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-144">The base frequencies in the X and Y direction.</span></span> <span data-ttu-id="ec2f4-145">Cette propriété est de type float et doit être supérieure à 0.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-145">This property is a float and must be greater than 0.</span></span> <span data-ttu-id="ec2f4-146">Les unités sont spécifiées en 1/DIP.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-146">The units are specified in 1/DIPs.</span></span> <br/> <span data-ttu-id="ec2f4-147">Une valeur de 1 (1/DIP) pour la fréquence de base se traduit par un bruit Perl qui termine un cycle entier entre deux pixels.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-147">A value of 1 (1/DIPs) for the base frequency results in the Perlin noise completing an entire cycle between two pixels.</span></span> <span data-ttu-id="ec2f4-148">L’interpolation d’accélération pour ces pixels entraîne des pixels complètement aléatoires, car il n’y a aucune corrélation entre les pixels.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-148">The ease interpolation for these pixels results in completely random pixels, since there is no correlation between the pixels.</span></span><br/> <span data-ttu-id="ec2f4-149">Une valeur de 0.1 (1/DIP) pour la fréquence de base, la fonction de bruit perl se répète toutes les 10 dip.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-149">A value of 0.1(1/DIPs) for the base frequency, the Perlin noise function repeats every 10 DIPs.</span></span> <span data-ttu-id="ec2f4-150">Cela aboutit à une corrélation entre les pixels et l’effet de turbulence typique est visible.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-150">This results in correlation between pixels and the typical turbulence effect is visible.</span></span><br/> <span data-ttu-id="ec2f4-151">Le type est D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-151">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="ec2f4-152">La valeur par défaut est {0,01 f, 0,01 f}.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-152">The default value is {0.01f, 0.01f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec2f4-153">NumOctaves</span><span class="sxs-lookup"><span data-stu-id="ec2f4-153">NumOctaves</span></span><br/> <span data-ttu-id="ec2f4-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span><span class="sxs-lookup"><span data-stu-id="ec2f4-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span></span><br/></td>
<td><span data-ttu-id="ec2f4-155">Nombre d’octaves pour la fonction de bruit.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-155">The number of octaves for the noise function.</span></span> <span data-ttu-id="ec2f4-156">Cette propriété est un UINT32 et doit être supérieure à 0.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-156">This property is a UINT32 and must be greater than 0.</span></span><br/> <span data-ttu-id="ec2f4-157">Le type est UINT32.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-157">The type is UINT32.</span></span><br/> <span data-ttu-id="ec2f4-158">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-158">The default value is 1.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec2f4-159">Seed</span><span class="sxs-lookup"><span data-stu-id="ec2f4-159">Seed</span></span><br/> <span data-ttu-id="ec2f4-160">D2D1_TURBULENCE_PROP_SEED</span><span class="sxs-lookup"><span data-stu-id="ec2f4-160">D2D1_TURBULENCE_PROP_SEED</span></span><br/></td>
<td><span data-ttu-id="ec2f4-161">Valeur initiale pour le générateur Pseudo-aléatoire.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-161">The seed for the pseudo random generator.</span></span> <span data-ttu-id="ec2f4-162">Cette propriété n’est pas liée.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-162">This property is unbounded.</span></span><br/> <span data-ttu-id="ec2f4-163">Le type est UINT32.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-163">The type is UINT32.</span></span><br/> <span data-ttu-id="ec2f4-164">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-164">The default value is 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec2f4-165">Parasite</span><span class="sxs-lookup"><span data-stu-id="ec2f4-165">Noise</span></span><br/> <span data-ttu-id="ec2f4-166">D2D1_TURBULENCE_PROP_NOISE</span><span class="sxs-lookup"><span data-stu-id="ec2f4-166">D2D1_TURBULENCE_PROP_NOISE</span></span><br/></td>
<td><span data-ttu-id="ec2f4-167">Mode de bruit de turbulence.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-167">The turbulence noise mode.</span></span> <span data-ttu-id="ec2f4-168">Cette propriété peut être une <em>somme fractale</em> ou une <em>turbulence</em>.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-168">This property can be either <em>fractal sum</em> or <em>turbulence</em>.</span></span> <span data-ttu-id="ec2f4-169">Indique s’il faut générer une image bitmap basée sur le bruit fractal ou la fonction turbulence.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-169">Indicates whether to generate a bitmap based on Fractal Noise or the Turbulence function.</span></span> <span data-ttu-id="ec2f4-170">Pour plus d’informations, consultez <a href="#noise-modes">modes de bruit</a> .</span><span class="sxs-lookup"><span data-stu-id="ec2f4-170">See <a href="#noise-modes">Noise modes</a> for more info.</span></span> <br/> <span data-ttu-id="ec2f4-171">Le type est D2D1_TURBULENCE_NOISE.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-171">The type is D2D1_TURBULENCE_NOISE.</span></span><br/> <span data-ttu-id="ec2f4-172">La valeur par défaut est D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-172">The default value is D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec2f4-173">Agrafable</span><span class="sxs-lookup"><span data-stu-id="ec2f4-173">Stitchable</span></span><br/> <span data-ttu-id="ec2f4-174">D2D1_TURBULENCE_PROP_STITCHABLE</span><span class="sxs-lookup"><span data-stu-id="ec2f4-174">D2D1_TURBULENCE_PROP_STITCHABLE</span></span><br/></td>
<td><span data-ttu-id="ec2f4-175">Active ou désactive l’assemblage.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-175">Turns stitching on or off.</span></span> <span data-ttu-id="ec2f4-176">La fréquence de base est ajustée afin que la bitmap de sortie puisse être retouchée.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-176">The base frequency is adjusted so that output bitmap can be stitched.</span></span> <span data-ttu-id="ec2f4-177">Cela est utile si vous souhaitez afficher en mosaïque plusieurs copies de la sortie de l’effet de turbulence.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-177">This is useful if you want to tile multiple copies of the turbulence effect output.</span></span>
<ul>
<li><span data-ttu-id="ec2f4-178">True la bitmap de sortie peut être en mosaïque (à l’aide de l’effet de vignette) sans l’apparence des jointures.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-178">True   The output bitmap can be tiled (using the tile effect) without the appearance of seams.</span></span> <span data-ttu-id="ec2f4-179">La fréquence de base est ajustée afin que la bitmap de sortie puisse être retouchée.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-179">The base frequency is adjusted so that output bitmap can be stitched.</span></span></li>
<li><span data-ttu-id="ec2f4-180">False la fréquence de base n’est pas ajustée. les coutures peuvent donc apparaître entre les vignettes si la bitmap est affichée en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-180">False   The base frequency is not adjusted, so seams may appear between tiles if the bitmap is tiled.</span></span></li>
</ul>
<br/> <span data-ttu-id="ec2f4-181">Le type est BOOL.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-181">The type is BOOL.</span></span><br/> <span data-ttu-id="ec2f4-182">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-182">The default value is FALSE.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a><span data-ttu-id="ec2f4-183">Modes de bruit</span><span class="sxs-lookup"><span data-stu-id="ec2f4-183">Noise modes</span></span>



| <span data-ttu-id="ec2f4-184">Énumération</span><span class="sxs-lookup"><span data-stu-id="ec2f4-184">Enumeration</span></span>                           | <span data-ttu-id="ec2f4-185">Description</span><span class="sxs-lookup"><span data-stu-id="ec2f4-185">Description</span></span>                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec2f4-186">\_ \_ \_ Somme fractale du bruit de turbulence d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="ec2f4-186">D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM</span></span> | <span data-ttu-id="ec2f4-187">Calcule la somme des octaves, en décalant la plage de sortie de \[ -1, 1 \] à \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="ec2f4-187">Computes a sum of the octaves, shifting the output range from \[-1, 1\], to \[0, 1\].</span></span> |
| <span data-ttu-id="ec2f4-188">\_Turbulence du \_ bruit de turbulence d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="ec2f4-188">D2D1\_TURBULENCE\_NOISE\_TURBULENCE</span></span>   | <span data-ttu-id="ec2f4-189">Calcule la somme de la valeur absolue de chaque octave.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-189">Computes a sum of the absolute value of each octave.</span></span>                                  |



 

> [!Note]  
> <span data-ttu-id="ec2f4-190">Aucun mode ne contient une pince explicite des valeurs de sortie.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-190">Neither mode contains an explicit clamp of the output values.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="ec2f4-191">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="ec2f4-191">Output bitmap</span></span>

<span data-ttu-id="ec2f4-192">Cet effet génère une image bitmap de taille infinie logiquement.</span><span class="sxs-lookup"><span data-stu-id="ec2f4-192">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec2f4-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec2f4-193">Requirements</span></span>



| <span data-ttu-id="ec2f4-194">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec2f4-194">Requirement</span></span> | <span data-ttu-id="ec2f4-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec2f4-195">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec2f4-196">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec2f4-196">Minimum supported client</span></span> | <span data-ttu-id="ec2f4-197">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ec2f4-197">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ec2f4-198">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec2f4-198">Minimum supported server</span></span> | <span data-ttu-id="ec2f4-199">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ec2f4-199">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ec2f4-200">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec2f4-200">Header</span></span>                   | <span data-ttu-id="ec2f4-201">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ec2f4-201">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ec2f4-202">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ec2f4-202">Library</span></span>                  | <span data-ttu-id="ec2f4-203">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ec2f4-203">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ec2f4-204">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ec2f4-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec2f4-205">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ec2f4-205">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

