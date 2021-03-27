---
title: atomic_cmp_store (SM5-ASM)
description: Comparaison atomique et écriture en mémoire.
ms.assetid: 1B97E983-11A9-47E4-B274-E94083837C6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a5292d65b32988017044a2ec52680848dffbef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679161"
---
# <a name="atomic_cmp_store-sm5---asm"></a><span data-ttu-id="bf15e-103">\_stockage CMP atomique \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="bf15e-103">atomic\_cmp\_store (sm5 - asm)</span></span>

<span data-ttu-id="bf15e-104">Comparaison atomique et écriture en mémoire.</span><span class="sxs-lookup"><span data-stu-id="bf15e-104">Atomic compare and write to memory.</span></span>



| <span data-ttu-id="bf15e-105">Atomic \_ CMP \_ Store DST, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ \] , composant, src1 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="bf15e-105">atomic\_cmp\_store dst, dstAddress\[.swizzle\], src0\[.select\_component\], src1\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="bf15e-106">Élément</span><span class="sxs-lookup"><span data-stu-id="bf15e-106">Item</span></span>                                                                                                           | <span data-ttu-id="bf15e-107">Description</span><span class="sxs-lookup"><span data-stu-id="bf15e-107">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf15e-108"><span id="dst"></span><span id="DST"></span>*destination*</span><span class="sxs-lookup"><span data-stu-id="bf15e-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="bf15e-109">\[dans \] les composants à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="bf15e-109">\[in\] The components to compare with *src0*.</span></span> <span data-ttu-id="bf15e-110">Cette valeur doit être un affichage d’accès non ordonné (UAV) \# .</span><span class="sxs-lookup"><span data-stu-id="bf15e-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="bf15e-111">Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="bf15e-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="bf15e-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="bf15e-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="bf15e-113">\[dans \] l’adresse mémoire.</span><span class="sxs-lookup"><span data-stu-id="bf15e-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="bf15e-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bf15e-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="bf15e-115">\[dans \] la valeur 32 bits à comparer avec l' *heure d’été*.</span><span class="sxs-lookup"><span data-stu-id="bf15e-115">\[in\] The 32-bit value to compare with *dst*.</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="bf15e-116"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="bf15e-116"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                                | <span data-ttu-id="bf15e-117">\[dans \] la valeur à écrire dans la mémoire si les valeurs comparées sont identiques.</span><span class="sxs-lookup"><span data-stu-id="bf15e-117">\[in\] The value to write to memory if the compared values are identical.</span></span> <br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="bf15e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="bf15e-118">Remarks</span></span>

<span data-ttu-id="bf15e-119">Cette instruction effectue une comparaison de valeurs 32 bits de composant unique avec l’opérande *src0* avec l' *heure d’été* à 32 bits par adresse de composant *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="bf15e-119">This instruction performs a single component 32-bit value compare of operand *src0* with *dst* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="bf15e-120">Si les valeurs comparées sont identiques, la valeur 32 bits d’un seul composant dans *src1* est écrite dans la mémoire de destination.</span><span class="sxs-lookup"><span data-stu-id="bf15e-120">If the compared values are identical, the single-component 32-bit value in *src1* is written to destination memory.</span></span> <span data-ttu-id="bf15e-121">Dans le cas contraire, la destination n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="bf15e-121">Otherwise, the destination is not changed.</span></span>

<span data-ttu-id="bf15e-122">La totalité de l’opération de comparaison et d’écriture est effectuée de manière atomique.</span><span class="sxs-lookup"><span data-stu-id="bf15e-122">The entire compare and write operation is performed atomically.</span></span>

<span data-ttu-id="bf15e-123">Si *DST* est un u \# , il peut être déclaré comme brut, typé ou structuré.</span><span class="sxs-lookup"><span data-stu-id="bf15e-123">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="bf15e-124">Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .</span><span class="sxs-lookup"><span data-stu-id="bf15e-124">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="bf15e-125">Si l' *heure d’été* est g \# , elle doit être déclarée comme brute ou structurée.</span><span class="sxs-lookup"><span data-stu-id="bf15e-125">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="bf15e-126">Le nombre de composants pris à partir de l’adresse est déterminé par la dimensionnalité de l’heure d’été u \# ou g \# .</span><span class="sxs-lookup"><span data-stu-id="bf15e-126">The number of components taken from the address is determined by the dimensionality of dst u\# or g\#.</span></span>

<span data-ttu-id="bf15e-127">Rien n’est retourné au nuanceur.</span><span class="sxs-lookup"><span data-stu-id="bf15e-127">Nothing is returned to the shader.</span></span>

