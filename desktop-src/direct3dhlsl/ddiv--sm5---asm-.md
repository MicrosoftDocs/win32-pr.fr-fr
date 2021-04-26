---
title: DDIV (SM5-ASM)
description: Calcule une division à double précision au niveau du composant.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fc039b222b28a5fb1217d23c78470aff1739f7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999156"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="4e8ca-103">DDIV (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4e8ca-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="4e8ca-104">Calcule une division à double précision au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="4e8ca-105">DDIV \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="4e8ca-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="4e8ca-106">Élément</span><span class="sxs-lookup"><span data-stu-id="4e8ca-106">Item</span></span>                                                            | <span data-ttu-id="4e8ca-107">Description</span><span class="sxs-lookup"><span data-stu-id="4e8ca-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e8ca-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4e8ca-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4e8ca-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="4e8ca-110">La valeur de résultat doit être précise à 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="4e8ca-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4e8ca-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4e8ca-112">\[dans \] le dividende.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="4e8ca-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="4e8ca-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="4e8ca-114">\[dans \] le diviseur.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="4e8ca-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e8ca-115">Remarks</span></span>

<span data-ttu-id="4e8ca-116">L’instruction DDIV sera émise par le compilateur HLSL chaque fois que l’opérateur de division sera utilisé avec des doubles.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="4e8ca-117">La précision de cette instruction doit être de 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="4e8ca-118">Les nuanceurs qui utilisent cette instruction sont marqués d’un indicateur de nuanceur qui entraîne l’échec de la liaison de ces derniers, sauf si toutes les conditions suivantes sont remplies.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="4e8ca-119">Le système prend en charge DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="4e8ca-120">Le système comprend un pilote WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="4e8ca-121">Le pilote fournit une prise en charge pour cette instruction via les **\_ options d3d11 des données de la fonctionnalité d3d11 \_ \_ \_ . ExtendedDoublesShaderInstructions** défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="4e8ca-122">Le tableau suivant présente les résultats btained lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité positif ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="4e8ca-123">Dans ce tableau, F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="4e8ca-123">In this table F means finite-real number.</span></span>



