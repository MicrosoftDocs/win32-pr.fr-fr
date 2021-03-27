---
title: Not (SM4-ASM)
description: Not au niveau du bit.
ms.assetid: AC7EBBC2-4B52-4793-812C-B25897FB8D05
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0bf224e6e5af7f2db6bcbaf7ae287ba2d399727
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971598"
---
# <a name="not-sm4---asm"></a><span data-ttu-id="53c8d-103">Not (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="53c8d-103">not (sm4 - asm)</span></span>

<span data-ttu-id="53c8d-104">Not au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="53c8d-104">Bitwise not.</span></span>



| <span data-ttu-id="53c8d-105">non dest \[ . Mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="53c8d-105">not dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------|



 



| <span data-ttu-id="53c8d-106">Élément</span><span class="sxs-lookup"><span data-stu-id="53c8d-106">Item</span></span>                                                            | <span data-ttu-id="53c8d-107">Description</span><span class="sxs-lookup"><span data-stu-id="53c8d-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="53c8d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="53c8d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="53c8d-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="53c8d-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="53c8d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="53c8d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="53c8d-111">\[dans \] les composants d’origine.</span><span class="sxs-lookup"><span data-stu-id="53c8d-111">\[in\] The original components.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="53c8d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="53c8d-112">Remarks</span></span>

<span data-ttu-id="53c8d-113">Cette instruction effectue un complément à un au niveau du composant de chaque valeur 32 bits dans *src0*.</span><span class="sxs-lookup"><span data-stu-id="53c8d-113">This instruction performs a component-wise one's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="53c8d-114">Les résultats 32 bits sont stockés dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="53c8d-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="53c8d-115">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="53c8d-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="53c8d-116">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="53c8d-116">Vertex Shader</span></span> | <span data-ttu-id="53c8d-117">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="53c8d-117">Geometry Shader</span></span> | <span data-ttu-id="53c8d-118">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="53c8d-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="53c8d-119">x</span><span class="sxs-lookup"><span data-stu-id="53c8d-119">x</span></span>             | <span data-ttu-id="53c8d-120">x</span><span class="sxs-lookup"><span data-stu-id="53c8d-120">x</span></span>               | <span data-ttu-id="53c8d-121">x</span><span class="sxs-lookup"><span data-stu-id="53c8d-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="53c8d-122">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="53c8d-122">Minimum Shader Model</span></span>

<span data-ttu-id="53c8d-123">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="53c8d-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="53c8d-124">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="53c8d-124">Shader Model</span></span>                                              | <span data-ttu-id="53c8d-125">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="53c8d-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="53c8d-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="53c8d-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="53c8d-127">Oui</span><span class="sxs-lookup"><span data-stu-id="53c8d-127">yes</span></span>       |
| [<span data-ttu-id="53c8d-128">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="53c8d-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="53c8d-129">Oui</span><span class="sxs-lookup"><span data-stu-id="53c8d-129">yes</span></span>       |
| [<span data-ttu-id="53c8d-130">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="53c8d-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="53c8d-131">Oui</span><span class="sxs-lookup"><span data-stu-id="53c8d-131">yes</span></span>       |
| [<span data-ttu-id="53c8d-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53c8d-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="53c8d-133">non</span><span class="sxs-lookup"><span data-stu-id="53c8d-133">no</span></span>        |
| [<span data-ttu-id="53c8d-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53c8d-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="53c8d-135">non</span><span class="sxs-lookup"><span data-stu-id="53c8d-135">no</span></span>        |
| [<span data-ttu-id="53c8d-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53c8d-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="53c8d-137">non</span><span class="sxs-lookup"><span data-stu-id="53c8d-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="53c8d-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53c8d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53c8d-139">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53c8d-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





