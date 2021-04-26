---
title: Add (SM4-ASM)
description: Ajout de 2 vecteurs au niveau du composant.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e34f0a95ad9ee9ae4bdeed317eef133e3773311
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994976"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="9c826-103">Add (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9c826-103">add (sm4 - asm)</span></span>

<span data-ttu-id="9c826-104">Ajout de 2 vecteurs au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="9c826-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="9c826-105">Ajoutez \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9c826-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9c826-106">Élément</span><span class="sxs-lookup"><span data-stu-id="9c826-106">Item</span></span>                                                            | <span data-ttu-id="9c826-107">Description</span><span class="sxs-lookup"><span data-stu-id="9c826-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9c826-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9c826-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9c826-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9c826-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="9c826-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9c826-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9c826-111">\[dans \] le vecteur à ajouter à *src1*.</span><span class="sxs-lookup"><span data-stu-id="9c826-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="9c826-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="9c826-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="9c826-113">\[dans \] le vecteur à ajouter à *src0*.</span><span class="sxs-lookup"><span data-stu-id="9c826-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="9c826-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9c826-114">Remarks</span></span>

<span data-ttu-id="9c826-115">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="9c826-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="9c826-116">F signifie nombre réel fini.</span><span class="sxs-lookup"><span data-stu-id="9c826-116">F means finite real number.</span></span>



