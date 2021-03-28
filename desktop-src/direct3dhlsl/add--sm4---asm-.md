---
title: Add (SM4-ASM)
description: Ajout de 2 vecteurs au niveau du composant.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5630b983c88da3ba512b5fece6202e0217b2ed39
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507727"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="72e04-103">Add (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="72e04-103">add (sm4 - asm)</span></span>

<span data-ttu-id="72e04-104">Ajout de 2 vecteurs au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="72e04-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="72e04-105">Ajoutez \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="72e04-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="72e04-106">Élément</span><span class="sxs-lookup"><span data-stu-id="72e04-106">Item</span></span>                                                            | <span data-ttu-id="72e04-107">Description</span><span class="sxs-lookup"><span data-stu-id="72e04-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="72e04-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="72e04-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="72e04-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="72e04-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="72e04-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="72e04-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="72e04-111">\[dans \] le vecteur à ajouter à *src1*.</span><span class="sxs-lookup"><span data-stu-id="72e04-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="72e04-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="72e04-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="72e04-113">\[dans \] le vecteur à ajouter à *src0*.</span><span class="sxs-lookup"><span data-stu-id="72e04-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="72e04-114">Notes</span><span class="sxs-lookup"><span data-stu-id="72e04-114">Remarks</span></span>

<span data-ttu-id="72e04-115">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="72e04-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="72e04-116">F signifie nombre réel fini.</span><span class="sxs-lookup"><span data-stu-id="72e04-116">F means finite real number.</span></span>



