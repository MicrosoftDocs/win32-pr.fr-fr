---
title: atomic_iadd (SM5-ASM)
description: Entier atomique ajouté à la mémoire.
ms.assetid: 093C7FA5-41BF-4BDD-A35D-1AACE8CB9B5C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a8652d4e29aae9f32a84f7a4e4d477abd54b7c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313732"
---
# <a name="atomic_iadd-sm5---asm"></a><span data-ttu-id="c840e-103">Atomic \_ IAdd (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c840e-103">atomic\_iadd (sm5 - asm)</span></span>

<span data-ttu-id="c840e-104">Entier atomique ajouté à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="c840e-104">Atomic integer add to memory.</span></span>



| <span data-ttu-id="c840e-105">Atomic \_ IAdd DST, dstAddress \[ . Swizzle \] , src0 \[ . Select, \_ composant\]</span><span class="sxs-lookup"><span data-stu-id="c840e-105">atomic\_iadd dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|----------------------------------------------------------------------|



 



| <span data-ttu-id="c840e-106">Élément</span><span class="sxs-lookup"><span data-stu-id="c840e-106">Item</span></span>                                                                                                           | <span data-ttu-id="c840e-107">Description</span><span class="sxs-lookup"><span data-stu-id="c840e-107">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c840e-108"><span id="dst"></span><span id="DST"></span>*destination*</span><span class="sxs-lookup"><span data-stu-id="c840e-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="c840e-109">\[dans \] les composants à ajouter avec *src0*.</span><span class="sxs-lookup"><span data-stu-id="c840e-109">\[in\] The components to add with *src0*.</span></span> <span data-ttu-id="c840e-110">Cette valeur doit être un affichage d’accès non ordonné (UAV) \# .</span><span class="sxs-lookup"><span data-stu-id="c840e-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="c840e-111">Dans le nuanceur de calcul, il peut également s’agir d’une mémoire partagée de groupe de threads (g \# ).</span><span class="sxs-lookup"><span data-stu-id="c840e-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="c840e-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="c840e-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="c840e-113">\[dans \] l’adresse mémoire.</span><span class="sxs-lookup"><span data-stu-id="c840e-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="c840e-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c840e-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="c840e-115">\[dans \] les composants à ajouter à l' *heure d’été*.</span><span class="sxs-lookup"><span data-stu-id="c840e-115">\[in\] The components to add to *dst*.</span></span><br/>                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="c840e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c840e-116">Remarks</span></span>

<span data-ttu-id="c840e-117">Cette instruction effectue un seul composant de l’opérande 32-bit *src0* , en l’ajoutant à l' *heure d’été* à 32 bits par adresse de composant *dstAddress*, exécuté atomiquement.</span><span class="sxs-lookup"><span data-stu-id="c840e-117">This instruction performs a single component 32-bit integer add of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span> <span data-ttu-id="c840e-118">Cette instruction ne tient pas compte de la signature.</span><span class="sxs-lookup"><span data-stu-id="c840e-118">This instruction is insensitive to sign.</span></span>

<span data-ttu-id="c840e-119">Le nombre de composants pris à partir de l’adresse est déterminé par la dimensionnalité de l' *heure d’été* u \# ou g \# .</span><span class="sxs-lookup"><span data-stu-id="c840e-119">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="c840e-120">Si *DST* est un u \# , il peut être déclaré comme brut, typé ou structuré.</span><span class="sxs-lookup"><span data-stu-id="c840e-120">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="c840e-121">Si elle est typée, elle doit être déclarée en tant que UINT/Saint-avec le format de ressource lié R32 \_ uint/Saint-est \_ .</span><span class="sxs-lookup"><span data-stu-id="c840e-121">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="c840e-122">Si l' *heure d’été* est g \# , elle doit être déclarée comme brute ou structurée.</span><span class="sxs-lookup"><span data-stu-id="c840e-122">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="c840e-123">Rien n’est retourné au nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c840e-123">Nothing is returned to the shader.</span></span>

