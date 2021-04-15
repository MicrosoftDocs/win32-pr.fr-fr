---
title: imm_atomic_consume (SM5-ASM)
description: Décrémenter atomiquement le compteur 32 bits masqué stocké avec un nombre ou ajouter la vue d’accès non ordonné (UAV), en retournant la nouvelle valeur.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1c6fe01ddb92b2ce870b16254f75c52cadd341
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990788"
---
# <a name="imm_atomic_consume-sm5---asm"></a><span data-ttu-id="4e09e-103">IMM \_ Atomic \_ consume (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4e09e-103">imm\_atomic\_consume (sm5 - asm)</span></span>

<span data-ttu-id="4e09e-104">Décrémenter atomiquement le compteur 32 bits masqué stocké avec un nombre ou ajouter la vue d’accès non ordonné (UAV), en retournant la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="4e09e-104">Atomically decrement the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the new value.</span></span>



| <span data-ttu-id="4e09e-105">IMM \_ Atomic \_ consomme dst0 \[ . \_ \_ masque de composant unique \] , dstUAV</span><span class="sxs-lookup"><span data-stu-id="4e09e-105">imm\_atomic\_consume dst0\[.single\_component\_mask\], dstUAV</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="4e09e-106">Élément</span><span class="sxs-lookup"><span data-stu-id="4e09e-106">Item</span></span>                                                                                           | <span data-ttu-id="4e09e-107">Description</span><span class="sxs-lookup"><span data-stu-id="4e09e-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="4e09e-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="4e09e-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="4e09e-109">\[dans \] contient la valeur de compteur d’origine retournée.</span><span class="sxs-lookup"><span data-stu-id="4e09e-109">\[in\] Contains the returned original counter value.</span></span><br/>           |
| <span data-ttu-id="4e09e-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="4e09e-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="4e09e-111">\[dans \] une mémoire tampon structurée UAV avec l’indicateur Count ou Append.</span><span class="sxs-lookup"><span data-stu-id="4e09e-111">\[in\] A structured buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="4e09e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4e09e-112">Remarks</span></span>

<span data-ttu-id="4e09e-113">Consultez [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) pour une discussion sur la validité de la valeur du nombre retourné selon que le UAV est Count ou Append.</span><span class="sxs-lookup"><span data-stu-id="4e09e-113">See [imm\_atomic\_alloc](imm-atomic-alloc--sm5---asm-.md) for a discussion about the validity of the returned count value depending on whether the UAV is Count or Append.</span></span> <span data-ttu-id="4e09e-114">Il en va de même pour la **\_ \_ consommation atomique IMM**.</span><span class="sxs-lookup"><span data-stu-id="4e09e-114">The same applies for **imm\_atomic\_consume**.</span></span>

<span data-ttu-id="4e09e-115">**IMM \_ Atomic \_ consume** effectue une décrémentation atomique de la valeur de compteur, en retournant la nouvelle valeur à *dst0*.</span><span class="sxs-lookup"><span data-stu-id="4e09e-115">**imm\_atomic\_consume** does an atomic decrement of the counter value, returning the new value to *dst0*.</span></span>

<span data-ttu-id="4e09e-116">Il n’y a pas de fixation du nombre. il est donc encapsulé sur un dépassement de capacité négatif.</span><span class="sxs-lookup"><span data-stu-id="4e09e-116">There is no clamping of the count, so it wraps on underflow.</span></span>

