---
title: imm_atomic_alloc (SM5-ASM)
description: Incrémentez atomiquement le compteur 32 bits masqué stocké avec un nombre ou ajoutez la vue d’accès non ordonné (UAV), en retournant la valeur d’origine.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679150"
---
# <a name="imm_atomic_alloc-sm5---asm"></a><span data-ttu-id="309e3-103">IMM \_ Atomic \_ Alloc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="309e3-103">imm\_atomic\_alloc (sm5 - asm)</span></span>

<span data-ttu-id="309e3-104">Incrémentez atomiquement le compteur 32 bits masqué stocké avec un nombre ou ajoutez la vue d’accès non ordonné (UAV), en retournant la valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="309e3-104">Atomically increment the hidden 32-bit counter stored with a Count or Append unordered access view (UAV), returning the original value.</span></span>



| <span data-ttu-id="309e3-105">IMM \_ Atomic \_ Alloc dst0 \[ . \_ \_ masque de composant unique \] , dstUAV</span><span class="sxs-lookup"><span data-stu-id="309e3-105">imm\_atomic\_alloc dst0\[.single\_component\_mask\], dstUAV</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="309e3-106">Élément</span><span class="sxs-lookup"><span data-stu-id="309e3-106">Item</span></span>                                                                                           | <span data-ttu-id="309e3-107">Description</span><span class="sxs-lookup"><span data-stu-id="309e3-107">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="309e3-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="309e3-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                | <span data-ttu-id="309e3-109">\[dans \] contient la valeur de compteur retournée.</span><span class="sxs-lookup"><span data-stu-id="309e3-109">\[in\] Contains the returned counter value.</span></span><br/>                    |
| <span data-ttu-id="309e3-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="309e3-110"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="309e3-111">\[dans \] une mémoire tampon structurée UAV avec l’indicateur Count ou Append.</span><span class="sxs-lookup"><span data-stu-id="309e3-111">\[in\] A Structured Buffer UAV with the Count or Append flag.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="309e3-112">Notes</span><span class="sxs-lookup"><span data-stu-id="309e3-112">Remarks</span></span>

<span data-ttu-id="309e3-113">Il existe une valeur de compteur entière non signée 32 bits associée à chaque vue de la mémoire tampon Count ou Append qui est initialisée lorsque la vue est liée au pipeline, y compris l’option permettant de conserver la valeur précédente.</span><span class="sxs-lookup"><span data-stu-id="309e3-113">There is a hidden unsigned 32-bit integer counter value associated with each Count or Append Buffer view which is initialized when the view is bound to the pipeline, including the option to keep the previous value.</span></span>

<span data-ttu-id="309e3-114">Cette instruction effectue un incrément atomique de la valeur de compteur, en retournant l’original à *dst0*.</span><span class="sxs-lookup"><span data-stu-id="309e3-114">This instruction does an atomic increment of the counter value, returning the original to *dst0*.</span></span>

<span data-ttu-id="309e3-115">Pour un UAV Append, la valeur retournée est valide uniquement pendant la durée de l’appel du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="309e3-115">For an Append UAV, the returned value is only valid for the duration of the shader invocation.</span></span> <span data-ttu-id="309e3-116">Après cela, l’implémentation peut réorganiser la disposition de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="309e3-116">after that the implementation may rearrange the memory layout.</span></span> <span data-ttu-id="309e3-117">Tout adressage mémoire basé sur la valeur retournée doit être limité à l’appel du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="309e3-117">Any memory addressing based on the returned value must be limited to the shader invocation.</span></span>

<span data-ttu-id="309e3-118">Pour un UAV Append, dans l’appel du nuanceur, le compilateur HLSL peut utiliser la valeur retournée comme index de struct à utiliser pour accéder à la mémoire tampon structurée.</span><span class="sxs-lookup"><span data-stu-id="309e3-118">For an Append UAV, within the shader invocation the HLSL compiler can use the returned value as the struct index to use for accessing the structured buffer.</span></span> <span data-ttu-id="309e3-119">L’accès à n’importe quel index de struct autre que ceux qui sont retournés par les appels à **IMM \_ Atomic \_ Alloc** ou [ \_ consomment](imm-atomic-consume--sm5---asm-.md) des résultats indéfinis dans le sens où l’emplacement de la mémoire au sein du UAV fait l’objet d’un accès aléatoire est aléatoire et fixe uniquement pendant la durée de vie de l’appel du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="309e3-119">Accessing any struct index other than those locations returned by call(s) to **imm\_atomic\_alloc** or [\_consume](imm-atomic-consume--sm5---asm-.md) produce undefined results in that exactly which memory location within the UAV is being accessed is random and only fixed for the lifetime of the shader invocation.</span></span>

<span data-ttu-id="309e3-120">Pour un UAV Count, la valeur retournée peut être enregistrée par l’application en tant que référence à un emplacement fixe dans le UAV qui est explicite une fois l’appel du nuanceur terminé.</span><span class="sxs-lookup"><span data-stu-id="309e3-120">For a Count UAV, the returned value can be saved by the application as a reference to a fixed location within the UAV that is meaningful after the shader invocation is over.</span></span> <span data-ttu-id="309e3-121">Tout emplacement dans un UAV Count peut toujours être accessible indépendamment de la valeur de Count.</span><span class="sxs-lookup"><span data-stu-id="309e3-121">Any location in a Count UAV may always be accessed independent of what the count value is.</span></span>

