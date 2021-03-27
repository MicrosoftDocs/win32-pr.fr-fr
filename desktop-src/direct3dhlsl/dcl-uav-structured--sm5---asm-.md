---
title: dcl_uav_structured (SM5-ASM)
description: Déclarez une vue d’accès non triée (UAV) pour une utilisation par un nuanceur. | dcl_uav_structured (SM5-ASM)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc02396f4837a095506e736d81ea8c00eb0669f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211458"
---
# <a name="dcl_uav_structured-sm5---asm"></a><span data-ttu-id="0936c-104">DCL \_ UAV \_ structurée (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0936c-104">dcl\_uav\_structured (sm5 - asm)</span></span>

<span data-ttu-id="0936c-105">Déclarez une vue d’accès non triée (UAV) pour une utilisation par un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0936c-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="0936c-106">DCL \_ UAV \_ structuré \[ \_ GLC \] dstUAV, structByteStride</span><span class="sxs-lookup"><span data-stu-id="0936c-106">dcl\_uav\_structured\[\_glc\] dstUAV, structByteStride</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="0936c-107">Élément</span><span class="sxs-lookup"><span data-stu-id="0936c-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="0936c-108">Description</span><span class="sxs-lookup"><span data-stu-id="0936c-108">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="0936c-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="0936c-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                                         | <span data-ttu-id="0936c-110">\[dans \] le UAV.</span><span class="sxs-lookup"><span data-stu-id="0936c-110">\[in\] The UAV.</span></span><br/>                            |
| <span data-ttu-id="0936c-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="0936c-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="0936c-112">\[dans \] la taille de la structure en octets.</span><span class="sxs-lookup"><span data-stu-id="0936c-112">\[in\] The size of the structure in bytes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0936c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0936c-113">Remarks</span></span>

<span data-ttu-id="0936c-114">*dstUAV* est un \# Registre u déclaré comme référence à un UnorderedAccessView d’une mémoire tampon structurée avec la valeur Stride spécifiée qui doit être liée à \# l’emplacement UAV au niveau de l’API.</span><span class="sxs-lookup"><span data-stu-id="0936c-114">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a structured buffer with the specified stride that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="0936c-115">Le contenu de la structure n’a pas de type ; les opérations effectuées sur la mémoire peuvent interpréter implicitement les données comme ayant un type.</span><span class="sxs-lookup"><span data-stu-id="0936c-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="0936c-116">*structByteStride* est la taille de la structure en octets dans la mémoire tampon en cours de déclaration.</span><span class="sxs-lookup"><span data-stu-id="0936c-116">*structByteStride* is the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="0936c-117">Cette valeur doit être supérieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="0936c-117">This value must be greater than zero.</span></span> <span data-ttu-id="0936c-118">*structByteStride* est de type uint et doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="0936c-118">*structByteStride* is of type uint, and must be a multiple of 4.</span></span>

<span data-ttu-id="0936c-119">Les instructions qui font référence à un u structuré \# prennent une adresse 2D, où le premier composant sélectionne la \[ structure \] , et le deuxième composant choisit le décalage dans la \[ structure, en octets alignés \] .</span><span class="sxs-lookup"><span data-stu-id="0936c-119">Instructions that reference a structured u\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, in aligned bytes\].</span></span>

<span data-ttu-id="0936c-120">L' \_ indicateur GLC signifie « cohérence globale ».</span><span class="sxs-lookup"><span data-stu-id="0936c-120">The \_glc flag means for"globally coherent".</span></span> <span data-ttu-id="0936c-121">L’absence de \_ GLC signifie que le UAV est déclaré comme « cohérent par le groupe » dans le nuanceur de calcul, ou « cohérent localement » dans un appel de nuanceur de pixel unique.</span><span class="sxs-lookup"><span data-stu-id="0936c-121">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="0936c-122">L' \_ indicateur OPC est le compteur de préservation de l’ordre.</span><span class="sxs-lookup"><span data-stu-id="0936c-122">The \_opc flag is the order preserving counter.</span></span> <span data-ttu-id="0936c-123">Elle indique que si un UAV est lié à \# l’emplacement (u \# ), il doit avoir été créé avec l’indicateur de compteur.</span><span class="sxs-lookup"><span data-stu-id="0936c-123">It indicates that if a UAV is bound to slot \# (u\#), it must have been created with the COUNTER flag.</span></span> <span data-ttu-id="0936c-124">Cela signifie que les opérations d' [ \_ \_ allocation atomique](imm-atomic-alloc--sm5---asm-.md) d’un IMM ou d’un IMM dans le nuanceur manipulent un compteur dont les valeurs peuvent être utilisées dans le nuanceur en tant que référence permanente à un emplacement dans le UAV. [ \_ \_ ](imm-atomic-consume--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="0936c-124">This means that [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) operations in the shader manipulate a counter whose values can be used in the shader as a permanent reference to a location in the UAV.</span></span> <span data-ttu-id="0936c-125">Les données ne peuvent pas être réorganisées après le dépassement du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0936c-125">Data cannot be reordered after the shader is over.</span></span>

<span data-ttu-id="0936c-126">L’absence de l' \_ indicateur OPC signifie que si le nuanceur utilise des instructions[IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) ou [IMM \_ Atomic \_ consume](imm-atomic-consume--sm5---asm-.md) et qu’un UAV est lié à l’emplacement \# (u), il doit avoir été créé avec l’indicateur Append, qui fournit un compteur qui ne garantit pas que l’ordre est conservé après l’appel du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0936c-126">The absence of the \_opc flag means that if the shader uses[imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions and a UAV is bound to slot \# (u), it must have been created with the APPEND flag, which provides a counter that does not guarantee order is preserved after the shader invocation.</span></span>