| <span data-ttu-id="4e8ca-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-124">**src0 src1 ->**</span></span> | <span data-ttu-id="4e8ca-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-125">**-inf**</span></span> | <span data-ttu-id="4e8ca-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-126">**-F**</span></span> | <span data-ttu-id="4e8ca-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-127">**-1.0**</span></span> | <span data-ttu-id="4e8ca-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-128">**-0**</span></span> | <span data-ttu-id="4e8ca-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-129">**+0**</span></span> | <span data-ttu-id="4e8ca-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-130">**+1.0**</span></span> | <span data-ttu-id="4e8ca-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-131">**+F**</span></span> | <span data-ttu-id="4e8ca-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-132">**+inf**</span></span> | <span data-ttu-id="4e8ca-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-133">**NaN**</span></span> |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="4e8ca-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-134">**-inf**</span></span>            | <span data-ttu-id="4e8ca-135">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-135">NaN</span></span>      | <span data-ttu-id="4e8ca-136">+inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-136">+inf</span></span>   | <span data-ttu-id="4e8ca-137">+inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-137">+inf</span></span>     | <span data-ttu-id="4e8ca-138">+inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-138">+inf</span></span>   | <span data-ttu-id="4e8ca-139">-inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-139">-inf</span></span>   | <span data-ttu-id="4e8ca-140">-inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-140">-inf</span></span>     | <span data-ttu-id="4e8ca-141">-inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-141">-inf</span></span>   | <span data-ttu-id="4e8ca-142">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-142">NaN</span></span>      | <span data-ttu-id="4e8ca-143">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-143">NaN</span></span>     |
| <span data-ttu-id="4e8ca-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-144">**-F**</span></span>              | <span data-ttu-id="4e8ca-145">+0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-145">+0</span></span>       | <span data-ttu-id="4e8ca-146">+ F</span><span class="sxs-lookup"><span data-stu-id="4e8ca-146">+F</span></span>     | <span data-ttu-id="4e8ca-147">-src0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-147">-src0</span></span>    | <span data-ttu-id="4e8ca-148">+inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-148">+inf</span></span>   | <span data-ttu-id="4e8ca-149">-inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-149">-inf</span></span>   | <span data-ttu-id="4e8ca-150">src0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-150">src0</span></span>     | <span data-ttu-id="4e8ca-151">-F</span><span class="sxs-lookup"><span data-stu-id="4e8ca-151">-F</span></span>     | <span data-ttu-id="4e8ca-152">-0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-152">-0</span></span>       | <span data-ttu-id="4e8ca-153">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-153">NaN</span></span>     |
| <span data-ttu-id="4e8ca-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-154">**-0**</span></span>              | <span data-ttu-id="4e8ca-155">+0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-155">+0</span></span>       | <span data-ttu-id="4e8ca-156">+0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-156">+0</span></span>     | <span data-ttu-id="4e8ca-157">+0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-157">+0</span></span>       | <span data-ttu-id="4e8ca-158">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-158">NaN</span></span>    | <span data-ttu-id="4e8ca-159">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-159">NaN</span></span>    | <span data-ttu-id="4e8ca-160">-0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-160">-0</span></span>       | <span data-ttu-id="4e8ca-161">-0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-161">-0</span></span>     | <span data-ttu-id="4e8ca-162">-0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-162">-0</span></span>       | <span data-ttu-id="4e8ca-163">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-163">NaN</span></span>     |
| <span data-ttu-id="4e8ca-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-164">**+0**</span></span>              | <span data-ttu-id="4e8ca-165">-0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-165">-0</span></span>       | <span data-ttu-id="4e8ca-166">-0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-166">-0</span></span>     | <span data-ttu-id="4e8ca-167">-0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-167">-0</span></span>       | <span data-ttu-id="4e8ca-168">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-168">NaN</span></span>    | <span data-ttu-id="4e8ca-169">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-169">NaN</span></span>    | <span data-ttu-id="4e8ca-170">+0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-170">+0</span></span>       | <span data-ttu-id="4e8ca-171">+0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-171">+0</span></span>     | <span data-ttu-id="4e8ca-172">+0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-172">+0</span></span>       | <span data-ttu-id="4e8ca-173">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-173">NaN</span></span>     |
| <span data-ttu-id="4e8ca-174">**+ F**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-174">**+F**</span></span>              | <span data-ttu-id="4e8ca-175">-0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-175">-0</span></span>       | <span data-ttu-id="4e8ca-176">-F</span><span class="sxs-lookup"><span data-stu-id="4e8ca-176">-F</span></span>     | <span data-ttu-id="4e8ca-177">-src0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-177">-src0</span></span>    | <span data-ttu-id="4e8ca-178">-inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-178">-inf</span></span>   | <span data-ttu-id="4e8ca-179">+inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-179">+inf</span></span>   | <span data-ttu-id="4e8ca-180">src0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-180">src0</span></span>     | <span data-ttu-id="4e8ca-181">+ F</span><span class="sxs-lookup"><span data-stu-id="4e8ca-181">+F</span></span>     | <span data-ttu-id="4e8ca-182">+0</span><span class="sxs-lookup"><span data-stu-id="4e8ca-182">+0</span></span>       | <span data-ttu-id="4e8ca-183">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-183">NaN</span></span>     |
| <span data-ttu-id="4e8ca-184">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-184">**+inf**</span></span>            | <span data-ttu-id="4e8ca-185">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-185">NaN</span></span>      | <span data-ttu-id="4e8ca-186">-inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-186">-inf</span></span>   | <span data-ttu-id="4e8ca-187">-inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-187">-inf</span></span>     | <span data-ttu-id="4e8ca-188">-inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-188">-inf</span></span>   | <span data-ttu-id="4e8ca-189">+inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-189">+inf</span></span>   | <span data-ttu-id="4e8ca-190">+inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-190">+inf</span></span>     | <span data-ttu-id="4e8ca-191">+inf</span><span class="sxs-lookup"><span data-stu-id="4e8ca-191">+inf</span></span>   | <span data-ttu-id="4e8ca-192">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-192">NaN</span></span>      | <span data-ttu-id="4e8ca-193">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-193">NaN</span></span>     |
| <span data-ttu-id="4e8ca-194">**NaN**</span><span class="sxs-lookup"><span data-stu-id="4e8ca-194">**NaN**</span></span>             | <span data-ttu-id="4e8ca-195">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-195">NaN</span></span>      | <span data-ttu-id="4e8ca-196">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-196">NaN</span></span>    | <span data-ttu-id="4e8ca-197">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-197">NaN</span></span>      | <span data-ttu-id="4e8ca-198">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-198">NaN</span></span>    | <span data-ttu-id="4e8ca-199">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-199">NaN</span></span>    | <span data-ttu-id="4e8ca-200">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-200">NaN</span></span>      | <span data-ttu-id="4e8ca-201">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-201">NaN</span></span>    | <span data-ttu-id="4e8ca-202">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-202">NaN</span></span>      | <span data-ttu-id="4e8ca-203">NaN</span><span class="sxs-lookup"><span data-stu-id="4e8ca-203">NaN</span></span>     |



 

