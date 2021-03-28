---
title: DDIV (SM5-ASM)
description: Calcule une division à double précision au niveau du composant.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f5c3aae9d416d24f41de8d8308c5a69be9d016
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990732"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="5b9d1-103">DDIV (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5b9d1-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="5b9d1-104">Calcule une division à double précision au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="5b9d1-105">DDIV \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5b9d1-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="5b9d1-106">Élément</span><span class="sxs-lookup"><span data-stu-id="5b9d1-106">Item</span></span>                                                            | <span data-ttu-id="5b9d1-107">Description</span><span class="sxs-lookup"><span data-stu-id="5b9d1-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b9d1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5b9d1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5b9d1-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="5b9d1-110">La valeur de résultat doit être précise à 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="5b9d1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5b9d1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5b9d1-112">\[dans \] le dividende.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="5b9d1-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="5b9d1-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="5b9d1-114">\[dans \] le diviseur.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="5b9d1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5b9d1-115">Remarks</span></span>

<span data-ttu-id="5b9d1-116">L’instruction DDIV sera émise par le compilateur HLSL chaque fois que l’opérateur de division sera utilisé avec des doubles.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="5b9d1-117">La précision de cette instruction doit être de 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="5b9d1-118">Les nuanceurs qui utilisent cette instruction sont marqués d’un indicateur de nuanceur qui entraîne l’échec de la liaison de ces derniers, sauf si toutes les conditions suivantes sont remplies.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="5b9d1-119">Le système prend en charge DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="5b9d1-120">Le système comprend un pilote WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="5b9d1-121">Le pilote fournit une prise en charge pour cette instruction via les **\_ options d3d11 des données de la fonctionnalité d3d11 \_ \_ \_ . ExtendedDoublesShaderInstructions** défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="5b9d1-122">Le tableau suivant présente les résultats btained lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité positif ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="5b9d1-123">Dans ce tableau, F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="5b9d1-123">In this table F means finite-real number.</span></span>



