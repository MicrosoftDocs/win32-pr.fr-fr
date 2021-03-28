---
title: UDIV (SM4-ASM)
description: Division d’entier non signé.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a3dd2f4170a3c8fe522af12d412cfae49396da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381171"
---
# <a name="udiv-sm4---asm"></a><span data-ttu-id="c42f9-103">UDIV (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c42f9-103">udiv (sm4 - asm)</span></span>

<span data-ttu-id="c42f9-104">Division d’entier non signé.</span><span class="sxs-lookup"><span data-stu-id="c42f9-104">Unsigned integer divide.</span></span>



| <span data-ttu-id="c42f9-105">UDIV destQUOT \[ . Mask \] , destREM \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c42f9-105">udiv destQUOT\[.mask\], destREM\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="c42f9-106">Élément</span><span class="sxs-lookup"><span data-stu-id="c42f9-106">Item</span></span>                                                                                                   | <span data-ttu-id="c42f9-107">Description</span><span class="sxs-lookup"><span data-stu-id="c42f9-107">Description</span></span>                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c42f9-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*</span><span class="sxs-lookup"><span data-stu-id="c42f9-108"><span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*</span></span><br/> | <span data-ttu-id="c42f9-109">\[dans \] l’adresse du quotient résultant.</span><span class="sxs-lookup"><span data-stu-id="c42f9-109">\[in\] The address of the resulting quotient.</span></span><br/>   |
| <span data-ttu-id="c42f9-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*</span><span class="sxs-lookup"><span data-stu-id="c42f9-110"><span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*</span></span><br/>     | <span data-ttu-id="c42f9-111">\[dans \] l’adresse du reste résultant.</span><span class="sxs-lookup"><span data-stu-id="c42f9-111">\[in\] The address of the resulting remainder.</span></span><br/>  |
| <span data-ttu-id="c42f9-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c42f9-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                        | <span data-ttu-id="c42f9-113">\[dans \] les composants à diviser par *src1*.</span><span class="sxs-lookup"><span data-stu-id="c42f9-113">\[in\] The components to be divided by *src1*.</span></span><br/>  |
| <span data-ttu-id="c42f9-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c42f9-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                        | <span data-ttu-id="c42f9-115">\[dans \] les composants par abordé pour diviser *src0*.</span><span class="sxs-lookup"><span data-stu-id="c42f9-115">\[in\] The components by whch to divide *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c42f9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c42f9-116">Remarks</span></span>

<span data-ttu-id="c42f9-117">Cette instruction effectue une division non signée au niveau du composant de l’opérande 32 bits *src0* par l’opérande 32 bits *src1*.</span><span class="sxs-lookup"><span data-stu-id="c42f9-117">This instruction performs a component-wise unsigned divide of the 32-bit operand *src0* by the 32-bit operand *src1*.</span></span> <span data-ttu-id="c42f9-118">Les résultats des divisions sont les quotients de 32 bits placés dans *destQUOT* et les restes de 32 bits placés dans *destREM*.</span><span class="sxs-lookup"><span data-stu-id="c42f9-118">The results of the divides are the 32-bit quotients placed in *destQUOT* and 32-bit remainders placed in *destREM*.</span></span>

<span data-ttu-id="c42f9-119">La division par zéro retourne 0xFFFFFFFF pour le quotient et le reste.</span><span class="sxs-lookup"><span data-stu-id="c42f9-119">Divide by zero returns 0xffffffff for both quotient and remainder.</span></span>

<span data-ttu-id="c42f9-120">Vous pouvez spécifier *destQUOT* ou *destREM* comme null au lieu de spécifier un registre, si le quotient ou le reste ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="c42f9-120">You can specifiy either *destQUOT* or *destREM* as NULL instead of specifying a register, if the quotient or remainder are not needed.</span></span>

<span data-ttu-id="c42f9-121">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="c42f9-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c42f9-122">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="c42f9-122">Vertex Shader</span></span> | <span data-ttu-id="c42f9-123">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="c42f9-123">Geometry Shader</span></span> | <span data-ttu-id="c42f9-124">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c42f9-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c42f9-125">x</span><span class="sxs-lookup"><span data-stu-id="c42f9-125">x</span></span>             | <span data-ttu-id="c42f9-126">x</span><span class="sxs-lookup"><span data-stu-id="c42f9-126">x</span></span>               | <span data-ttu-id="c42f9-127">x</span><span class="sxs-lookup"><span data-stu-id="c42f9-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c42f9-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c42f9-128">Minimum Shader Model</span></span>

<span data-ttu-id="c42f9-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="c42f9-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c42f9-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c42f9-130">Shader Model</span></span>                                              | <span data-ttu-id="c42f9-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="c42f9-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c42f9-132">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="c42f9-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c42f9-133">Oui</span><span class="sxs-lookup"><span data-stu-id="c42f9-133">yes</span></span>       |
| [<span data-ttu-id="c42f9-134">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="c42f9-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c42f9-135">Oui</span><span class="sxs-lookup"><span data-stu-id="c42f9-135">yes</span></span>       |
| [<span data-ttu-id="c42f9-136">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="c42f9-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c42f9-137">Oui</span><span class="sxs-lookup"><span data-stu-id="c42f9-137">yes</span></span>       |
| [<span data-ttu-id="c42f9-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c42f9-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c42f9-139">non</span><span class="sxs-lookup"><span data-stu-id="c42f9-139">no</span></span>        |
| [<span data-ttu-id="c42f9-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c42f9-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c42f9-141">non</span><span class="sxs-lookup"><span data-stu-id="c42f9-141">no</span></span>        |
| [<span data-ttu-id="c42f9-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c42f9-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c42f9-143">non</span><span class="sxs-lookup"><span data-stu-id="c42f9-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c42f9-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c42f9-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c42f9-145">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c42f9-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





