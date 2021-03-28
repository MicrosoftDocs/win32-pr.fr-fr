---
title: dcl_uav_raw (SM5-ASM)
description: Déclarez une vue d’accès non triée (UAV) pour une utilisation par un nuanceur. | dcl_uav_raw (SM5-ASM)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f47614d5a9327f2d686a36db6bfe4afeb653788
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991949"
---
# <a name="dcl_uav_raw-sm5---asm"></a><span data-ttu-id="afcd1-104">DCL \_ UAV \_ brute (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="afcd1-104">dcl\_uav\_raw (sm5 - asm)</span></span>

<span data-ttu-id="afcd1-105">Déclarez une vue d’accès non triée (UAV) pour une utilisation par un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="afcd1-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="afcd1-106">DCL \_ UAV \_ brute \[ \_ GLC \] dstUAV</span><span class="sxs-lookup"><span data-stu-id="afcd1-106">dcl\_uav\_raw\[\_glc\] dstUAV</span></span> |
|-------------------------------|



 



| <span data-ttu-id="afcd1-107">Élément</span><span class="sxs-lookup"><span data-stu-id="afcd1-107">Item</span></span>                                                                                           | <span data-ttu-id="afcd1-108">Description</span><span class="sxs-lookup"><span data-stu-id="afcd1-108">Description</span></span>                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="afcd1-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="afcd1-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="afcd1-110">\[dans \] le UAV.</span><span class="sxs-lookup"><span data-stu-id="afcd1-110">\[in\] The UAV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="afcd1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="afcd1-111">Remarks</span></span>

<span data-ttu-id="afcd1-112">*dstUAV* est un \# Registre u déclaré comme référence à un UnorderedAccessView d’une mémoire tampon, où la mémoire tampon apparaît sous la forme d’un tableau 1D simple d’entrées non typées 32 bits.</span><span class="sxs-lookup"><span data-stu-id="afcd1-112">*dstUAV* is a u\# register declared as a reference to an UnorderedAccessView of a Buffer, where the buffer appears as a simple 1D array of 32-bit untyped entries.</span></span>

<span data-ttu-id="afcd1-113">Les opérations effectuées sur la mémoire peuvent interpréter implicitement les données comme ayant un type.</span><span class="sxs-lookup"><span data-stu-id="afcd1-113">Operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="afcd1-114">L' \_ indicateur GLC signifie « cohérence globale ».</span><span class="sxs-lookup"><span data-stu-id="afcd1-114">The \_glc flag means "globally coherent".</span></span> <span data-ttu-id="afcd1-115">L’absence de \_ GLC signifie que le UAV est déclaré comme « cohérent par le groupe » dans le nuanceur de calcul, ou « cohérent localement » dans un appel de nuanceur de pixel unique.</span><span class="sxs-lookup"><span data-stu-id="afcd1-115">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="afcd1-116">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="afcd1-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="afcd1-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="afcd1-117">Vertex</span></span> | <span data-ttu-id="afcd1-118">Forme</span><span class="sxs-lookup"><span data-stu-id="afcd1-118">Hull</span></span> | <span data-ttu-id="afcd1-119">Domain</span><span class="sxs-lookup"><span data-stu-id="afcd1-119">Domain</span></span> | <span data-ttu-id="afcd1-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="afcd1-120">Geometry</span></span> | <span data-ttu-id="afcd1-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="afcd1-121">Pixel</span></span> | <span data-ttu-id="afcd1-122">Compute</span><span class="sxs-lookup"><span data-stu-id="afcd1-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="afcd1-123">X</span><span class="sxs-lookup"><span data-stu-id="afcd1-123">X</span></span>     | <span data-ttu-id="afcd1-124">X</span><span class="sxs-lookup"><span data-stu-id="afcd1-124">X</span></span>       |



 

<span data-ttu-id="afcd1-125">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="afcd1-125">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="afcd1-126">Sommet</span><span class="sxs-lookup"><span data-stu-id="afcd1-126">Vertex</span></span> | <span data-ttu-id="afcd1-127">Forme</span><span class="sxs-lookup"><span data-stu-id="afcd1-127">Hull</span></span> | <span data-ttu-id="afcd1-128">Domain</span><span class="sxs-lookup"><span data-stu-id="afcd1-128">Domain</span></span> | <span data-ttu-id="afcd1-129">Géométrie</span><span class="sxs-lookup"><span data-stu-id="afcd1-129">Geometry</span></span> | <span data-ttu-id="afcd1-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="afcd1-130">Pixel</span></span> | <span data-ttu-id="afcd1-131">Compute</span><span class="sxs-lookup"><span data-stu-id="afcd1-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="afcd1-132">X</span><span class="sxs-lookup"><span data-stu-id="afcd1-132">X</span></span>      | <span data-ttu-id="afcd1-133">X</span><span class="sxs-lookup"><span data-stu-id="afcd1-133">X</span></span>    | <span data-ttu-id="afcd1-134">X</span><span class="sxs-lookup"><span data-stu-id="afcd1-134">X</span></span>      | <span data-ttu-id="afcd1-135">X</span><span class="sxs-lookup"><span data-stu-id="afcd1-135">X</span></span>        | <span data-ttu-id="afcd1-136">X</span><span class="sxs-lookup"><span data-stu-id="afcd1-136">X</span></span>     | <span data-ttu-id="afcd1-137">X</span><span class="sxs-lookup"><span data-stu-id="afcd1-137">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="afcd1-138">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="afcd1-138">Minimum Shader Model</span></span>

<span data-ttu-id="afcd1-139">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="afcd1-139">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="afcd1-140">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="afcd1-140">Shader Model</span></span>                                              | <span data-ttu-id="afcd1-141">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="afcd1-141">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="afcd1-142">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="afcd1-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="afcd1-143">Oui</span><span class="sxs-lookup"><span data-stu-id="afcd1-143">yes</span></span>       |
| [<span data-ttu-id="afcd1-144">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="afcd1-144">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="afcd1-145">non</span><span class="sxs-lookup"><span data-stu-id="afcd1-145">no</span></span>        |
| [<span data-ttu-id="afcd1-146">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="afcd1-146">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="afcd1-147">non</span><span class="sxs-lookup"><span data-stu-id="afcd1-147">no</span></span>        |
| [<span data-ttu-id="afcd1-148">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="afcd1-148">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="afcd1-149">non</span><span class="sxs-lookup"><span data-stu-id="afcd1-149">no</span></span>        |
| [<span data-ttu-id="afcd1-150">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="afcd1-150">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="afcd1-151">non</span><span class="sxs-lookup"><span data-stu-id="afcd1-151">no</span></span>        |
| [<span data-ttu-id="afcd1-152">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="afcd1-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="afcd1-153">non</span><span class="sxs-lookup"><span data-stu-id="afcd1-153">no</span></span>        |



 

> [!Note]  
> <span data-ttu-id="afcd1-154">Cette instruction est prise en charge dans cs \_ 4 \_ 0 et CS \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="afcd1-154">This instruction is supported in cs\_4\_0 and cs\_4\_1.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="afcd1-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="afcd1-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afcd1-156">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="afcd1-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





