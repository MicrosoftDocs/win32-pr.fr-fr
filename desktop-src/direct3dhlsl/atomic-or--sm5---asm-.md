---
title: atomic_or (SM5-ASM)
description: Au niveau du bit atomique ou en mémoire.
ms.assetid: 5AFB96AA-267B-454E-9526-BA61A876ED42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 245f1b02edd74712471206b095f0c8a9040962b6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507723"
---
# <a name="atomic_or-sm5---asm"></a><span data-ttu-id="63e8d-103">Atomic \_ ou (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="63e8d-103">atomic\_or (sm5 - asm)</span></span>

<span data-ttu-id="63e8d-104">Au niveau du bit atomique ou en mémoire.</span><span class="sxs-lookup"><span data-stu-id="63e8d-104">Atomic bitwise OR to memory.</span></span>



| <span data-ttu-id="63e8d-105">Atomic \_ ou DST, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="63e8d-105">atomic\_or dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="63e8d-106">Élément</span><span class="sxs-lookup"><span data-stu-id="63e8d-106">Item</span></span>                                                                                                           | <span data-ttu-id="63e8d-107">Description</span><span class="sxs-lookup"><span data-stu-id="63e8d-107">Description</span></span>                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e8d-108"><span id="dst"></span><span id="DST"></span>*destination*</span><span class="sxs-lookup"><span data-stu-id="63e8d-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="63e8d-109">\[dans \] les composants de ou avec *src0*.</span><span class="sxs-lookup"><span data-stu-id="63e8d-109">\[in\] The components to OR with *src0*.</span></span> <span data-ttu-id="63e8d-110">Cette valeur doit être un affichage d’accès non ordonné (UAV) \# .</span><span class="sxs-lookup"><span data-stu-id="63e8d-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="63e8d-111">Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="63e8d-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="63e8d-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="63e8d-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="63e8d-113">\[dans \] l’adresse mémoire.</span><span class="sxs-lookup"><span data-stu-id="63e8d-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                |
| <span data-ttu-id="63e8d-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="63e8d-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="63e8d-115">\[dans \] les composants de ou avec l' *heure d’été*.</span><span class="sxs-lookup"><span data-stu-id="63e8d-115">\[in\] The components to OR with *dst*.</span></span><br/>                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="63e8d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="63e8d-116">Remarks</span></span>

<span data-ttu-id="63e8d-117">Cette instruction effectue un seul composant au niveau du bit 32 bits ou d’un opérande *src0* en *heure d’été* à 32 bits par adresse de composant *dstAddress*, exécuté atomiquement.</span><span class="sxs-lookup"><span data-stu-id="63e8d-117">This instruction performs a single component 32-bit bitwise OR of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span>

<span data-ttu-id="63e8d-118">Le nombre de composants pris à partir de l’adresse est déterminé par la dimensionnalité de l' *heure d’été* u \# ou g \# .</span><span class="sxs-lookup"><span data-stu-id="63e8d-118">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="63e8d-119">Si *DST* est un u \# , il peut être déclaré comme brut, typé ou structuré.</span><span class="sxs-lookup"><span data-stu-id="63e8d-119">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="63e8d-120">Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .</span><span class="sxs-lookup"><span data-stu-id="63e8d-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="63e8d-121">Si l' *heure d’été* est g \# , elle doit être déclarée comme brute ou structurée.</span><span class="sxs-lookup"><span data-stu-id="63e8d-121">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="63e8d-122">Rien n’est retourné au nuanceur.</span><span class="sxs-lookup"><span data-stu-id="63e8d-122">Nothing is returned to the shader.</span></span>