|                    |          |            |             |        |        |            |            |          |         |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="72e04-117">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="72e04-117">**src0 src1->**</span></span> | <span data-ttu-id="72e04-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="72e04-118">**-inf**</span></span> | <span data-ttu-id="72e04-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="72e04-119">**-F**</span></span>     | <span data-ttu-id="72e04-120">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="72e04-120">**-denorm**</span></span> | <span data-ttu-id="72e04-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="72e04-121">**-0**</span></span> | <span data-ttu-id="72e04-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="72e04-122">**+0**</span></span> | <span data-ttu-id="72e04-123">**dénorme**</span><span class="sxs-lookup"><span data-stu-id="72e04-123">**denorm**</span></span> | <span data-ttu-id="72e04-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="72e04-124">**+F**</span></span>     | <span data-ttu-id="72e04-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="72e04-125">**+inf**</span></span> | <span data-ttu-id="72e04-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="72e04-126">**NaN**</span></span> |
| <span data-ttu-id="72e04-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="72e04-127">**-inf**</span></span>           | <span data-ttu-id="72e04-128">-inf</span><span class="sxs-lookup"><span data-stu-id="72e04-128">-inf</span></span>     | <span data-ttu-id="72e04-129">-inf</span><span class="sxs-lookup"><span data-stu-id="72e04-129">-inf</span></span>       | <span data-ttu-id="72e04-130">-inf</span><span class="sxs-lookup"><span data-stu-id="72e04-130">-inf</span></span>        | <span data-ttu-id="72e04-131">-inf</span><span class="sxs-lookup"><span data-stu-id="72e04-131">-inf</span></span>   | <span data-ttu-id="72e04-132">-inf</span><span class="sxs-lookup"><span data-stu-id="72e04-132">-inf</span></span>   | <span data-ttu-id="72e04-133">-inf</span><span class="sxs-lookup"><span data-stu-id="72e04-133">-inf</span></span>       | <span data-ttu-id="72e04-134">-inf</span><span class="sxs-lookup"><span data-stu-id="72e04-134">-inf</span></span>       | <span data-ttu-id="72e04-135">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-135">NaN</span></span>      | <span data-ttu-id="72e04-136">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-136">NaN</span></span>     |
| <span data-ttu-id="72e04-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="72e04-137">**-F**</span></span>             | <span data-ttu-id="72e04-138">-inf</span><span class="sxs-lookup"><span data-stu-id="72e04-138">-inf</span></span>     | <span data-ttu-id="72e04-139">-F</span><span class="sxs-lookup"><span data-stu-id="72e04-139">-F</span></span>         | <span data-ttu-id="72e04-140">src0</span><span class="sxs-lookup"><span data-stu-id="72e04-140">src0</span></span>        | <span data-ttu-id="72e04-141">src0</span><span class="sxs-lookup"><span data-stu-id="72e04-141">src0</span></span>   | <span data-ttu-id="72e04-142">src0</span><span class="sxs-lookup"><span data-stu-id="72e04-142">src0</span></span>   | <span data-ttu-id="72e04-143">src0</span><span class="sxs-lookup"><span data-stu-id="72e04-143">src0</span></span>       | <span data-ttu-id="72e04-144">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="72e04-144">+-F or +-0</span></span> | <span data-ttu-id="72e04-145">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-145">+inf</span></span>     | <span data-ttu-id="72e04-146">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-146">NaN</span></span>     |
| <span data-ttu-id="72e04-147">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="72e04-147">**-denorm**</span></span>        | <span data-ttu-id="72e04-148">-inf</span><span class="sxs-lookup"><span data-stu-id="72e04-148">-inf</span></span>     | <span data-ttu-id="72e04-149">src1</span><span class="sxs-lookup"><span data-stu-id="72e04-149">src1</span></span>       | <span data-ttu-id="72e04-150">-0</span><span class="sxs-lookup"><span data-stu-id="72e04-150">-0</span></span>          | <span data-ttu-id="72e04-151">-0</span><span class="sxs-lookup"><span data-stu-id="72e04-151">-0</span></span>     | <span data-ttu-id="72e04-152">+0</span><span class="sxs-lookup"><span data-stu-id="72e04-152">+0</span></span>     | <span data-ttu-id="72e04-153">+0</span><span class="sxs-lookup"><span data-stu-id="72e04-153">+0</span></span>         | <span data-ttu-id="72e04-154">src1</span><span class="sxs-lookup"><span data-stu-id="72e04-154">src1</span></span>       | <span data-ttu-id="72e04-155">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-155">+inf</span></span>     | <span data-ttu-id="72e04-156">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-156">NaN</span></span>     |
| <span data-ttu-id="72e04-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="72e04-157">**-0**</span></span>             | <span data-ttu-id="72e04-158">-inf</span><span class="sxs-lookup"><span data-stu-id="72e04-158">-inf</span></span>     | <span data-ttu-id="72e04-159">src1</span><span class="sxs-lookup"><span data-stu-id="72e04-159">src1</span></span>       | <span data-ttu-id="72e04-160">-0</span><span class="sxs-lookup"><span data-stu-id="72e04-160">-0</span></span>          | <span data-ttu-id="72e04-161">-0</span><span class="sxs-lookup"><span data-stu-id="72e04-161">-0</span></span>     | <span data-ttu-id="72e04-162">+0</span><span class="sxs-lookup"><span data-stu-id="72e04-162">+0</span></span>     | <span data-ttu-id="72e04-163">+0</span><span class="sxs-lookup"><span data-stu-id="72e04-163">+0</span></span>         | <span data-ttu-id="72e04-164">src1</span><span class="sxs-lookup"><span data-stu-id="72e04-164">src1</span></span>       | <span data-ttu-id="72e04-165">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-165">+inf</span></span>     | <span data-ttu-id="72e04-166">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-166">NaN</span></span>     |
| <span data-ttu-id="72e04-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="72e04-167">**+0**</span></span>             | <span data-ttu-id="72e04-168">i-INF</span><span class="sxs-lookup"><span data-stu-id="72e04-168">i-inf</span></span>    | <span data-ttu-id="72e04-169">src1</span><span class="sxs-lookup"><span data-stu-id="72e04-169">src1</span></span>       | <span data-ttu-id="72e04-170">+0</span><span class="sxs-lookup"><span data-stu-id="72e04-170">+0</span></span>          | <span data-ttu-id="72e04-171">+0</span><span class="sxs-lookup"><span data-stu-id="72e04-171">+0</span></span>     | <span data-ttu-id="72e04-172">+0</span><span class="sxs-lookup"><span data-stu-id="72e04-172">+0</span></span>     | <span data-ttu-id="72e04-173">+0</span><span class="sxs-lookup"><span data-stu-id="72e04-173">+0</span></span>         | <span data-ttu-id="72e04-174">src1</span><span class="sxs-lookup"><span data-stu-id="72e04-174">src1</span></span>       | <span data-ttu-id="72e04-175">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-175">+inf</span></span>     | <span data-ttu-id="72e04-176">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-176">NaN</span></span>     |
| <span data-ttu-id="72e04-177">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="72e04-177">**+denorm**</span></span>        | <span data-ttu-id="72e04-178">-inf</span><span class="sxs-lookup"><span data-stu-id="72e04-178">-inf</span></span>     | <span data-ttu-id="72e04-179">src1</span><span class="sxs-lookup"><span data-stu-id="72e04-179">src1</span></span>       | <span data-ttu-id="72e04-180">+0</span><span class="sxs-lookup"><span data-stu-id="72e04-180">+0</span></span>          | <span data-ttu-id="72e04-181">+0</span><span class="sxs-lookup"><span data-stu-id="72e04-181">+0</span></span>     | <span data-ttu-id="72e04-182">+0</span><span class="sxs-lookup"><span data-stu-id="72e04-182">+0</span></span>     | <span data-ttu-id="72e04-183">+0</span><span class="sxs-lookup"><span data-stu-id="72e04-183">+0</span></span>         | <span data-ttu-id="72e04-184">src1</span><span class="sxs-lookup"><span data-stu-id="72e04-184">src1</span></span>       | <span data-ttu-id="72e04-185">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-185">+inf</span></span>     | <span data-ttu-id="72e04-186">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-186">NaN</span></span>     |
| <span data-ttu-id="72e04-187">**+ F**</span><span class="sxs-lookup"><span data-stu-id="72e04-187">**+F**</span></span>             | <span data-ttu-id="72e04-188">-inf</span><span class="sxs-lookup"><span data-stu-id="72e04-188">-inf</span></span>     | <span data-ttu-id="72e04-189">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="72e04-189">+-F or +-0</span></span> | <span data-ttu-id="72e04-190">src0</span><span class="sxs-lookup"><span data-stu-id="72e04-190">src0</span></span>        | <span data-ttu-id="72e04-191">src0</span><span class="sxs-lookup"><span data-stu-id="72e04-191">src0</span></span>   | <span data-ttu-id="72e04-192">src0</span><span class="sxs-lookup"><span data-stu-id="72e04-192">src0</span></span>   | <span data-ttu-id="72e04-193">src0</span><span class="sxs-lookup"><span data-stu-id="72e04-193">src0</span></span>       | <span data-ttu-id="72e04-194">+ F</span><span class="sxs-lookup"><span data-stu-id="72e04-194">+F</span></span>         | <span data-ttu-id="72e04-195">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-195">+inf</span></span>     | <span data-ttu-id="72e04-196">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-196">NaN</span></span>     |
| <span data-ttu-id="72e04-197">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="72e04-197">**+inf**</span></span>           | <span data-ttu-id="72e04-198">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-198">NaN</span></span>      | <span data-ttu-id="72e04-199">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-199">+inf</span></span>       | <span data-ttu-id="72e04-200">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-200">+inf</span></span>        | <span data-ttu-id="72e04-201">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-201">+inf</span></span>   | <span data-ttu-id="72e04-202">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-202">+inf</span></span>   | <span data-ttu-id="72e04-203">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-203">+inf</span></span>       | <span data-ttu-id="72e04-204">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-204">+inf</span></span>       | <span data-ttu-id="72e04-205">+inf</span><span class="sxs-lookup"><span data-stu-id="72e04-205">+inf</span></span>     | <span data-ttu-id="72e04-206">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-206">NaN</span></span>     |
| <span data-ttu-id="72e04-207">**NaN**</span><span class="sxs-lookup"><span data-stu-id="72e04-207">**NaN**</span></span>            | <span data-ttu-id="72e04-208">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-208">NaN</span></span>      | <span data-ttu-id="72e04-209">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-209">NaN</span></span>        | <span data-ttu-id="72e04-210">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-210">NaN</span></span>         | <span data-ttu-id="72e04-211">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-211">NaN</span></span>    | <span data-ttu-id="72e04-212">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-212">NaN</span></span>    | <span data-ttu-id="72e04-213">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-213">NaN</span></span>        | <span data-ttu-id="72e04-214">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-214">NaN</span></span>        | <span data-ttu-id="72e04-215">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-215">NaN</span></span>      | <span data-ttu-id="72e04-216">NaN</span><span class="sxs-lookup"><span data-stu-id="72e04-216">NaN</span></span>     |



 

