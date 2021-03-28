---
title: Mad (SM4-ASM)
description: Ajout par multiplication au niveau du composant.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d34823cdb3545f29426117b35903c97c08c5807
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030569"
---
# <a name="mad-sm4---asm"></a><span data-ttu-id="4c860-103">Mad (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4c860-103">mad (sm4 - asm)</span></span>

<span data-ttu-id="4c860-104">Multiplier par le composant & ajouter.</span><span class="sxs-lookup"><span data-stu-id="4c860-104">Component-wise multiply & add.</span></span>



| <span data-ttu-id="4c860-105">: Mad \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="4c860-105">:mad\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="4c860-106">Élément</span><span class="sxs-lookup"><span data-stu-id="4c860-106">Item</span></span>                                                            | <span data-ttu-id="4c860-107">Description</span><span class="sxs-lookup"><span data-stu-id="4c860-107">Description</span></span>                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c860-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4c860-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4c860-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="4c860-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="4c860-110">*dest*  =  . *src0* \* *src1*  +  *src2*</span><span class="sxs-lookup"><span data-stu-id="4c860-110">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="4c860-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4c860-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4c860-112">\[dans \] le multiplicande.</span><span class="sxs-lookup"><span data-stu-id="4c860-112">\[in\] The multiplicand.</span></span><br/>                                                          |
| <span data-ttu-id="4c860-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="4c860-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="4c860-114">\[dans \] le multiplicateur.</span><span class="sxs-lookup"><span data-stu-id="4c860-114">\[in\] The multiplier.</span></span><br/>                                                            |
| <span data-ttu-id="4c860-115"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="4c860-115"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="4c860-116">\[dans \] le addend.</span><span class="sxs-lookup"><span data-stu-id="4c860-116">\[in\] The addend.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="4c860-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4c860-117">Remarks</span></span>

<span data-ttu-id="4c860-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="4c860-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4c860-119">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="4c860-119">Vertex Shader</span></span> | <span data-ttu-id="4c860-120">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="4c860-120">Geometry Shader</span></span> | <span data-ttu-id="4c860-121">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="4c860-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4c860-122">x</span><span class="sxs-lookup"><span data-stu-id="4c860-122">x</span></span>             | <span data-ttu-id="4c860-123">x</span><span class="sxs-lookup"><span data-stu-id="4c860-123">x</span></span>               | <span data-ttu-id="4c860-124">x</span><span class="sxs-lookup"><span data-stu-id="4c860-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4c860-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4c860-125">Minimum Shader Model</span></span>

<span data-ttu-id="4c860-126">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="4c860-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4c860-127">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4c860-127">Shader Model</span></span>                                              | <span data-ttu-id="4c860-128">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="4c860-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4c860-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4c860-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4c860-130">Oui</span><span class="sxs-lookup"><span data-stu-id="4c860-130">yes</span></span>       |
| [<span data-ttu-id="4c860-131">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="4c860-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4c860-132">Oui</span><span class="sxs-lookup"><span data-stu-id="4c860-132">yes</span></span>       |
| [<span data-ttu-id="4c860-133">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="4c860-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4c860-134">Oui</span><span class="sxs-lookup"><span data-stu-id="4c860-134">yes</span></span>       |
| [<span data-ttu-id="4c860-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c860-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4c860-136">non</span><span class="sxs-lookup"><span data-stu-id="4c860-136">no</span></span>        |
| [<span data-ttu-id="4c860-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c860-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4c860-138">non</span><span class="sxs-lookup"><span data-stu-id="4c860-138">no</span></span>        |
| [<span data-ttu-id="4c860-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c860-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4c860-140">non</span><span class="sxs-lookup"><span data-stu-id="4c860-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4c860-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c860-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c860-142">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c860-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