<span data-ttu-id="309e3-122">Il n’y a pas de fixation du nombre. il est donc encapsulé en cas de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="309e3-122">There is no clamping of the count, so it wraps on overflow.</span></span>

<span data-ttu-id="309e3-123">Le même nuanceur ne peut pas tenter à la fois l' **\_ \_ allocation atomique de IMM** et le **IMM \_ Atomic \_ consommer** sur le même UAV.</span><span class="sxs-lookup"><span data-stu-id="309e3-123">The same shader cannot attempt both **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span> <span data-ttu-id="309e3-124">En outre, le GPU ne peut pas autoriser plusieurs appels de nuanceur à mélanger **\_ Atomic Atomic \_ Alloc** et **IMM \_ Atomic \_ consommer** sur le même UAV.</span><span class="sxs-lookup"><span data-stu-id="309e3-124">Further, the GPU cannot allow multiple shader invocations to mix **imm\_atomic\_alloc** and **imm\_atomic\_consume** on the same UAV.</span></span>

<span data-ttu-id="309e3-125">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="309e3-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="309e3-126">Sommet</span><span class="sxs-lookup"><span data-stu-id="309e3-126">Vertex</span></span> | <span data-ttu-id="309e3-127">Forme</span><span class="sxs-lookup"><span data-stu-id="309e3-127">Hull</span></span> | <span data-ttu-id="309e3-128">Domain</span><span class="sxs-lookup"><span data-stu-id="309e3-128">Domain</span></span> | <span data-ttu-id="309e3-129">Géométrie</span><span class="sxs-lookup"><span data-stu-id="309e3-129">Geometry</span></span> | <span data-ttu-id="309e3-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="309e3-130">Pixel</span></span> | <span data-ttu-id="309e3-131">Compute</span><span class="sxs-lookup"><span data-stu-id="309e3-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="309e3-132">X</span><span class="sxs-lookup"><span data-stu-id="309e3-132">X</span></span>     | <span data-ttu-id="309e3-133">X</span><span class="sxs-lookup"><span data-stu-id="309e3-133">X</span></span>       |



 

<span data-ttu-id="309e3-134">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="309e3-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="309e3-135">Sommet</span><span class="sxs-lookup"><span data-stu-id="309e3-135">Vertex</span></span> | <span data-ttu-id="309e3-136">Forme</span><span class="sxs-lookup"><span data-stu-id="309e3-136">Hull</span></span> | <span data-ttu-id="309e3-137">Domain</span><span class="sxs-lookup"><span data-stu-id="309e3-137">Domain</span></span> | <span data-ttu-id="309e3-138">Géométrie</span><span class="sxs-lookup"><span data-stu-id="309e3-138">Geometry</span></span> | <span data-ttu-id="309e3-139">Pixel</span><span class="sxs-lookup"><span data-stu-id="309e3-139">Pixel</span></span> | <span data-ttu-id="309e3-140">Compute</span><span class="sxs-lookup"><span data-stu-id="309e3-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="309e3-141">X</span><span class="sxs-lookup"><span data-stu-id="309e3-141">X</span></span>      | <span data-ttu-id="309e3-142">X</span><span class="sxs-lookup"><span data-stu-id="309e3-142">X</span></span>    | <span data-ttu-id="309e3-143">X</span><span class="sxs-lookup"><span data-stu-id="309e3-143">X</span></span>      | <span data-ttu-id="309e3-144">X</span><span class="sxs-lookup"><span data-stu-id="309e3-144">X</span></span>        | <span data-ttu-id="309e3-145">X</span><span class="sxs-lookup"><span data-stu-id="309e3-145">X</span></span>     | <span data-ttu-id="309e3-146">X</span><span class="sxs-lookup"><span data-stu-id="309e3-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="309e3-147">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="309e3-147">Minimum Shader Model</span></span>

<span data-ttu-id="309e3-148">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="309e3-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="309e3-149">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="309e3-149">Shader Model</span></span>                                              | <span data-ttu-id="309e3-150">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="309e3-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="309e3-151">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="309e3-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="309e3-152">Oui</span><span class="sxs-lookup"><span data-stu-id="309e3-152">yes</span></span>       |
| [<span data-ttu-id="309e3-153">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="309e3-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="309e3-154">non</span><span class="sxs-lookup"><span data-stu-id="309e3-154">no</span></span>        |
| [<span data-ttu-id="309e3-155">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="309e3-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="309e3-156">non</span><span class="sxs-lookup"><span data-stu-id="309e3-156">no</span></span>        |
| [<span data-ttu-id="309e3-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="309e3-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="309e3-158">non</span><span class="sxs-lookup"><span data-stu-id="309e3-158">no</span></span>        |
| [<span data-ttu-id="309e3-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="309e3-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="309e3-160">non</span><span class="sxs-lookup"><span data-stu-id="309e3-160">no</span></span>        |
| [<span data-ttu-id="309e3-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="309e3-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="309e3-162">non</span><span class="sxs-lookup"><span data-stu-id="309e3-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="309e3-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="309e3-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="309e3-164">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="309e3-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





