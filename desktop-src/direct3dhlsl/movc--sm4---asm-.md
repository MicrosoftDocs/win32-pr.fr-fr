---
title: MOVC (SM4-ASM)
description: Déplacement conditionnel au niveau du composant. | MOVC (SM4-ASM)
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3116b7bc13102386c57c9b8c63d3534147a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991961"
---
# <a name="movc-sm4---asm"></a><span data-ttu-id="09d9b-104">MOVC (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="09d9b-104">movc (sm4 - asm)</span></span>

<span data-ttu-id="09d9b-105">Déplacement conditionnel au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="09d9b-105">Component-wise conditional move.</span></span>



| <span data-ttu-id="09d9b-106">MOVC \[ \_ SAT \] dest \[ . Mask \] , src0 \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="09d9b-106">movc\[\_sat\] dest\[.mask\], src0\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="09d9b-107">Élément</span><span class="sxs-lookup"><span data-stu-id="09d9b-107">Item</span></span>                                                            | <span data-ttu-id="09d9b-108">Description</span><span class="sxs-lookup"><span data-stu-id="09d9b-108">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09d9b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="09d9b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="09d9b-110">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="09d9b-110">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="09d9b-111">Si *src0*, puis *dest*  =  *src1* else *dest*  =  *src2*</span><span class="sxs-lookup"><span data-stu-id="09d9b-111">If *src0*, then *dest* = *src1* else *dest* = *src2*</span></span><br/> |
| <span data-ttu-id="09d9b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="09d9b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="09d9b-113">\[dans \] les composants sur lesquels tester la condition.</span><span class="sxs-lookup"><span data-stu-id="09d9b-113">\[in\] The components on which to test the condition.</span></span><br/>                                                               |
| <span data-ttu-id="09d9b-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="09d9b-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="09d9b-115">\[dans \] les composants à déplacer.</span><span class="sxs-lookup"><span data-stu-id="09d9b-115">\[in\] The components to move.</span></span> <br/>                                                                                     |
| <span data-ttu-id="09d9b-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="09d9b-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="09d9b-117">\[dans \] les composants à déplacer.</span><span class="sxs-lookup"><span data-stu-id="09d9b-117">\[in\] The components to move.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="09d9b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="09d9b-118">Remarks</span></span>

<span data-ttu-id="09d9b-119">L’exemple suivant montre comment utiliser cette instruction.</span><span class="sxs-lookup"><span data-stu-id="09d9b-119">The following example shows how to use this instruction.</span></span>

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

<span data-ttu-id="09d9b-120">Les modificateurs sur *src1* et *src2*, à l’exception de Swizzle, supposent que les données sont à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="09d9b-120">The modifiers on *src1* and *src2*, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="09d9b-121">L’absence de modificateurs déplace uniquement les données sans modifier les bits.</span><span class="sxs-lookup"><span data-stu-id="09d9b-121">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="09d9b-122">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="09d9b-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="09d9b-123">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="09d9b-123">Vertex Shader</span></span> | <span data-ttu-id="09d9b-124">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="09d9b-124">Geometry Shader</span></span> | <span data-ttu-id="09d9b-125">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="09d9b-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="09d9b-126">x</span><span class="sxs-lookup"><span data-stu-id="09d9b-126">x</span></span>             | <span data-ttu-id="09d9b-127">x</span><span class="sxs-lookup"><span data-stu-id="09d9b-127">x</span></span>               | <span data-ttu-id="09d9b-128">x</span><span class="sxs-lookup"><span data-stu-id="09d9b-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="09d9b-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="09d9b-129">Minimum Shader Model</span></span>

<span data-ttu-id="09d9b-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="09d9b-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="09d9b-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="09d9b-131">Shader Model</span></span>                                              | <span data-ttu-id="09d9b-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="09d9b-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="09d9b-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="09d9b-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="09d9b-134">Oui</span><span class="sxs-lookup"><span data-stu-id="09d9b-134">yes</span></span>       |
| [<span data-ttu-id="09d9b-135">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="09d9b-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="09d9b-136">Oui</span><span class="sxs-lookup"><span data-stu-id="09d9b-136">yes</span></span>       |
| [<span data-ttu-id="09d9b-137">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="09d9b-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="09d9b-138">Oui</span><span class="sxs-lookup"><span data-stu-id="09d9b-138">yes</span></span>       |
| [<span data-ttu-id="09d9b-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="09d9b-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="09d9b-140">non</span><span class="sxs-lookup"><span data-stu-id="09d9b-140">no</span></span>        |
| [<span data-ttu-id="09d9b-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="09d9b-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="09d9b-142">non</span><span class="sxs-lookup"><span data-stu-id="09d9b-142">no</span></span>        |
| [<span data-ttu-id="09d9b-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="09d9b-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="09d9b-144">non</span><span class="sxs-lookup"><span data-stu-id="09d9b-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="09d9b-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09d9b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09d9b-146">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="09d9b-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





