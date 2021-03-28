---
title: atomic_and (SM5-ASM)
description: Bits atomique et mémoire.
ms.assetid: 5FA731E0-7D18-4416-9579-FCA01FF5FC38
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef21f2f9d49a05f1eeb828ee1ce54ad1f162d7a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971606"
---
# <a name="atomic_and-sm5---asm"></a><span data-ttu-id="7ac7f-103">Atomic \_ et (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7ac7f-103">atomic\_and (sm5 - asm)</span></span>

<span data-ttu-id="7ac7f-104">Bits atomique et mémoire.</span><span class="sxs-lookup"><span data-stu-id="7ac7f-104">Atomic bitwise AND to memory.</span></span>



| <span data-ttu-id="7ac7f-105">Atomic \_ et DST, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="7ac7f-105">atomic\_and dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|---------------------------------------------------------------------|



 



| <span data-ttu-id="7ac7f-106">Élément</span><span class="sxs-lookup"><span data-stu-id="7ac7f-106">Item</span></span>                                                                                                           | <span data-ttu-id="7ac7f-107">Description</span><span class="sxs-lookup"><span data-stu-id="7ac7f-107">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac7f-108"><span id="dst"></span><span id="DST"></span>*destination*</span><span class="sxs-lookup"><span data-stu-id="7ac7f-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="7ac7f-109">\[dans \] les composants de et avec *src0*.</span><span class="sxs-lookup"><span data-stu-id="7ac7f-109">\[in\] The components to AND with *src0*.</span></span> <span data-ttu-id="7ac7f-110">Cette valeur doit être un affichage d’accès non ordonné (UAV) \# .</span><span class="sxs-lookup"><span data-stu-id="7ac7f-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="7ac7f-111">Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="7ac7f-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="7ac7f-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="7ac7f-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="7ac7f-113">\[dans \] l’adresse mémoire.</span><span class="sxs-lookup"><span data-stu-id="7ac7f-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="7ac7f-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7ac7f-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="7ac7f-115">\[dans \] les composants de et avec l' *heure d’été*.</span><span class="sxs-lookup"><span data-stu-id="7ac7f-115">\[in\] The components to AND with *dst*.</span></span><br/>                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="7ac7f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7ac7f-116">Remarks</span></span>

<span data-ttu-id="7ac7f-117">Cette opération effectue un composant unique au niveau du bit 32 bits et de l’opérande *src0* en *heure d’été* à 32 bits par adresse de composant *dstAddress*, exécuté atomiquement.</span><span class="sxs-lookup"><span data-stu-id="7ac7f-117">This operation performs a single component 32-bit bitwise AND of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span>

<span data-ttu-id="7ac7f-118">Le nombre de composants pris à partir de l’adresse est déterminé par la dimensionnalité de l' *heure d’été* u \# ou g \# .</span><span class="sxs-lookup"><span data-stu-id="7ac7f-118">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="7ac7f-119">Si *DST* est un u \# , il peut être déclaré comme brut, typé ou structuré.</span><span class="sxs-lookup"><span data-stu-id="7ac7f-119">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="7ac7f-120">Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .</span><span class="sxs-lookup"><span data-stu-id="7ac7f-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="7ac7f-121">Si l' *heure d’été* est g \# , elle doit être déclarée comme brute ou structurée.</span><span class="sxs-lookup"><span data-stu-id="7ac7f-121">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="7ac7f-122">Rien n’est retourné au nuanceur.</span><span class="sxs-lookup"><span data-stu-id="7ac7f-122">Nothing is returned to the shader.</span></span>

