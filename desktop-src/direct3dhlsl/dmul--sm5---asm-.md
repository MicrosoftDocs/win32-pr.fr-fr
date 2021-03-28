---
title: dmul (SM5-ASM)
description: Multiplication à double précision au niveau du composant.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18cce59ae237610b1038d90e02dff429812b4f00
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990749"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="186f6-103">dmul (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="186f6-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="186f6-104">Multiplication à double précision au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="186f6-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="186f6-105">dmul \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="186f6-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="186f6-106">Élément</span><span class="sxs-lookup"><span data-stu-id="186f6-106">Item</span></span>                                                            | <span data-ttu-id="186f6-107">Description</span><span class="sxs-lookup"><span data-stu-id="186f6-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186f6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="186f6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="186f6-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="186f6-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="186f6-110">*dest*  =  . *src0* \* *src1*</span><span class="sxs-lookup"><span data-stu-id="186f6-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="186f6-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="186f6-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="186f6-112">\[dans \] les composants à multiplier avec *src1*.</span><span class="sxs-lookup"><span data-stu-id="186f6-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="186f6-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="186f6-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="186f6-114">\[dans \] les composants à multiplier avec *src0*.</span><span class="sxs-lookup"><span data-stu-id="186f6-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="186f6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="186f6-115">Remarks</span></span>

<span data-ttu-id="186f6-116">Les Swizzles valides pour les paramètres sources sont. XYZW,. Xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="186f6-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="186f6-117">Les masques de *dest* valides sont. XY,. ZW et. XYZW.</span><span class="sxs-lookup"><span data-stu-id="186f6-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="186f6-118">Les mappages *src* suivants sont postérieurs à Swizzle :</span><span class="sxs-lookup"><span data-stu-id="186f6-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="186f6-119">*dest* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="186f6-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="186f6-120">*src0* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="186f6-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="186f6-121">*src1* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="186f6-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="186f6-122">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="186f6-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="186f6-123">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="186f6-123">F means finite-real number.</span></span>