|                     |          |        |          |        |        |          |        |          |         |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="5b9d1-124">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-124">**src0 src1 ->**</span></span> | <span data-ttu-id="5b9d1-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-125">**-inf**</span></span> | <span data-ttu-id="5b9d1-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-126">**-F**</span></span> | <span data-ttu-id="5b9d1-127">**-1,0**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-127">**-1.0**</span></span> | <span data-ttu-id="5b9d1-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-128">**-0**</span></span> | <span data-ttu-id="5b9d1-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-129">**+0**</span></span> | <span data-ttu-id="5b9d1-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-130">**+1.0**</span></span> | <span data-ttu-id="5b9d1-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-131">**+F**</span></span> | <span data-ttu-id="5b9d1-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-132">**+inf**</span></span> | <span data-ttu-id="5b9d1-133">**NaN**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-133">**NaN**</span></span> |
| <span data-ttu-id="5b9d1-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-134">**-inf**</span></span>            | <span data-ttu-id="5b9d1-135">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-135">NaN</span></span>      | <span data-ttu-id="5b9d1-136">+inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-136">+inf</span></span>   | <span data-ttu-id="5b9d1-137">+inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-137">+inf</span></span>     | <span data-ttu-id="5b9d1-138">+inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-138">+inf</span></span>   | <span data-ttu-id="5b9d1-139">-inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-139">-inf</span></span>   | <span data-ttu-id="5b9d1-140">-inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-140">-inf</span></span>     | <span data-ttu-id="5b9d1-141">-inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-141">-inf</span></span>   | <span data-ttu-id="5b9d1-142">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-142">NaN</span></span>      | <span data-ttu-id="5b9d1-143">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-143">NaN</span></span>     |
| <span data-ttu-id="5b9d1-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-144">**-F**</span></span>              | <span data-ttu-id="5b9d1-145">+0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-145">+0</span></span>       | <span data-ttu-id="5b9d1-146">+ F</span><span class="sxs-lookup"><span data-stu-id="5b9d1-146">+F</span></span>     | <span data-ttu-id="5b9d1-147">-src0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-147">-src0</span></span>    | <span data-ttu-id="5b9d1-148">+inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-148">+inf</span></span>   | <span data-ttu-id="5b9d1-149">-inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-149">-inf</span></span>   | <span data-ttu-id="5b9d1-150">src0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-150">src0</span></span>     | <span data-ttu-id="5b9d1-151">-F</span><span class="sxs-lookup"><span data-stu-id="5b9d1-151">-F</span></span>     | <span data-ttu-id="5b9d1-152">-0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-152">-0</span></span>       | <span data-ttu-id="5b9d1-153">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-153">NaN</span></span>     |
| <span data-ttu-id="5b9d1-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-154">**-0**</span></span>              | <span data-ttu-id="5b9d1-155">+0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-155">+0</span></span>       | <span data-ttu-id="5b9d1-156">+0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-156">+0</span></span>     | <span data-ttu-id="5b9d1-157">+0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-157">+0</span></span>       | <span data-ttu-id="5b9d1-158">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-158">NaN</span></span>    | <span data-ttu-id="5b9d1-159">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-159">NaN</span></span>    | <span data-ttu-id="5b9d1-160">-0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-160">-0</span></span>       | <span data-ttu-id="5b9d1-161">-0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-161">-0</span></span>     | <span data-ttu-id="5b9d1-162">-0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-162">-0</span></span>       | <span data-ttu-id="5b9d1-163">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-163">NaN</span></span>     |
| <span data-ttu-id="5b9d1-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-164">**+0**</span></span>              | <span data-ttu-id="5b9d1-165">-0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-165">-0</span></span>       | <span data-ttu-id="5b9d1-166">-0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-166">-0</span></span>     | <span data-ttu-id="5b9d1-167">-0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-167">-0</span></span>       | <span data-ttu-id="5b9d1-168">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-168">NaN</span></span>    | <span data-ttu-id="5b9d1-169">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-169">NaN</span></span>    | <span data-ttu-id="5b9d1-170">+0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-170">+0</span></span>       | <span data-ttu-id="5b9d1-171">+0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-171">+0</span></span>     | <span data-ttu-id="5b9d1-172">+0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-172">+0</span></span>       | <span data-ttu-id="5b9d1-173">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-173">NaN</span></span>     |
| <span data-ttu-id="5b9d1-174">**+ F**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-174">**+F**</span></span>              | <span data-ttu-id="5b9d1-175">-0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-175">-0</span></span>       | <span data-ttu-id="5b9d1-176">-F</span><span class="sxs-lookup"><span data-stu-id="5b9d1-176">-F</span></span>     | <span data-ttu-id="5b9d1-177">-src0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-177">-src0</span></span>    | <span data-ttu-id="5b9d1-178">-inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-178">-inf</span></span>   | <span data-ttu-id="5b9d1-179">+inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-179">+inf</span></span>   | <span data-ttu-id="5b9d1-180">src0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-180">src0</span></span>     | <span data-ttu-id="5b9d1-181">+ F</span><span class="sxs-lookup"><span data-stu-id="5b9d1-181">+F</span></span>     | <span data-ttu-id="5b9d1-182">+0</span><span class="sxs-lookup"><span data-stu-id="5b9d1-182">+0</span></span>       | <span data-ttu-id="5b9d1-183">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-183">NaN</span></span>     |
| <span data-ttu-id="5b9d1-184">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-184">**+inf**</span></span>            | <span data-ttu-id="5b9d1-185">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-185">NaN</span></span>      | <span data-ttu-id="5b9d1-186">-inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-186">-inf</span></span>   | <span data-ttu-id="5b9d1-187">-inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-187">-inf</span></span>     | <span data-ttu-id="5b9d1-188">-inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-188">-inf</span></span>   | <span data-ttu-id="5b9d1-189">+inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-189">+inf</span></span>   | <span data-ttu-id="5b9d1-190">+inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-190">+inf</span></span>     | <span data-ttu-id="5b9d1-191">+inf</span><span class="sxs-lookup"><span data-stu-id="5b9d1-191">+inf</span></span>   | <span data-ttu-id="5b9d1-192">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-192">NaN</span></span>      | <span data-ttu-id="5b9d1-193">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-193">NaN</span></span>     |
| <span data-ttu-id="5b9d1-194">**NaN**</span><span class="sxs-lookup"><span data-stu-id="5b9d1-194">**NaN**</span></span>             | <span data-ttu-id="5b9d1-195">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-195">NaN</span></span>      | <span data-ttu-id="5b9d1-196">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-196">NaN</span></span>    | <span data-ttu-id="5b9d1-197">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-197">NaN</span></span>      | <span data-ttu-id="5b9d1-198">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-198">NaN</span></span>    | <span data-ttu-id="5b9d1-199">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-199">NaN</span></span>    | <span data-ttu-id="5b9d1-200">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-200">NaN</span></span>      | <span data-ttu-id="5b9d1-201">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-201">NaN</span></span>    | <span data-ttu-id="5b9d1-202">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-202">NaN</span></span>      | <span data-ttu-id="5b9d1-203">NaN</span><span class="sxs-lookup"><span data-stu-id="5b9d1-203">NaN</span></span>     |



 

