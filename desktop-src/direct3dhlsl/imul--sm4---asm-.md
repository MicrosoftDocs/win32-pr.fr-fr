---
title: imul (SM4-ASM)
description: Multiplication de l’entier signé.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f62fc389ad1e0fb6b23dd6c419ff8b3933b41
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679149"
---
# <a name="imul-sm4---asm"></a><span data-ttu-id="c1d11-103">imul (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c1d11-103">imul (sm4 - asm)</span></span>

<span data-ttu-id="c1d11-104">Multiplication de l’entier signé.</span><span class="sxs-lookup"><span data-stu-id="c1d11-104">Signed integer multiply.</span></span>



| <span data-ttu-id="c1d11-105">imul destHI \[ . Mask \] , destLO \[ . Mask \] , \[ - \] src0 \[ . Swizzle \] , \[ - \] src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c1d11-105">imul destHI\[.mask\], destLO\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------|



 



| <span data-ttu-id="c1d11-106">Élément</span><span class="sxs-lookup"><span data-stu-id="c1d11-106">Item</span></span>                                                                                           | <span data-ttu-id="c1d11-107">Description</span><span class="sxs-lookup"><span data-stu-id="c1d11-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c1d11-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span><span class="sxs-lookup"><span data-stu-id="c1d11-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="c1d11-109">\[dans \] l’adresse des 32 bits de poids fort du résultat.</span><span class="sxs-lookup"><span data-stu-id="c1d11-109">\[in\] The address of the high 32 bits of the result.</span></span><br/> |
| <span data-ttu-id="c1d11-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span><span class="sxs-lookup"><span data-stu-id="c1d11-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="c1d11-111">\[dans \] l’adresse des 32 bits de poids faible du résultat.</span><span class="sxs-lookup"><span data-stu-id="c1d11-111">\[in\] The address of the low 32 bits of the result.</span></span><br/>  |
| <span data-ttu-id="c1d11-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c1d11-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="c1d11-113">\[dans \] la valeur à multiplier avec *src1*.</span><span class="sxs-lookup"><span data-stu-id="c1d11-113">\[in\] The value to multiply with *src1*.</span></span><br/>             |
| <span data-ttu-id="c1d11-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c1d11-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="c1d11-115">\[dans \] la valeur à multiplier avec *src0*.</span><span class="sxs-lookup"><span data-stu-id="c1d11-115">\[in\] The value to multiply with *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="c1d11-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c1d11-116">Remarks</span></span>

<span data-ttu-id="c1d11-117">Multiplication au niveau du composant des opérandes 32 bits *src0* et *src1* (les deux sont signés), ce qui génère le résultat complet 64 bits (par composant) complet.</span><span class="sxs-lookup"><span data-stu-id="c1d11-117">Component-wise multiply of 32-bit operands *src0* and *src1* (both are signed), producing the correct full 64-bit (per component) result.</span></span> <span data-ttu-id="c1d11-118">Les 32 bits de poids faible (par composant) sont placés dans *destLO*.</span><span class="sxs-lookup"><span data-stu-id="c1d11-118">The low 32 bits (per component) are placed in *destLO*.</span></span> <span data-ttu-id="c1d11-119">Les 32 bits de poids fort (par composant) sont placés dans *destHI*.</span><span class="sxs-lookup"><span data-stu-id="c1d11-119">The high 32 bits (per component) are placed in *destHI*.</span></span>

<span data-ttu-id="c1d11-120">*DestHI* ou *destLO* peut être spécifié comme null au lieu de spécifier un registre, si les 32 bits de poids fort ou faible du résultat de 64 bits ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="c1d11-120">Either *destHI* or *destLO* may be specified as NULL instead of specifying a register, if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="c1d11-121">Le modificateur de négation facultatif sur les opérandes source prend le complément à 2 avant d’effectuer une opération arithmétique.</span><span class="sxs-lookup"><span data-stu-id="c1d11-121">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="c1d11-122">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="c1d11-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c1d11-123">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="c1d11-123">Vertex Shader</span></span> | <span data-ttu-id="c1d11-124">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="c1d11-124">Geometry Shader</span></span> | <span data-ttu-id="c1d11-125">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c1d11-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c1d11-126">x</span><span class="sxs-lookup"><span data-stu-id="c1d11-126">x</span></span>             | <span data-ttu-id="c1d11-127">x</span><span class="sxs-lookup"><span data-stu-id="c1d11-127">x</span></span>               | <span data-ttu-id="c1d11-128">x</span><span class="sxs-lookup"><span data-stu-id="c1d11-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c1d11-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c1d11-129">Minimum Shader Model</span></span>

<span data-ttu-id="c1d11-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="c1d11-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c1d11-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c1d11-131">Shader Model</span></span>                                              | <span data-ttu-id="c1d11-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="c1d11-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c1d11-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="c1d11-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c1d11-134">Oui</span><span class="sxs-lookup"><span data-stu-id="c1d11-134">yes</span></span>       |
| [<span data-ttu-id="c1d11-135">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="c1d11-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c1d11-136">Oui</span><span class="sxs-lookup"><span data-stu-id="c1d11-136">yes</span></span>       |
| [<span data-ttu-id="c1d11-137">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="c1d11-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c1d11-138">Oui</span><span class="sxs-lookup"><span data-stu-id="c1d11-138">yes</span></span>       |
| [<span data-ttu-id="c1d11-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1d11-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c1d11-140">non</span><span class="sxs-lookup"><span data-stu-id="c1d11-140">no</span></span>        |
| [<span data-ttu-id="c1d11-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1d11-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c1d11-142">non</span><span class="sxs-lookup"><span data-stu-id="c1d11-142">no</span></span>        |
| [<span data-ttu-id="c1d11-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1d11-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c1d11-144">non</span><span class="sxs-lookup"><span data-stu-id="c1d11-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c1d11-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c1d11-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1d11-146">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1d11-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





