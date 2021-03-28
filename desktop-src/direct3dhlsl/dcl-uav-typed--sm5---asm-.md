---
title: dcl_uav_typed (SM5-ASM)
description: Déclarez une vue d’accès non triée (UAV) pour une utilisation par un nuanceur. | dcl_uav_typed (SM5-ASM)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b789714c7ec825620b73e387fa8a4dd73e1a590d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992101"
---
# <a name="dcl_uav_typed-sm5---asm"></a><span data-ttu-id="8edf9-104">DCL \_ UAV \_ typée (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8edf9-104">dcl\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="8edf9-105">Déclarez une vue d’accès non triée (UAV) pour une utilisation par un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="8edf9-105">Declare an unordered access view (UAV) for use by a shader.</span></span>



| <span data-ttu-id="8edf9-106">DCL \_ UAV \_ typé \[ \_ GLC \] dstUAV, dimension, type</span><span class="sxs-lookup"><span data-stu-id="8edf9-106">dcl\_uav\_typed\[\_glc\] dstUAV, dimension, type</span></span> |
|--------------------------------------------------|



 



| <span data-ttu-id="8edf9-107">Élément</span><span class="sxs-lookup"><span data-stu-id="8edf9-107">Item</span></span>                                                                                           | <span data-ttu-id="8edf9-108">Description</span><span class="sxs-lookup"><span data-stu-id="8edf9-108">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8edf9-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="8edf9-109"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/> | <span data-ttu-id="8edf9-110">\[dans \] le UAV.</span><span class="sxs-lookup"><span data-stu-id="8edf9-110">\[in\] The UAV.</span></span><br/>                                                                        |
| <span data-ttu-id="8edf9-111"><span id="dimension"></span><span id="DIMENSION"></span>*codes*</span><span class="sxs-lookup"><span data-stu-id="8edf9-111"><span id="dimension"></span><span id="DIMENSION"></span>*dimension*</span></span><br/>                 | <span data-ttu-id="8edf9-112">\[dans \] spécifie le nombre de dimensions fournies par les instructions qui accèdent au UAV.</span><span class="sxs-lookup"><span data-stu-id="8edf9-112">\[in\] Specifies how many dimensions the instructions accessing the UAV are providing.</span></span><br/> |
| <span data-ttu-id="8edf9-113"><span id="type"></span><span id="TYPE"></span>*entrer*</span><span class="sxs-lookup"><span data-stu-id="8edf9-113"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                                | <span data-ttu-id="8edf9-114">\[dans \] le type de UAV.</span><span class="sxs-lookup"><span data-stu-id="8edf9-114">\[in\] The type of the UAV.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="8edf9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8edf9-115">Remarks</span></span>

<span data-ttu-id="8edf9-116">*dstUAV* est un \# Registre u qui est déclaré en tant que référence à un UnorderedAccessView qui doit être lié à \# l’emplacement UAV au niveau de l’API.</span><span class="sxs-lookup"><span data-stu-id="8edf9-116">*dstUAV* is a u\# register being declared as a reference to an UnorderedAccessView that must be bound to UAV slot \# at the API.</span></span>

<span data-ttu-id="8edf9-117">La dimension doit être buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray ou Texture3D.</span><span class="sxs-lookup"><span data-stu-id="8edf9-117">The dimension must be buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray, or Texture3D.</span></span> <span data-ttu-id="8edf9-118">Cela indique le nombre de dimensions fournies par toutes les instructions qui accèdent au UAV : 1 (Texture1D, buffer), 2 (Texture1DArray, Texture2D) ou 3 (Texture2DArray, Texture3D).</span><span class="sxs-lookup"><span data-stu-id="8edf9-118">This indicates how many dimensions any instructions accessing the UAV are providing: 1 (Texture1D, Buffer), 2 (Texture1DArray, Texture2D) or 3 (Texture2DArray, Texture3D).</span></span>

<span data-ttu-id="8edf9-119">Le type est {UNORM, RONFLEr, UINT, Saint, FLOAT}.</span><span class="sxs-lookup"><span data-stu-id="8edf9-119">Type is {UNORM,SNORM,UINT,SINT,FLOAT}.</span></span> <span data-ttu-id="8edf9-120">Les opérations effectuées avec l’u déclaré \# doivent être compatibles avec le type déclaré ici, et la UAV liée à l’emplacement \# doit également avoir le même type.</span><span class="sxs-lookup"><span data-stu-id="8edf9-120">Operations done with the declared u\# must be compatible with the type declared here, and the UAV bound to slot \# must also have the same type.</span></span>

