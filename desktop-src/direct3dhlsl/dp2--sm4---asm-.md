---
title: DP2 (SM4-ASM)
description: vecteur à deux dimensions-produit des composants RG, POS-Swizzle.
ms.assetid: E35F6A8B-6D8E-4660-B0F3-95B76BC19229
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4073def6cb315dc0268d1ce8e3f28039b9b2a69
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381146"
---
# <a name="dp2-sm4---asm"></a><span data-ttu-id="f3c48-103">DP2 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f3c48-103">dp2 (sm4 - asm)</span></span>

<span data-ttu-id="f3c48-104">vecteur à deux dimensions-produit des composants RG, POS-Swizzle.</span><span class="sxs-lookup"><span data-stu-id="f3c48-104">2-dimensional vector dot-product of components rg, POS-swizzle.</span></span>



| <span data-ttu-id="f3c48-105">DP2 \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f3c48-105">dp2\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f3c48-106">Élément</span><span class="sxs-lookup"><span data-stu-id="f3c48-106">Item</span></span>                                                            | <span data-ttu-id="f3c48-107">Description</span><span class="sxs-lookup"><span data-stu-id="f3c48-107">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c48-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f3c48-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f3c48-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f3c48-109">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="f3c48-110">*dest*  =  . *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*</span><span class="sxs-lookup"><span data-stu-id="f3c48-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g*</span></span><br/> |
| <span data-ttu-id="f3c48-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f3c48-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f3c48-112">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f3c48-112">\[in\] The components in the operation.</span></span><br/>                                                                             |
| <span data-ttu-id="f3c48-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="f3c48-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="f3c48-114">\[dans \] les composants de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f3c48-114">\[in\] The components in the operation.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="f3c48-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f3c48-115">Remarks</span></span>

<span data-ttu-id="f3c48-116">Résultat scalaire répliqué sur les composants dans le masque d’écriture.</span><span class="sxs-lookup"><span data-stu-id="f3c48-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="f3c48-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="f3c48-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f3c48-118">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="f3c48-118">Vertex Shader</span></span> | <span data-ttu-id="f3c48-119">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="f3c48-119">Geometry Shader</span></span> | <span data-ttu-id="f3c48-120">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="f3c48-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f3c48-121">x</span><span class="sxs-lookup"><span data-stu-id="f3c48-121">x</span></span>             | <span data-ttu-id="f3c48-122">x</span><span class="sxs-lookup"><span data-stu-id="f3c48-122">x</span></span>               | <span data-ttu-id="f3c48-123">x</span><span class="sxs-lookup"><span data-stu-id="f3c48-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f3c48-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f3c48-124">Minimum Shader Model</span></span>

<span data-ttu-id="f3c48-125">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f3c48-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f3c48-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f3c48-126">Shader Model</span></span>                                              | <span data-ttu-id="f3c48-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f3c48-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f3c48-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f3c48-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f3c48-129">Oui</span><span class="sxs-lookup"><span data-stu-id="f3c48-129">yes</span></span>       |
| [<span data-ttu-id="f3c48-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="f3c48-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f3c48-131">Oui</span><span class="sxs-lookup"><span data-stu-id="f3c48-131">yes</span></span>       |
| [<span data-ttu-id="f3c48-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f3c48-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f3c48-133">Oui</span><span class="sxs-lookup"><span data-stu-id="f3c48-133">yes</span></span>       |
| [<span data-ttu-id="f3c48-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3c48-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f3c48-135">non</span><span class="sxs-lookup"><span data-stu-id="f3c48-135">no</span></span>        |
| [<span data-ttu-id="f3c48-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3c48-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f3c48-137">non</span><span class="sxs-lookup"><span data-stu-id="f3c48-137">no</span></span>        |
| [<span data-ttu-id="f3c48-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3c48-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f3c48-139">non</span><span class="sxs-lookup"><span data-stu-id="f3c48-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f3c48-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3c48-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3c48-141">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3c48-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





