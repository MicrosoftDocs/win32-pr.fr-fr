---
title: DP4 (SM4-ASM)
description: vecteur à quatre dimensions-produit des composants RVBA, POS-Swizzle.
ms.assetid: A41EC054-0060-49CA-90FB-A096E63DD27D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a91a253d4e8b53bc044e658c3fe75d8f7547da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940567"
---
# <a name="dp4-sm4---asm"></a><span data-ttu-id="d6494-103">DP4 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d6494-103">dp4 (sm4 - asm)</span></span>

<span data-ttu-id="d6494-104">vecteur à quatre dimensions-produit des composants RVBA, POS-Swizzle.</span><span class="sxs-lookup"><span data-stu-id="d6494-104">4-dimensional vector dot-product of components rgba, POS-swizzle.</span></span>



| <span data-ttu-id="d6494-105">DP4 \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="d6494-105">dp4\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d6494-106">Élément</span><span class="sxs-lookup"><span data-stu-id="d6494-106">Item</span></span>                                                            | <span data-ttu-id="d6494-107">Description</span><span class="sxs-lookup"><span data-stu-id="d6494-107">Description</span></span>                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6494-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d6494-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d6494-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d6494-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="d6494-110">*dest*  =  . *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*  +  *src0. b* src1. b src0. \*  +  *a* \* *src1. a*</span><span class="sxs-lookup"><span data-stu-id="d6494-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g* + *src0.b* \* *src1.b*+ *src0.a* \* *src1.a*</span></span><br/> |
| <span data-ttu-id="d6494-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d6494-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d6494-112">\[dans \] les composants de opération.</span><span class="sxs-lookup"><span data-stu-id="d6494-112">\[in\] The components in the opertation.</span></span><br/>                                                                                                          |
| <span data-ttu-id="d6494-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="d6494-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d6494-114">\[dans \] les composants de opération.</span><span class="sxs-lookup"><span data-stu-id="d6494-114">\[in\] The components in the opertation.</span></span><br/>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="d6494-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d6494-115">Remarks</span></span>

<span data-ttu-id="d6494-116">Résultat scalaire répliqué sur les composants dans le masque d’écriture.</span><span class="sxs-lookup"><span data-stu-id="d6494-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="d6494-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="d6494-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d6494-118">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="d6494-118">Vertex Shader</span></span> | <span data-ttu-id="d6494-119">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="d6494-119">Geometry Shader</span></span> | <span data-ttu-id="d6494-120">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d6494-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d6494-121">x</span><span class="sxs-lookup"><span data-stu-id="d6494-121">x</span></span>             | <span data-ttu-id="d6494-122">x</span><span class="sxs-lookup"><span data-stu-id="d6494-122">x</span></span>               | <span data-ttu-id="d6494-123">x</span><span class="sxs-lookup"><span data-stu-id="d6494-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d6494-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d6494-124">Minimum Shader Model</span></span>

<span data-ttu-id="d6494-125">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d6494-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d6494-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d6494-126">Shader Model</span></span>                                              | <span data-ttu-id="d6494-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d6494-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d6494-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="d6494-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d6494-129">Oui</span><span class="sxs-lookup"><span data-stu-id="d6494-129">yes</span></span>       |
| [<span data-ttu-id="d6494-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="d6494-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d6494-131">Oui</span><span class="sxs-lookup"><span data-stu-id="d6494-131">yes</span></span>       |
| [<span data-ttu-id="d6494-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="d6494-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d6494-133">Oui</span><span class="sxs-lookup"><span data-stu-id="d6494-133">yes</span></span>       |
| [<span data-ttu-id="d6494-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6494-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d6494-135">non</span><span class="sxs-lookup"><span data-stu-id="d6494-135">no</span></span>        |
| [<span data-ttu-id="d6494-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6494-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d6494-137">non</span><span class="sxs-lookup"><span data-stu-id="d6494-137">no</span></span>        |
| [<span data-ttu-id="d6494-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6494-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d6494-139">non</span><span class="sxs-lookup"><span data-stu-id="d6494-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d6494-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6494-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6494-141">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6494-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





