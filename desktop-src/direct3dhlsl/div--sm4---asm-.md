---
title: div (SM4-ASM)
description: Division au niveau du composant.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 332d494adc2cc9bebe2e714b47ff2c5a6b299966
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030576"
---
# <a name="div-sm4---asm"></a><span data-ttu-id="01646-103">div (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="01646-103">div (sm4 - asm)</span></span>

<span data-ttu-id="01646-104">Division au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="01646-104">Component-wise divide.</span></span>



| <span data-ttu-id="01646-105">div \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="01646-105">div\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="01646-106">Élément</span><span class="sxs-lookup"><span data-stu-id="01646-106">Item</span></span>                                                            | <span data-ttu-id="01646-107">Description</span><span class="sxs-lookup"><span data-stu-id="01646-107">Description</span></span>                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="01646-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="01646-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="01646-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="01646-109">\[in\] The result of the operation.</span></span><br/> |
| <span data-ttu-id="01646-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="01646-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="01646-111">\[dans \] le dividende.</span><span class="sxs-lookup"><span data-stu-id="01646-111">\[in\] The dividend.</span></span><br/>                |
| <span data-ttu-id="01646-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="01646-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="01646-113">\[dans \] le diviseur.</span><span class="sxs-lookup"><span data-stu-id="01646-113">\[in\] The divisor.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="01646-114">Notes</span><span class="sxs-lookup"><span data-stu-id="01646-114">Remarks</span></span>

<span data-ttu-id="01646-115">Le tableau suivant présente les résultats obtenus lors de l’exécution de l’instruction avec différentes classes de nombres, en supposant qu’aucun dépassement de capacité ou négatif ne se produit.</span><span class="sxs-lookup"><span data-stu-id="01646-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="01646-116">Vous devez noter les deux implémentations de division autorisées : a/b et a \* (1/b).</span><span class="sxs-lookup"><span data-stu-id="01646-116">You should note the two allowed implementations of divide: a/b and a\*(1/b).</span></span>

<span data-ttu-id="01646-117">L’un des résultats est qu’il existe des exceptions au tableau ci-dessous pour les valeurs de dénominateur volumineuses (supérieures à 8.5070592 e + 37), où 1/dénominateur est une dénorme.</span><span class="sxs-lookup"><span data-stu-id="01646-117">One outcome of this is that there are exceptions to the table below for large denominator values (greater than 8.5070592e+37), where 1/denominator is a denorm.</span></span> <span data-ttu-id="01646-118">Étant donné que les implémentations peuvent effectuer une division en tant que \* (1/b) au lieu d’un/b directement, et une valeur de 1/ \[ grande \] est une dénorme qui peut être vidée, certains cas de la table produisent des résultats différents.</span><span class="sxs-lookup"><span data-stu-id="01646-118">Because implementations may perform divide as a\*(1/b), instead of a/b directly, and 1/\[large value\] is a denorm that could get flushed, some cases in the table would produce different results.</span></span> <span data-ttu-id="01646-119">Par exemple, la valeur (+/-) INF/(+/-) \[ > 8.5070592 e + 37 \] peut produire Nan sur certaines implémentations, mais (+/-) INF sur d’autres implémentations</span><span class="sxs-lookup"><span data-stu-id="01646-119">For example, (+/-)INF / (+/-)\[value > 8.5070592e+37\] may produce NaN on some implementations, but (+/-)INF on other implementations</span></span>

<span data-ttu-id="01646-120">Dans ce tableau, F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="01646-120">In this table F means finite-real number.</span></span>



