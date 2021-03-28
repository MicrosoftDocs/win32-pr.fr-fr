---
title: imm_atomic_iadd (SM5-ASM)
description: Entier atomique immédiat ajouté à la mémoire. Retourne la valeur en mémoire avant l’ajout.
ms.assetid: 24136B4C-D37C-4449-A318-57145BB8D8E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2695e23707fb61cd576748e2e83829cd7dc65259
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381203"
---
# <a name="imm_atomic_iadd-sm5---asm"></a><span data-ttu-id="e5ceb-104">IMM \_ Atomic \_ IAdd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e5ceb-104">imm\_atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="e5ceb-105">Entier atomique immédiat ajouté à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-105">Immediate atomic integer add to memory.</span></span> <span data-ttu-id="e5ceb-106">Retourne la valeur en mémoire avant l’ajout.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-106">Returns the value in memory before the add.</span></span>



| <span data-ttu-id="e5ceb-107">IMM \_ Atomic \_ IAdd dst0 \[ . \_ \_ masque de composant unique \] , dst1, dstAddress \[ . Swizzle \] , src0 \[ . Sélectionner un \_ composant\]</span><span class="sxs-lookup"><span data-stu-id="e5ceb-107">imm\_atomic\_iadd dst0\[.single\_component\_mask\], dst1, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e5ceb-108">Élément</span><span class="sxs-lookup"><span data-stu-id="e5ceb-108">Item</span></span>                                                                                                           | <span data-ttu-id="e5ceb-109">Description</span><span class="sxs-lookup"><span data-stu-id="e5ceb-109">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ceb-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="e5ceb-110"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="e5ceb-111">\[dans \] contient la valeur dans *dst1* avant l’écriture.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-111">\[in\] Contains the value in *dst1* before the write.</span></span> <br/>                                                                           |
| <span data-ttu-id="e5ceb-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span><span class="sxs-lookup"><span data-stu-id="e5ceb-112"><span id="dst1"></span><span id="DST1"></span>*dst1*</span></span><br/>                                                | <span data-ttu-id="e5ceb-113">Cette valeur doit être un affichage d’accès non ordonné (UAV) \# .</span><span class="sxs-lookup"><span data-stu-id="e5ceb-113">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="e5ceb-114">Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="e5ceb-114">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="e5ceb-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="e5ceb-115"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="e5ceb-116">\[dans \] le nAddress de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-116">\[in\] The memory naddress.</span></span><br/>                                                                                                      |
| <span data-ttu-id="e5ceb-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e5ceb-117"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="e5ceb-118">\[dans \] la valeur à ajouter à *dst1*.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-118">\[in\] The value to add to *dst1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="e5ceb-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e5ceb-119">Remarks</span></span>

<span data-ttu-id="e5ceb-120">Cette instruction exécute un seul composant de l’opérande 32 bits *src0* avec *dst1* à 32 bits par adresse de composant *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-120">This instruction performs a single component 32-bit integer add of operand *src0* with *dst1* at 32-bit per component address *dstAddress*.</span></span> <span data-ttu-id="e5ceb-121">La signature n’est pas sensible.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-121">It is insensitive to sign.</span></span>

<span data-ttu-id="e5ceb-122">Si *dst1* est un u \# , il a peut-être été déclaré comme brut, typé ou structuré.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-122">If *dst1* is a u\#, it may have been declared as raw, typed or structured.</span></span> <span data-ttu-id="e5ceb-123">Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .</span><span class="sxs-lookup"><span data-stu-id="e5ceb-123">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="e5ceb-124">Si *dst1* est g \# , il doit être déclaré comme RAW ou Structured.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-124">If *dst1* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="e5ceb-125">La valeur dans *dst1* Memory avant addition est retournée à *dst0*.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-125">The value in *dst1* memory before addition is returned to *dst0*.</span></span>

<span data-ttu-id="e5ceb-126">Le nombre de composants pris à partir de l’adresse est déterminé par la dimensionnalité de *dst1*.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-126">The number of components taken from the address is determined by the dimensionality of *dst1*.</span></span>

<span data-ttu-id="e5ceb-127">La totalité de l’opération est effectuée atomiquement.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-127">The entire operation is performed atomically.</span></span>

<span data-ttu-id="e5ceb-128">Si l’appel du nuanceur est inactif, par exemple si le pixel a été ignoré plus tôt dans son exécution, ou s’il n’existe qu’un appel d’assistance à un réel pixel/échantillon pour les dérivés, cette instruction ne modifie pas le tout la mémoire *dst1* , et la valeur retournée n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-128">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst1* memory at all, and the returned value is undefined.</span></span>

