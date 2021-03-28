---
title: imm_atomic_exch (SM5-ASM)
description: Échange atomique immédiat vers la mémoire.
ms.assetid: D06AE57E-52A4-4579-84FF-7DE9E713A5E3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb38cd696af079c5ae7dc896db619b95dd1d1d6c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101097"
---
# <a name="imm_atomic_exch-sm5---asm"></a><span data-ttu-id="36dfa-103">IMM \_ Atomic \_ Exch (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="36dfa-103">imm\_atomic\_exch (sm5 - asm)</span></span>

<span data-ttu-id="36dfa-104">Échange atomique immédiat vers la mémoire.</span><span class="sxs-lookup"><span data-stu-id="36dfa-104">Immediate atomic exchange to memory.</span></span>



| <span data-ttu-id="36dfa-105">IMM \_ Atomic \_ Exch dst0 \[ . unique \_ \_ masque \] de composant, dst1, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="36dfa-105">imm\_atomic\_exch dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="36dfa-106">Élément</span><span class="sxs-lookup"><span data-stu-id="36dfa-106">Item</span></span>                                                                                                           | <span data-ttu-id="36dfa-107">Description</span><span class="sxs-lookup"><span data-stu-id="36dfa-107">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36dfa-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="36dfa-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="36dfa-109">\[dans \] contient la valeur de *dst1* avant l’écriture.</span><span class="sxs-lookup"><span data-stu-id="36dfa-109">\[in\] Contains the value from *dst1* before the write.</span></span><br/>                                                                |
| <span data-ttu-id="36dfa-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="36dfa-110"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="36dfa-111">\[dans \] un affichage d’accès non ordonné (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="36dfa-111">\[in\] An unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="36dfa-112">Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="36dfa-112">In the Compute Shader this can also be Thread Group Shared Memory (g\#).</span></span> <br/> |
| <span data-ttu-id="36dfa-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="36dfa-113"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="36dfa-114">\[dans \] l’adresse mémoire.</span><span class="sxs-lookup"><span data-stu-id="36dfa-114">\[in\] The memory address.</span></span><br/>                                                                                             |
| <span data-ttu-id="36dfa-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="36dfa-115"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="36dfa-116">\[dans \] la valeur à écrire dans *Dst1* sur *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="36dfa-116">\[in\] The value to write to *dst1* at *dstAddress*.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="36dfa-117">Notes</span><span class="sxs-lookup"><span data-stu-id="36dfa-117">Remarks</span></span>

<span data-ttu-id="36dfa-118">Cette instruction effectue une écriture d’une valeur de composant unique de 32 bits d’opérande *src0* à *dst1* à 32 bits par adresse de composant *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="36dfa-118">This instruction performs a single component 32-bit value write of operand *src0* to *dst1* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="36dfa-119">Si *dst1* est un u \# , il a peut-être été déclaré comme brut, typé ou structuré.</span><span class="sxs-lookup"><span data-stu-id="36dfa-119">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="36dfa-120">Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .</span><span class="sxs-lookup"><span data-stu-id="36dfa-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="36dfa-121">Si *dst1* est g \# , il doit être déclaré comme RAW ou Structured.</span><span class="sxs-lookup"><span data-stu-id="36dfa-121">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="36dfa-122">Le nombre de composants pris à partir de l’adresse est déterminé par la dimensionnalité de la ressource déclarée sur *dst1*.</span><span class="sxs-lookup"><span data-stu-id="36dfa-122">The number of components taken from the address is determined by the dimensionality of the resource declared at *dst1*.</span></span>

<span data-ttu-id="36dfa-123">La valeur 32 bits d’origine dans la mémoire de destination est écrite dans *dst0*.</span><span class="sxs-lookup"><span data-stu-id="36dfa-123">The original 32-bit value in the destination memory is written to *dst0*.</span></span>

<span data-ttu-id="36dfa-124">La totalité de l’opération est effectuée atomiquement.</span><span class="sxs-lookup"><span data-stu-id="36dfa-124">The entire operation is performed atomically.</span></span>