|                     |          |            |             |        |        |             |            |          |         |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="01646-121">**src0 src1->**</span><span class="sxs-lookup"><span data-stu-id="01646-121">**src0 src1 ->**</span></span> | <span data-ttu-id="01646-122">**-INF**</span><span class="sxs-lookup"><span data-stu-id="01646-122">**-inf**</span></span> | <span data-ttu-id="01646-123">**-F**</span><span class="sxs-lookup"><span data-stu-id="01646-123">**-F**</span></span>     | <span data-ttu-id="01646-124">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="01646-124">**-denorm**</span></span> | <span data-ttu-id="01646-125">**-0**</span><span class="sxs-lookup"><span data-stu-id="01646-125">**-0**</span></span> | <span data-ttu-id="01646-126">**+0**</span><span class="sxs-lookup"><span data-stu-id="01646-126">**+0**</span></span> | <span data-ttu-id="01646-127">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="01646-127">**+denorm**</span></span> | <span data-ttu-id="01646-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="01646-128">**+F**</span></span>     | <span data-ttu-id="01646-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="01646-129">**+inf**</span></span> | <span data-ttu-id="01646-130">**Nan**</span><span class="sxs-lookup"><span data-stu-id="01646-130">**Nan**</span></span> |
| <span data-ttu-id="01646-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="01646-131">**-inf**</span></span>            | <span data-ttu-id="01646-132">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-132">-inf</span></span>     | <span data-ttu-id="01646-133">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-133">-inf</span></span>       | <span data-ttu-id="01646-134">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-134">-inf</span></span>        | <span data-ttu-id="01646-135">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-135">-inf</span></span>   | <span data-ttu-id="01646-136">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-136">-inf</span></span>   | <span data-ttu-id="01646-137">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-137">-inf</span></span>        | <span data-ttu-id="01646-138">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-138">-inf</span></span>       | <span data-ttu-id="01646-139">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-139">NaN</span></span>      | <span data-ttu-id="01646-140">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-140">NaN</span></span>     |
| <span data-ttu-id="01646-141">**-F**</span><span class="sxs-lookup"><span data-stu-id="01646-141">**-F**</span></span>              | <span data-ttu-id="01646-142">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-142">-inf</span></span>     | <span data-ttu-id="01646-143">-F</span><span class="sxs-lookup"><span data-stu-id="01646-143">-F</span></span>         | <span data-ttu-id="01646-144">src0</span><span class="sxs-lookup"><span data-stu-id="01646-144">src0</span></span>        | <span data-ttu-id="01646-145">src0</span><span class="sxs-lookup"><span data-stu-id="01646-145">src0</span></span>   | <span data-ttu-id="01646-146">src0</span><span class="sxs-lookup"><span data-stu-id="01646-146">src0</span></span>   | <span data-ttu-id="01646-147">src0</span><span class="sxs-lookup"><span data-stu-id="01646-147">src0</span></span>        | <span data-ttu-id="01646-148">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="01646-148">+-F or +-0</span></span> | <span data-ttu-id="01646-149">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-149">+inf</span></span>     | <span data-ttu-id="01646-150">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-150">NaN</span></span>     |
| <span data-ttu-id="01646-151">**-dénorme**</span><span class="sxs-lookup"><span data-stu-id="01646-151">**-denorm**</span></span>         | <span data-ttu-id="01646-152">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-152">-inf</span></span>     | <span data-ttu-id="01646-153">src1</span><span class="sxs-lookup"><span data-stu-id="01646-153">src1</span></span>       | <span data-ttu-id="01646-154">-0</span><span class="sxs-lookup"><span data-stu-id="01646-154">-0</span></span>          | <span data-ttu-id="01646-155">-0</span><span class="sxs-lookup"><span data-stu-id="01646-155">-0</span></span>     | <span data-ttu-id="01646-156">+0</span><span class="sxs-lookup"><span data-stu-id="01646-156">+0</span></span>     | <span data-ttu-id="01646-157">+0</span><span class="sxs-lookup"><span data-stu-id="01646-157">+0</span></span>          | <span data-ttu-id="01646-158">src1</span><span class="sxs-lookup"><span data-stu-id="01646-158">src1</span></span>       | <span data-ttu-id="01646-159">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-159">+inf</span></span>     | <span data-ttu-id="01646-160">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-160">NaN</span></span>     |
| <span data-ttu-id="01646-161">**-0**</span><span class="sxs-lookup"><span data-stu-id="01646-161">**-0**</span></span>              | <span data-ttu-id="01646-162">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-162">-inf</span></span>     | <span data-ttu-id="01646-163">src1</span><span class="sxs-lookup"><span data-stu-id="01646-163">src1</span></span>       | <span data-ttu-id="01646-164">-0</span><span class="sxs-lookup"><span data-stu-id="01646-164">-0</span></span>          | <span data-ttu-id="01646-165">-0</span><span class="sxs-lookup"><span data-stu-id="01646-165">-0</span></span>     | <span data-ttu-id="01646-166">+0</span><span class="sxs-lookup"><span data-stu-id="01646-166">+0</span></span>     | <span data-ttu-id="01646-167">+0</span><span class="sxs-lookup"><span data-stu-id="01646-167">+0</span></span>          | <span data-ttu-id="01646-168">src1</span><span class="sxs-lookup"><span data-stu-id="01646-168">src1</span></span>       | <span data-ttu-id="01646-169">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-169">+inf</span></span>     | <span data-ttu-id="01646-170">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-170">NaN</span></span>     |
| <span data-ttu-id="01646-171">**+0**</span><span class="sxs-lookup"><span data-stu-id="01646-171">**+0**</span></span>              | <span data-ttu-id="01646-172">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-172">-inf</span></span>     | <span data-ttu-id="01646-173">src1</span><span class="sxs-lookup"><span data-stu-id="01646-173">src1</span></span>       | <span data-ttu-id="01646-174">+0</span><span class="sxs-lookup"><span data-stu-id="01646-174">+0</span></span>          | <span data-ttu-id="01646-175">+0</span><span class="sxs-lookup"><span data-stu-id="01646-175">+0</span></span>     | <span data-ttu-id="01646-176">+0</span><span class="sxs-lookup"><span data-stu-id="01646-176">+0</span></span>     | <span data-ttu-id="01646-177">+0</span><span class="sxs-lookup"><span data-stu-id="01646-177">+0</span></span>          | <span data-ttu-id="01646-178">src1</span><span class="sxs-lookup"><span data-stu-id="01646-178">src1</span></span>       | <span data-ttu-id="01646-179">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-179">+inf</span></span>     | <span data-ttu-id="01646-180">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-180">NaN</span></span>     |
| <span data-ttu-id="01646-181">**+ dénorme**</span><span class="sxs-lookup"><span data-stu-id="01646-181">**+denorm**</span></span>         | <span data-ttu-id="01646-182">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-182">-inf</span></span>     | <span data-ttu-id="01646-183">src1</span><span class="sxs-lookup"><span data-stu-id="01646-183">src1</span></span>       | <span data-ttu-id="01646-184">+0</span><span class="sxs-lookup"><span data-stu-id="01646-184">+0</span></span>          | <span data-ttu-id="01646-185">+0</span><span class="sxs-lookup"><span data-stu-id="01646-185">+0</span></span>     | <span data-ttu-id="01646-186">+0</span><span class="sxs-lookup"><span data-stu-id="01646-186">+0</span></span>     | <span data-ttu-id="01646-187">+0</span><span class="sxs-lookup"><span data-stu-id="01646-187">+0</span></span>          | <span data-ttu-id="01646-188">src1</span><span class="sxs-lookup"><span data-stu-id="01646-188">src1</span></span>       | <span data-ttu-id="01646-189">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-189">+inf</span></span>     | <span data-ttu-id="01646-190">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-190">NaN</span></span>     |
| <span data-ttu-id="01646-191">**+ F**</span><span class="sxs-lookup"><span data-stu-id="01646-191">**+F**</span></span>              | <span data-ttu-id="01646-192">-inf</span><span class="sxs-lookup"><span data-stu-id="01646-192">-inf</span></span>     | <span data-ttu-id="01646-193">+-F ou +-0</span><span class="sxs-lookup"><span data-stu-id="01646-193">+-F or +-0</span></span> | <span data-ttu-id="01646-194">src0</span><span class="sxs-lookup"><span data-stu-id="01646-194">src0</span></span>        | <span data-ttu-id="01646-195">src0</span><span class="sxs-lookup"><span data-stu-id="01646-195">src0</span></span>   | <span data-ttu-id="01646-196">src0</span><span class="sxs-lookup"><span data-stu-id="01646-196">src0</span></span>   | <span data-ttu-id="01646-197">src0</span><span class="sxs-lookup"><span data-stu-id="01646-197">src0</span></span>        | <span data-ttu-id="01646-198">+ F</span><span class="sxs-lookup"><span data-stu-id="01646-198">+F</span></span>         | <span data-ttu-id="01646-199">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-199">+inf</span></span>     | <span data-ttu-id="01646-200">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-200">NaN</span></span>     |
| <span data-ttu-id="01646-201">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="01646-201">**+inf**</span></span>            | <span data-ttu-id="01646-202">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-202">NaN</span></span>      | <span data-ttu-id="01646-203">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-203">+inf</span></span>       | <span data-ttu-id="01646-204">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-204">+inf</span></span>        | <span data-ttu-id="01646-205">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-205">+inf</span></span>   | <span data-ttu-id="01646-206">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-206">+inf</span></span>   | <span data-ttu-id="01646-207">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-207">+inf</span></span>        | <span data-ttu-id="01646-208">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-208">+inf</span></span>       | <span data-ttu-id="01646-209">+inf</span><span class="sxs-lookup"><span data-stu-id="01646-209">+inf</span></span>     | <span data-ttu-id="01646-210">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-210">NaN</span></span>     |
| <span data-ttu-id="01646-211">**NaN**</span><span class="sxs-lookup"><span data-stu-id="01646-211">**NaN**</span></span>             | <span data-ttu-id="01646-212">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-212">NaN</span></span>      | <span data-ttu-id="01646-213">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-213">NaN</span></span>        | <span data-ttu-id="01646-214">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-214">NaN</span></span>         | <span data-ttu-id="01646-215">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-215">NaN</span></span>    | <span data-ttu-id="01646-216">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-216">NaN</span></span>    | <span data-ttu-id="01646-217">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-217">NaN</span></span>         | <span data-ttu-id="01646-218">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-218">NaN</span></span>        | <span data-ttu-id="01646-219">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-219">NaN</span></span>      | <span data-ttu-id="01646-220">NaN</span><span class="sxs-lookup"><span data-stu-id="01646-220">NaN</span></span>     |



 

