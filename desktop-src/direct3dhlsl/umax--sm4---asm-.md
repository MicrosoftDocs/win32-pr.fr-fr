---
title: Umax (SM4-ASM)
description: Entier non signé au niveau du composant maximal.
ms.assetid: 86BCF7A7-99CA-481B-82B4-E0BA30963344
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceb1fda620facce31132f56ed888d18022ca27ec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381170"
---
# <a name="umax-sm4---asm"></a><span data-ttu-id="08a4f-103">Umax (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="08a4f-103">umax (sm4 - asm)</span></span>

<span data-ttu-id="08a4f-104">Entier non signé au niveau du composant maximal.</span><span class="sxs-lookup"><span data-stu-id="08a4f-104">Component-wise unsigned integer maximum.</span></span>



| <span data-ttu-id="08a4f-105">Umax dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="08a4f-105">umax dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\],</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="08a4f-106">Élément</span><span class="sxs-lookup"><span data-stu-id="08a4f-106">Item</span></span>                                                            | <span data-ttu-id="08a4f-107">Description</span><span class="sxs-lookup"><span data-stu-id="08a4f-107">Description</span></span>                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a4f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="08a4f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="08a4f-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="08a4f-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="08a4f-110">*dest*  =  . *src0*  >  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="08a4f-110">*dest* = *src0* > *src1* ?</span></span> <span data-ttu-id="08a4f-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="08a4f-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="08a4f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="08a4f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="08a4f-113">\[dans \] la valeur à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="08a4f-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                                      |
| <span data-ttu-id="08a4f-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="08a4f-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="08a4f-115">\[dans \] la valeur à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="08a4f-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="08a4f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="08a4f-116">Remarks</span></span>

<span data-ttu-id="08a4f-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="08a4f-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="08a4f-118">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="08a4f-118">Vertex Shader</span></span> | <span data-ttu-id="08a4f-119">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="08a4f-119">Geometry Shader</span></span> | <span data-ttu-id="08a4f-120">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="08a4f-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="08a4f-121">x</span><span class="sxs-lookup"><span data-stu-id="08a4f-121">x</span></span>             | <span data-ttu-id="08a4f-122">x</span><span class="sxs-lookup"><span data-stu-id="08a4f-122">x</span></span>               | <span data-ttu-id="08a4f-123">x</span><span class="sxs-lookup"><span data-stu-id="08a4f-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="08a4f-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="08a4f-124">Minimum Shader Model</span></span>

<span data-ttu-id="08a4f-125">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="08a4f-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="08a4f-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="08a4f-126">Shader Model</span></span>                                              | <span data-ttu-id="08a4f-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="08a4f-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="08a4f-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="08a4f-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="08a4f-129">Oui</span><span class="sxs-lookup"><span data-stu-id="08a4f-129">yes</span></span>       |
| [<span data-ttu-id="08a4f-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="08a4f-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="08a4f-131">Oui</span><span class="sxs-lookup"><span data-stu-id="08a4f-131">yes</span></span>       |
| [<span data-ttu-id="08a4f-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="08a4f-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="08a4f-133">Oui</span><span class="sxs-lookup"><span data-stu-id="08a4f-133">yes</span></span>       |
| [<span data-ttu-id="08a4f-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08a4f-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="08a4f-135">non</span><span class="sxs-lookup"><span data-stu-id="08a4f-135">no</span></span>        |
| [<span data-ttu-id="08a4f-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08a4f-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="08a4f-137">non</span><span class="sxs-lookup"><span data-stu-id="08a4f-137">no</span></span>        |
| [<span data-ttu-id="08a4f-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08a4f-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="08a4f-139">non</span><span class="sxs-lookup"><span data-stu-id="08a4f-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="08a4f-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08a4f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08a4f-141">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="08a4f-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





