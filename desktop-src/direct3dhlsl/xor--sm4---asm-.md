---
title: XOR (SM4-ASM)
description: XOR au niveau du bit.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a998bd1e95793f463d7f234b464a542bed4fc0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381129"
---
# <a name="xor-sm4---asm"></a><span data-ttu-id="eb5c6-103">XOR (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="eb5c6-103">xor (sm4 - asm)</span></span>

<span data-ttu-id="eb5c6-104">XOR au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-104">Bitwise xor.</span></span>



| <span data-ttu-id="eb5c6-105">XOR dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="eb5c6-105">xor dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="eb5c6-106">Élément</span><span class="sxs-lookup"><span data-stu-id="eb5c6-106">Item</span></span>                                                            | <span data-ttu-id="eb5c6-107">Description</span><span class="sxs-lookup"><span data-stu-id="eb5c6-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eb5c6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="eb5c6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="eb5c6-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-109">\[in\] The result of the operation.</span></span><br/>       |
| <span data-ttu-id="eb5c6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="eb5c6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="eb5c6-111">\[dans \] les composants à XOR avec *src1*.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-111">\[in\] The components to XOR with *src1*.</span></span><br/> |
| <span data-ttu-id="eb5c6-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="eb5c6-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="eb5c6-113">\[dans \] les composants à XOR avec *src0*.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-113">\[in\] The components to XOR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb5c6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="eb5c6-114">Remarks</span></span>

<span data-ttu-id="eb5c6-115">Cette instruction effectue un XOR logique au niveau du composant de chaque paire de valeurs 32 bits à partir de *src0* et *src1*.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-115">This instruction performs a component-wise logical XOR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="eb5c6-116">les résultats 32 bits sont placés dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-116">32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="eb5c6-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="eb5c6-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eb5c6-118">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="eb5c6-118">Vertex Shader</span></span> | <span data-ttu-id="eb5c6-119">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="eb5c6-119">Geometry Shader</span></span> | <span data-ttu-id="eb5c6-120">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="eb5c6-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="eb5c6-121">x</span><span class="sxs-lookup"><span data-stu-id="eb5c6-121">x</span></span>             | <span data-ttu-id="eb5c6-122">x</span><span class="sxs-lookup"><span data-stu-id="eb5c6-122">x</span></span>               | <span data-ttu-id="eb5c6-123">x</span><span class="sxs-lookup"><span data-stu-id="eb5c6-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eb5c6-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="eb5c6-124">Minimum Shader Model</span></span>

<span data-ttu-id="eb5c6-125">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="eb5c6-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="eb5c6-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="eb5c6-126">Shader Model</span></span>                                              | <span data-ttu-id="eb5c6-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="eb5c6-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eb5c6-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="eb5c6-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eb5c6-129">Oui</span><span class="sxs-lookup"><span data-stu-id="eb5c6-129">yes</span></span>       |
| [<span data-ttu-id="eb5c6-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="eb5c6-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eb5c6-131">Oui</span><span class="sxs-lookup"><span data-stu-id="eb5c6-131">yes</span></span>       |
| [<span data-ttu-id="eb5c6-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="eb5c6-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eb5c6-133">Oui</span><span class="sxs-lookup"><span data-stu-id="eb5c6-133">yes</span></span>       |
| [<span data-ttu-id="eb5c6-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb5c6-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eb5c6-135">non</span><span class="sxs-lookup"><span data-stu-id="eb5c6-135">no</span></span>        |
| [<span data-ttu-id="eb5c6-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb5c6-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eb5c6-137">non</span><span class="sxs-lookup"><span data-stu-id="eb5c6-137">no</span></span>        |
| [<span data-ttu-id="eb5c6-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb5c6-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eb5c6-139">non</span><span class="sxs-lookup"><span data-stu-id="eb5c6-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eb5c6-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb5c6-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb5c6-141">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eb5c6-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