<span data-ttu-id="72e04-217">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="72e04-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="72e04-218">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="72e04-218">Vertex Shader</span></span> | <span data-ttu-id="72e04-219">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="72e04-219">Geometry Shader</span></span> | <span data-ttu-id="72e04-220">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="72e04-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="72e04-221">x</span><span class="sxs-lookup"><span data-stu-id="72e04-221">x</span></span>             | <span data-ttu-id="72e04-222">x</span><span class="sxs-lookup"><span data-stu-id="72e04-222">x</span></span>               | <span data-ttu-id="72e04-223">x</span><span class="sxs-lookup"><span data-stu-id="72e04-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="72e04-224">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="72e04-224">Minimum Shader Model</span></span>

<span data-ttu-id="72e04-225">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="72e04-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="72e04-226">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="72e04-226">Shader Model</span></span>                                              | <span data-ttu-id="72e04-227">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="72e04-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="72e04-228">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="72e04-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="72e04-229">Oui</span><span class="sxs-lookup"><span data-stu-id="72e04-229">yes</span></span>       |
| [<span data-ttu-id="72e04-230">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="72e04-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="72e04-231">Oui</span><span class="sxs-lookup"><span data-stu-id="72e04-231">yes</span></span>       |
| [<span data-ttu-id="72e04-232">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="72e04-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="72e04-233">Oui</span><span class="sxs-lookup"><span data-stu-id="72e04-233">yes</span></span>       |
| [<span data-ttu-id="72e04-234">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="72e04-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="72e04-235">non</span><span class="sxs-lookup"><span data-stu-id="72e04-235">no</span></span>        |
| [<span data-ttu-id="72e04-236">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="72e04-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="72e04-237">non</span><span class="sxs-lookup"><span data-stu-id="72e04-237">no</span></span>        |
| [<span data-ttu-id="72e04-238">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="72e04-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="72e04-239">non</span><span class="sxs-lookup"><span data-stu-id="72e04-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="72e04-240">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72e04-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72e04-241">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="72e04-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





