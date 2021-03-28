---
title: swapc (SM5-ASM)
description: Effectue un échange conditionnel au niveau du composant des valeurs entre deux registres d’entrée.
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d2ee674a1cb1067594b0e96c739ff8df73b152
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990768"
---
# <a name="swapc-sm5---asm"></a><span data-ttu-id="d9603-103">swapc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d9603-103">swapc (sm5 - asm)</span></span>

<span data-ttu-id="d9603-104">Effectue un échange conditionnel au niveau du composant des valeurs entre deux registres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d9603-104">Performs a component-wise conditional swap of the values between two input registers.</span></span>



| <span data-ttu-id="d9603-105">swapc dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d9603-105">swapc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d9603-106">Élément</span><span class="sxs-lookup"><span data-stu-id="d9603-106">Item</span></span>                                                               | <span data-ttu-id="d9603-107">Description</span><span class="sxs-lookup"><span data-stu-id="d9603-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9603-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="d9603-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="d9603-109">\[dans \] Register avec des masques d’écriture non vides arbitraires.</span><span class="sxs-lookup"><span data-stu-id="d9603-109">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="d9603-110">Doit être différent de *dest1*.</span><span class="sxs-lookup"><span data-stu-id="d9603-110">Must be different than *dest1*.</span></span><br/> |
| <span data-ttu-id="d9603-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="d9603-111"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="d9603-112">\[dans \] Register avec des masques d’écriture non vides arbitraires.</span><span class="sxs-lookup"><span data-stu-id="d9603-112">\[in\] Register with arbitrary nonempty write masks.</span></span> <span data-ttu-id="d9603-113">Doit être différent de *dest0*.</span><span class="sxs-lookup"><span data-stu-id="d9603-113">Must be different than *dest0*.</span></span><br/> |
| <span data-ttu-id="d9603-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d9603-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="d9603-115">\[dans \] fournit 4 conditions.</span><span class="sxs-lookup"><span data-stu-id="d9603-115">\[in\] Provides 4 conditions.</span></span> <span data-ttu-id="d9603-116">Une valeur entière différente de zéro signifie **true**.</span><span class="sxs-lookup"><span data-stu-id="d9603-116">A nonzero integer value means **true**.</span></span> <br/>               |
| <span data-ttu-id="d9603-117"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="d9603-117"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="d9603-118">\[dans l' \] une des valeurs à permuter.</span><span class="sxs-lookup"><span data-stu-id="d9603-118">\[in\] One of the values to be swapped.</span></span><br/>                                              |
| <span data-ttu-id="d9603-119"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="d9603-119"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/>    | <span data-ttu-id="d9603-120">\[dans l' \] une des valeurs à permuter.</span><span class="sxs-lookup"><span data-stu-id="d9603-120">\[in\] One of the values to be swapped.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="d9603-121">Notes</span><span class="sxs-lookup"><span data-stu-id="d9603-121">Remarks</span></span>

<span data-ttu-id="d9603-122">L’encodage de cette instruction tente d’exprimer compactement plusieurs swaps conditionnels parallèles de scalaires dans des registres de composants de 2 4, avec une flexibilité mineure dans la disposition des paires de nombres impliquées dans l’échange.</span><span class="sxs-lookup"><span data-stu-id="d9603-122">The encoding of this instruction attempts to compactly express multiple parallel conditional swaps of scalars across two 4-component registers, with minor flexibility in the arrangement of the pairs of numbers involved in swapping.</span></span>

<span data-ttu-id="d9603-123">Le choix du Registre et de la valeur pour *src0*, *src1* et *src2* sont sans contrainte, comme [MOVC](movc--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="d9603-123">The choice of register and value for *src0*, *src1*, and *src2* are unconstrained in any way, like [movc](movc--sm4---asm-.md).</span></span>

<span data-ttu-id="d9603-124">La sémantique de cette instruction peut être décrite par les opérations équivalentes à l’aide de l’instruction **MOVC** .</span><span class="sxs-lookup"><span data-stu-id="d9603-124">The semantics of this instruction can be described by the equivalent operations with the **movc** instruction.</span></span> <span data-ttu-id="d9603-125">Le pire cas est illustré dans l’exemple suivant, en s’assurant que les registres de destination ne sont pas mis à jour jusqu’à la fin.</span><span class="sxs-lookup"><span data-stu-id="d9603-125">The worst case is shown in the following example, making sure destination registers are not updated until the end.</span></span>

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

<span data-ttu-id="d9603-126">Vous pouvez choisir le mode de traitement de la tâche, si ce n’est pas direct.</span><span class="sxs-lookup"><span data-stu-id="d9603-126">You can choose how to tackle the task, if not directly.</span></span> <span data-ttu-id="d9603-127">Par exemple, le même effet peut être obtenu à l’aide d’une séquence allant jusqu’à 4 swaps conditionnels scalaires simples ou, comme ci-dessus, deux instructions **MOVC** de vecteurs, plus toute surcharge pour s’assurer que les valeurs sources ne sont pas écrasées par des opérations antérieures au milieu de l’expansion.</span><span class="sxs-lookup"><span data-stu-id="d9603-127">For example, the same effect can be achieved by a sequence of up to 4 simple scalar conditional swaps, or as above, two vector **movc** instructions, plus any overhead to make sure the source values are not clobbered by earlier operations in the midst of the expansion.</span></span>

<span data-ttu-id="d9603-128">Utilisez cette instruction pour le tri.</span><span class="sxs-lookup"><span data-stu-id="d9603-128">Use this instruction for sorting.</span></span>

<span data-ttu-id="d9603-129">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="d9603-129">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d9603-130">Sommet</span><span class="sxs-lookup"><span data-stu-id="d9603-130">Vertex</span></span> | <span data-ttu-id="d9603-131">Forme</span><span class="sxs-lookup"><span data-stu-id="d9603-131">Hull</span></span> | <span data-ttu-id="d9603-132">Domain</span><span class="sxs-lookup"><span data-stu-id="d9603-132">Domain</span></span> | <span data-ttu-id="d9603-133">Géométrie</span><span class="sxs-lookup"><span data-stu-id="d9603-133">Geometry</span></span> | <span data-ttu-id="d9603-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="d9603-134">Pixel</span></span> | <span data-ttu-id="d9603-135">Compute</span><span class="sxs-lookup"><span data-stu-id="d9603-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d9603-136">X</span><span class="sxs-lookup"><span data-stu-id="d9603-136">X</span></span>      | <span data-ttu-id="d9603-137">X</span><span class="sxs-lookup"><span data-stu-id="d9603-137">X</span></span>    | <span data-ttu-id="d9603-138">X</span><span class="sxs-lookup"><span data-stu-id="d9603-138">X</span></span>      | <span data-ttu-id="d9603-139">X</span><span class="sxs-lookup"><span data-stu-id="d9603-139">X</span></span>        | <span data-ttu-id="d9603-140">X</span><span class="sxs-lookup"><span data-stu-id="d9603-140">X</span></span>     | <span data-ttu-id="d9603-141">X</span><span class="sxs-lookup"><span data-stu-id="d9603-141">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d9603-142">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d9603-142">Minimum Shader Model</span></span>

<span data-ttu-id="d9603-143">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="d9603-143">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d9603-144">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d9603-144">Shader Model</span></span>                                              | <span data-ttu-id="d9603-145">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d9603-145">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d9603-146">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="d9603-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d9603-147">Oui</span><span class="sxs-lookup"><span data-stu-id="d9603-147">yes</span></span>       |
| [<span data-ttu-id="d9603-148">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="d9603-148">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d9603-149">non</span><span class="sxs-lookup"><span data-stu-id="d9603-149">no</span></span>        |
| [<span data-ttu-id="d9603-150">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="d9603-150">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d9603-151">non</span><span class="sxs-lookup"><span data-stu-id="d9603-151">no</span></span>        |
| [<span data-ttu-id="d9603-152">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9603-152">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d9603-153">non</span><span class="sxs-lookup"><span data-stu-id="d9603-153">no</span></span>        |
| [<span data-ttu-id="d9603-154">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9603-154">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d9603-155">non</span><span class="sxs-lookup"><span data-stu-id="d9603-155">no</span></span>        |
| [<span data-ttu-id="d9603-156">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9603-156">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d9603-157">non</span><span class="sxs-lookup"><span data-stu-id="d9603-157">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d9603-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9603-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9603-159">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9603-159">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