| <span data-ttu-id="9c826-117">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="9c826-117">**src0 src1->**</span></span> | <span data-ttu-id="9c826-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="9c826-118">**-inf**</span></span> | <span data-ttu-id="9c826-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="9c826-119">**-F**</span></span>     | <span data-ttu-id="9c826-120">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="9c826-120">**-denorm**</span></span> | <span data-ttu-id="9c826-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="9c826-121">**-0**</span></span> | <span data-ttu-id="9c826-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="9c826-122">**+0**</span></span> | <span data-ttu-id="9c826-123">**dénorme**</span><span class="sxs-lookup"><span data-stu-id="9c826-123">**denorm**</span></span> | <span data-ttu-id="9c826-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="9c826-124">**+F**</span></span>     | <span data-ttu-id="9c826-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="9c826-125">**+inf**</span></span> | <span data-ttu-id="9c826-126">**NaN**</span><span class="sxs-lookup"><span data-stu-id="9c826-126">**NaN**</span></span> |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="9c826-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="9c826-127">**-inf**</span></span>           | <span data-ttu-id="9c826-128">-inf</span><span class="sxs-lookup"><span data-stu-id="9c826-128">-inf</span></span>     | <span data-ttu-id="9c826-129">-inf</span><span class="sxs-lookup"><span data-stu-id="9c826-129">-inf</span></span>       | <span data-ttu-id="9c826-130">-inf</span><span class="sxs-lookup"><span data-stu-id="9c826-130">-inf</span></span>        | <span data-ttu-id="9c826-131">-inf</span><span class="sxs-lookup"><span data-stu-id="9c826-131">-inf</span></span>   | <span data-ttu-id="9c826-132">-inf</span><span class="sxs-lookup"><span data-stu-id="9c826-132">-inf</span></span>   | <span data-ttu-id="9c826-133">-inf</span><span class="sxs-lookup"><span data-stu-id="9c826-133">-inf</span></span>       | <span data-ttu-id="9c826-134">-inf</span><span class="sxs-lookup"><span data-stu-id="9c826-134">-inf</span></span>       | <span data-ttu-id="9c826-135">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-135">NaN</span></span>      | <span data-ttu-id="9c826-136">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-136">NaN</span></span>     |
| <span data-ttu-id="9c826-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="9c826-137">**-F**</span></span>             | <span data-ttu-id="9c826-138">-inf</span><span class="sxs-lookup"><span data-stu-id="9c826-138">-inf</span></span>     | <span data-ttu-id="9c826-139">-F</span><span class="sxs-lookup"><span data-stu-id="9c826-139">-F</span></span>         | <span data-ttu-id="9c826-140">src0</span><span class="sxs-lookup"><span data-stu-id="9c826-140">src0</span></span>        | <span data-ttu-id="9c826-141">src0</span><span class="sxs-lookup"><span data-stu-id="9c826-141">src0</span></span>   | <span data-ttu-id="9c826-142">src0</span><span class="sxs-lookup"><span data-stu-id="9c826-142">src0</span></span>   | <span data-ttu-id="9c826-143">src0</span><span class="sxs-lookup"><span data-stu-id="9c826-143">src0</span></span>       | <span data-ttu-id="9c826-144">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="9c826-144">+-F or +-0</span></span> | <span data-ttu-id="9c826-145">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-145">+inf</span></span>     | <span data-ttu-id="9c826-146">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-146">NaN</span></span>     |
| <span data-ttu-id="9c826-147">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="9c826-147">**-denorm**</span></span>        | <span data-ttu-id="9c826-148">-inf</span><span class="sxs-lookup"><span data-stu-id="9c826-148">-inf</span></span>     | <span data-ttu-id="9c826-149">src1</span><span class="sxs-lookup"><span data-stu-id="9c826-149">src1</span></span>       | <span data-ttu-id="9c826-150">-0</span><span class="sxs-lookup"><span data-stu-id="9c826-150">-0</span></span>          | <span data-ttu-id="9c826-151">-0</span><span class="sxs-lookup"><span data-stu-id="9c826-151">-0</span></span>     | <span data-ttu-id="9c826-152">+0</span><span class="sxs-lookup"><span data-stu-id="9c826-152">+0</span></span>     | <span data-ttu-id="9c826-153">+0</span><span class="sxs-lookup"><span data-stu-id="9c826-153">+0</span></span>         | <span data-ttu-id="9c826-154">src1</span><span class="sxs-lookup"><span data-stu-id="9c826-154">src1</span></span>       | <span data-ttu-id="9c826-155">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-155">+inf</span></span>     | <span data-ttu-id="9c826-156">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-156">NaN</span></span>     |
| <span data-ttu-id="9c826-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="9c826-157">**-0**</span></span>             | <span data-ttu-id="9c826-158">-inf</span><span class="sxs-lookup"><span data-stu-id="9c826-158">-inf</span></span>     | <span data-ttu-id="9c826-159">src1</span><span class="sxs-lookup"><span data-stu-id="9c826-159">src1</span></span>       | <span data-ttu-id="9c826-160">-0</span><span class="sxs-lookup"><span data-stu-id="9c826-160">-0</span></span>          | <span data-ttu-id="9c826-161">-0</span><span class="sxs-lookup"><span data-stu-id="9c826-161">-0</span></span>     | <span data-ttu-id="9c826-162">+0</span><span class="sxs-lookup"><span data-stu-id="9c826-162">+0</span></span>     | <span data-ttu-id="9c826-163">+0</span><span class="sxs-lookup"><span data-stu-id="9c826-163">+0</span></span>         | <span data-ttu-id="9c826-164">src1</span><span class="sxs-lookup"><span data-stu-id="9c826-164">src1</span></span>       | <span data-ttu-id="9c826-165">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-165">+inf</span></span>     | <span data-ttu-id="9c826-166">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-166">NaN</span></span>     |
| <span data-ttu-id="9c826-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="9c826-167">**+0**</span></span>             | <span data-ttu-id="9c826-168">i-INF</span><span class="sxs-lookup"><span data-stu-id="9c826-168">i-inf</span></span>    | <span data-ttu-id="9c826-169">src1</span><span class="sxs-lookup"><span data-stu-id="9c826-169">src1</span></span>       | <span data-ttu-id="9c826-170">+0</span><span class="sxs-lookup"><span data-stu-id="9c826-170">+0</span></span>          | <span data-ttu-id="9c826-171">+0</span><span class="sxs-lookup"><span data-stu-id="9c826-171">+0</span></span>     | <span data-ttu-id="9c826-172">+0</span><span class="sxs-lookup"><span data-stu-id="9c826-172">+0</span></span>     | <span data-ttu-id="9c826-173">+0</span><span class="sxs-lookup"><span data-stu-id="9c826-173">+0</span></span>         | <span data-ttu-id="9c826-174">src1</span><span class="sxs-lookup"><span data-stu-id="9c826-174">src1</span></span>       | <span data-ttu-id="9c826-175">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-175">+inf</span></span>     | <span data-ttu-id="9c826-176">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-176">NaN</span></span>     |
| <span data-ttu-id="9c826-177">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="9c826-177">**+denorm**</span></span>        | <span data-ttu-id="9c826-178">-inf</span><span class="sxs-lookup"><span data-stu-id="9c826-178">-inf</span></span>     | <span data-ttu-id="9c826-179">src1</span><span class="sxs-lookup"><span data-stu-id="9c826-179">src1</span></span>       | <span data-ttu-id="9c826-180">+0</span><span class="sxs-lookup"><span data-stu-id="9c826-180">+0</span></span>          | <span data-ttu-id="9c826-181">+0</span><span class="sxs-lookup"><span data-stu-id="9c826-181">+0</span></span>     | <span data-ttu-id="9c826-182">+0</span><span class="sxs-lookup"><span data-stu-id="9c826-182">+0</span></span>     | <span data-ttu-id="9c826-183">+0</span><span class="sxs-lookup"><span data-stu-id="9c826-183">+0</span></span>         | <span data-ttu-id="9c826-184">src1</span><span class="sxs-lookup"><span data-stu-id="9c826-184">src1</span></span>       | <span data-ttu-id="9c826-185">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-185">+inf</span></span>     | <span data-ttu-id="9c826-186">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-186">NaN</span></span>     |
| <span data-ttu-id="9c826-187">**+ F**</span><span class="sxs-lookup"><span data-stu-id="9c826-187">**+F**</span></span>             | <span data-ttu-id="9c826-188">-inf</span><span class="sxs-lookup"><span data-stu-id="9c826-188">-inf</span></span>     | <span data-ttu-id="9c826-189">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="9c826-189">+-F or +-0</span></span> | <span data-ttu-id="9c826-190">src0</span><span class="sxs-lookup"><span data-stu-id="9c826-190">src0</span></span>        | <span data-ttu-id="9c826-191">src0</span><span class="sxs-lookup"><span data-stu-id="9c826-191">src0</span></span>   | <span data-ttu-id="9c826-192">src0</span><span class="sxs-lookup"><span data-stu-id="9c826-192">src0</span></span>   | <span data-ttu-id="9c826-193">src0</span><span class="sxs-lookup"><span data-stu-id="9c826-193">src0</span></span>       | <span data-ttu-id="9c826-194">+ F</span><span class="sxs-lookup"><span data-stu-id="9c826-194">+F</span></span>         | <span data-ttu-id="9c826-195">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-195">+inf</span></span>     | <span data-ttu-id="9c826-196">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-196">NaN</span></span>     |
| <span data-ttu-id="9c826-197">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="9c826-197">**+inf**</span></span>           | <span data-ttu-id="9c826-198">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-198">NaN</span></span>      | <span data-ttu-id="9c826-199">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-199">+inf</span></span>       | <span data-ttu-id="9c826-200">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-200">+inf</span></span>        | <span data-ttu-id="9c826-201">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-201">+inf</span></span>   | <span data-ttu-id="9c826-202">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-202">+inf</span></span>   | <span data-ttu-id="9c826-203">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-203">+inf</span></span>       | <span data-ttu-id="9c826-204">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-204">+inf</span></span>       | <span data-ttu-id="9c826-205">+inf</span><span class="sxs-lookup"><span data-stu-id="9c826-205">+inf</span></span>     | <span data-ttu-id="9c826-206">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-206">NaN</span></span>     |
| <span data-ttu-id="9c826-207">**NaN**</span><span class="sxs-lookup"><span data-stu-id="9c826-207">**NaN**</span></span>            | <span data-ttu-id="9c826-208">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-208">NaN</span></span>      | <span data-ttu-id="9c826-209">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-209">NaN</span></span>        | <span data-ttu-id="9c826-210">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-210">NaN</span></span>         | <span data-ttu-id="9c826-211">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-211">NaN</span></span>    | <span data-ttu-id="9c826-212">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-212">NaN</span></span>    | <span data-ttu-id="9c826-213">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-213">NaN</span></span>        | <span data-ttu-id="9c826-214">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-214">NaN</span></span>        | <span data-ttu-id="9c826-215">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-215">NaN</span></span>      | <span data-ttu-id="9c826-216">NaN</span><span class="sxs-lookup"><span data-stu-id="9c826-216">NaN</span></span>     |



 

