---
title: umul (SM4-ASM)
description: Multiplication d’entier non signé.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581696ef5aa7d027c30b4ae866d06401275ef4bc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381169"
---
# <a name="umul-sm4---asm"></a><span data-ttu-id="f7afb-103">umul (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f7afb-103">umul (sm4 - asm)</span></span>

<span data-ttu-id="f7afb-104">Multiplication d’entier non signé.</span><span class="sxs-lookup"><span data-stu-id="f7afb-104">Unsigned integer multiply.</span></span>



| <span data-ttu-id="f7afb-105">umul destHI \[ . Mask \] , destLO \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f7afb-105">umul destHI\[.mask\], destLO\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="f7afb-106">Élément</span><span class="sxs-lookup"><span data-stu-id="f7afb-106">Item</span></span>                                                                                           | <span data-ttu-id="f7afb-107">Description</span><span class="sxs-lookup"><span data-stu-id="f7afb-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f7afb-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span><span class="sxs-lookup"><span data-stu-id="f7afb-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="f7afb-109">\[dans \] les 32 bits de poids fort du résultat, par composant.</span><span class="sxs-lookup"><span data-stu-id="f7afb-109">\[in\] The high 32 bits of the result, per component.</span></span><br/> |
| <span data-ttu-id="f7afb-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span><span class="sxs-lookup"><span data-stu-id="f7afb-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="f7afb-111">\[dans \] les 32 bits de poids faible du résultat, par composant.</span><span class="sxs-lookup"><span data-stu-id="f7afb-111">\[in\] The low 32 bits of the result, per component.</span></span><br/>  |
| <span data-ttu-id="f7afb-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f7afb-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="f7afb-113">\[dans \] les composants par lesquels multiplier *src1*.</span><span class="sxs-lookup"><span data-stu-id="f7afb-113">\[in\] The components by which to multiply *src1*.</span></span><br/>    |
| <span data-ttu-id="f7afb-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="f7afb-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="f7afb-115">\[dans \] les composants par lesquels multiplier *src0*.</span><span class="sxs-lookup"><span data-stu-id="f7afb-115">\[in\] The components by which to multiply *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="f7afb-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f7afb-116">Remarks</span></span>

<span data-ttu-id="f7afb-117">Cette instruction effectue une multiplication au niveau du composant des opérandes 32 bits non signés *src0* et *src1*, ce qui produit le résultat 64 bits complet par composant.</span><span class="sxs-lookup"><span data-stu-id="f7afb-117">This instruction performs a component-wise multiply of unsigned 32-bit operands *src0* and *src1*, producing the correct full 64-bit result per component.</span></span> <span data-ttu-id="f7afb-118">Les 32 bits de poids faible par composant sont placés dans *destLO*.</span><span class="sxs-lookup"><span data-stu-id="f7afb-118">The low 32 bits per component are placed in *destLO*.</span></span> <span data-ttu-id="f7afb-119">La haute 32 bits par composant est placée dans *destHI*.</span><span class="sxs-lookup"><span data-stu-id="f7afb-119">The high 32 bits per component are placed in *destHI*.</span></span>

<span data-ttu-id="f7afb-120">Vous pouvez spécifier *destHI* ou *destLO* comme null au lieu de spécifier un registre si les 32 bits de poids fort ou faible du résultat de 64 bits ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="f7afb-120">You can specify either *destHI* or *destLO* as NULL instead of specifying a register if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="f7afb-121">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="f7afb-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f7afb-122">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="f7afb-122">Vertex Shader</span></span> | <span data-ttu-id="f7afb-123">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="f7afb-123">Geometry Shader</span></span> | <span data-ttu-id="f7afb-124">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="f7afb-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f7afb-125">x</span><span class="sxs-lookup"><span data-stu-id="f7afb-125">x</span></span>             | <span data-ttu-id="f7afb-126">x</span><span class="sxs-lookup"><span data-stu-id="f7afb-126">x</span></span>               | <span data-ttu-id="f7afb-127">x</span><span class="sxs-lookup"><span data-stu-id="f7afb-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f7afb-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f7afb-128">Minimum Shader Model</span></span>

<span data-ttu-id="f7afb-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f7afb-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f7afb-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f7afb-130">Shader Model</span></span>                                              | <span data-ttu-id="f7afb-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f7afb-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f7afb-132">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f7afb-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f7afb-133">Oui</span><span class="sxs-lookup"><span data-stu-id="f7afb-133">yes</span></span>       |
| [<span data-ttu-id="f7afb-134">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="f7afb-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f7afb-135">Oui</span><span class="sxs-lookup"><span data-stu-id="f7afb-135">yes</span></span>       |
| [<span data-ttu-id="f7afb-136">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f7afb-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f7afb-137">Oui</span><span class="sxs-lookup"><span data-stu-id="f7afb-137">yes</span></span>       |
| [<span data-ttu-id="f7afb-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7afb-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f7afb-139">non</span><span class="sxs-lookup"><span data-stu-id="f7afb-139">no</span></span>        |
| [<span data-ttu-id="f7afb-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7afb-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f7afb-141">non</span><span class="sxs-lookup"><span data-stu-id="f7afb-141">no</span></span>        |
| [<span data-ttu-id="f7afb-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7afb-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f7afb-143">non</span><span class="sxs-lookup"><span data-stu-id="f7afb-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f7afb-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7afb-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7afb-145">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7afb-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





