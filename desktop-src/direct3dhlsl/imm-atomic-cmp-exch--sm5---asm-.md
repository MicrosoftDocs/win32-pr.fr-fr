---
title: imm_atomic_cmp_exch (SM5-ASM)
description: Comparer et échanger immédiatement avec la mémoire.
ms.assetid: 317A69E1-0E0A-45C8-8E0A-B88659ADBECC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63e1be030d7cce0d6f0a581788db39a599272b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841685"
---
# <a name="imm_atomic_cmp_exch-sm5---asm"></a><span data-ttu-id="e1464-103">IMM \_ Atomic \_ CMP \_ Exch (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e1464-103">imm\_atomic\_cmp\_exch (sm5 - asm)</span></span>

<span data-ttu-id="e1464-104">Comparer et échanger immédiatement avec la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e1464-104">Immediate compare and exchange to memory.</span></span>



| <span data-ttu-id="e1464-105">IMM \_ Atomic \_ CMP \_ Exch dst0 \[ . \_ \_ masque de composant unique \] , dst1, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ \] , src1 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="e1464-105">imm\_atomic\_cmp\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\], src1\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e1464-106">Élément</span><span class="sxs-lookup"><span data-stu-id="e1464-106">Item</span></span>                                                                                                           | <span data-ttu-id="e1464-107">Description</span><span class="sxs-lookup"><span data-stu-id="e1464-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1464-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="e1464-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="e1464-109">\[out \] contient *dst1* avant l’écriture.</span><span class="sxs-lookup"><span data-stu-id="e1464-109">\[out\] Contains *dst1* before the write.</span></span><br/>                                                                              |
| <span data-ttu-id="e1464-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="e1464-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="e1464-111">\[dans \] un affichage d’accès non ordonné (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="e1464-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="e1464-112">Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="e1464-112">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="e1464-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="e1464-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="e1464-114">\[dans \] la mémoire de destination.</span><span class="sxs-lookup"><span data-stu-id="e1464-114">\[in\] The destination memory.</span></span><br/>                                                                                         |
| <span data-ttu-id="e1464-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e1464-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="e1464-116">\[dans \] la valeur à comparer à *dst1*.</span><span class="sxs-lookup"><span data-stu-id="e1464-116">\[in\] The value to compare to *dst1*.</span></span><br/>                                                                                 |
| <span data-ttu-id="e1464-117"><span id="scr1"></span><span id="SCR1"></span>*scr1*</span><span class="sxs-lookup"><span data-stu-id="e1464-117"><span id="scr1"></span><span id="SCR1"></span>*scr1*</span></span><br/>                                                | <span data-ttu-id="e1464-118">\[dans \] la valeur écrite dans la mémoire de destination si les valeurs comparées sont identiques.</span><span class="sxs-lookup"><span data-stu-id="e1464-118">\[in\] The value written to the destination memory if the compared values are identical.</span></span><br/>                               |



 

<span data-ttu-id="e1464-119">Cette instruction effectue une comparaison de valeurs 32 bits de composant unique avec l’opérande *src0* avec *dst1* à 32 bits par adresse de composant *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="e1464-119">This instruction performs a single component 32-bit value compare of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="e1464-120">Si *dst1* est un u \# , il a peut-être été déclaré comme brut, typé ou structuré.</span><span class="sxs-lookup"><span data-stu-id="e1464-120">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="e1464-121">Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .</span><span class="sxs-lookup"><span data-stu-id="e1464-121">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="e1464-122">Si *dst1* est g \# , il doit être déclaré comme RAW ou Structured.</span><span class="sxs-lookup"><span data-stu-id="e1464-122">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="e1464-123">Si les valeurs comparées sont identiques, la valeur 32 bits d’un seul composant dans *src1* est écrite dans la mémoire de destination.</span><span class="sxs-lookup"><span data-stu-id="e1464-123">If the compared values are identical, the single-component 32-bit value in *src1* is written to the destination memory.</span></span> <span data-ttu-id="e1464-124">Dans le cas contraire, la mémoire de destination n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="e1464-124">Otherwise, the destination memory is not changed.</span></span>

<span data-ttu-id="e1464-125">La valeur 32 bits d’origine dans la mémoire de destination est toujours écrite dans *dst0*.</span><span class="sxs-lookup"><span data-stu-id="e1464-125">The original 32-bit value in the destination memory is always written to *dst0*.</span></span>

<span data-ttu-id="e1464-126">La totalité de l’opération est effectuée atomiquement.</span><span class="sxs-lookup"><span data-stu-id="e1464-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="e1464-127">Si l’appel du nuanceur est inactif, par exemple si le pixel a été ignoré plus tôt dans son exécution, ou s’il n’existe qu’un appel d’assistance à un réel pixel/échantillon pour les dérivés, cette instruction ne modifie pas le tout la mémoire *dst1* , et la valeur retournée n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="e1464-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="e1464-128">L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, alors que le contenu entier du UAV devient non défini.</span><span class="sxs-lookup"><span data-stu-id="e1464-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="e1464-129">L’adressage hors limites sur u \# ou g \# entraîne le retour d’un résultat non défini au nuanceur dans *dst0*.</span><span class="sxs-lookup"><span data-stu-id="e1464-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="e1464-130">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="e1464-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e1464-131">Sommet</span><span class="sxs-lookup"><span data-stu-id="e1464-131">Vertex</span></span> | <span data-ttu-id="e1464-132">Forme</span><span class="sxs-lookup"><span data-stu-id="e1464-132">Hull</span></span> | <span data-ttu-id="e1464-133">Domain</span><span class="sxs-lookup"><span data-stu-id="e1464-133">Domain</span></span> | <span data-ttu-id="e1464-134">Géométrie</span><span class="sxs-lookup"><span data-stu-id="e1464-134">Geometry</span></span> | <span data-ttu-id="e1464-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="e1464-135">Pixel</span></span> | <span data-ttu-id="e1464-136">Compute</span><span class="sxs-lookup"><span data-stu-id="e1464-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e1464-137">X</span><span class="sxs-lookup"><span data-stu-id="e1464-137">X</span></span>     | <span data-ttu-id="e1464-138">X</span><span class="sxs-lookup"><span data-stu-id="e1464-138">X</span></span>       |



 

<span data-ttu-id="e1464-139">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e1464-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="e1464-140">Sommet</span><span class="sxs-lookup"><span data-stu-id="e1464-140">Vertex</span></span> | <span data-ttu-id="e1464-141">Forme</span><span class="sxs-lookup"><span data-stu-id="e1464-141">Hull</span></span> | <span data-ttu-id="e1464-142">Domain</span><span class="sxs-lookup"><span data-stu-id="e1464-142">Domain</span></span> | <span data-ttu-id="e1464-143">Géométrie</span><span class="sxs-lookup"><span data-stu-id="e1464-143">Geometry</span></span> | <span data-ttu-id="e1464-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="e1464-144">Pixel</span></span> | <span data-ttu-id="e1464-145">Compute</span><span class="sxs-lookup"><span data-stu-id="e1464-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e1464-146">X</span><span class="sxs-lookup"><span data-stu-id="e1464-146">X</span></span>      | <span data-ttu-id="e1464-147">X</span><span class="sxs-lookup"><span data-stu-id="e1464-147">X</span></span>    | <span data-ttu-id="e1464-148">X</span><span class="sxs-lookup"><span data-stu-id="e1464-148">X</span></span>      | <span data-ttu-id="e1464-149">X</span><span class="sxs-lookup"><span data-stu-id="e1464-149">X</span></span>        | <span data-ttu-id="e1464-150">X</span><span class="sxs-lookup"><span data-stu-id="e1464-150">X</span></span>     | <span data-ttu-id="e1464-151">X</span><span class="sxs-lookup"><span data-stu-id="e1464-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e1464-152">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="e1464-152">Minimum Shader Model</span></span>

<span data-ttu-id="e1464-153">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="e1464-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e1464-154">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="e1464-154">Shader Model</span></span>                                              | <span data-ttu-id="e1464-155">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="e1464-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e1464-156">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="e1464-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e1464-157">Oui</span><span class="sxs-lookup"><span data-stu-id="e1464-157">yes</span></span>       |
| [<span data-ttu-id="e1464-158">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="e1464-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e1464-159">non</span><span class="sxs-lookup"><span data-stu-id="e1464-159">no</span></span>        |
| [<span data-ttu-id="e1464-160">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="e1464-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e1464-161">non</span><span class="sxs-lookup"><span data-stu-id="e1464-161">no</span></span>        |
| [<span data-ttu-id="e1464-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1464-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e1464-163">non</span><span class="sxs-lookup"><span data-stu-id="e1464-163">no</span></span>        |
| [<span data-ttu-id="e1464-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1464-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e1464-165">non</span><span class="sxs-lookup"><span data-stu-id="e1464-165">no</span></span>        |
| [<span data-ttu-id="e1464-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1464-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e1464-167">non</span><span class="sxs-lookup"><span data-stu-id="e1464-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e1464-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1464-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1464-169">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1464-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