<span data-ttu-id="9c826-217">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="9c826-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9c826-218">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="9c826-218">Vertex Shader</span></span> | <span data-ttu-id="9c826-219">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="9c826-219">Geometry Shader</span></span> | <span data-ttu-id="9c826-220">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="9c826-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9c826-221">x</span><span class="sxs-lookup"><span data-stu-id="9c826-221">x</span></span>             | <span data-ttu-id="9c826-222">x</span><span class="sxs-lookup"><span data-stu-id="9c826-222">x</span></span>               | <span data-ttu-id="9c826-223">x</span><span class="sxs-lookup"><span data-stu-id="9c826-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9c826-224">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9c826-224">Minimum Shader Model</span></span>

<span data-ttu-id="9c826-225">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="9c826-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9c826-226">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9c826-226">Shader Model</span></span>                                              | <span data-ttu-id="9c826-227">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c826-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9c826-228">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9c826-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9c826-229">oui</span><span class="sxs-lookup"><span data-stu-id="9c826-229">yes</span></span>       |
| [<span data-ttu-id="9c826-230">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="9c826-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9c826-231">oui</span><span class="sxs-lookup"><span data-stu-id="9c826-231">yes</span></span>       |
| [<span data-ttu-id="9c826-232">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="9c826-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9c826-233">oui</span><span class="sxs-lookup"><span data-stu-id="9c826-233">yes</span></span>       |
| [<span data-ttu-id="9c826-234">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c826-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9c826-235">non</span><span class="sxs-lookup"><span data-stu-id="9c826-235">no</span></span>        |
| [<span data-ttu-id="9c826-236">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c826-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9c826-237">non</span><span class="sxs-lookup"><span data-stu-id="9c826-237">no</span></span>        |
| [<span data-ttu-id="9c826-238">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c826-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9c826-239">non</span><span class="sxs-lookup"><span data-stu-id="9c826-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9c826-240">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c826-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c826-241">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c826-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