<span data-ttu-id="7ac7f-123">Si l’appel du nuanceur est inactif, par exemple si le pixel a été ignoré plus tôt dans son exécution, ou s’il n’existe qu’un appel de pixel/échantillon pour servir d’assistance à un réel pixel/échantillon pour les dérivés, cette instruction ne modifie pas la mémoire de l' *heure d’été* (en mode silencieux).</span><span class="sxs-lookup"><span data-stu-id="7ac7f-123">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="7ac7f-124">L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, alors que le contenu entier du UAV devient non défini.</span><span class="sxs-lookup"><span data-stu-id="7ac7f-124">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="7ac7f-125">En dehors des limites d’adressage sur g \# (les limites de ce g particulier \# , par opposition à toute la mémoire partagée), la totalité du contenu de la mémoire partagée devient non définie.</span><span class="sxs-lookup"><span data-stu-id="7ac7f-125">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="7ac7f-126">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="7ac7f-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7ac7f-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="7ac7f-127">Vertex</span></span> | <span data-ttu-id="7ac7f-128">Forme</span><span class="sxs-lookup"><span data-stu-id="7ac7f-128">Hull</span></span> | <span data-ttu-id="7ac7f-129">Domain</span><span class="sxs-lookup"><span data-stu-id="7ac7f-129">Domain</span></span> | <span data-ttu-id="7ac7f-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="7ac7f-130">Geometry</span></span> | <span data-ttu-id="7ac7f-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="7ac7f-131">Pixel</span></span> | <span data-ttu-id="7ac7f-132">Compute</span><span class="sxs-lookup"><span data-stu-id="7ac7f-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7ac7f-133">X</span><span class="sxs-lookup"><span data-stu-id="7ac7f-133">X</span></span>     | <span data-ttu-id="7ac7f-134">X</span><span class="sxs-lookup"><span data-stu-id="7ac7f-134">X</span></span>       |



 

<span data-ttu-id="7ac7f-135">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7ac7f-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="7ac7f-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="7ac7f-136">Vertex</span></span> | <span data-ttu-id="7ac7f-137">Forme</span><span class="sxs-lookup"><span data-stu-id="7ac7f-137">Hull</span></span> | <span data-ttu-id="7ac7f-138">Domain</span><span class="sxs-lookup"><span data-stu-id="7ac7f-138">Domain</span></span> | <span data-ttu-id="7ac7f-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="7ac7f-139">Geometry</span></span> | <span data-ttu-id="7ac7f-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="7ac7f-140">Pixel</span></span> | <span data-ttu-id="7ac7f-141">Compute</span><span class="sxs-lookup"><span data-stu-id="7ac7f-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7ac7f-142">X</span><span class="sxs-lookup"><span data-stu-id="7ac7f-142">X</span></span>      | <span data-ttu-id="7ac7f-143">X</span><span class="sxs-lookup"><span data-stu-id="7ac7f-143">X</span></span>    | <span data-ttu-id="7ac7f-144">X</span><span class="sxs-lookup"><span data-stu-id="7ac7f-144">X</span></span>      | <span data-ttu-id="7ac7f-145">X</span><span class="sxs-lookup"><span data-stu-id="7ac7f-145">X</span></span>        | <span data-ttu-id="7ac7f-146">X</span><span class="sxs-lookup"><span data-stu-id="7ac7f-146">X</span></span>     | <span data-ttu-id="7ac7f-147">X</span><span class="sxs-lookup"><span data-stu-id="7ac7f-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7ac7f-148">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="7ac7f-148">Minimum Shader Model</span></span>

<span data-ttu-id="7ac7f-149">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="7ac7f-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7ac7f-150">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="7ac7f-150">Shader Model</span></span>                                              | <span data-ttu-id="7ac7f-151">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="7ac7f-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7ac7f-152">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="7ac7f-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7ac7f-153">Oui</span><span class="sxs-lookup"><span data-stu-id="7ac7f-153">yes</span></span>       |
| [<span data-ttu-id="7ac7f-154">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="7ac7f-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7ac7f-155">non</span><span class="sxs-lookup"><span data-stu-id="7ac7f-155">no</span></span>        |
| [<span data-ttu-id="7ac7f-156">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="7ac7f-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7ac7f-157">non</span><span class="sxs-lookup"><span data-stu-id="7ac7f-157">no</span></span>        |
| [<span data-ttu-id="7ac7f-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ac7f-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7ac7f-159">non</span><span class="sxs-lookup"><span data-stu-id="7ac7f-159">no</span></span>        |
| [<span data-ttu-id="7ac7f-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ac7f-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7ac7f-161">non</span><span class="sxs-lookup"><span data-stu-id="7ac7f-161">no</span></span>        |
| [<span data-ttu-id="7ac7f-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ac7f-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7ac7f-163">non</span><span class="sxs-lookup"><span data-stu-id="7ac7f-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7ac7f-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ac7f-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ac7f-165">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7ac7f-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