<span data-ttu-id="4e8ca-204">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="4e8ca-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4e8ca-205">Sommet</span><span class="sxs-lookup"><span data-stu-id="4e8ca-205">Vertex</span></span> | <span data-ttu-id="4e8ca-206">Forme</span><span class="sxs-lookup"><span data-stu-id="4e8ca-206">Hull</span></span> | <span data-ttu-id="4e8ca-207">Domain</span><span class="sxs-lookup"><span data-stu-id="4e8ca-207">Domain</span></span> | <span data-ttu-id="4e8ca-208">Géométrie</span><span class="sxs-lookup"><span data-stu-id="4e8ca-208">Geometry</span></span> | <span data-ttu-id="4e8ca-209">Pixel</span><span class="sxs-lookup"><span data-stu-id="4e8ca-209">Pixel</span></span> | <span data-ttu-id="4e8ca-210">Calcul</span><span class="sxs-lookup"><span data-stu-id="4e8ca-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4e8ca-211">X</span><span class="sxs-lookup"><span data-stu-id="4e8ca-211">X</span></span>      | <span data-ttu-id="4e8ca-212">X</span><span class="sxs-lookup"><span data-stu-id="4e8ca-212">X</span></span>    | <span data-ttu-id="4e8ca-213">X</span><span class="sxs-lookup"><span data-stu-id="4e8ca-213">X</span></span>      | <span data-ttu-id="4e8ca-214">X</span><span class="sxs-lookup"><span data-stu-id="4e8ca-214">X</span></span>        | <span data-ttu-id="4e8ca-215">X</span><span class="sxs-lookup"><span data-stu-id="4e8ca-215">X</span></span>     | <span data-ttu-id="4e8ca-216">X</span><span class="sxs-lookup"><span data-stu-id="4e8ca-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4e8ca-217">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4e8ca-217">Minimum Shader Model</span></span>

<span data-ttu-id="4e8ca-218">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="4e8ca-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4e8ca-219">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4e8ca-219">Shader Model</span></span>                                              | <span data-ttu-id="4e8ca-220">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e8ca-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4e8ca-221">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4e8ca-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4e8ca-222">oui</span><span class="sxs-lookup"><span data-stu-id="4e8ca-222">yes</span></span>       |
| [<span data-ttu-id="4e8ca-223">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="4e8ca-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4e8ca-224">non</span><span class="sxs-lookup"><span data-stu-id="4e8ca-224">no</span></span>        |
| [<span data-ttu-id="4e8ca-225">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="4e8ca-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4e8ca-226">non</span><span class="sxs-lookup"><span data-stu-id="4e8ca-226">no</span></span>        |
| [<span data-ttu-id="4e8ca-227">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e8ca-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4e8ca-228">non</span><span class="sxs-lookup"><span data-stu-id="4e8ca-228">no</span></span>        |
| [<span data-ttu-id="4e8ca-229">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e8ca-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4e8ca-230">non</span><span class="sxs-lookup"><span data-stu-id="4e8ca-230">no</span></span>        |
| [<span data-ttu-id="4e8ca-231">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e8ca-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4e8ca-232">non</span><span class="sxs-lookup"><span data-stu-id="4e8ca-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4e8ca-233">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e8ca-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e8ca-234">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e8ca-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





