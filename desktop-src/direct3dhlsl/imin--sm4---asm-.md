---
title: Imin (SM4-ASM)
description: Entier au niveau du composant minimal.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942384e7a988e4919a483e09c75e476d5a6917ba
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381204"
---
# <a name="imin-sm4---asm"></a><span data-ttu-id="3af2d-103">Imin (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3af2d-103">imin (sm4 - asm)</span></span>

<span data-ttu-id="3af2d-104">Entier au niveau du composant minimal.</span><span class="sxs-lookup"><span data-stu-id="3af2d-104">Component-wise integer minimum.</span></span>



| <span data-ttu-id="3af2d-105">Imin dest \[ . Mask \] , \[  - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="3af2d-105">imin dest\[.mask\], \[ -\]src0\[.swizzle\], \[-\]src1\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="3af2d-106">Élément</span><span class="sxs-lookup"><span data-stu-id="3af2d-106">Item</span></span>                                                            | <span data-ttu-id="3af2d-107">Description</span><span class="sxs-lookup"><span data-stu-id="3af2d-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3af2d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3af2d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3af2d-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3af2d-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="3af2d-110">*dest*  =  . *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="3af2d-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="3af2d-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="3af2d-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="3af2d-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3af2d-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3af2d-113">\[dans \] la valeur à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="3af2d-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                       |
| <span data-ttu-id="3af2d-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="3af2d-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="3af2d-115">\[dans \] la valeur à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="3af2d-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="3af2d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="3af2d-116">Remarks</span></span>

<span data-ttu-id="3af2d-117">Le modificateur de négation facultatif sur les opérandes source prend le complément à 2 avant d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="3af2d-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="3af2d-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="3af2d-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3af2d-119">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="3af2d-119">Vertex Shader</span></span> | <span data-ttu-id="3af2d-120">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="3af2d-120">Geometry Shader</span></span> | <span data-ttu-id="3af2d-121">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="3af2d-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3af2d-122">x</span><span class="sxs-lookup"><span data-stu-id="3af2d-122">x</span></span>             | <span data-ttu-id="3af2d-123">x</span><span class="sxs-lookup"><span data-stu-id="3af2d-123">x</span></span>               | <span data-ttu-id="3af2d-124">x</span><span class="sxs-lookup"><span data-stu-id="3af2d-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3af2d-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3af2d-125">Minimum Shader Model</span></span>

<span data-ttu-id="3af2d-126">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="3af2d-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3af2d-127">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3af2d-127">Shader Model</span></span>                                              | <span data-ttu-id="3af2d-128">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3af2d-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3af2d-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3af2d-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3af2d-130">Oui</span><span class="sxs-lookup"><span data-stu-id="3af2d-130">yes</span></span>       |
| [<span data-ttu-id="3af2d-131">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="3af2d-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3af2d-132">Oui</span><span class="sxs-lookup"><span data-stu-id="3af2d-132">yes</span></span>       |
| [<span data-ttu-id="3af2d-133">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="3af2d-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3af2d-134">Oui</span><span class="sxs-lookup"><span data-stu-id="3af2d-134">yes</span></span>       |
| [<span data-ttu-id="3af2d-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3af2d-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3af2d-136">non</span><span class="sxs-lookup"><span data-stu-id="3af2d-136">no</span></span>        |
| [<span data-ttu-id="3af2d-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3af2d-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3af2d-138">non</span><span class="sxs-lookup"><span data-stu-id="3af2d-138">no</span></span>        |
| [<span data-ttu-id="3af2d-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3af2d-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3af2d-140">non</span><span class="sxs-lookup"><span data-stu-id="3af2d-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3af2d-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3af2d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3af2d-142">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3af2d-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