<span data-ttu-id="bf15e-128">Si l’appel du nuanceur est inactif, par exemple si le pixel a été ignoré plus tôt dans son exécution, ou si une instruction pixel/échantillon ne modifie pas la mémoire de l' *heure d’été* (en mode silencieux).</span><span class="sxs-lookup"><span data-stu-id="bf15e-128">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="bf15e-129">L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, alors que le contenu entier du UAV devient non défini.</span><span class="sxs-lookup"><span data-stu-id="bf15e-129">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="bf15e-130">En dehors des limites d’adressage sur g \# (les limites de ce g particulier \# , par opposition à toute la mémoire partagée), la totalité du contenu de la mémoire partagée devient non définie.</span><span class="sxs-lookup"><span data-stu-id="bf15e-130">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="bf15e-131">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="bf15e-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bf15e-132">Sommet</span><span class="sxs-lookup"><span data-stu-id="bf15e-132">Vertex</span></span> | <span data-ttu-id="bf15e-133">Forme</span><span class="sxs-lookup"><span data-stu-id="bf15e-133">Hull</span></span> | <span data-ttu-id="bf15e-134">Domain</span><span class="sxs-lookup"><span data-stu-id="bf15e-134">Domain</span></span> | <span data-ttu-id="bf15e-135">Géométrie</span><span class="sxs-lookup"><span data-stu-id="bf15e-135">Geometry</span></span> | <span data-ttu-id="bf15e-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="bf15e-136">Pixel</span></span> | <span data-ttu-id="bf15e-137">Compute</span><span class="sxs-lookup"><span data-stu-id="bf15e-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="bf15e-138">X</span><span class="sxs-lookup"><span data-stu-id="bf15e-138">X</span></span>     | <span data-ttu-id="bf15e-139">X</span><span class="sxs-lookup"><span data-stu-id="bf15e-139">X</span></span>       |



 

<span data-ttu-id="bf15e-140">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bf15e-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="bf15e-141">Sommet</span><span class="sxs-lookup"><span data-stu-id="bf15e-141">Vertex</span></span> | <span data-ttu-id="bf15e-142">Forme</span><span class="sxs-lookup"><span data-stu-id="bf15e-142">Hull</span></span> | <span data-ttu-id="bf15e-143">Domain</span><span class="sxs-lookup"><span data-stu-id="bf15e-143">Domain</span></span> | <span data-ttu-id="bf15e-144">Géométrie</span><span class="sxs-lookup"><span data-stu-id="bf15e-144">Geometry</span></span> | <span data-ttu-id="bf15e-145">Pixel</span><span class="sxs-lookup"><span data-stu-id="bf15e-145">Pixel</span></span> | <span data-ttu-id="bf15e-146">Compute</span><span class="sxs-lookup"><span data-stu-id="bf15e-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bf15e-147">X</span><span class="sxs-lookup"><span data-stu-id="bf15e-147">X</span></span>      | <span data-ttu-id="bf15e-148">X</span><span class="sxs-lookup"><span data-stu-id="bf15e-148">X</span></span>    | <span data-ttu-id="bf15e-149">X</span><span class="sxs-lookup"><span data-stu-id="bf15e-149">X</span></span>      | <span data-ttu-id="bf15e-150">X</span><span class="sxs-lookup"><span data-stu-id="bf15e-150">X</span></span>        | <span data-ttu-id="bf15e-151">X</span><span class="sxs-lookup"><span data-stu-id="bf15e-151">X</span></span>     | <span data-ttu-id="bf15e-152">X</span><span class="sxs-lookup"><span data-stu-id="bf15e-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bf15e-153">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="bf15e-153">Minimum Shader Model</span></span>

<span data-ttu-id="bf15e-154">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="bf15e-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="bf15e-155">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="bf15e-155">Shader Model</span></span>                                              | <span data-ttu-id="bf15e-156">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="bf15e-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bf15e-157">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="bf15e-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bf15e-158">Oui</span><span class="sxs-lookup"><span data-stu-id="bf15e-158">yes</span></span>       |
| [<span data-ttu-id="bf15e-159">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="bf15e-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bf15e-160">non</span><span class="sxs-lookup"><span data-stu-id="bf15e-160">no</span></span>        |
| [<span data-ttu-id="bf15e-161">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="bf15e-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bf15e-162">non</span><span class="sxs-lookup"><span data-stu-id="bf15e-162">no</span></span>        |
| [<span data-ttu-id="bf15e-163">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf15e-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bf15e-164">non</span><span class="sxs-lookup"><span data-stu-id="bf15e-164">no</span></span>        |
| [<span data-ttu-id="bf15e-165">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf15e-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bf15e-166">non</span><span class="sxs-lookup"><span data-stu-id="bf15e-166">no</span></span>        |
| [<span data-ttu-id="bf15e-167">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf15e-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bf15e-168">non</span><span class="sxs-lookup"><span data-stu-id="bf15e-168">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bf15e-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf15e-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf15e-170">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf15e-170">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