<span data-ttu-id="4e09e-117">Le même nuanceur ne peut pas tenter à la fois l' **\_ \_ allocation atomique de IMM** et le **IMM \_ Atomic \_ consommer** sur le même UAV.</span><span class="sxs-lookup"><span data-stu-id="4e09e-117">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="4e09e-118">En outre, le GPU ne peut pas autoriser plusieurs appels de nuanceur à mélanger **\_ Atomic Atomic \_ Alloc** et **IMM \_ Atomic \_ consommer** sur le même UAV.</span><span class="sxs-lookup"><span data-stu-id="4e09e-118">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="4e09e-119">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="4e09e-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4e09e-120">Sommet</span><span class="sxs-lookup"><span data-stu-id="4e09e-120">Vertex</span></span> | <span data-ttu-id="4e09e-121">Forme</span><span class="sxs-lookup"><span data-stu-id="4e09e-121">Hull</span></span> | <span data-ttu-id="4e09e-122">Domain</span><span class="sxs-lookup"><span data-stu-id="4e09e-122">Domain</span></span> | <span data-ttu-id="4e09e-123">Géométrie</span><span class="sxs-lookup"><span data-stu-id="4e09e-123">Geometry</span></span> | <span data-ttu-id="4e09e-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="4e09e-124">Pixel</span></span> | <span data-ttu-id="4e09e-125">Compute</span><span class="sxs-lookup"><span data-stu-id="4e09e-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4e09e-126">X</span><span class="sxs-lookup"><span data-stu-id="4e09e-126">X</span></span>     | <span data-ttu-id="4e09e-127">X</span><span class="sxs-lookup"><span data-stu-id="4e09e-127">X</span></span>       |



 

<span data-ttu-id="4e09e-128">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4e09e-128">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="4e09e-129">Sommet</span><span class="sxs-lookup"><span data-stu-id="4e09e-129">Vertex</span></span> | <span data-ttu-id="4e09e-130">Forme</span><span class="sxs-lookup"><span data-stu-id="4e09e-130">Hull</span></span> | <span data-ttu-id="4e09e-131">Domain</span><span class="sxs-lookup"><span data-stu-id="4e09e-131">Domain</span></span> | <span data-ttu-id="4e09e-132">Géométrie</span><span class="sxs-lookup"><span data-stu-id="4e09e-132">Geometry</span></span> | <span data-ttu-id="4e09e-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="4e09e-133">Pixel</span></span> | <span data-ttu-id="4e09e-134">Compute</span><span class="sxs-lookup"><span data-stu-id="4e09e-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4e09e-135">X</span><span class="sxs-lookup"><span data-stu-id="4e09e-135">X</span></span>      | <span data-ttu-id="4e09e-136">X</span><span class="sxs-lookup"><span data-stu-id="4e09e-136">X</span></span>    | <span data-ttu-id="4e09e-137">X</span><span class="sxs-lookup"><span data-stu-id="4e09e-137">X</span></span>      | <span data-ttu-id="4e09e-138">X</span><span class="sxs-lookup"><span data-stu-id="4e09e-138">X</span></span>        | <span data-ttu-id="4e09e-139">X</span><span class="sxs-lookup"><span data-stu-id="4e09e-139">X</span></span>     | <span data-ttu-id="4e09e-140">X</span><span class="sxs-lookup"><span data-stu-id="4e09e-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4e09e-141">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4e09e-141">Minimum Shader Model</span></span>

<span data-ttu-id="4e09e-142">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="4e09e-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4e09e-143">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4e09e-143">Shader Model</span></span>                                              | <span data-ttu-id="4e09e-144">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="4e09e-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4e09e-145">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4e09e-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4e09e-146">Oui</span><span class="sxs-lookup"><span data-stu-id="4e09e-146">yes</span></span>       |
| [<span data-ttu-id="4e09e-147">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="4e09e-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4e09e-148">non</span><span class="sxs-lookup"><span data-stu-id="4e09e-148">no</span></span>        |
| [<span data-ttu-id="4e09e-149">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="4e09e-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4e09e-150">non</span><span class="sxs-lookup"><span data-stu-id="4e09e-150">no</span></span>        |
| [<span data-ttu-id="4e09e-151">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e09e-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4e09e-152">non</span><span class="sxs-lookup"><span data-stu-id="4e09e-152">no</span></span>        |
| [<span data-ttu-id="4e09e-153">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e09e-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4e09e-154">non</span><span class="sxs-lookup"><span data-stu-id="4e09e-154">no</span></span>        |
| [<span data-ttu-id="4e09e-155">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e09e-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4e09e-156">non</span><span class="sxs-lookup"><span data-stu-id="4e09e-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4e09e-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e09e-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e09e-158">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4e09e-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