<span data-ttu-id="63e8d-123">Si l’appel du nuanceur est inactif, par exemple si le pixel a été ignoré plus tôt dans son exécution, ou si un appel pixel/échantillon n’existe que pour servir d’assistance à un réel pixel/échantillon pour les dérivés, cette instruction ne modifie pas la mémoire de l' *heure d’été* (en mode silencieux).</span><span class="sxs-lookup"><span data-stu-id="63e8d-123">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or if a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="63e8d-124">L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, le contenu entier du UAV devient non défini.</span><span class="sxs-lookup"><span data-stu-id="63e8d-124">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and the byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="63e8d-125">En dehors des limites d’adressage sur g \# (les limites de ce g particulier \# , par opposition à toute la mémoire partagée), la totalité du contenu de la mémoire partagée devient non définie.</span><span class="sxs-lookup"><span data-stu-id="63e8d-125">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="63e8d-126">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="63e8d-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="63e8d-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="63e8d-127">Vertex</span></span> | <span data-ttu-id="63e8d-128">Forme</span><span class="sxs-lookup"><span data-stu-id="63e8d-128">Hull</span></span> | <span data-ttu-id="63e8d-129">Domain</span><span class="sxs-lookup"><span data-stu-id="63e8d-129">Domain</span></span> | <span data-ttu-id="63e8d-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="63e8d-130">Geometry</span></span> | <span data-ttu-id="63e8d-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="63e8d-131">Pixel</span></span> | <span data-ttu-id="63e8d-132">Compute</span><span class="sxs-lookup"><span data-stu-id="63e8d-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="63e8d-133">X</span><span class="sxs-lookup"><span data-stu-id="63e8d-133">X</span></span>     | <span data-ttu-id="63e8d-134">X</span><span class="sxs-lookup"><span data-stu-id="63e8d-134">X</span></span>       |



 

<span data-ttu-id="63e8d-135">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63e8d-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="63e8d-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="63e8d-136">Vertex</span></span> | <span data-ttu-id="63e8d-137">Forme</span><span class="sxs-lookup"><span data-stu-id="63e8d-137">Hull</span></span> | <span data-ttu-id="63e8d-138">Domain</span><span class="sxs-lookup"><span data-stu-id="63e8d-138">Domain</span></span> | <span data-ttu-id="63e8d-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="63e8d-139">Geometry</span></span> | <span data-ttu-id="63e8d-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="63e8d-140">Pixel</span></span> | <span data-ttu-id="63e8d-141">Compute</span><span class="sxs-lookup"><span data-stu-id="63e8d-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="63e8d-142">X</span><span class="sxs-lookup"><span data-stu-id="63e8d-142">X</span></span>      | <span data-ttu-id="63e8d-143">X</span><span class="sxs-lookup"><span data-stu-id="63e8d-143">X</span></span>    | <span data-ttu-id="63e8d-144">X</span><span class="sxs-lookup"><span data-stu-id="63e8d-144">X</span></span>      | <span data-ttu-id="63e8d-145">X</span><span class="sxs-lookup"><span data-stu-id="63e8d-145">X</span></span>        | <span data-ttu-id="63e8d-146">X</span><span class="sxs-lookup"><span data-stu-id="63e8d-146">X</span></span>     | <span data-ttu-id="63e8d-147">X</span><span class="sxs-lookup"><span data-stu-id="63e8d-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="63e8d-148">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="63e8d-148">Minimum Shader Model</span></span>

<span data-ttu-id="63e8d-149">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="63e8d-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="63e8d-150">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="63e8d-150">Shader Model</span></span>                                              | <span data-ttu-id="63e8d-151">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="63e8d-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="63e8d-152">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="63e8d-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="63e8d-153">Oui</span><span class="sxs-lookup"><span data-stu-id="63e8d-153">yes</span></span>       |
| [<span data-ttu-id="63e8d-154">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="63e8d-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="63e8d-155">non</span><span class="sxs-lookup"><span data-stu-id="63e8d-155">no</span></span>        |
| [<span data-ttu-id="63e8d-156">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="63e8d-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="63e8d-157">non</span><span class="sxs-lookup"><span data-stu-id="63e8d-157">no</span></span>        |
| [<span data-ttu-id="63e8d-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="63e8d-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="63e8d-159">non</span><span class="sxs-lookup"><span data-stu-id="63e8d-159">no</span></span>        |
| [<span data-ttu-id="63e8d-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="63e8d-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="63e8d-161">non</span><span class="sxs-lookup"><span data-stu-id="63e8d-161">no</span></span>        |
| [<span data-ttu-id="63e8d-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="63e8d-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="63e8d-163">non</span><span class="sxs-lookup"><span data-stu-id="63e8d-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="63e8d-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63e8d-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63e8d-165">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="63e8d-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