<span data-ttu-id="c840e-124">Si l’appel du nuanceur est inactif, par exemple si le pixel a été ignoré plus tôt dans son exécution, ou si un appel pixel/échantillon n’existe que pour servir d’assistance à un réel pixel/échantillon pour les dérivés, cette instruction ne modifie pas la mémoire de l' *heure d’été* (en mode silencieux).</span><span class="sxs-lookup"><span data-stu-id="c840e-124">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or if a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="c840e-125">L’adressage hors limites sur u n' \# entraîne pas l’écriture dans la mémoire, sauf si u \# est structuré et que l’offset d’octet dans le struct (composant « second » de l’adresse) est à l’origine de l’accès hors limites, alors que le contenu entier du UAV devient non défini.</span><span class="sxs-lookup"><span data-stu-id="c840e-125">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="c840e-126">En dehors des limites d’adressage sur g \# (les limites de ce g particulier \# , par opposition à toute la mémoire partagée), la totalité du contenu de la mémoire partagée devient non définie.</span><span class="sxs-lookup"><span data-stu-id="c840e-126">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="c840e-127">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="c840e-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c840e-128">Sommet</span><span class="sxs-lookup"><span data-stu-id="c840e-128">Vertex</span></span> | <span data-ttu-id="c840e-129">Forme</span><span class="sxs-lookup"><span data-stu-id="c840e-129">Hull</span></span> | <span data-ttu-id="c840e-130">Domain</span><span class="sxs-lookup"><span data-stu-id="c840e-130">Domain</span></span> | <span data-ttu-id="c840e-131">Géométrie</span><span class="sxs-lookup"><span data-stu-id="c840e-131">Geometry</span></span> | <span data-ttu-id="c840e-132">Pixel</span><span class="sxs-lookup"><span data-stu-id="c840e-132">Pixel</span></span> | <span data-ttu-id="c840e-133">Compute</span><span class="sxs-lookup"><span data-stu-id="c840e-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c840e-134">X</span><span class="sxs-lookup"><span data-stu-id="c840e-134">X</span></span>     | <span data-ttu-id="c840e-135">X</span><span class="sxs-lookup"><span data-stu-id="c840e-135">X</span></span>       |



 

<span data-ttu-id="c840e-136">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c840e-136">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="c840e-137">Sommet</span><span class="sxs-lookup"><span data-stu-id="c840e-137">Vertex</span></span> | <span data-ttu-id="c840e-138">Forme</span><span class="sxs-lookup"><span data-stu-id="c840e-138">Hull</span></span> | <span data-ttu-id="c840e-139">Domain</span><span class="sxs-lookup"><span data-stu-id="c840e-139">Domain</span></span> | <span data-ttu-id="c840e-140">Géométrie</span><span class="sxs-lookup"><span data-stu-id="c840e-140">Geometry</span></span> | <span data-ttu-id="c840e-141">Pixel</span><span class="sxs-lookup"><span data-stu-id="c840e-141">Pixel</span></span> | <span data-ttu-id="c840e-142">Compute</span><span class="sxs-lookup"><span data-stu-id="c840e-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c840e-143">X</span><span class="sxs-lookup"><span data-stu-id="c840e-143">X</span></span>      | <span data-ttu-id="c840e-144">X</span><span class="sxs-lookup"><span data-stu-id="c840e-144">X</span></span>    | <span data-ttu-id="c840e-145">X</span><span class="sxs-lookup"><span data-stu-id="c840e-145">X</span></span>      | <span data-ttu-id="c840e-146">X</span><span class="sxs-lookup"><span data-stu-id="c840e-146">X</span></span>        | <span data-ttu-id="c840e-147">X</span><span class="sxs-lookup"><span data-stu-id="c840e-147">X</span></span>     | <span data-ttu-id="c840e-148">X</span><span class="sxs-lookup"><span data-stu-id="c840e-148">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c840e-149">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c840e-149">Minimum Shader Model</span></span>

<span data-ttu-id="c840e-150">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="c840e-150">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c840e-151">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c840e-151">Shader Model</span></span>                                              | <span data-ttu-id="c840e-152">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="c840e-152">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c840e-153">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="c840e-153">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c840e-154">Oui</span><span class="sxs-lookup"><span data-stu-id="c840e-154">yes</span></span>       |
| [<span data-ttu-id="c840e-155">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="c840e-155">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c840e-156">non</span><span class="sxs-lookup"><span data-stu-id="c840e-156">no</span></span>        |
| [<span data-ttu-id="c840e-157">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="c840e-157">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c840e-158">non</span><span class="sxs-lookup"><span data-stu-id="c840e-158">no</span></span>        |
| [<span data-ttu-id="c840e-159">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c840e-159">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c840e-160">non</span><span class="sxs-lookup"><span data-stu-id="c840e-160">no</span></span>        |
| [<span data-ttu-id="c840e-161">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c840e-161">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c840e-162">non</span><span class="sxs-lookup"><span data-stu-id="c840e-162">no</span></span>        |
| [<span data-ttu-id="c840e-163">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c840e-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c840e-164">non</span><span class="sxs-lookup"><span data-stu-id="c840e-164">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c840e-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c840e-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c840e-166">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c840e-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