|                    |          |        |          |        |        |          |        |          |         |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="186f6-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="186f6-124">**src0 src1->**</span></span> | <span data-ttu-id="186f6-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="186f6-125">**-inf**</span></span> | <span data-ttu-id="186f6-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="186f6-126">**-F**</span></span> | <span data-ttu-id="186f6-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="186f6-127">**-1.0**</span></span> | <span data-ttu-id="186f6-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="186f6-128">**-0**</span></span> | <span data-ttu-id="186f6-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="186f6-129">**+0**</span></span> | <span data-ttu-id="186f6-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="186f6-130">**+1.0**</span></span> | <span data-ttu-id="186f6-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="186f6-131">**+F**</span></span> | <span data-ttu-id="186f6-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="186f6-132">**+inf**</span></span> | <span data-ttu-id="186f6-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="186f6-133">**NaN**</span></span> |
| <span data-ttu-id="186f6-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="186f6-134">**-inf**</span></span>           | <span data-ttu-id="186f6-135">+inf</span><span class="sxs-lookup"><span data-stu-id="186f6-135">+inf</span></span>     | <span data-ttu-id="186f6-136">+inf</span><span class="sxs-lookup"><span data-stu-id="186f6-136">+inf</span></span>   | <span data-ttu-id="186f6-137">+inf</span><span class="sxs-lookup"><span data-stu-id="186f6-137">+inf</span></span>     | <span data-ttu-id="186f6-138">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-138">NaN</span></span>    | <span data-ttu-id="186f6-139">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-139">NaN</span></span>    | <span data-ttu-id="186f6-140">-inf</span><span class="sxs-lookup"><span data-stu-id="186f6-140">-inf</span></span>     | <span data-ttu-id="186f6-141">-inf</span><span class="sxs-lookup"><span data-stu-id="186f6-141">-inf</span></span>   | <span data-ttu-id="186f6-142">-inf</span><span class="sxs-lookup"><span data-stu-id="186f6-142">-inf</span></span>     | <span data-ttu-id="186f6-143">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-143">NaN</span></span>     |
| <span data-ttu-id="186f6-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="186f6-144">**-F**</span></span>             | <span data-ttu-id="186f6-145">+inf</span><span class="sxs-lookup"><span data-stu-id="186f6-145">+inf</span></span>     | <span data-ttu-id="186f6-146">+ F</span><span class="sxs-lookup"><span data-stu-id="186f6-146">+F</span></span>     | <span data-ttu-id="186f6-147">-src0</span><span class="sxs-lookup"><span data-stu-id="186f6-147">-src0</span></span>    | <span data-ttu-id="186f6-148">+0</span><span class="sxs-lookup"><span data-stu-id="186f6-148">+0</span></span>     | <span data-ttu-id="186f6-149">-0</span><span class="sxs-lookup"><span data-stu-id="186f6-149">-0</span></span>     | <span data-ttu-id="186f6-150">src0</span><span class="sxs-lookup"><span data-stu-id="186f6-150">src0</span></span>     | <span data-ttu-id="186f6-151">-F</span><span class="sxs-lookup"><span data-stu-id="186f6-151">-F</span></span>     | <span data-ttu-id="186f6-152">-inf</span><span class="sxs-lookup"><span data-stu-id="186f6-152">-inf</span></span>     | <span data-ttu-id="186f6-153">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-153">NaN</span></span>     |
| <span data-ttu-id="186f6-154">**-1.0 f**</span><span class="sxs-lookup"><span data-stu-id="186f6-154">**-1.0F**</span></span>          | <span data-ttu-id="186f6-155">+inf</span><span class="sxs-lookup"><span data-stu-id="186f6-155">+inf</span></span>     | <span data-ttu-id="186f6-156">-src1</span><span class="sxs-lookup"><span data-stu-id="186f6-156">-src1</span></span>  | <span data-ttu-id="186f6-157">+ 1,0</span><span class="sxs-lookup"><span data-stu-id="186f6-157">+1.0</span></span>     | <span data-ttu-id="186f6-158">+0</span><span class="sxs-lookup"><span data-stu-id="186f6-158">+0</span></span>     | <span data-ttu-id="186f6-159">-0</span><span class="sxs-lookup"><span data-stu-id="186f6-159">-0</span></span>     | <span data-ttu-id="186f6-160">-1.0</span><span class="sxs-lookup"><span data-stu-id="186f6-160">-1.0</span></span>     | <span data-ttu-id="186f6-161">-src1</span><span class="sxs-lookup"><span data-stu-id="186f6-161">-src1</span></span>  | <span data-ttu-id="186f6-162">-inf</span><span class="sxs-lookup"><span data-stu-id="186f6-162">-inf</span></span>     | <span data-ttu-id="186f6-163">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-163">NaN</span></span>     |
| <span data-ttu-id="186f6-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="186f6-164">**-0**</span></span>             | <span data-ttu-id="186f6-165">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-165">NaN</span></span>      | <span data-ttu-id="186f6-166">+0</span><span class="sxs-lookup"><span data-stu-id="186f6-166">+0</span></span>     | <span data-ttu-id="186f6-167">+0</span><span class="sxs-lookup"><span data-stu-id="186f6-167">+0</span></span>       | <span data-ttu-id="186f6-168">+0</span><span class="sxs-lookup"><span data-stu-id="186f6-168">+0</span></span>     | <span data-ttu-id="186f6-169">-0</span><span class="sxs-lookup"><span data-stu-id="186f6-169">-0</span></span>     | <span data-ttu-id="186f6-170">-0</span><span class="sxs-lookup"><span data-stu-id="186f6-170">-0</span></span>       | <span data-ttu-id="186f6-171">-0</span><span class="sxs-lookup"><span data-stu-id="186f6-171">-0</span></span>     | <span data-ttu-id="186f6-172">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-172">NaN</span></span>      | <span data-ttu-id="186f6-173">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-173">NaN</span></span>     |
| <span data-ttu-id="186f6-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="186f6-174">**+0**</span></span>             | <span data-ttu-id="186f6-175">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-175">NaN</span></span>      | <span data-ttu-id="186f6-176">-0</span><span class="sxs-lookup"><span data-stu-id="186f6-176">-0</span></span>     | <span data-ttu-id="186f6-177">-0</span><span class="sxs-lookup"><span data-stu-id="186f6-177">-0</span></span>       | <span data-ttu-id="186f6-178">-0</span><span class="sxs-lookup"><span data-stu-id="186f6-178">-0</span></span>     | <span data-ttu-id="186f6-179">+0</span><span class="sxs-lookup"><span data-stu-id="186f6-179">+0</span></span>     | <span data-ttu-id="186f6-180">+0</span><span class="sxs-lookup"><span data-stu-id="186f6-180">+0</span></span>       | <span data-ttu-id="186f6-181">+0</span><span class="sxs-lookup"><span data-stu-id="186f6-181">+0</span></span>     | <span data-ttu-id="186f6-182">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-182">NaN</span></span>      | <span data-ttu-id="186f6-183">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-183">NaN</span></span>     |
| <span data-ttu-id="186f6-184">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="186f6-184">**+1.0**</span></span>           | <span data-ttu-id="186f6-185">-inf</span><span class="sxs-lookup"><span data-stu-id="186f6-185">-inf</span></span>     | <span data-ttu-id="186f6-186">src1</span><span class="sxs-lookup"><span data-stu-id="186f6-186">src1</span></span>   | <span data-ttu-id="186f6-187">-1.0</span><span class="sxs-lookup"><span data-stu-id="186f6-187">-1.0</span></span>     | <span data-ttu-id="186f6-188">-0</span><span class="sxs-lookup"><span data-stu-id="186f6-188">-0</span></span>     | <span data-ttu-id="186f6-189">+0</span><span class="sxs-lookup"><span data-stu-id="186f6-189">+0</span></span>     | <span data-ttu-id="186f6-190">+1</span><span class="sxs-lookup"><span data-stu-id="186f6-190">+1</span></span>       | <span data-ttu-id="186f6-191">src1</span><span class="sxs-lookup"><span data-stu-id="186f6-191">src1</span></span>   | <span data-ttu-id="186f6-192">+inf</span><span class="sxs-lookup"><span data-stu-id="186f6-192">+inf</span></span>     | <span data-ttu-id="186f6-193">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-193">NaN</span></span>     |
| <span data-ttu-id="186f6-194">**+ F**</span><span class="sxs-lookup"><span data-stu-id="186f6-194">**+F**</span></span>             | <span data-ttu-id="186f6-195">-inf</span><span class="sxs-lookup"><span data-stu-id="186f6-195">-inf</span></span>     | <span data-ttu-id="186f6-196">-F</span><span class="sxs-lookup"><span data-stu-id="186f6-196">-F</span></span>     | <span data-ttu-id="186f6-197">-src0</span><span class="sxs-lookup"><span data-stu-id="186f6-197">-src0</span></span>    | <span data-ttu-id="186f6-198">-0</span><span class="sxs-lookup"><span data-stu-id="186f6-198">-0</span></span>     | <span data-ttu-id="186f6-199">+0</span><span class="sxs-lookup"><span data-stu-id="186f6-199">+0</span></span>     | <span data-ttu-id="186f6-200">src0</span><span class="sxs-lookup"><span data-stu-id="186f6-200">src0</span></span>     | <span data-ttu-id="186f6-201">+ F</span><span class="sxs-lookup"><span data-stu-id="186f6-201">+F</span></span>     | <span data-ttu-id="186f6-202">+inf</span><span class="sxs-lookup"><span data-stu-id="186f6-202">+inf</span></span>     | <span data-ttu-id="186f6-203">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-203">NaN</span></span>     |
| <span data-ttu-id="186f6-204">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="186f6-204">**+inf**</span></span>           | <span data-ttu-id="186f6-205">-inf</span><span class="sxs-lookup"><span data-stu-id="186f6-205">-inf</span></span>     | <span data-ttu-id="186f6-206">-inf</span><span class="sxs-lookup"><span data-stu-id="186f6-206">-inf</span></span>   | <span data-ttu-id="186f6-207">-inf</span><span class="sxs-lookup"><span data-stu-id="186f6-207">-inf</span></span>     | <span data-ttu-id="186f6-208">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-208">NaN</span></span>    | <span data-ttu-id="186f6-209">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-209">NaN</span></span>    | <span data-ttu-id="186f6-210">+inf</span><span class="sxs-lookup"><span data-stu-id="186f6-210">+inf</span></span>     | <span data-ttu-id="186f6-211">+inf</span><span class="sxs-lookup"><span data-stu-id="186f6-211">+inf</span></span>   | <span data-ttu-id="186f6-212">+inf</span><span class="sxs-lookup"><span data-stu-id="186f6-212">+inf</span></span>     | <span data-ttu-id="186f6-213">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-213">NaN</span></span>     |
| <span data-ttu-id="186f6-214">**NaN**</span><span class="sxs-lookup"><span data-stu-id="186f6-214">**NaN**</span></span>            | <span data-ttu-id="186f6-215">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-215">NaN</span></span>      | <span data-ttu-id="186f6-216">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-216">NaN</span></span>    | <span data-ttu-id="186f6-217">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-217">NaN</span></span>      | <span data-ttu-id="186f6-218">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-218">NaN</span></span>    | <span data-ttu-id="186f6-219">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-219">NaN</span></span>    | <span data-ttu-id="186f6-220">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-220">NaN</span></span>      | <span data-ttu-id="186f6-221">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-221">NaN</span></span>    | <span data-ttu-id="186f6-222">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-222">NaN</span></span>      | <span data-ttu-id="186f6-223">NaN</span><span class="sxs-lookup"><span data-stu-id="186f6-223">NaN</span></span>     |



 

