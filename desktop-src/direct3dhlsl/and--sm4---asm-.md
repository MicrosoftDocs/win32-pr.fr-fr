---
title: et (SM4-ASM)
description: Opérateur AND au niveau du bit.
ms.assetid: 403DA289-E2CF-4736-8882-4131F884F777
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec9474322aafda2706502898902d01d0e13143
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679162"
---
# <a name="and-sm4---asm"></a><span data-ttu-id="ad80d-103">et (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ad80d-103">and (sm4 - asm)</span></span>

<span data-ttu-id="ad80d-104">And **au niveau du** bit.</span><span class="sxs-lookup"><span data-stu-id="ad80d-104">Bitwise **AND**.</span></span>



| <span data-ttu-id="ad80d-105">et dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ad80d-105">and dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="ad80d-106">Élément</span><span class="sxs-lookup"><span data-stu-id="ad80d-106">Item</span></span>                                                            | <span data-ttu-id="ad80d-107">Description</span><span class="sxs-lookup"><span data-stu-id="ad80d-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ad80d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ad80d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ad80d-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="ad80d-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="ad80d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ad80d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ad80d-111">\[dans \] la valeur 32 bits vers **et** avec *src1*.</span><span class="sxs-lookup"><span data-stu-id="ad80d-111">\[in\] The 32-bit value to **AND** with *src1*.</span></span><br/>    |
| <span data-ttu-id="ad80d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ad80d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="ad80d-113">\[dans \] la valeur 32 bits vers **et** avec *src0*.</span><span class="sxs-lookup"><span data-stu-id="ad80d-113">\[in\] The 32-bit value to **AND** with *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="ad80d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ad80d-114">Remarks</span></span>

<span data-ttu-id="ad80d-115">**And** logique au niveau du composant de chaque paire de valeurs 32 bits à partir de *src0* et *src1*.</span><span class="sxs-lookup"><span data-stu-id="ad80d-115">Component-wise logical **AND** of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="ad80d-116">Les résultats 32 bits sont placés dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="ad80d-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="ad80d-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="ad80d-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ad80d-118">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="ad80d-118">Vertex Shader</span></span> | <span data-ttu-id="ad80d-119">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="ad80d-119">Geometry Shader</span></span> | <span data-ttu-id="ad80d-120">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="ad80d-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ad80d-121">x</span><span class="sxs-lookup"><span data-stu-id="ad80d-121">x</span></span>             | <span data-ttu-id="ad80d-122">x</span><span class="sxs-lookup"><span data-stu-id="ad80d-122">x</span></span>               | <span data-ttu-id="ad80d-123">x</span><span class="sxs-lookup"><span data-stu-id="ad80d-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ad80d-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="ad80d-124">Minimum Shader Model</span></span>

<span data-ttu-id="ad80d-125">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="ad80d-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ad80d-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="ad80d-126">Shader Model</span></span>                                              | <span data-ttu-id="ad80d-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="ad80d-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ad80d-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="ad80d-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ad80d-129">Oui</span><span class="sxs-lookup"><span data-stu-id="ad80d-129">yes</span></span>       |
| [<span data-ttu-id="ad80d-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="ad80d-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ad80d-131">Oui</span><span class="sxs-lookup"><span data-stu-id="ad80d-131">yes</span></span>       |
| [<span data-ttu-id="ad80d-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="ad80d-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ad80d-133">Oui</span><span class="sxs-lookup"><span data-stu-id="ad80d-133">yes</span></span>       |
| [<span data-ttu-id="ad80d-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ad80d-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ad80d-135">non</span><span class="sxs-lookup"><span data-stu-id="ad80d-135">no</span></span>        |
| [<span data-ttu-id="ad80d-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ad80d-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ad80d-137">non</span><span class="sxs-lookup"><span data-stu-id="ad80d-137">no</span></span>        |
| [<span data-ttu-id="ad80d-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ad80d-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ad80d-139">non</span><span class="sxs-lookup"><span data-stu-id="ad80d-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ad80d-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ad80d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad80d-141">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ad80d-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