<span data-ttu-id="36dfa-125">Si l’appel du nuanceur est inactif, par exemple si le pixel a été ignoré plus tôt dans son exécution, ou s’il n’existe qu’un appel d’assistance à un réel pixel/échantillon pour les dérivés, cette instruction ne modifie pas le tout la mémoire *dst1* , et la valeur retournée n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="36dfa-125">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="36dfa-126">L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, alors que le contenu entier du UAV devient non défini.</span><span class="sxs-lookup"><span data-stu-id="36dfa-126">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="36dfa-127">L’adressage hors limites sur u \# ou g \# entraîne le retour d’un résultat non défini au nuanceur dans *dst0*.</span><span class="sxs-lookup"><span data-stu-id="36dfa-127">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="36dfa-128">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="36dfa-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="36dfa-129">Sommet</span><span class="sxs-lookup"><span data-stu-id="36dfa-129">Vertex</span></span> | <span data-ttu-id="36dfa-130">Forme</span><span class="sxs-lookup"><span data-stu-id="36dfa-130">Hull</span></span> | <span data-ttu-id="36dfa-131">Domain</span><span class="sxs-lookup"><span data-stu-id="36dfa-131">Domain</span></span> | <span data-ttu-id="36dfa-132">Géométrie</span><span class="sxs-lookup"><span data-stu-id="36dfa-132">Geometry</span></span> | <span data-ttu-id="36dfa-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="36dfa-133">Pixel</span></span> | <span data-ttu-id="36dfa-134">Compute</span><span class="sxs-lookup"><span data-stu-id="36dfa-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="36dfa-135">X</span><span class="sxs-lookup"><span data-stu-id="36dfa-135">X</span></span>     | <span data-ttu-id="36dfa-136">X</span><span class="sxs-lookup"><span data-stu-id="36dfa-136">X</span></span>       |



 

<span data-ttu-id="36dfa-137">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="36dfa-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="36dfa-138">Sommet</span><span class="sxs-lookup"><span data-stu-id="36dfa-138">Vertex</span></span> | <span data-ttu-id="36dfa-139">Forme</span><span class="sxs-lookup"><span data-stu-id="36dfa-139">Hull</span></span> | <span data-ttu-id="36dfa-140">Domain</span><span class="sxs-lookup"><span data-stu-id="36dfa-140">Domain</span></span> | <span data-ttu-id="36dfa-141">Géométrie</span><span class="sxs-lookup"><span data-stu-id="36dfa-141">Geometry</span></span> | <span data-ttu-id="36dfa-142">Pixel</span><span class="sxs-lookup"><span data-stu-id="36dfa-142">Pixel</span></span> | <span data-ttu-id="36dfa-143">Compute</span><span class="sxs-lookup"><span data-stu-id="36dfa-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="36dfa-144">X</span><span class="sxs-lookup"><span data-stu-id="36dfa-144">X</span></span>      | <span data-ttu-id="36dfa-145">X</span><span class="sxs-lookup"><span data-stu-id="36dfa-145">X</span></span>    | <span data-ttu-id="36dfa-146">X</span><span class="sxs-lookup"><span data-stu-id="36dfa-146">X</span></span>      | <span data-ttu-id="36dfa-147">X</span><span class="sxs-lookup"><span data-stu-id="36dfa-147">X</span></span>        | <span data-ttu-id="36dfa-148">X</span><span class="sxs-lookup"><span data-stu-id="36dfa-148">X</span></span>     | <span data-ttu-id="36dfa-149">X</span><span class="sxs-lookup"><span data-stu-id="36dfa-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="36dfa-150">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="36dfa-150">Minimum Shader Model</span></span>

<span data-ttu-id="36dfa-151">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="36dfa-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="36dfa-152">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="36dfa-152">Shader Model</span></span>                                              | <span data-ttu-id="36dfa-153">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="36dfa-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="36dfa-154">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="36dfa-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="36dfa-155">Oui</span><span class="sxs-lookup"><span data-stu-id="36dfa-155">yes</span></span>       |
| [<span data-ttu-id="36dfa-156">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="36dfa-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="36dfa-157">non</span><span class="sxs-lookup"><span data-stu-id="36dfa-157">no</span></span>        |
| [<span data-ttu-id="36dfa-158">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="36dfa-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="36dfa-159">non</span><span class="sxs-lookup"><span data-stu-id="36dfa-159">no</span></span>        |
| [<span data-ttu-id="36dfa-160">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="36dfa-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="36dfa-161">non</span><span class="sxs-lookup"><span data-stu-id="36dfa-161">no</span></span>        |
| [<span data-ttu-id="36dfa-162">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="36dfa-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="36dfa-163">non</span><span class="sxs-lookup"><span data-stu-id="36dfa-163">no</span></span>        |
| [<span data-ttu-id="36dfa-164">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="36dfa-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="36dfa-165">non</span><span class="sxs-lookup"><span data-stu-id="36dfa-165">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="36dfa-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36dfa-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36dfa-167">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="36dfa-167">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