<span data-ttu-id="8edf9-121">L' \_ indicateur GLC signifie « cohérence globale ».</span><span class="sxs-lookup"><span data-stu-id="8edf9-121">The \_glc flag stands for "globally coherent".</span></span> <span data-ttu-id="8edf9-122">L’absence de \_ GLC signifie que le UAV est déclaré comme « cohérent par le groupe » dans le nuanceur de calcul, ou « cohérent localement » dans un appel de nuanceur de pixel unique.</span><span class="sxs-lookup"><span data-stu-id="8edf9-122">The absence of \_glc means the UAV is being declared only as "group coherent" in the compute shader, or "locally coherent" in a single pixel shader invocation.</span></span>

<span data-ttu-id="8edf9-123">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="8edf9-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8edf9-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="8edf9-124">Vertex</span></span> | <span data-ttu-id="8edf9-125">Forme</span><span class="sxs-lookup"><span data-stu-id="8edf9-125">Hull</span></span> | <span data-ttu-id="8edf9-126">Domain</span><span class="sxs-lookup"><span data-stu-id="8edf9-126">Domain</span></span> | <span data-ttu-id="8edf9-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="8edf9-127">Geometry</span></span> | <span data-ttu-id="8edf9-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="8edf9-128">Pixel</span></span> | <span data-ttu-id="8edf9-129">Compute</span><span class="sxs-lookup"><span data-stu-id="8edf9-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8edf9-130">X</span><span class="sxs-lookup"><span data-stu-id="8edf9-130">X</span></span>     | <span data-ttu-id="8edf9-131">X</span><span class="sxs-lookup"><span data-stu-id="8edf9-131">X</span></span>       |



 

<span data-ttu-id="8edf9-132">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8edf9-132">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="8edf9-133">Sommet</span><span class="sxs-lookup"><span data-stu-id="8edf9-133">Vertex</span></span> | <span data-ttu-id="8edf9-134">Forme</span><span class="sxs-lookup"><span data-stu-id="8edf9-134">Hull</span></span> | <span data-ttu-id="8edf9-135">Domain</span><span class="sxs-lookup"><span data-stu-id="8edf9-135">Domain</span></span> | <span data-ttu-id="8edf9-136">Géométrie</span><span class="sxs-lookup"><span data-stu-id="8edf9-136">Geometry</span></span> | <span data-ttu-id="8edf9-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="8edf9-137">Pixel</span></span> | <span data-ttu-id="8edf9-138">Compute</span><span class="sxs-lookup"><span data-stu-id="8edf9-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8edf9-139">X</span><span class="sxs-lookup"><span data-stu-id="8edf9-139">X</span></span>      | <span data-ttu-id="8edf9-140">X</span><span class="sxs-lookup"><span data-stu-id="8edf9-140">X</span></span>    | <span data-ttu-id="8edf9-141">X</span><span class="sxs-lookup"><span data-stu-id="8edf9-141">X</span></span>      | <span data-ttu-id="8edf9-142">X</span><span class="sxs-lookup"><span data-stu-id="8edf9-142">X</span></span>        | <span data-ttu-id="8edf9-143">X</span><span class="sxs-lookup"><span data-stu-id="8edf9-143">X</span></span>     | <span data-ttu-id="8edf9-144">X</span><span class="sxs-lookup"><span data-stu-id="8edf9-144">X</span></span>       |



 

> [!Note]  
> <span data-ttu-id="8edf9-145">Cette instruction n’est pas prise en charge dans le nuanceur de calcul 4. x.</span><span class="sxs-lookup"><span data-stu-id="8edf9-145">This instruction is not supported in compute shader 4.x.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="8edf9-146">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="8edf9-146">Minimum Shader Model</span></span>

<span data-ttu-id="8edf9-147">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="8edf9-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8edf9-148">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="8edf9-148">Shader Model</span></span>                                              | <span data-ttu-id="8edf9-149">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="8edf9-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8edf9-150">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="8edf9-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8edf9-151">Oui</span><span class="sxs-lookup"><span data-stu-id="8edf9-151">yes</span></span>       |
| [<span data-ttu-id="8edf9-152">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="8edf9-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8edf9-153">non</span><span class="sxs-lookup"><span data-stu-id="8edf9-153">no</span></span>        |
| [<span data-ttu-id="8edf9-154">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="8edf9-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8edf9-155">non</span><span class="sxs-lookup"><span data-stu-id="8edf9-155">no</span></span>        |
| [<span data-ttu-id="8edf9-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8edf9-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8edf9-157">non</span><span class="sxs-lookup"><span data-stu-id="8edf9-157">no</span></span>        |
| [<span data-ttu-id="8edf9-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8edf9-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8edf9-159">non</span><span class="sxs-lookup"><span data-stu-id="8edf9-159">no</span></span>        |
| [<span data-ttu-id="8edf9-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8edf9-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8edf9-161">non</span><span class="sxs-lookup"><span data-stu-id="8edf9-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8edf9-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8edf9-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8edf9-163">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8edf9-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





