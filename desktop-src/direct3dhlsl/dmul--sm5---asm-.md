---
title: dmul (SM5-ASM)
description: Multiplication à double précision au niveau du composant.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5d311cb5c958e8b7403197027c9854d1a93a64
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999086"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="a8dd5-103">dmul (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a8dd5-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="a8dd5-104">Multiplication à double précision au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="a8dd5-105">dmul \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a8dd5-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a8dd5-106">Élément</span><span class="sxs-lookup"><span data-stu-id="a8dd5-106">Item</span></span>                                                            | <span data-ttu-id="a8dd5-107">Description</span><span class="sxs-lookup"><span data-stu-id="a8dd5-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8dd5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a8dd5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a8dd5-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="a8dd5-110">*dest*  =  . *src0* \* *src1*</span><span class="sxs-lookup"><span data-stu-id="a8dd5-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="a8dd5-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a8dd5-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a8dd5-112">\[dans \] les composants à multiplier avec *src1*.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="a8dd5-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a8dd5-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a8dd5-114">\[dans \] les composants à multiplier avec *src0*.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="a8dd5-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="a8dd5-115">Remarks</span></span>

<span data-ttu-id="a8dd5-116">Les Swizzles valides pour les paramètres sources sont. XYZW,. Xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="a8dd5-117">Les masques de *dest* valides sont. XY,. ZW et. XYZW.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="a8dd5-118">Les mappages *src* suivants sont postérieurs à Swizzle :</span><span class="sxs-lookup"><span data-stu-id="a8dd5-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="a8dd5-119">*dest* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="a8dd5-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="a8dd5-120">*src0* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="a8dd5-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="a8dd5-121">*src1* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="a8dd5-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="a8dd5-122">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="a8dd5-123">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-123">F means finite-real number.</span></span>



