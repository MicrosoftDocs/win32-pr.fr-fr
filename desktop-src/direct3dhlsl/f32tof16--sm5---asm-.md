---
title: f32tof16 (SM5-ASM)
description: Conversion float16 à float32 au niveau du composant. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974398"
---
# <a name="f32tof16-sm5---asm"></a><span data-ttu-id="0b534-104">f32tof16 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0b534-104">f32tof16 (sm5 - asm)</span></span>

<span data-ttu-id="0b534-105">Conversion float16 à float32 au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="0b534-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="0b534-106">f32tof16 dest \[ . Mask \] , \[ - \] src \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0b534-106">f32tof16 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="0b534-107">Élément</span><span class="sxs-lookup"><span data-stu-id="0b534-107">Item</span></span>                                                            | <span data-ttu-id="0b534-108">Description</span><span class="sxs-lookup"><span data-stu-id="0b534-108">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="0b534-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0b534-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0b534-110">\[dans \] l’adresse du résultat de float16.</span><span class="sxs-lookup"><span data-stu-id="0b534-110">\[in\] The address of float16 result.</span></span><br/> |
| <span data-ttu-id="0b534-111"><span id="src"></span><span id="SRC"></span>*sources*</span><span class="sxs-lookup"><span data-stu-id="0b534-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="0b534-112">\[dans \] la valeur float32 à convertir.</span><span class="sxs-lookup"><span data-stu-id="0b534-112">\[in\] The float32 value to convert.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="0b534-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0b534-113">Remarks</span></span>

<span data-ttu-id="0b534-114">Cette instruction effectue une conversion au niveau du composant d’une valeur float32 en un résultat de valeur float16 placé dans le LSB 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0b534-114">This instruction performs a component-wise conversion of a float32 value to a float16 value result placed in LSB 16 bits.</span></span>

<span data-ttu-id="0b534-115">Cette instruction suit les règles D3D pour la conversion à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="0b534-115">This instruction follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="0b534-116">Utilisez cette instruction pour la compression des données pilotées par un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0b534-116">Use this instruction for shader-driven data compression.</span></span>

<span data-ttu-id="0b534-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="0b534-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0b534-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="0b534-118">Vertex</span></span> | <span data-ttu-id="0b534-119">Forme</span><span class="sxs-lookup"><span data-stu-id="0b534-119">Hull</span></span> | <span data-ttu-id="0b534-120">Domain</span><span class="sxs-lookup"><span data-stu-id="0b534-120">Domain</span></span> | <span data-ttu-id="0b534-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="0b534-121">Geometry</span></span> | <span data-ttu-id="0b534-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="0b534-122">Pixel</span></span> | <span data-ttu-id="0b534-123">Compute</span><span class="sxs-lookup"><span data-stu-id="0b534-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0b534-124">X</span><span class="sxs-lookup"><span data-stu-id="0b534-124">X</span></span>      | <span data-ttu-id="0b534-125">X</span><span class="sxs-lookup"><span data-stu-id="0b534-125">X</span></span>    | <span data-ttu-id="0b534-126">X</span><span class="sxs-lookup"><span data-stu-id="0b534-126">X</span></span>      | <span data-ttu-id="0b534-127">X</span><span class="sxs-lookup"><span data-stu-id="0b534-127">X</span></span>        | <span data-ttu-id="0b534-128">X</span><span class="sxs-lookup"><span data-stu-id="0b534-128">X</span></span>     | <span data-ttu-id="0b534-129">X</span><span class="sxs-lookup"><span data-stu-id="0b534-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0b534-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0b534-130">Minimum Shader Model</span></span>

<span data-ttu-id="0b534-131">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="0b534-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0b534-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0b534-132">Shader Model</span></span>                                              | <span data-ttu-id="0b534-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0b534-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0b534-134">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="0b534-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0b534-135">Oui</span><span class="sxs-lookup"><span data-stu-id="0b534-135">yes</span></span>       |
| [<span data-ttu-id="0b534-136">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="0b534-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0b534-137">non</span><span class="sxs-lookup"><span data-stu-id="0b534-137">no</span></span>        |
| [<span data-ttu-id="0b534-138">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="0b534-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0b534-139">non</span><span class="sxs-lookup"><span data-stu-id="0b534-139">no</span></span>        |
| [<span data-ttu-id="0b534-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b534-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0b534-141">non</span><span class="sxs-lookup"><span data-stu-id="0b534-141">no</span></span>        |
| [<span data-ttu-id="0b534-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b534-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0b534-143">non</span><span class="sxs-lookup"><span data-stu-id="0b534-143">no</span></span>        |
| [<span data-ttu-id="0b534-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b534-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0b534-145">non</span><span class="sxs-lookup"><span data-stu-id="0b534-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0b534-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b534-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b534-147">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b534-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





