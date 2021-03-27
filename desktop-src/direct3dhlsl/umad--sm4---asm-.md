---
title: UMAD (SM4-ASM)
description: Entier non signé multiplier et ajouter.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce52925622cb2f6f7cf53dec0e3f6f65d3fdcb58
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679129"
---
# <a name="umad-sm4---asm"></a><span data-ttu-id="c363c-103">UMAD (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c363c-103">umad (sm4 - asm)</span></span>

<span data-ttu-id="c363c-104">Entier non signé multiplier et ajouter.</span><span class="sxs-lookup"><span data-stu-id="c363c-104">Unsigned integer multiply and add.</span></span>



| <span data-ttu-id="c363c-105">UMAD dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c363c-105">umad dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="c363c-106">Élément</span><span class="sxs-lookup"><span data-stu-id="c363c-106">Item</span></span>                                                            | <span data-ttu-id="c363c-107">Description</span><span class="sxs-lookup"><span data-stu-id="c363c-107">Description</span></span>                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c363c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c363c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c363c-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c363c-109">\[in\] The address of the result of the operation.</span></span><br/>           |
| <span data-ttu-id="c363c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c363c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c363c-111">\[dans \] la valeur à multiplier avec *src1*.</span><span class="sxs-lookup"><span data-stu-id="c363c-111">\[in\] The value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="c363c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c363c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c363c-113">\[dans \] la valeur à multiplier avec *src1*.</span><span class="sxs-lookup"><span data-stu-id="c363c-113">\[in\] The value to multiply with *src1*.</span></span><br/>                     |
| <span data-ttu-id="c363c-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="c363c-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="c363c-115">\[\]valeur à ajouter au produit de *src0* et *src1*.</span><span class="sxs-lookup"><span data-stu-id="c363c-115">\[in\] The value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c363c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c363c-116">Remarks</span></span>

<span data-ttu-id="c363c-117">[Umul](umul--sm4---asm-.md) des opérandes 32 bits *src0* et *src1* non signés, en conservant les 32 bits de poids faible, par composant, du résultat.</span><span class="sxs-lookup"><span data-stu-id="c363c-117">Component-wise [umul](umul--sm4---asm-.md) of 32-bit operands *src0* and *src1* unsigned, keeping the low 32-bits, per component, of the result.</span></span> <span data-ttu-id="c363c-118">Cette instruction effectue ensuite un [IAdd](iadd--sm4---asm-.md) de *src2*, en produisant le résultat à faible bit de 32 bits (par composant).</span><span class="sxs-lookup"><span data-stu-id="c363c-118">This instruction then performs an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="c363c-119">Les résultats 32 bits sont placés dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="c363c-119">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="c363c-120">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="c363c-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c363c-121">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="c363c-121">Vertex Shader</span></span> | <span data-ttu-id="c363c-122">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="c363c-122">Geometry Shader</span></span> | <span data-ttu-id="c363c-123">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c363c-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c363c-124">x</span><span class="sxs-lookup"><span data-stu-id="c363c-124">x</span></span>             | <span data-ttu-id="c363c-125">x</span><span class="sxs-lookup"><span data-stu-id="c363c-125">x</span></span>               | <span data-ttu-id="c363c-126">x</span><span class="sxs-lookup"><span data-stu-id="c363c-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c363c-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c363c-127">Minimum Shader Model</span></span>

<span data-ttu-id="c363c-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="c363c-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c363c-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c363c-129">Shader Model</span></span>                                              | <span data-ttu-id="c363c-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="c363c-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c363c-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="c363c-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c363c-132">Oui</span><span class="sxs-lookup"><span data-stu-id="c363c-132">yes</span></span>       |
| [<span data-ttu-id="c363c-133">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="c363c-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c363c-134">Oui</span><span class="sxs-lookup"><span data-stu-id="c363c-134">yes</span></span>       |
| [<span data-ttu-id="c363c-135">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="c363c-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c363c-136">Oui</span><span class="sxs-lookup"><span data-stu-id="c363c-136">yes</span></span>       |
| [<span data-ttu-id="c363c-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c363c-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c363c-138">non</span><span class="sxs-lookup"><span data-stu-id="c363c-138">no</span></span>        |
| [<span data-ttu-id="c363c-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c363c-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c363c-140">non</span><span class="sxs-lookup"><span data-stu-id="c363c-140">no</span></span>        |
| [<span data-ttu-id="c363c-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c363c-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c363c-142">non</span><span class="sxs-lookup"><span data-stu-id="c363c-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c363c-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c363c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c363c-144">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c363c-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





