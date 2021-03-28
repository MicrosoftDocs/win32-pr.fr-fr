---
title: bfrev (SM5-ASM)
description: Inversez un nombre de 32 bits.
ms.assetid: 24F8209A-093E-4737-BF50-12F228024E9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11bf0f07b6c66babf8e7f91108f86ba753420fc2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990784"
---
# <a name="bfrev-sm5---asm"></a><span data-ttu-id="35ccd-103">bfrev (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="35ccd-103">bfrev (sm5 - asm)</span></span>

<span data-ttu-id="35ccd-104">Inversez un nombre de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="35ccd-104">Reverse a 32-bit number.</span></span>



| <span data-ttu-id="35ccd-105">bfrev dest \[ . Mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="35ccd-105">bfrev dest\[.mask\], src0\[.swizzle\]</span></span> |
|---------------------------------------|



 



| <span data-ttu-id="35ccd-106">Élément</span><span class="sxs-lookup"><span data-stu-id="35ccd-106">Item</span></span>                                                            | <span data-ttu-id="35ccd-107">Description</span><span class="sxs-lookup"><span data-stu-id="35ccd-107">Description</span></span>                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="35ccd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="35ccd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="35ccd-109">\[dans \] l’adresse de *src0* avec bits inversé.</span><span class="sxs-lookup"><span data-stu-id="35ccd-109">\[in\] The address for *src0* with bits reversed.</span></span><br/> |
| <span data-ttu-id="35ccd-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="35ccd-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="35ccd-111">\[dans \] le nombre 32 bits à inverser.</span><span class="sxs-lookup"><span data-stu-id="35ccd-111">\[in\] The 32-bit number to reverse.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="35ccd-112">Notes</span><span class="sxs-lookup"><span data-stu-id="35ccd-112">Remarks</span></span>

<span data-ttu-id="35ccd-113">Par exemple, pour 0x12345678 sinon, le résultat est 0x1e6a2c48.</span><span class="sxs-lookup"><span data-stu-id="35ccd-113">For example, given 0x12345678 the result would be 0x1e6a2c48.</span></span>

<span data-ttu-id="35ccd-114">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="35ccd-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="35ccd-115">Sommet</span><span class="sxs-lookup"><span data-stu-id="35ccd-115">Vertex</span></span> | <span data-ttu-id="35ccd-116">Forme</span><span class="sxs-lookup"><span data-stu-id="35ccd-116">Hull</span></span> | <span data-ttu-id="35ccd-117">Domain</span><span class="sxs-lookup"><span data-stu-id="35ccd-117">Domain</span></span> | <span data-ttu-id="35ccd-118">Géométrie</span><span class="sxs-lookup"><span data-stu-id="35ccd-118">Geometry</span></span> | <span data-ttu-id="35ccd-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="35ccd-119">Pixel</span></span> | <span data-ttu-id="35ccd-120">Compute</span><span class="sxs-lookup"><span data-stu-id="35ccd-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="35ccd-121">X</span><span class="sxs-lookup"><span data-stu-id="35ccd-121">X</span></span>      | <span data-ttu-id="35ccd-122">X</span><span class="sxs-lookup"><span data-stu-id="35ccd-122">X</span></span>    | <span data-ttu-id="35ccd-123">X</span><span class="sxs-lookup"><span data-stu-id="35ccd-123">X</span></span>      | <span data-ttu-id="35ccd-124">X</span><span class="sxs-lookup"><span data-stu-id="35ccd-124">X</span></span>        | <span data-ttu-id="35ccd-125">X</span><span class="sxs-lookup"><span data-stu-id="35ccd-125">X</span></span>     | <span data-ttu-id="35ccd-126">X</span><span class="sxs-lookup"><span data-stu-id="35ccd-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="35ccd-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="35ccd-127">Minimum Shader Model</span></span>

<span data-ttu-id="35ccd-128">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="35ccd-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="35ccd-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="35ccd-129">Shader Model</span></span>                                              | <span data-ttu-id="35ccd-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="35ccd-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="35ccd-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="35ccd-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="35ccd-132">Oui</span><span class="sxs-lookup"><span data-stu-id="35ccd-132">yes</span></span>       |
| [<span data-ttu-id="35ccd-133">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="35ccd-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="35ccd-134">non</span><span class="sxs-lookup"><span data-stu-id="35ccd-134">no</span></span>        |
| [<span data-ttu-id="35ccd-135">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="35ccd-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="35ccd-136">non</span><span class="sxs-lookup"><span data-stu-id="35ccd-136">no</span></span>        |
| [<span data-ttu-id="35ccd-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35ccd-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="35ccd-138">non</span><span class="sxs-lookup"><span data-stu-id="35ccd-138">no</span></span>        |
| [<span data-ttu-id="35ccd-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35ccd-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="35ccd-140">non</span><span class="sxs-lookup"><span data-stu-id="35ccd-140">no</span></span>        |
| [<span data-ttu-id="35ccd-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35ccd-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="35ccd-142">non</span><span class="sxs-lookup"><span data-stu-id="35ccd-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="35ccd-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35ccd-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35ccd-144">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35ccd-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