| <span data-ttu-id="a8dd5-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-124">**src0 src1->**</span></span> | <span data-ttu-id="a8dd5-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-125">**-inf**</span></span> | <span data-ttu-id="a8dd5-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-126">**-F**</span></span> | <span data-ttu-id="a8dd5-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-127">**-1.0**</span></span> | <span data-ttu-id="a8dd5-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-128">**-0**</span></span> | <span data-ttu-id="a8dd5-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-129">**+0**</span></span> | <span data-ttu-id="a8dd5-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-130">**+1.0**</span></span> | <span data-ttu-id="a8dd5-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-131">**+F**</span></span> | <span data-ttu-id="a8dd5-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-132">**+inf**</span></span> | <span data-ttu-id="a8dd5-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-133">**NaN**</span></span> |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="a8dd5-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-134">**-inf**</span></span>           | <span data-ttu-id="a8dd5-135">+inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-135">+inf</span></span>     | <span data-ttu-id="a8dd5-136">+inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-136">+inf</span></span>   | <span data-ttu-id="a8dd5-137">+inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-137">+inf</span></span>     | <span data-ttu-id="a8dd5-138">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-138">NaN</span></span>    | <span data-ttu-id="a8dd5-139">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-139">NaN</span></span>    | <span data-ttu-id="a8dd5-140">-inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-140">-inf</span></span>     | <span data-ttu-id="a8dd5-141">-inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-141">-inf</span></span>   | <span data-ttu-id="a8dd5-142">-inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-142">-inf</span></span>     | <span data-ttu-id="a8dd5-143">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-143">NaN</span></span>     |
| <span data-ttu-id="a8dd5-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-144">**-F**</span></span>             | <span data-ttu-id="a8dd5-145">+inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-145">+inf</span></span>     | <span data-ttu-id="a8dd5-146">+ F</span><span class="sxs-lookup"><span data-stu-id="a8dd5-146">+F</span></span>     | <span data-ttu-id="a8dd5-147">-src0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-147">-src0</span></span>    | <span data-ttu-id="a8dd5-148">+0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-148">+0</span></span>     | <span data-ttu-id="a8dd5-149">-0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-149">-0</span></span>     | <span data-ttu-id="a8dd5-150">src0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-150">src0</span></span>     | <span data-ttu-id="a8dd5-151">-F</span><span class="sxs-lookup"><span data-stu-id="a8dd5-151">-F</span></span>     | <span data-ttu-id="a8dd5-152">-inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-152">-inf</span></span>     | <span data-ttu-id="a8dd5-153">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-153">NaN</span></span>     |
| <span data-ttu-id="a8dd5-154">**-1.0 f**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-154">**-1.0F**</span></span>          | <span data-ttu-id="a8dd5-155">+inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-155">+inf</span></span>     | <span data-ttu-id="a8dd5-156">-src1</span><span class="sxs-lookup"><span data-stu-id="a8dd5-156">-src1</span></span>  | <span data-ttu-id="a8dd5-157">+ 1,0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-157">+1.0</span></span>     | <span data-ttu-id="a8dd5-158">+0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-158">+0</span></span>     | <span data-ttu-id="a8dd5-159">-0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-159">-0</span></span>     | <span data-ttu-id="a8dd5-160">-1.0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-160">-1.0</span></span>     | <span data-ttu-id="a8dd5-161">-src1</span><span class="sxs-lookup"><span data-stu-id="a8dd5-161">-src1</span></span>  | <span data-ttu-id="a8dd5-162">-inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-162">-inf</span></span>     | <span data-ttu-id="a8dd5-163">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-163">NaN</span></span>     |
| <span data-ttu-id="a8dd5-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-164">**-0**</span></span>             | <span data-ttu-id="a8dd5-165">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-165">NaN</span></span>      | <span data-ttu-id="a8dd5-166">+0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-166">+0</span></span>     | <span data-ttu-id="a8dd5-167">+0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-167">+0</span></span>       | <span data-ttu-id="a8dd5-168">+0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-168">+0</span></span>     | <span data-ttu-id="a8dd5-169">-0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-169">-0</span></span>     | <span data-ttu-id="a8dd5-170">-0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-170">-0</span></span>       | <span data-ttu-id="a8dd5-171">-0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-171">-0</span></span>     | <span data-ttu-id="a8dd5-172">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-172">NaN</span></span>      | <span data-ttu-id="a8dd5-173">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-173">NaN</span></span>     |
| <span data-ttu-id="a8dd5-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-174">**+0**</span></span>             | <span data-ttu-id="a8dd5-175">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-175">NaN</span></span>      | <span data-ttu-id="a8dd5-176">-0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-176">-0</span></span>     | <span data-ttu-id="a8dd5-177">-0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-177">-0</span></span>       | <span data-ttu-id="a8dd5-178">-0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-178">-0</span></span>     | <span data-ttu-id="a8dd5-179">+0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-179">+0</span></span>     | <span data-ttu-id="a8dd5-180">+0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-180">+0</span></span>       | <span data-ttu-id="a8dd5-181">+0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-181">+0</span></span>     | <span data-ttu-id="a8dd5-182">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-182">NaN</span></span>      | <span data-ttu-id="a8dd5-183">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-183">NaN</span></span>     |
| <span data-ttu-id="a8dd5-184">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-184">**+1.0**</span></span>           | <span data-ttu-id="a8dd5-185">-inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-185">-inf</span></span>     | <span data-ttu-id="a8dd5-186">src1</span><span class="sxs-lookup"><span data-stu-id="a8dd5-186">src1</span></span>   | <span data-ttu-id="a8dd5-187">-1.0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-187">-1.0</span></span>     | <span data-ttu-id="a8dd5-188">-0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-188">-0</span></span>     | <span data-ttu-id="a8dd5-189">+0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-189">+0</span></span>     | <span data-ttu-id="a8dd5-190">+1</span><span class="sxs-lookup"><span data-stu-id="a8dd5-190">+1</span></span>       | <span data-ttu-id="a8dd5-191">src1</span><span class="sxs-lookup"><span data-stu-id="a8dd5-191">src1</span></span>   | <span data-ttu-id="a8dd5-192">+inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-192">+inf</span></span>     | <span data-ttu-id="a8dd5-193">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-193">NaN</span></span>     |
| <span data-ttu-id="a8dd5-194">**+ F**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-194">**+F**</span></span>             | <span data-ttu-id="a8dd5-195">-inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-195">-inf</span></span>     | <span data-ttu-id="a8dd5-196">-F</span><span class="sxs-lookup"><span data-stu-id="a8dd5-196">-F</span></span>     | <span data-ttu-id="a8dd5-197">-src0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-197">-src0</span></span>    | <span data-ttu-id="a8dd5-198">-0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-198">-0</span></span>     | <span data-ttu-id="a8dd5-199">+0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-199">+0</span></span>     | <span data-ttu-id="a8dd5-200">src0</span><span class="sxs-lookup"><span data-stu-id="a8dd5-200">src0</span></span>     | <span data-ttu-id="a8dd5-201">+ F</span><span class="sxs-lookup"><span data-stu-id="a8dd5-201">+F</span></span>     | <span data-ttu-id="a8dd5-202">+inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-202">+inf</span></span>     | <span data-ttu-id="a8dd5-203">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-203">NaN</span></span>     |
| <span data-ttu-id="a8dd5-204">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-204">**+inf**</span></span>           | <span data-ttu-id="a8dd5-205">-inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-205">-inf</span></span>     | <span data-ttu-id="a8dd5-206">-inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-206">-inf</span></span>   | <span data-ttu-id="a8dd5-207">-inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-207">-inf</span></span>     | <span data-ttu-id="a8dd5-208">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-208">NaN</span></span>    | <span data-ttu-id="a8dd5-209">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-209">NaN</span></span>    | <span data-ttu-id="a8dd5-210">+inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-210">+inf</span></span>     | <span data-ttu-id="a8dd5-211">+inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-211">+inf</span></span>   | <span data-ttu-id="a8dd5-212">+inf</span><span class="sxs-lookup"><span data-stu-id="a8dd5-212">+inf</span></span>     | <span data-ttu-id="a8dd5-213">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-213">NaN</span></span>     |
| <span data-ttu-id="a8dd5-214">**NaN**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-214">**NaN**</span></span>            | <span data-ttu-id="a8dd5-215">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-215">NaN</span></span>      | <span data-ttu-id="a8dd5-216">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-216">NaN</span></span>    | <span data-ttu-id="a8dd5-217">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-217">NaN</span></span>      | <span data-ttu-id="a8dd5-218">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-218">NaN</span></span>    | <span data-ttu-id="a8dd5-219">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-219">NaN</span></span>    | <span data-ttu-id="a8dd5-220">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-220">NaN</span></span>      | <span data-ttu-id="a8dd5-221">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-221">NaN</span></span>    | <span data-ttu-id="a8dd5-222">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-222">NaN</span></span>      | <span data-ttu-id="a8dd5-223">NaN</span><span class="sxs-lookup"><span data-stu-id="a8dd5-223">NaN</span></span>     |



 

