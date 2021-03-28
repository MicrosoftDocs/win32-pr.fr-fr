---
title: imm_atomic_umin (SM5-ASM)
description: Min non signé atomique immédiat en mémoire. Retourne la valeur en mémoire avant l’opération max.
ms.assetid: B4556DA0-EE34-4420-A3AE-B340B4B1EB83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8c65b2b5a58859e0729f567d9575f889b589821
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030560"
---
# <a name="imm_atomic_umin-sm5---asm"></a><span data-ttu-id="f1c8a-104">IMM \_ Atomic \_ Umin (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f1c8a-104">imm\_atomic\_umin (sm5 - asm)</span></span>

<span data-ttu-id="f1c8a-105">Min non signé atomique immédiat en mémoire.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-105">Immediate atomic unsigned min to memory.</span></span> <span data-ttu-id="f1c8a-106">Retourne la valeur en mémoire avant l’opération max.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-106">Returns value in memory before the max operation.</span></span>



| <span data-ttu-id="f1c8a-107">IMM \_ Atomic \_ Umin dst0 \[ . \_ \_ masque de composant unique \] , dst1, dstAddress \[ . Swizzle \] , src0 \[ . Sélectionner un \_ composant\]</span><span class="sxs-lookup"><span data-stu-id="f1c8a-107">imm\_atomic\_umin dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f1c8a-108">Élément</span><span class="sxs-lookup"><span data-stu-id="f1c8a-108">Item</span></span>                                                                                                           | <span data-ttu-id="f1c8a-109">Description</span><span class="sxs-lookup"><span data-stu-id="f1c8a-109">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c8a-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="f1c8a-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="f1c8a-111">\[dans \] contient la valeur de *dst1* avant cette instruction.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-111">\[in\] Contains the value from *dst1* before this instruction.</span></span><br/>                                                         |
| <span data-ttu-id="f1c8a-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="f1c8a-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="f1c8a-113">\[dans \] un affichage d’accès non ordonné (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="f1c8a-113">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="f1c8a-114">Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="f1c8a-114">In the compute shader this can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="f1c8a-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="f1c8a-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="f1c8a-116">\[dans \] l’adresse mémoire.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-116">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="f1c8a-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f1c8a-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="f1c8a-118">\[dans \] la valeur à comparer à *Dst1* sur *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-118">\[in\] The value to compare to *dst1* at *dstAddress*.</span></span><br/>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="f1c8a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f1c8a-119">Remarks</span></span>

<span data-ttu-id="f1c8a-120">Cette instruction exécute un seul composant 32 bits non signé de l’opérande *src0* avec *dst1* à 32 bits par adresse de composant *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-120">This instruction performs a single component 32-bit unsigned minimum of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="f1c8a-121">Si *dst1* est un u \# , il a peut-être été déclaré comme brut, typé ou structuré.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-121">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="f1c8a-122">Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .</span><span class="sxs-lookup"><span data-stu-id="f1c8a-122">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="f1c8a-123">Si *dst1* est g \# , il doit être déclaré comme RAW ou Structured.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-123">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="f1c8a-124">La valeur de la mémoire *dst1* avant min est retournée à *dst0*.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-124">The value in *dst1* memory before min is returned to *dst0*.</span></span>

<span data-ttu-id="f1c8a-125">Le nombre de composants pris à partir de l’adresse est déterminé par la dimensionnalité de *dst1*.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-125">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="f1c8a-126">La totalité de l’opération est effectuée atomiquement.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-126">The entire operation is performed atomically.</span></span>

<span data-ttu-id="f1c8a-127">Si l’appel du nuanceur est inactif, par exemple si le pixel qui a été ignoré précédemment dans son exécution, ou un appel pixel/échantillon n’existe que pour servir d’assistance à un réel pixel/échantillon pour les dérivés, cette instruction ne modifie pas du tout la mémoire *dst1* , et la valeur retournée n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-127">If the shader invocation is inactive, for example if the pixel having been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="f1c8a-128">L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, alors que le contenu entier du UAV devient non défini.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-128">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="f1c8a-129">L’adressage hors limites sur u \# ou g \# entraîne le retour d’un résultat non défini au nuanceur dans *dst0*.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-129">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="f1c8a-130">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="f1c8a-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f1c8a-131">Sommet</span><span class="sxs-lookup"><span data-stu-id="f1c8a-131">Vertex</span></span> | <span data-ttu-id="f1c8a-132">Forme</span><span class="sxs-lookup"><span data-stu-id="f1c8a-132">Hull</span></span> | <span data-ttu-id="f1c8a-133">Domain</span><span class="sxs-lookup"><span data-stu-id="f1c8a-133">Domain</span></span> | <span data-ttu-id="f1c8a-134">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f1c8a-134">Geometry</span></span> | <span data-ttu-id="f1c8a-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="f1c8a-135">Pixel</span></span> | <span data-ttu-id="f1c8a-136">Compute</span><span class="sxs-lookup"><span data-stu-id="f1c8a-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f1c8a-137">X</span><span class="sxs-lookup"><span data-stu-id="f1c8a-137">X</span></span>     | <span data-ttu-id="f1c8a-138">X</span><span class="sxs-lookup"><span data-stu-id="f1c8a-138">X</span></span>       |



 

<span data-ttu-id="f1c8a-139">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f1c8a-139">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="f1c8a-140">Sommet</span><span class="sxs-lookup"><span data-stu-id="f1c8a-140">Vertex</span></span> | <span data-ttu-id="f1c8a-141">Forme</span><span class="sxs-lookup"><span data-stu-id="f1c8a-141">Hull</span></span> | <span data-ttu-id="f1c8a-142">Domain</span><span class="sxs-lookup"><span data-stu-id="f1c8a-142">Domain</span></span> | <span data-ttu-id="f1c8a-143">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f1c8a-143">Geometry</span></span> | <span data-ttu-id="f1c8a-144">Pixel</span><span class="sxs-lookup"><span data-stu-id="f1c8a-144">Pixel</span></span> | <span data-ttu-id="f1c8a-145">Compute</span><span class="sxs-lookup"><span data-stu-id="f1c8a-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f1c8a-146">X</span><span class="sxs-lookup"><span data-stu-id="f1c8a-146">X</span></span>      | <span data-ttu-id="f1c8a-147">X</span><span class="sxs-lookup"><span data-stu-id="f1c8a-147">X</span></span>    | <span data-ttu-id="f1c8a-148">X</span><span class="sxs-lookup"><span data-stu-id="f1c8a-148">X</span></span>      | <span data-ttu-id="f1c8a-149">X</span><span class="sxs-lookup"><span data-stu-id="f1c8a-149">X</span></span>        | <span data-ttu-id="f1c8a-150">X</span><span class="sxs-lookup"><span data-stu-id="f1c8a-150">X</span></span>     | <span data-ttu-id="f1c8a-151">X</span><span class="sxs-lookup"><span data-stu-id="f1c8a-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f1c8a-152">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f1c8a-152">Minimum Shader Model</span></span>

<span data-ttu-id="f1c8a-153">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="f1c8a-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f1c8a-154">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f1c8a-154">Shader Model</span></span>                                              | <span data-ttu-id="f1c8a-155">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f1c8a-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f1c8a-156">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f1c8a-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f1c8a-157">Oui</span><span class="sxs-lookup"><span data-stu-id="f1c8a-157">yes</span></span>       |
| [<span data-ttu-id="f1c8a-158">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="f1c8a-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f1c8a-159">non</span><span class="sxs-lookup"><span data-stu-id="f1c8a-159">no</span></span>        |
| [<span data-ttu-id="f1c8a-160">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f1c8a-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f1c8a-161">non</span><span class="sxs-lookup"><span data-stu-id="f1c8a-161">no</span></span>        |
| [<span data-ttu-id="f1c8a-162">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f1c8a-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f1c8a-163">non</span><span class="sxs-lookup"><span data-stu-id="f1c8a-163">no</span></span>        |
| [<span data-ttu-id="f1c8a-164">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f1c8a-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f1c8a-165">non</span><span class="sxs-lookup"><span data-stu-id="f1c8a-165">no</span></span>        |
| [<span data-ttu-id="f1c8a-166">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f1c8a-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f1c8a-167">non</span><span class="sxs-lookup"><span data-stu-id="f1c8a-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f1c8a-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f1c8a-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c8a-169">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f1c8a-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