<span data-ttu-id="186f6-224">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="186f6-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="186f6-225">Sommet</span><span class="sxs-lookup"><span data-stu-id="186f6-225">Vertex</span></span> | <span data-ttu-id="186f6-226">Forme</span><span class="sxs-lookup"><span data-stu-id="186f6-226">Hull</span></span> | <span data-ttu-id="186f6-227">Domain</span><span class="sxs-lookup"><span data-stu-id="186f6-227">Domain</span></span> | <span data-ttu-id="186f6-228">Géométrie</span><span class="sxs-lookup"><span data-stu-id="186f6-228">Geometry</span></span> | <span data-ttu-id="186f6-229">Pixel</span><span class="sxs-lookup"><span data-stu-id="186f6-229">Pixel</span></span> | <span data-ttu-id="186f6-230">Compute</span><span class="sxs-lookup"><span data-stu-id="186f6-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="186f6-231">X</span><span class="sxs-lookup"><span data-stu-id="186f6-231">X</span></span>      | <span data-ttu-id="186f6-232">X</span><span class="sxs-lookup"><span data-stu-id="186f6-232">X</span></span>    | <span data-ttu-id="186f6-233">X</span><span class="sxs-lookup"><span data-stu-id="186f6-233">X</span></span>      | <span data-ttu-id="186f6-234">X</span><span class="sxs-lookup"><span data-stu-id="186f6-234">X</span></span>        | <span data-ttu-id="186f6-235">X</span><span class="sxs-lookup"><span data-stu-id="186f6-235">X</span></span>     | <span data-ttu-id="186f6-236">X</span><span class="sxs-lookup"><span data-stu-id="186f6-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="186f6-237">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="186f6-237">Minimum Shader Model</span></span>

