---
title: Umin (SM4-ASM)
description: Entier non signé au niveau du composant minimal.
ms.assetid: 134B128F-7B47-4819-A576-80766EDB14C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 059b9660e4969b252c867a009a920259c92bff18
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101077"
---
# <a name="umin-sm4---asm"></a><span data-ttu-id="bebd9-103">Umin (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="bebd9-103">umin (sm4 - asm)</span></span>

<span data-ttu-id="bebd9-104">Entier non signé au niveau du composant minimal.</span><span class="sxs-lookup"><span data-stu-id="bebd9-104">Component-wise unsigned integer minimum.</span></span>



| <span data-ttu-id="bebd9-105">Umin dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="bebd9-105">umin dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\],</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="bebd9-106">Élément</span><span class="sxs-lookup"><span data-stu-id="bebd9-106">Item</span></span>                                                            | <span data-ttu-id="bebd9-107">Description</span><span class="sxs-lookup"><span data-stu-id="bebd9-107">Description</span></span>                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bebd9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="bebd9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="bebd9-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="bebd9-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="bebd9-110">*dest*  =  . *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="bebd9-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="bebd9-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="bebd9-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="bebd9-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bebd9-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="bebd9-113">\[dans \] la valeur à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="bebd9-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                                      |
| <span data-ttu-id="bebd9-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="bebd9-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="bebd9-115">\[dans \] la valeur à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="bebd9-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="bebd9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="bebd9-116">Remarks</span></span>

<span data-ttu-id="bebd9-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="bebd9-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bebd9-118">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="bebd9-118">Vertex Shader</span></span> | <span data-ttu-id="bebd9-119">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="bebd9-119">Geometry Shader</span></span> | <span data-ttu-id="bebd9-120">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="bebd9-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="bebd9-121">x</span><span class="sxs-lookup"><span data-stu-id="bebd9-121">x</span></span>             | <span data-ttu-id="bebd9-122">x</span><span class="sxs-lookup"><span data-stu-id="bebd9-122">x</span></span>               | <span data-ttu-id="bebd9-123">x</span><span class="sxs-lookup"><span data-stu-id="bebd9-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bebd9-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="bebd9-124">Minimum Shader Model</span></span>

<span data-ttu-id="bebd9-125">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="bebd9-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bebd9-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="bebd9-126">Shader Model</span></span>                                              | <span data-ttu-id="bebd9-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="bebd9-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bebd9-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="bebd9-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bebd9-129">Oui</span><span class="sxs-lookup"><span data-stu-id="bebd9-129">yes</span></span>       |
| [<span data-ttu-id="bebd9-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="bebd9-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bebd9-131">Oui</span><span class="sxs-lookup"><span data-stu-id="bebd9-131">yes</span></span>       |
| [<span data-ttu-id="bebd9-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="bebd9-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bebd9-133">Oui</span><span class="sxs-lookup"><span data-stu-id="bebd9-133">yes</span></span>       |
| [<span data-ttu-id="bebd9-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bebd9-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bebd9-135">non</span><span class="sxs-lookup"><span data-stu-id="bebd9-135">no</span></span>        |
| [<span data-ttu-id="bebd9-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bebd9-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bebd9-137">non</span><span class="sxs-lookup"><span data-stu-id="bebd9-137">no</span></span>        |
| [<span data-ttu-id="bebd9-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bebd9-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bebd9-139">non</span><span class="sxs-lookup"><span data-stu-id="bebd9-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bebd9-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bebd9-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bebd9-141">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bebd9-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