<span data-ttu-id="01646-221">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="01646-221">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="01646-222">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="01646-222">Vertex Shader</span></span> | <span data-ttu-id="01646-223">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="01646-223">Geometry Shader</span></span> | <span data-ttu-id="01646-224">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="01646-224">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="01646-225">x</span><span class="sxs-lookup"><span data-stu-id="01646-225">x</span></span>             | <span data-ttu-id="01646-226">x</span><span class="sxs-lookup"><span data-stu-id="01646-226">x</span></span>               | <span data-ttu-id="01646-227">x</span><span class="sxs-lookup"><span data-stu-id="01646-227">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="01646-228">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="01646-228">Minimum Shader Model</span></span>

<span data-ttu-id="01646-229">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="01646-229">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="01646-230">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="01646-230">Shader Model</span></span>                                              | <span data-ttu-id="01646-231">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="01646-231">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="01646-232">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="01646-232">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="01646-233">Oui</span><span class="sxs-lookup"><span data-stu-id="01646-233">yes</span></span>       |
| [<span data-ttu-id="01646-234">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="01646-234">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="01646-235">Oui</span><span class="sxs-lookup"><span data-stu-id="01646-235">yes</span></span>       |
| [<span data-ttu-id="01646-236">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="01646-236">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="01646-237">Oui</span><span class="sxs-lookup"><span data-stu-id="01646-237">yes</span></span>       |
| [<span data-ttu-id="01646-238">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01646-238">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="01646-239">non</span><span class="sxs-lookup"><span data-stu-id="01646-239">no</span></span>        |
| [<span data-ttu-id="01646-240">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01646-240">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="01646-241">non</span><span class="sxs-lookup"><span data-stu-id="01646-241">no</span></span>        |
| [<span data-ttu-id="01646-242">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01646-242">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="01646-243">non</span><span class="sxs-lookup"><span data-stu-id="01646-243">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="01646-244">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01646-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01646-245">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01646-245">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





