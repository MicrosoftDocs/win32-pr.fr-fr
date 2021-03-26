---
title: dadd (SM5-ASM)
description: Ajout à double précision au niveau du composant.
ms.assetid: 416F1103-E27B-4AFC-9ED1-492FF8A93492
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e217a03a5ba9e4da0d365bbfd15e4283f1a69cb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381134"
---
# <a name="dadd-sm5---asm"></a><span data-ttu-id="811a9-103">dadd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="811a9-103">dadd (sm5 - asm)</span></span>

<span data-ttu-id="811a9-104">Ajout à double précision au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="811a9-104">Component-wise double-precision add.</span></span>



| <span data-ttu-id="811a9-105">dadd \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="811a9-105">dadd\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="811a9-106">Élément</span><span class="sxs-lookup"><span data-stu-id="811a9-106">Item</span></span>                                                            | <span data-ttu-id="811a9-107">Description</span><span class="sxs-lookup"><span data-stu-id="811a9-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="811a9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="811a9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="811a9-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="811a9-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="811a9-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="811a9-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="811a9-111">\[dans \] les composants à ajouter avec *src1*.</span><span class="sxs-lookup"><span data-stu-id="811a9-111">\[in\] The components to add with *src1*.</span></span><br/>          |
| <span data-ttu-id="811a9-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="811a9-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="811a9-113">\[dans \] les composants à ajouter avec *src0*</span><span class="sxs-lookup"><span data-stu-id="811a9-113">\[in\] The components to add with *src0*</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="811a9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="811a9-114">Remarks</span></span>

<span data-ttu-id="811a9-115">Les Swizzles valides pour les paramètres sources sont. XYZW,. Xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="811a9-115">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="811a9-116">Les masques de *dest* valides sont. XY,. ZW et. XYZW.</span><span class="sxs-lookup"><span data-stu-id="811a9-116">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="811a9-117">Les mappages suivants sont postérieurs à Swizzle :</span><span class="sxs-lookup"><span data-stu-id="811a9-117">The following mappings are post-swizzle:</span></span>

-   <span data-ttu-id="811a9-118">*dest* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="811a9-118">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="811a9-119">*src0* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="811a9-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="811a9-120">*src1* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="811a9-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="811a9-121">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="811a9-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="811a9-122">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="811a9-122">F means finite-real number.</span></span>