<span data-ttu-id="5b9d1-204">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="5b9d1-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5b9d1-205">Sommet</span><span class="sxs-lookup"><span data-stu-id="5b9d1-205">Vertex</span></span> | <span data-ttu-id="5b9d1-206">Forme</span><span class="sxs-lookup"><span data-stu-id="5b9d1-206">Hull</span></span> | <span data-ttu-id="5b9d1-207">Domain</span><span class="sxs-lookup"><span data-stu-id="5b9d1-207">Domain</span></span> | <span data-ttu-id="5b9d1-208">Géométrie</span><span class="sxs-lookup"><span data-stu-id="5b9d1-208">Geometry</span></span> | <span data-ttu-id="5b9d1-209">Pixel</span><span class="sxs-lookup"><span data-stu-id="5b9d1-209">Pixel</span></span> | <span data-ttu-id="5b9d1-210">Compute</span><span class="sxs-lookup"><span data-stu-id="5b9d1-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5b9d1-211">X</span><span class="sxs-lookup"><span data-stu-id="5b9d1-211">X</span></span>      | <span data-ttu-id="5b9d1-212">X</span><span class="sxs-lookup"><span data-stu-id="5b9d1-212">X</span></span>    | <span data-ttu-id="5b9d1-213">X</span><span class="sxs-lookup"><span data-stu-id="5b9d1-213">X</span></span>      | <span data-ttu-id="5b9d1-214">X</span><span class="sxs-lookup"><span data-stu-id="5b9d1-214">X</span></span>        | <span data-ttu-id="5b9d1-215">X</span><span class="sxs-lookup"><span data-stu-id="5b9d1-215">X</span></span>     | <span data-ttu-id="5b9d1-216">X</span><span class="sxs-lookup"><span data-stu-id="5b9d1-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5b9d1-217">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5b9d1-217">Minimum Shader Model</span></span>

<span data-ttu-id="5b9d1-218">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="5b9d1-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5b9d1-219">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5b9d1-219">Shader Model</span></span>                                              | <span data-ttu-id="5b9d1-220">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5b9d1-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5b9d1-221">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="5b9d1-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5b9d1-222">Oui</span><span class="sxs-lookup"><span data-stu-id="5b9d1-222">yes</span></span>       |
| [<span data-ttu-id="5b9d1-223">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="5b9d1-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5b9d1-224">non</span><span class="sxs-lookup"><span data-stu-id="5b9d1-224">no</span></span>        |
| [<span data-ttu-id="5b9d1-225">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="5b9d1-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5b9d1-226">non</span><span class="sxs-lookup"><span data-stu-id="5b9d1-226">no</span></span>        |
| [<span data-ttu-id="5b9d1-227">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5b9d1-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5b9d1-228">non</span><span class="sxs-lookup"><span data-stu-id="5b9d1-228">no</span></span>        |
| [<span data-ttu-id="5b9d1-229">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5b9d1-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5b9d1-230">non</span><span class="sxs-lookup"><span data-stu-id="5b9d1-230">no</span></span>        |
| [<span data-ttu-id="5b9d1-231">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5b9d1-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5b9d1-232">non</span><span class="sxs-lookup"><span data-stu-id="5b9d1-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5b9d1-233">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b9d1-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b9d1-234">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5b9d1-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