<span data-ttu-id="186f6-238">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="186f6-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="186f6-239">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="186f6-239">Shader Model</span></span>                                              | <span data-ttu-id="186f6-240">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="186f6-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="186f6-241">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="186f6-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="186f6-242">Oui</span><span class="sxs-lookup"><span data-stu-id="186f6-242">yes</span></span>       |
| [<span data-ttu-id="186f6-243">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="186f6-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="186f6-244">non</span><span class="sxs-lookup"><span data-stu-id="186f6-244">no</span></span>        |
| [<span data-ttu-id="186f6-245">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="186f6-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="186f6-246">non</span><span class="sxs-lookup"><span data-stu-id="186f6-246">no</span></span>        |
| [<span data-ttu-id="186f6-247">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="186f6-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="186f6-248">non</span><span class="sxs-lookup"><span data-stu-id="186f6-248">no</span></span>        |
| [<span data-ttu-id="186f6-249">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="186f6-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="186f6-250">non</span><span class="sxs-lookup"><span data-stu-id="186f6-250">no</span></span>        |
| [<span data-ttu-id="186f6-251">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="186f6-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="186f6-252">non</span><span class="sxs-lookup"><span data-stu-id="186f6-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="186f6-253">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="186f6-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="186f6-254">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="186f6-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