<table>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="811a9-123"><strong>src0</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-123"><strong>src0</strong></span></span><br /><span data-ttu-id="811a9-124">
<strong>src1-></strong></span><span class="sxs-lookup"><span data-stu-id="811a9-124">
<strong>src1-></strong></span></span><br />
</dl></td>
<td><span data-ttu-id="811a9-125"><strong>-INF</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-125"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="811a9-126"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-126"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="811a9-127"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-127"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="811a9-128"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-128"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="811a9-129"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-129"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="811a9-130"><strong>+ INF</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-130"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="811a9-131"><strong>NaN</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-131"><strong>NaN</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="811a9-132"><strong>-INF</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-132"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="811a9-133">-inf</span><span class="sxs-lookup"><span data-stu-id="811a9-133">-inf</span></span></td>
<td><span data-ttu-id="811a9-134">-inf</span><span class="sxs-lookup"><span data-stu-id="811a9-134">-inf</span></span></td>
<td><span data-ttu-id="811a9-135">-inf</span><span class="sxs-lookup"><span data-stu-id="811a9-135">-inf</span></span></td>
<td><span data-ttu-id="811a9-136">-inf</span><span class="sxs-lookup"><span data-stu-id="811a9-136">-inf</span></span></td>
<td><span data-ttu-id="811a9-137">-inf</span><span class="sxs-lookup"><span data-stu-id="811a9-137">-inf</span></span></td>
<td><span data-ttu-id="811a9-138">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-138">NaN</span></span></td>
<td><span data-ttu-id="811a9-139">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-139">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="811a9-140"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-140"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="811a9-141">-inf</span><span class="sxs-lookup"><span data-stu-id="811a9-141">-inf</span></span></td>
<td><span data-ttu-id="811a9-142">-F</span><span class="sxs-lookup"><span data-stu-id="811a9-142">-F</span></span></td>
<td><span data-ttu-id="811a9-143">src0</span><span class="sxs-lookup"><span data-stu-id="811a9-143">src0</span></span></td>
<td><span data-ttu-id="811a9-144">src0</span><span class="sxs-lookup"><span data-stu-id="811a9-144">src0</span></span></td>
<td><span data-ttu-id="811a9-145">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="811a9-145">+-F or +-0</span></span></td>
<td><span data-ttu-id="811a9-146">+inf</span><span class="sxs-lookup"><span data-stu-id="811a9-146">+inf</span></span></td>
<td><span data-ttu-id="811a9-147">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-147">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="811a9-148"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-148"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="811a9-149">-inf</span><span class="sxs-lookup"><span data-stu-id="811a9-149">-inf</span></span></td>
<td><span data-ttu-id="811a9-150">src1</span><span class="sxs-lookup"><span data-stu-id="811a9-150">src1</span></span></td>
<td><span data-ttu-id="811a9-151">-0</span><span class="sxs-lookup"><span data-stu-id="811a9-151">-0</span></span></td>
<td><span data-ttu-id="811a9-152">+0</span><span class="sxs-lookup"><span data-stu-id="811a9-152">+0</span></span></td>
<td><span data-ttu-id="811a9-153">src1</span><span class="sxs-lookup"><span data-stu-id="811a9-153">src1</span></span></td>
<td><span data-ttu-id="811a9-154">+inf</span><span class="sxs-lookup"><span data-stu-id="811a9-154">+inf</span></span></td>
<td><span data-ttu-id="811a9-155">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-155">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="811a9-156"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-156"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="811a9-157">-inf</span><span class="sxs-lookup"><span data-stu-id="811a9-157">-inf</span></span></td>
<td><span data-ttu-id="811a9-158">src1</span><span class="sxs-lookup"><span data-stu-id="811a9-158">src1</span></span></td>
<td><span data-ttu-id="811a9-159">+0</span><span class="sxs-lookup"><span data-stu-id="811a9-159">+0</span></span></td>
<td><span data-ttu-id="811a9-160">+0</span><span class="sxs-lookup"><span data-stu-id="811a9-160">+0</span></span></td>
<td><span data-ttu-id="811a9-161">src1</span><span class="sxs-lookup"><span data-stu-id="811a9-161">src1</span></span></td>
<td><span data-ttu-id="811a9-162">+inf</span><span class="sxs-lookup"><span data-stu-id="811a9-162">+inf</span></span></td>
<td><span data-ttu-id="811a9-163">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-163">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="811a9-164"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-164"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="811a9-165">-inf</span><span class="sxs-lookup"><span data-stu-id="811a9-165">-inf</span></span></td>
<td><span data-ttu-id="811a9-166">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="811a9-166">+-F or +-0</span></span></td>
<td><span data-ttu-id="811a9-167">src0</span><span class="sxs-lookup"><span data-stu-id="811a9-167">src0</span></span></td>
<td><span data-ttu-id="811a9-168">src0</span><span class="sxs-lookup"><span data-stu-id="811a9-168">src0</span></span></td>
<td><span data-ttu-id="811a9-169">+ F</span><span class="sxs-lookup"><span data-stu-id="811a9-169">+F</span></span></td>
<td><span data-ttu-id="811a9-170">+inf</span><span class="sxs-lookup"><span data-stu-id="811a9-170">+inf</span></span></td>
<td><span data-ttu-id="811a9-171">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-171">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="811a9-172"><strong>+ INF</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-172"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="811a9-173">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-173">NaN</span></span></td>
<td><span data-ttu-id="811a9-174">+inf</span><span class="sxs-lookup"><span data-stu-id="811a9-174">+inf</span></span></td>
<td><span data-ttu-id="811a9-175">+inf</span><span class="sxs-lookup"><span data-stu-id="811a9-175">+inf</span></span></td>
<td><span data-ttu-id="811a9-176">+inf</span><span class="sxs-lookup"><span data-stu-id="811a9-176">+inf</span></span></td>
<td><span data-ttu-id="811a9-177">+inf</span><span class="sxs-lookup"><span data-stu-id="811a9-177">+inf</span></span></td>
<td><span data-ttu-id="811a9-178">+inf</span><span class="sxs-lookup"><span data-stu-id="811a9-178">+inf</span></span></td>
<td><span data-ttu-id="811a9-179">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-179">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="811a9-180"><strong>NaN</strong></span><span class="sxs-lookup"><span data-stu-id="811a9-180"><strong>NaN</strong></span></span></td>
<td><span data-ttu-id="811a9-181">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-181">NaN</span></span></td>
<td><span data-ttu-id="811a9-182">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-182">NaN</span></span></td>
<td><span data-ttu-id="811a9-183">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-183">NaN</span></span></td>
<td><span data-ttu-id="811a9-184">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-184">NaN</span></span></td>
<td><span data-ttu-id="811a9-185">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-185">NaN</span></span></td>
<td><span data-ttu-id="811a9-186">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-186">NaN</span></span></td>
<td><span data-ttu-id="811a9-187">NaN</span><span class="sxs-lookup"><span data-stu-id="811a9-187">NaN</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="811a9-188">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="811a9-188">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="811a9-189">Sommet</span><span class="sxs-lookup"><span data-stu-id="811a9-189">Vertex</span></span> | <span data-ttu-id="811a9-190">Forme</span><span class="sxs-lookup"><span data-stu-id="811a9-190">Hull</span></span> | <span data-ttu-id="811a9-191">Domain</span><span class="sxs-lookup"><span data-stu-id="811a9-191">Domain</span></span> | <span data-ttu-id="811a9-192">Géométrie</span><span class="sxs-lookup"><span data-stu-id="811a9-192">Geometry</span></span> | <span data-ttu-id="811a9-193">Pixel</span><span class="sxs-lookup"><span data-stu-id="811a9-193">Pixel</span></span> | <span data-ttu-id="811a9-194">Compute</span><span class="sxs-lookup"><span data-stu-id="811a9-194">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="811a9-195">X</span><span class="sxs-lookup"><span data-stu-id="811a9-195">X</span></span>      | <span data-ttu-id="811a9-196">X</span><span class="sxs-lookup"><span data-stu-id="811a9-196">X</span></span>    | <span data-ttu-id="811a9-197">X</span><span class="sxs-lookup"><span data-stu-id="811a9-197">X</span></span>      | <span data-ttu-id="811a9-198">X</span><span class="sxs-lookup"><span data-stu-id="811a9-198">X</span></span>        | <span data-ttu-id="811a9-199">X</span><span class="sxs-lookup"><span data-stu-id="811a9-199">X</span></span>     | <span data-ttu-id="811a9-200">X</span><span class="sxs-lookup"><span data-stu-id="811a9-200">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="811a9-201">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="811a9-201">Minimum Shader Model</span></span>