<span data-ttu-id="a8dd5-224">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="a8dd5-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a8dd5-225">Sommet</span><span class="sxs-lookup"><span data-stu-id="a8dd5-225">Vertex</span></span> | <span data-ttu-id="a8dd5-226">Forme</span><span class="sxs-lookup"><span data-stu-id="a8dd5-226">Hull</span></span> | <span data-ttu-id="a8dd5-227">Domain</span><span class="sxs-lookup"><span data-stu-id="a8dd5-227">Domain</span></span> | <span data-ttu-id="a8dd5-228">Géométrie</span><span class="sxs-lookup"><span data-stu-id="a8dd5-228">Geometry</span></span> | <span data-ttu-id="a8dd5-229">Pixel</span><span class="sxs-lookup"><span data-stu-id="a8dd5-229">Pixel</span></span> | <span data-ttu-id="a8dd5-230">Calcul</span><span class="sxs-lookup"><span data-stu-id="a8dd5-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a8dd5-231">X</span><span class="sxs-lookup"><span data-stu-id="a8dd5-231">X</span></span>      | <span data-ttu-id="a8dd5-232">X</span><span class="sxs-lookup"><span data-stu-id="a8dd5-232">X</span></span>    | <span data-ttu-id="a8dd5-233">X</span><span class="sxs-lookup"><span data-stu-id="a8dd5-233">X</span></span>      | <span data-ttu-id="a8dd5-234">X</span><span class="sxs-lookup"><span data-stu-id="a8dd5-234">X</span></span>        | <span data-ttu-id="a8dd5-235">X</span><span class="sxs-lookup"><span data-stu-id="a8dd5-235">X</span></span>     | <span data-ttu-id="a8dd5-236">X</span><span class="sxs-lookup"><span data-stu-id="a8dd5-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a8dd5-237">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="a8dd5-237">Minimum Shader Model</span></span>

<span data-ttu-id="a8dd5-238">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="a8dd5-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a8dd5-239">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a8dd5-239">Shader Model</span></span>                                              | <span data-ttu-id="a8dd5-240">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8dd5-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a8dd5-241">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="a8dd5-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a8dd5-242">oui</span><span class="sxs-lookup"><span data-stu-id="a8dd5-242">yes</span></span>       |
| [<span data-ttu-id="a8dd5-243">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="a8dd5-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a8dd5-244">non</span><span class="sxs-lookup"><span data-stu-id="a8dd5-244">no</span></span>        |
| [<span data-ttu-id="a8dd5-245">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="a8dd5-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a8dd5-246">non</span><span class="sxs-lookup"><span data-stu-id="a8dd5-246">no</span></span>        |
| [<span data-ttu-id="a8dd5-247">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8dd5-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a8dd5-248">non</span><span class="sxs-lookup"><span data-stu-id="a8dd5-248">no</span></span>        |
| [<span data-ttu-id="a8dd5-249">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8dd5-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a8dd5-250">non</span><span class="sxs-lookup"><span data-stu-id="a8dd5-250">no</span></span>        |
| [<span data-ttu-id="a8dd5-251">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8dd5-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a8dd5-252">non</span><span class="sxs-lookup"><span data-stu-id="a8dd5-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a8dd5-253">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8dd5-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8dd5-254">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8dd5-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





