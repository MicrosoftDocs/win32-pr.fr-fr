---
title: imm_atomic_imax (SM5-ASM)
description: Max signed atomique max. de la mémoire. Retourne la valeur en mémoire avant l’opération max.
ms.assetid: 360E542C-F3F6-4103-8A22-4914A5103D17
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8143073065955a00df412ecf453cc523d7e98493
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940571"
---
# <a name="imm_atomic_imax-sm5---asm"></a><span data-ttu-id="f5866-104">IMM \_ Atomic \_ IMAX (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f5866-104">imm\_atomic\_imax (sm5 - asm)</span></span>

<span data-ttu-id="f5866-105">Max signed atomique max. de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f5866-105">Immediate atomic signed max to memory.</span></span> <span data-ttu-id="f5866-106">Retourne la valeur en mémoire avant l’opération max.</span><span class="sxs-lookup"><span data-stu-id="f5866-106">Returns value in memory before the max operation.</span></span>



| <span data-ttu-id="f5866-107">IMM \_ Atomic \_ IMAX dst0 \[ . \_ \_ masque de composant unique \] , dst1, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="f5866-107">imm\_atomic\_imax dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f5866-108">Élément</span><span class="sxs-lookup"><span data-stu-id="f5866-108">Item</span></span>                                                                                                           | <span data-ttu-id="f5866-109">Description</span><span class="sxs-lookup"><span data-stu-id="f5866-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5866-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="f5866-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="f5866-111">\[dans \] contient la valeur de *dst1* avant cette instruction.</span><span class="sxs-lookup"><span data-stu-id="f5866-111">\[in\] Contains the value from *dst1* before this instruction.</span></span><br/>                                                         |
| <span data-ttu-id="f5866-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="f5866-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="f5866-113">\[dans \] un affichage d’accès non ordonné (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="f5866-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="f5866-114">Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="f5866-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="f5866-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="f5866-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="f5866-116">\[dans \] l’adresse mémoire.</span><span class="sxs-lookup"><span data-stu-id="f5866-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="f5866-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f5866-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="f5866-118">\[dans \] la valeur à comparer à *Dst1* sur *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="f5866-118">\[in\] The value to compare to *dst1* at *dstAddress*.</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="f5866-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f5866-119">Remarks</span></span>

<span data-ttu-id="f5866-120">Cette instruction effectue un composant unique signé 32 bits *src0* avec *dst1* à 32 bits par adresse de composant *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="f5866-120">This instruction performs a single component 32-bit signed maximum of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="f5866-121">Si *dst1* est un u \# , il a peut-être été déclaré comme brut, typé ou structuré.</span><span class="sxs-lookup"><span data-stu-id="f5866-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="f5866-122">Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .</span><span class="sxs-lookup"><span data-stu-id="f5866-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="f5866-123">Si *dst1* est g \# , il doit être déclaré comme RAW ou Structured.</span><span class="sxs-lookup"><span data-stu-id="f5866-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="f5866-124">La valeur dans *dst1* Memory avant Max est retournée à *dst0*.</span><span class="sxs-lookup"><span data-stu-id="f5866-124">The value in *dst1* memory before max is returned to *dst0*.</span></span>

<span data-ttu-id="f5866-125">Le nombre de composants pris à partir de l’adresse est déterminé par la dimensionnalité de *dst1*.</span><span class="sxs-lookup"><span data-stu-id="f5866-125">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="f5866-126">La totalité de l’opération est effectuée atomiquement.</span><span class="sxs-lookup"><span data-stu-id="f5866-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="f5866-127">Si l’appel du nuanceur est inactif, par exemple si le pixel a été ignoré plus tôt dans son exécution, ou s’il n’existe qu’un appel d’assistance à un réel pixel/échantillon pour les dérivés, cette instruction ne modifie pas le tout la mémoire *dst1* , et la valeur retournée n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="f5866-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="f5866-128">L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, alors que le contenu entier du UAV devient non défini.</span><span class="sxs-lookup"><span data-stu-id="f5866-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="f5866-129">L’adressage hors limites sur u \# ou g \# entraîne le retour d’un résultat non défini au nuanceur dans *dst0*.</span><span class="sxs-lookup"><span data-stu-id="f5866-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="f5866-130">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="f5866-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f5866-131">Sommet</span><span class="sxs-lookup"><span data-stu-id="f5866-131">Vertex</span></span> | <span data-ttu-id="f5866-132">Forme</span><span class="sxs-lookup"><span data-stu-id="f5866-132">Hull</span></span> | <span data-ttu-id="f5866-133">Domain</span><span class="sxs-lookup"><span data-stu-id="f5866-133">Domain</span></span> | <span data-ttu-id="f5866-134">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f5866-134">Geometry</span></span> | <span data-ttu-id="f5866-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="f5866-135">Pixel</span></span> | <span data-ttu-id="f5866-136">Compute</span><span class="sxs-lookup"><span data-stu-id="f5866-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f5866-137">X</span><span class="sxs-lookup"><span data-stu-id="f5866-137">X</span></span>     | <span data-ttu-id="f5866-138">X</span><span class="sxs-lookup"><span data-stu-id="f5866-138">X</span></span>       |



 

<span data-ttu-id="f5866-139">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f5866-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="f5866-140">Sommet</span><span class="sxs-lookup"><span data-stu-id="f5866-140">Vertex</span></span> | <span data-ttu-id="f5866-141">Forme</span><span class="sxs-lookup"><span data-stu-id="f5866-141">Hull</span></span> | <span data-ttu-id="f5866-142">Domain</span><span class="sxs-lookup"><span data-stu-id="f5866-142">Domain</span></span> | <span data-ttu-id="f5866-143">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f5866-143">Geometry</span></span> | <span data-ttu-id="f5866-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="f5866-144">Pixel</span></span> | <span data-ttu-id="f5866-145">Compute</span><span class="sxs-lookup"><span data-stu-id="f5866-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f5866-146">X</span><span class="sxs-lookup"><span data-stu-id="f5866-146">X</span></span>      | <span data-ttu-id="f5866-147">X</span><span class="sxs-lookup"><span data-stu-id="f5866-147">X</span></span>    | <span data-ttu-id="f5866-148">X</span><span class="sxs-lookup"><span data-stu-id="f5866-148">X</span></span>      | <span data-ttu-id="f5866-149">X</span><span class="sxs-lookup"><span data-stu-id="f5866-149">X</span></span>        | <span data-ttu-id="f5866-150">X</span><span class="sxs-lookup"><span data-stu-id="f5866-150">X</span></span>     | <span data-ttu-id="f5866-151">X</span><span class="sxs-lookup"><span data-stu-id="f5866-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f5866-152">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f5866-152">Minimum Shader Model</span></span>

<span data-ttu-id="f5866-153">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="f5866-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f5866-154">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f5866-154">Shader Model</span></span>                                              | <span data-ttu-id="f5866-155">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f5866-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f5866-156">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f5866-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f5866-157">Oui</span><span class="sxs-lookup"><span data-stu-id="f5866-157">yes</span></span>       |
| [<span data-ttu-id="f5866-158">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="f5866-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f5866-159">non</span><span class="sxs-lookup"><span data-stu-id="f5866-159">no</span></span>        |
| [<span data-ttu-id="f5866-160">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f5866-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f5866-161">non</span><span class="sxs-lookup"><span data-stu-id="f5866-161">no</span></span>        |
| [<span data-ttu-id="f5866-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5866-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f5866-163">non</span><span class="sxs-lookup"><span data-stu-id="f5866-163">no</span></span>        |
| [<span data-ttu-id="f5866-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5866-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f5866-165">non</span><span class="sxs-lookup"><span data-stu-id="f5866-165">no</span></span>        |
| [<span data-ttu-id="f5866-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5866-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f5866-167">non</span><span class="sxs-lookup"><span data-stu-id="f5866-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f5866-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f5866-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5866-169">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5866-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





