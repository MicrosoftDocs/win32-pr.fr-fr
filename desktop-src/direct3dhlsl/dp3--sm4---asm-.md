---
title: DP3 (SM4-ASM)
description: vecteur 3D point-produit des composants RVB, POS-Swizzle.
ms.assetid: 8E6EA6CD-B5BB-4D64-8846-F7B9F7135582
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2598053abed93675107f15af762e0844d4938fbf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841645"
---
# <a name="dp3-sm4---asm"></a><span data-ttu-id="a5bcf-103">DP3 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a5bcf-103">dp3 (sm4 - asm)</span></span>

<span data-ttu-id="a5bcf-104">vecteur 3D point-produit des composants RVB, POS-Swizzle.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-104">3-dimensional vector dot-product of components rgb, POS-swizzle.</span></span>



| <span data-ttu-id="a5bcf-105">DP3 \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="a5bcf-105">dp3\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a5bcf-106">Élément</span><span class="sxs-lookup"><span data-stu-id="a5bcf-106">Item</span></span>                                                            | <span data-ttu-id="a5bcf-107">Description</span><span class="sxs-lookup"><span data-stu-id="a5bcf-107">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5bcf-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a5bcf-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a5bcf-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="a5bcf-110">*dest*  =  . *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*  +  *src0. b* \* *src1. b*</span><span class="sxs-lookup"><span data-stu-id="a5bcf-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g* + *src0.b* \* *src1.b*</span></span><br/> |
| <span data-ttu-id="a5bcf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a5bcf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a5bcf-112">\[dans \] les composants de opération.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-112">\[in\] The components in the opertation.</span></span><br/>                                                                                   |
| <span data-ttu-id="a5bcf-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a5bcf-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a5bcf-114">\[dans \] les composants de opération.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-114">\[in\] The components in the opertation.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="a5bcf-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a5bcf-115">Remarks</span></span>

<span data-ttu-id="a5bcf-116">Résultat scalaire répliqué sur les composants dans le masque d’écriture.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="a5bcf-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="a5bcf-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a5bcf-118">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="a5bcf-118">Vertex Shader</span></span> | <span data-ttu-id="a5bcf-119">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="a5bcf-119">Geometry Shader</span></span> | <span data-ttu-id="a5bcf-120">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="a5bcf-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a5bcf-121">x</span><span class="sxs-lookup"><span data-stu-id="a5bcf-121">x</span></span>             | <span data-ttu-id="a5bcf-122">x</span><span class="sxs-lookup"><span data-stu-id="a5bcf-122">x</span></span>               | <span data-ttu-id="a5bcf-123">x</span><span class="sxs-lookup"><span data-stu-id="a5bcf-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a5bcf-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="a5bcf-124">Minimum Shader Model</span></span>

<span data-ttu-id="a5bcf-125">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="a5bcf-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a5bcf-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a5bcf-126">Shader Model</span></span>                                              | <span data-ttu-id="a5bcf-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="a5bcf-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a5bcf-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="a5bcf-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a5bcf-129">Oui</span><span class="sxs-lookup"><span data-stu-id="a5bcf-129">yes</span></span>       |
| [<span data-ttu-id="a5bcf-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="a5bcf-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a5bcf-131">Oui</span><span class="sxs-lookup"><span data-stu-id="a5bcf-131">yes</span></span>       |
| [<span data-ttu-id="a5bcf-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="a5bcf-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a5bcf-133">Oui</span><span class="sxs-lookup"><span data-stu-id="a5bcf-133">yes</span></span>       |
| [<span data-ttu-id="a5bcf-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5bcf-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a5bcf-135">non</span><span class="sxs-lookup"><span data-stu-id="a5bcf-135">no</span></span>        |
| [<span data-ttu-id="a5bcf-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5bcf-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a5bcf-137">non</span><span class="sxs-lookup"><span data-stu-id="a5bcf-137">no</span></span>        |
| [<span data-ttu-id="a5bcf-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5bcf-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a5bcf-139">non</span><span class="sxs-lookup"><span data-stu-id="a5bcf-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a5bcf-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5bcf-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5bcf-141">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a5bcf-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