<span data-ttu-id="e5ceb-129">L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, alors que le contenu entier du UAV devient non défini.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-129">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="e5ceb-130">L’adressage hors limites sur u \# ou g \# entraîne le retour d’un résultat non défini au nuanceur dans *dst0*.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-130">Out of bounds addressing on u\# or g\# causes an undefined result to be returned to the shader in *dst0*.</span></span>

<span data-ttu-id="e5ceb-131">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="e5ceb-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e5ceb-132">Sommet</span><span class="sxs-lookup"><span data-stu-id="e5ceb-132">Vertex</span></span> | <span data-ttu-id="e5ceb-133">Forme</span><span class="sxs-lookup"><span data-stu-id="e5ceb-133">Hull</span></span> | <span data-ttu-id="e5ceb-134">Domain</span><span class="sxs-lookup"><span data-stu-id="e5ceb-134">Domain</span></span> | <span data-ttu-id="e5ceb-135">Géométrie</span><span class="sxs-lookup"><span data-stu-id="e5ceb-135">Geometry</span></span> | <span data-ttu-id="e5ceb-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="e5ceb-136">Pixel</span></span> | <span data-ttu-id="e5ceb-137">Compute</span><span class="sxs-lookup"><span data-stu-id="e5ceb-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e5ceb-138">X</span><span class="sxs-lookup"><span data-stu-id="e5ceb-138">X</span></span>     | <span data-ttu-id="e5ceb-139">X</span><span class="sxs-lookup"><span data-stu-id="e5ceb-139">X</span></span>       |



 

<span data-ttu-id="e5ceb-140">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e5ceb-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="e5ceb-141">Sommet</span><span class="sxs-lookup"><span data-stu-id="e5ceb-141">Vertex</span></span> | <span data-ttu-id="e5ceb-142">Forme</span><span class="sxs-lookup"><span data-stu-id="e5ceb-142">Hull</span></span> | <span data-ttu-id="e5ceb-143">Domain</span><span class="sxs-lookup"><span data-stu-id="e5ceb-143">Domain</span></span> | <span data-ttu-id="e5ceb-144">Géométrie</span><span class="sxs-lookup"><span data-stu-id="e5ceb-144">Geometry</span></span> | <span data-ttu-id="e5ceb-145">Pixel</span><span class="sxs-lookup"><span data-stu-id="e5ceb-145">Pixel</span></span> | <span data-ttu-id="e5ceb-146">Compute</span><span class="sxs-lookup"><span data-stu-id="e5ceb-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e5ceb-147">X</span><span class="sxs-lookup"><span data-stu-id="e5ceb-147">X</span></span>      | <span data-ttu-id="e5ceb-148">X</span><span class="sxs-lookup"><span data-stu-id="e5ceb-148">X</span></span>    | <span data-ttu-id="e5ceb-149">X</span><span class="sxs-lookup"><span data-stu-id="e5ceb-149">X</span></span>      | <span data-ttu-id="e5ceb-150">X</span><span class="sxs-lookup"><span data-stu-id="e5ceb-150">X</span></span>        | <span data-ttu-id="e5ceb-151">X</span><span class="sxs-lookup"><span data-stu-id="e5ceb-151">X</span></span>     | <span data-ttu-id="e5ceb-152">X</span><span class="sxs-lookup"><span data-stu-id="e5ceb-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e5ceb-153">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="e5ceb-153">Minimum Shader Model</span></span>

<span data-ttu-id="e5ceb-154">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="e5ceb-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e5ceb-155">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="e5ceb-155">Shader Model</span></span>                                              | <span data-ttu-id="e5ceb-156">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="e5ceb-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e5ceb-157">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="e5ceb-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e5ceb-158">Oui</span><span class="sxs-lookup"><span data-stu-id="e5ceb-158">yes</span></span>       |
| [<span data-ttu-id="e5ceb-159">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="e5ceb-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e5ceb-160">non</span><span class="sxs-lookup"><span data-stu-id="e5ceb-160">no</span></span>        |
| [<span data-ttu-id="e5ceb-161">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="e5ceb-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e5ceb-162">non</span><span class="sxs-lookup"><span data-stu-id="e5ceb-162">no</span></span>        |
| [<span data-ttu-id="e5ceb-163">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5ceb-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e5ceb-164">non</span><span class="sxs-lookup"><span data-stu-id="e5ceb-164">no</span></span>        |
| [<span data-ttu-id="e5ceb-165">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5ceb-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e5ceb-166">non</span><span class="sxs-lookup"><span data-stu-id="e5ceb-166">no</span></span>        |
| [<span data-ttu-id="e5ceb-167">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5ceb-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e5ceb-168">non</span><span class="sxs-lookup"><span data-stu-id="e5ceb-168">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e5ceb-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5ceb-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5ceb-170">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5ceb-170">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





