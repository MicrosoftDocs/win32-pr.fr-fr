---
title: f16tof32 (SM5-ASM)
description: Conversion float16 à float32 au niveau du composant. | f16tof32 (SM5-ASM)
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d53af1f2eab1f50dfded820bf27b2cda8f23e6b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974139"
---
# <a name="f16tof32-sm5---asm"></a><span data-ttu-id="c9dec-104">f16tof32 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c9dec-104">f16tof32 (sm5 - asm)</span></span>

<span data-ttu-id="c9dec-105">Conversion float16 à float32 au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="c9dec-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="c9dec-106">f16tof32 dest \[ . Mask \] , \[ - \] src \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c9dec-106">f16tof32 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="c9dec-107">Élément</span><span class="sxs-lookup"><span data-stu-id="c9dec-107">Item</span></span>                                                            | <span data-ttu-id="c9dec-108">Description</span><span class="sxs-lookup"><span data-stu-id="c9dec-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9dec-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c9dec-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c9dec-110">\[dans \] l’adresse du résultat float32.</span><span class="sxs-lookup"><span data-stu-id="c9dec-110">\[in\] The address of the float32 result.</span></span><br/> |
| <span data-ttu-id="c9dec-111"><span id="src"></span><span id="SRC"></span>*sources*</span><span class="sxs-lookup"><span data-stu-id="c9dec-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="c9dec-112">\[dans \] la valeur float16 à convertir.</span><span class="sxs-lookup"><span data-stu-id="c9dec-112">\[in\] The float16 value to convert.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="c9dec-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c9dec-113">Remarks</span></span>

<span data-ttu-id="c9dec-114">Cette opération effectue une conversion au niveau du composant d’une valeur float16 de LSB bits en un résultat float32.</span><span class="sxs-lookup"><span data-stu-id="c9dec-114">This operation performs a component-wise conversion of a float16 value from LSB bits to a float32 result.</span></span>

<span data-ttu-id="c9dec-115">Cette opération suit les règles D3D pour la conversion à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="c9dec-115">This operation follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="c9dec-116">Utilisez cette instruction pour la décompression des données pilotées par un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c9dec-116">Use this instruction for shader-driven data decompression.</span></span>

<span data-ttu-id="c9dec-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="c9dec-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c9dec-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="c9dec-118">Vertex</span></span> | <span data-ttu-id="c9dec-119">Forme</span><span class="sxs-lookup"><span data-stu-id="c9dec-119">Hull</span></span> | <span data-ttu-id="c9dec-120">Domain</span><span class="sxs-lookup"><span data-stu-id="c9dec-120">Domain</span></span> | <span data-ttu-id="c9dec-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="c9dec-121">Geometry</span></span> | <span data-ttu-id="c9dec-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="c9dec-122">Pixel</span></span> | <span data-ttu-id="c9dec-123">Compute</span><span class="sxs-lookup"><span data-stu-id="c9dec-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c9dec-124">X</span><span class="sxs-lookup"><span data-stu-id="c9dec-124">X</span></span>      | <span data-ttu-id="c9dec-125">X</span><span class="sxs-lookup"><span data-stu-id="c9dec-125">X</span></span>    | <span data-ttu-id="c9dec-126">X</span><span class="sxs-lookup"><span data-stu-id="c9dec-126">X</span></span>      | <span data-ttu-id="c9dec-127">X</span><span class="sxs-lookup"><span data-stu-id="c9dec-127">X</span></span>        | <span data-ttu-id="c9dec-128">X</span><span class="sxs-lookup"><span data-stu-id="c9dec-128">X</span></span>     | <span data-ttu-id="c9dec-129">X</span><span class="sxs-lookup"><span data-stu-id="c9dec-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c9dec-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c9dec-130">Minimum Shader Model</span></span>

<span data-ttu-id="c9dec-131">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="c9dec-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c9dec-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c9dec-132">Shader Model</span></span>                                              | <span data-ttu-id="c9dec-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="c9dec-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c9dec-134">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="c9dec-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c9dec-135">Oui</span><span class="sxs-lookup"><span data-stu-id="c9dec-135">yes</span></span>       |
| [<span data-ttu-id="c9dec-136">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="c9dec-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c9dec-137">non</span><span class="sxs-lookup"><span data-stu-id="c9dec-137">no</span></span>        |
| [<span data-ttu-id="c9dec-138">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="c9dec-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c9dec-139">non</span><span class="sxs-lookup"><span data-stu-id="c9dec-139">no</span></span>        |
| [<span data-ttu-id="c9dec-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9dec-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c9dec-141">non</span><span class="sxs-lookup"><span data-stu-id="c9dec-141">no</span></span>        |
| [<span data-ttu-id="c9dec-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9dec-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c9dec-143">non</span><span class="sxs-lookup"><span data-stu-id="c9dec-143">no</span></span>        |
| [<span data-ttu-id="c9dec-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9dec-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c9dec-145">non</span><span class="sxs-lookup"><span data-stu-id="c9dec-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c9dec-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9dec-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9dec-147">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c9dec-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





