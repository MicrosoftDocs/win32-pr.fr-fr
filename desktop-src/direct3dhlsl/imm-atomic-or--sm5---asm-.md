---
title: imm_atomic_or (SM5-ASM)
description: Au niveau du bit atomique immédiat ou en mémoire. Retourne la valeur en mémoire avant ou.
ms.assetid: 0ACE977D-5D0E-4E9C-A49F-B81D789B0D43
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2bc3b9afd2ba9f4dc63a8fb5c5818c1121c7ec6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030600"
---
# <a name="imm_atomic_or-sm5---asm"></a><span data-ttu-id="9d158-104">IMM \_ Atomic \_ ou (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9d158-104">imm\_atomic\_or (sm5 - asm)</span></span>

<span data-ttu-id="9d158-105">Au niveau du bit atomique immédiat ou en mémoire.</span><span class="sxs-lookup"><span data-stu-id="9d158-105">Immediate atomic bitwise OR to memory.</span></span> <span data-ttu-id="9d158-106">Retourne la valeur en mémoire avant ou.</span><span class="sxs-lookup"><span data-stu-id="9d158-106">Returns the value in memory before the OR.</span></span>



| <span data-ttu-id="9d158-107">IMM \_ Atomic \_ ou dst0 \[ . \_ \_ masque de composant unique \] , dst1, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="9d158-107">imm\_atomic\_or dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9d158-108">Élément</span><span class="sxs-lookup"><span data-stu-id="9d158-108">Item</span></span>                                                                                                           | <span data-ttu-id="9d158-109">Description</span><span class="sxs-lookup"><span data-stu-id="9d158-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d158-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="9d158-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="9d158-111">\[dans \] contient la valeur de *DST1* avant ou.</span><span class="sxs-lookup"><span data-stu-id="9d158-111">\[in\] Contains the value from *dst1* before the OR.</span></span><br/>                                                                   |
| <span data-ttu-id="9d158-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="9d158-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="9d158-113">\[dans \] un affichage d’accès non ordonné (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="9d158-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="9d158-114">Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="9d158-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="9d158-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="9d158-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="9d158-116">\[dans \] l’adresse mémoire.</span><span class="sxs-lookup"><span data-stu-id="9d158-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="9d158-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9d158-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="9d158-118">Valeur à ou avec *dst1*.</span><span class="sxs-lookup"><span data-stu-id="9d158-118">The value to OR with *dst1*.</span></span><br/>                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="9d158-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9d158-119">Remarks</span></span>

<span data-ttu-id="9d158-120">Cette instruction effectue un seul composant au niveau du bit 32 bits ou d’un opérande *src0* avec *dst1* à 32 bits par adresse de composant *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="9d158-120">This instruction performs a single component 32-bit bitwise OR of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="9d158-121">Si *dst1* est un u \# , il a peut-être été déclaré comme brut, typé ou structuré.</span><span class="sxs-lookup"><span data-stu-id="9d158-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="9d158-122">Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .</span><span class="sxs-lookup"><span data-stu-id="9d158-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="9d158-123">Si *dst1* est g \# , il doit être déclaré comme RAW ou Structured.</span><span class="sxs-lookup"><span data-stu-id="9d158-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="9d158-124">La valeur dans *dst1* Memory avant ou est retournée à *dst0*.</span><span class="sxs-lookup"><span data-stu-id="9d158-124">The value in *dst1* memory before the OR is returned to *dst0*.</span></span>

<span data-ttu-id="9d158-125">La totalité de l’opération est effectuée atomiquement.</span><span class="sxs-lookup"><span data-stu-id="9d158-125">The entire operation is performed atomically.</span></span>

<span data-ttu-id="9d158-126">Le nombre de composants pris à partir de l’adresse est déterminé par la dimensionnalité de la ressource déclarée sur *dst1*.</span><span class="sxs-lookup"><span data-stu-id="9d158-126">The number of components taken from the address is determined by the dimensionality of the resource declared at *dst1*.</span></span>

<span data-ttu-id="9d158-127">Si l’appel du nuanceur est inactif, par exemple si le pixel a été ignoré plus tôt dans son exécution, ou s’il n’existe qu’un appel d’assistance à un réel pixel/échantillon pour les dérivés, cette instruction ne modifie pas le tout la mémoire *dst1* , et la valeur retournée n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="9d158-127">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="9d158-128">L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, alors que le contenu entier du UAV devient non défini.</span><span class="sxs-lookup"><span data-stu-id="9d158-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="9d158-129">L’adressage hors limites sur u \# ou g \# entraîne le retour d’un résultat non défini au nuanceur dans *dst0*.</span><span class="sxs-lookup"><span data-stu-id="9d158-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="9d158-130">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="9d158-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9d158-131">Sommet</span><span class="sxs-lookup"><span data-stu-id="9d158-131">Vertex</span></span> | <span data-ttu-id="9d158-132">Forme</span><span class="sxs-lookup"><span data-stu-id="9d158-132">Hull</span></span> | <span data-ttu-id="9d158-133">Domain</span><span class="sxs-lookup"><span data-stu-id="9d158-133">Domain</span></span> | <span data-ttu-id="9d158-134">Géométrie</span><span class="sxs-lookup"><span data-stu-id="9d158-134">Geometry</span></span> | <span data-ttu-id="9d158-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="9d158-135">Pixel</span></span> | <span data-ttu-id="9d158-136">Compute</span><span class="sxs-lookup"><span data-stu-id="9d158-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9d158-137">X</span><span class="sxs-lookup"><span data-stu-id="9d158-137">X</span></span>     | <span data-ttu-id="9d158-138">X</span><span class="sxs-lookup"><span data-stu-id="9d158-138">X</span></span>       |



 

<span data-ttu-id="9d158-139">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9d158-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="9d158-140">Sommet</span><span class="sxs-lookup"><span data-stu-id="9d158-140">Vertex</span></span> | <span data-ttu-id="9d158-141">Forme</span><span class="sxs-lookup"><span data-stu-id="9d158-141">Hull</span></span> | <span data-ttu-id="9d158-142">Domain</span><span class="sxs-lookup"><span data-stu-id="9d158-142">Domain</span></span> | <span data-ttu-id="9d158-143">Géométrie</span><span class="sxs-lookup"><span data-stu-id="9d158-143">Geometry</span></span> | <span data-ttu-id="9d158-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="9d158-144">Pixel</span></span> | <span data-ttu-id="9d158-145">Compute</span><span class="sxs-lookup"><span data-stu-id="9d158-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9d158-146">X</span><span class="sxs-lookup"><span data-stu-id="9d158-146">X</span></span>      | <span data-ttu-id="9d158-147">X</span><span class="sxs-lookup"><span data-stu-id="9d158-147">X</span></span>    | <span data-ttu-id="9d158-148">X</span><span class="sxs-lookup"><span data-stu-id="9d158-148">X</span></span>      | <span data-ttu-id="9d158-149">X</span><span class="sxs-lookup"><span data-stu-id="9d158-149">X</span></span>        | <span data-ttu-id="9d158-150">X</span><span class="sxs-lookup"><span data-stu-id="9d158-150">X</span></span>     | <span data-ttu-id="9d158-151">X</span><span class="sxs-lookup"><span data-stu-id="9d158-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9d158-152">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9d158-152">Minimum Shader Model</span></span>

<span data-ttu-id="9d158-153">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="9d158-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9d158-154">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9d158-154">Shader Model</span></span>                                              | <span data-ttu-id="9d158-155">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="9d158-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9d158-156">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9d158-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9d158-157">Oui</span><span class="sxs-lookup"><span data-stu-id="9d158-157">yes</span></span>       |
| [<span data-ttu-id="9d158-158">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="9d158-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9d158-159">non</span><span class="sxs-lookup"><span data-stu-id="9d158-159">no</span></span>        |
| [<span data-ttu-id="9d158-160">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="9d158-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9d158-161">non</span><span class="sxs-lookup"><span data-stu-id="9d158-161">no</span></span>        |
| [<span data-ttu-id="9d158-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d158-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9d158-163">non</span><span class="sxs-lookup"><span data-stu-id="9d158-163">no</span></span>        |
| [<span data-ttu-id="9d158-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d158-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9d158-165">non</span><span class="sxs-lookup"><span data-stu-id="9d158-165">no</span></span>        |
| [<span data-ttu-id="9d158-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d158-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9d158-167">non</span><span class="sxs-lookup"><span data-stu-id="9d158-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9d158-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d158-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d158-169">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d158-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





