---
title: imad (SM4-ASM)
description: L’entier signé est multiplié et ajouté.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990716"
---
# <a name="imad-sm4---asm"></a><span data-ttu-id="12aaa-103">imad (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="12aaa-103">imad (sm4 - asm)</span></span>

<span data-ttu-id="12aaa-104">L’entier signé est multiplié et ajouté.</span><span class="sxs-lookup"><span data-stu-id="12aaa-104">Signed integer multiply and add.</span></span>



| <span data-ttu-id="12aaa-105">imad dest \[ . Mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle \] , \[ - \] src2 \[ . Swizzle</span><span class="sxs-lookup"><span data-stu-id="12aaa-105">imad dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\], \[-\]src2\[.swizzle</span></span> |
|---------------------------------------------------------------------------------------|



 



| <span data-ttu-id="12aaa-106">Élément</span><span class="sxs-lookup"><span data-stu-id="12aaa-106">Item</span></span>                                                            | <span data-ttu-id="12aaa-107">Description</span><span class="sxs-lookup"><span data-stu-id="12aaa-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="12aaa-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="12aaa-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="12aaa-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="12aaa-109">\[in\] The result of the operation.</span></span><br/>                      |
| <span data-ttu-id="12aaa-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="12aaa-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="12aaa-111">\[\]valeur à multiplier avec *src1*.</span><span class="sxs-lookup"><span data-stu-id="12aaa-111">\[in\] Value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="12aaa-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="12aaa-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="12aaa-113">\[\]valeur à multiplier avec *src0*.</span><span class="sxs-lookup"><span data-stu-id="12aaa-113">\[in\] Value to multiply with *src0*.</span></span><br/>                    |
| <span data-ttu-id="12aaa-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="12aaa-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="12aaa-115">\[\]valeur à ajouter au produit de *src0* et *src1*.</span><span class="sxs-lookup"><span data-stu-id="12aaa-115">\[in\] Value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="12aaa-116">Notes</span><span class="sxs-lookup"><span data-stu-id="12aaa-116">Remarks</span></span>

<span data-ttu-id="12aaa-117">[Imul](imul--sm4---asm-.md) au niveau du composant des opérandes 32 bits *src0* et *src1* (signé), en conservant le résultat 32 bas (par composant) du résultat, suivi d’un [IAdd](iadd--sm4---asm-.md) de *src2*, ce qui produit le résultat de 32 bits (par composant) correct.</span><span class="sxs-lookup"><span data-stu-id="12aaa-117">Component-wise [imul](imul--sm4---asm-.md) of 32-bit operands *src0* and *src1* (signed), keeping low 32-bits (per component) of the result, followed by an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="12aaa-118">Les résultats 32 bits sont placés dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="12aaa-118">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="12aaa-119">Le modificateur de négation facultatif sur les opérandes source prend le complément à 2 avant d’effectuer une opération arithmétique.</span><span class="sxs-lookup"><span data-stu-id="12aaa-119">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="12aaa-120">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="12aaa-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="12aaa-121">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="12aaa-121">Vertex Shader</span></span> | <span data-ttu-id="12aaa-122">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="12aaa-122">Geometry Shader</span></span> | <span data-ttu-id="12aaa-123">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="12aaa-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="12aaa-124">x</span><span class="sxs-lookup"><span data-stu-id="12aaa-124">x</span></span>             | <span data-ttu-id="12aaa-125">x</span><span class="sxs-lookup"><span data-stu-id="12aaa-125">x</span></span>               | <span data-ttu-id="12aaa-126">x</span><span class="sxs-lookup"><span data-stu-id="12aaa-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="12aaa-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="12aaa-127">Minimum Shader Model</span></span>

<span data-ttu-id="12aaa-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="12aaa-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="12aaa-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="12aaa-129">Shader Model</span></span>                                              | <span data-ttu-id="12aaa-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="12aaa-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="12aaa-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="12aaa-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="12aaa-132">Oui</span><span class="sxs-lookup"><span data-stu-id="12aaa-132">yes</span></span>       |
| [<span data-ttu-id="12aaa-133">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="12aaa-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="12aaa-134">Oui</span><span class="sxs-lookup"><span data-stu-id="12aaa-134">yes</span></span>       |
| [<span data-ttu-id="12aaa-135">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="12aaa-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="12aaa-136">Oui</span><span class="sxs-lookup"><span data-stu-id="12aaa-136">yes</span></span>       |
| [<span data-ttu-id="12aaa-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12aaa-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="12aaa-138">non</span><span class="sxs-lookup"><span data-stu-id="12aaa-138">no</span></span>        |
| [<span data-ttu-id="12aaa-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12aaa-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="12aaa-140">non</span><span class="sxs-lookup"><span data-stu-id="12aaa-140">no</span></span>        |
| [<span data-ttu-id="12aaa-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12aaa-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="12aaa-142">non</span><span class="sxs-lookup"><span data-stu-id="12aaa-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="12aaa-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12aaa-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12aaa-144">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12aaa-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