<span data-ttu-id="0936c-127">Si l' \_ indicateur OPC est absent et que le nuanceur ne contient pas d’instructions [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) ou [IMM \_ Atomic \_ Consumer](imm-atomic-consume--sm5---asm-.md) , une UAV liée à \# l’emplacement (u) est autorisée à avoir été créée avec l’indicateur de compteur (le compteur sera inutilisé par ce nuanceur), aucun indicateur (aucun compteur), mais pas avec l’indicateur Append.</span><span class="sxs-lookup"><span data-stu-id="0936c-127">If the \_opc flag is absent and the shader does not contain [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) or [imm\_atomic\_consume](imm-atomic-consume--sm5---asm-.md) instructions, a UAV bound to slot \# (u) is permitted to have been created with the COUNTER flag (the counter will go unused by this shader), no flag (no counter), but not with the APPEND flag.</span></span>

> [!Note]  
> <span data-ttu-id="0936c-128">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge la **\_ TGSM \_ structurée DCL**, mais pas la [ \_ TGSM \_ brute du DCL](dcl-tgsm-raw--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="0936c-128">cs\_4\_0 and cs\_4\_1 supports **dcl\_tgsm\_structured**, but not [dcl\_tgsm\_raw](dcl-tgsm-raw--sm5---asm-.md).</span></span>

 

<span data-ttu-id="0936c-129">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="0936c-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0936c-130">Sommet</span><span class="sxs-lookup"><span data-stu-id="0936c-130">Vertex</span></span> | <span data-ttu-id="0936c-131">Forme</span><span class="sxs-lookup"><span data-stu-id="0936c-131">Hull</span></span> | <span data-ttu-id="0936c-132">Domain</span><span class="sxs-lookup"><span data-stu-id="0936c-132">Domain</span></span> | <span data-ttu-id="0936c-133">Géométrie</span><span class="sxs-lookup"><span data-stu-id="0936c-133">Geometry</span></span> | <span data-ttu-id="0936c-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="0936c-134">Pixel</span></span> | <span data-ttu-id="0936c-135">Compute</span><span class="sxs-lookup"><span data-stu-id="0936c-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="0936c-136">X</span><span class="sxs-lookup"><span data-stu-id="0936c-136">X</span></span>     | <span data-ttu-id="0936c-137">X</span><span class="sxs-lookup"><span data-stu-id="0936c-137">X</span></span>       |



 

<span data-ttu-id="0936c-138">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0936c-138">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="0936c-139">Sommet</span><span class="sxs-lookup"><span data-stu-id="0936c-139">Vertex</span></span> | <span data-ttu-id="0936c-140">Forme</span><span class="sxs-lookup"><span data-stu-id="0936c-140">Hull</span></span> | <span data-ttu-id="0936c-141">Domain</span><span class="sxs-lookup"><span data-stu-id="0936c-141">Domain</span></span> | <span data-ttu-id="0936c-142">Géométrie</span><span class="sxs-lookup"><span data-stu-id="0936c-142">Geometry</span></span> | <span data-ttu-id="0936c-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="0936c-143">Pixel</span></span> | <span data-ttu-id="0936c-144">Compute</span><span class="sxs-lookup"><span data-stu-id="0936c-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0936c-145">X</span><span class="sxs-lookup"><span data-stu-id="0936c-145">X</span></span>      | <span data-ttu-id="0936c-146">X</span><span class="sxs-lookup"><span data-stu-id="0936c-146">X</span></span>    | <span data-ttu-id="0936c-147">X</span><span class="sxs-lookup"><span data-stu-id="0936c-147">X</span></span>      | <span data-ttu-id="0936c-148">X</span><span class="sxs-lookup"><span data-stu-id="0936c-148">X</span></span>        | <span data-ttu-id="0936c-149">X</span><span class="sxs-lookup"><span data-stu-id="0936c-149">X</span></span>     | <span data-ttu-id="0936c-150">X</span><span class="sxs-lookup"><span data-stu-id="0936c-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0936c-151">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0936c-151">Minimum Shader Model</span></span>

<span data-ttu-id="0936c-152">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="0936c-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0936c-153">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0936c-153">Shader Model</span></span>                                              | <span data-ttu-id="0936c-154">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0936c-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0936c-155">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="0936c-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0936c-156">Oui</span><span class="sxs-lookup"><span data-stu-id="0936c-156">yes</span></span>       |
| [<span data-ttu-id="0936c-157">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="0936c-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0936c-158">non</span><span class="sxs-lookup"><span data-stu-id="0936c-158">no</span></span>        |
| [<span data-ttu-id="0936c-159">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="0936c-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0936c-160">non</span><span class="sxs-lookup"><span data-stu-id="0936c-160">no</span></span>        |
| [<span data-ttu-id="0936c-161">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0936c-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0936c-162">non</span><span class="sxs-lookup"><span data-stu-id="0936c-162">no</span></span>        |
| [<span data-ttu-id="0936c-163">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0936c-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0936c-164">non</span><span class="sxs-lookup"><span data-stu-id="0936c-164">no</span></span>        |
| [<span data-ttu-id="0936c-165">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0936c-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0936c-166">non</span><span class="sxs-lookup"><span data-stu-id="0936c-166">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="0936c-167">Cette instruction est prise en charge dans cs \_ 4 \_ 0 et CS \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="0936c-167">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0936c-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0936c-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0936c-169">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0936c-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