<span data-ttu-id="811a9-202">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="811a9-202">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="811a9-203">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="811a9-203">Shader Model</span></span>                                              | <span data-ttu-id="811a9-204">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="811a9-204">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="811a9-205">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="811a9-205">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="811a9-206">Oui</span><span class="sxs-lookup"><span data-stu-id="811a9-206">yes</span></span>       |
| [<span data-ttu-id="811a9-207">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="811a9-207">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="811a9-208">non</span><span class="sxs-lookup"><span data-stu-id="811a9-208">no</span></span>        |
| [<span data-ttu-id="811a9-209">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="811a9-209">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="811a9-210">non</span><span class="sxs-lookup"><span data-stu-id="811a9-210">no</span></span>        |
| [<span data-ttu-id="811a9-211">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="811a9-211">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="811a9-212">non</span><span class="sxs-lookup"><span data-stu-id="811a9-212">no</span></span>        |
| [<span data-ttu-id="811a9-213">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="811a9-213">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="811a9-214">non</span><span class="sxs-lookup"><span data-stu-id="811a9-214">no</span></span>        |
| [<span data-ttu-id="811a9-215">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="811a9-215">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="811a9-216">non</span><span class="sxs-lookup"><span data-stu-id="811a9-216">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="811a9-217">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="811a9-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="811a9-218">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="811a9-218">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





