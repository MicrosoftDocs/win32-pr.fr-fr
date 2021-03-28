---
title: IAdd (SM4-ASM)
description: Addition d’entiers.
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b593484aa7c1ef376bb5febf141b144ddef338e0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381209"
---
# <a name="iadd-sm4---asm"></a><span data-ttu-id="480be-103">IAdd (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="480be-103">iadd (sm4 - asm)</span></span>

<span data-ttu-id="480be-104">Addition d’entiers.</span><span class="sxs-lookup"><span data-stu-id="480be-104">Integer addition.</span></span>



| <span data-ttu-id="480be-105">IAdd dest \[ . Mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="480be-105">iadd dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="480be-106">Élément</span><span class="sxs-lookup"><span data-stu-id="480be-106">Item</span></span>                                                            | <span data-ttu-id="480be-107">Description</span><span class="sxs-lookup"><span data-stu-id="480be-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="480be-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="480be-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="480be-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="480be-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="480be-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="480be-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="480be-111">\[dans \] le nombre à ajouter à *src1*.</span><span class="sxs-lookup"><span data-stu-id="480be-111">\[in\] The number to be added to *src1*.</span></span><br/>           |
| <span data-ttu-id="480be-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="480be-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="480be-113">\[dans \] le nombre à ajouter à *src0*.</span><span class="sxs-lookup"><span data-stu-id="480be-113">\[in\] The number to be added to *src0*.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="480be-114">Notes</span><span class="sxs-lookup"><span data-stu-id="480be-114">Remarks</span></span>

<span data-ttu-id="480be-115">Ajoutez au niveau du composant des opérandes 32 bits *src0* et *src1*, en plaçant le résultat correct de 32 bits dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="480be-115">Component-wise add of 32-bit operands *src0* and *src1*, placing the correct 32-bit result in *dest*.</span></span> <span data-ttu-id="480be-116">Aucun transport ou emprunt au-delà des valeurs 32 bits de chaque composant n’est effectué, donc cette instruction n’est pas sensible au caractère signé de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="480be-116">No carry or borrow beyond the 32-bit values of each component is performed, so this instruction is not sensitive to the signed-ness of its operands.</span></span>

<span data-ttu-id="480be-117">Le modificateur de négation facultatif sur les opérandes source prend le complément à 2 avant d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="480be-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="480be-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="480be-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="480be-119">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="480be-119">Vertex Shader</span></span> | <span data-ttu-id="480be-120">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="480be-120">Geometry Shader</span></span> | <span data-ttu-id="480be-121">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="480be-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="480be-122">x</span><span class="sxs-lookup"><span data-stu-id="480be-122">x</span></span>             | <span data-ttu-id="480be-123">x</span><span class="sxs-lookup"><span data-stu-id="480be-123">x</span></span>               | <span data-ttu-id="480be-124">x</span><span class="sxs-lookup"><span data-stu-id="480be-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="480be-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="480be-125">Minimum Shader Model</span></span>

<span data-ttu-id="480be-126">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="480be-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="480be-127">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="480be-127">Shader Model</span></span>                                              | <span data-ttu-id="480be-128">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="480be-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="480be-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="480be-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="480be-130">Oui</span><span class="sxs-lookup"><span data-stu-id="480be-130">yes</span></span>       |
| [<span data-ttu-id="480be-131">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="480be-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="480be-132">Oui</span><span class="sxs-lookup"><span data-stu-id="480be-132">yes</span></span>       |
| [<span data-ttu-id="480be-133">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="480be-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="480be-134">Oui</span><span class="sxs-lookup"><span data-stu-id="480be-134">yes</span></span>       |
| [<span data-ttu-id="480be-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="480be-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="480be-136">non</span><span class="sxs-lookup"><span data-stu-id="480be-136">no</span></span>        |
| [<span data-ttu-id="480be-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="480be-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="480be-138">non</span><span class="sxs-lookup"><span data-stu-id="480be-138">no</span></span>        |
| [<span data-ttu-id="480be-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="480be-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="480be-140">non</span><span class="sxs-lookup"><span data-stu-id="480be-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="480be-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="480be-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="480be-142">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="480be-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





