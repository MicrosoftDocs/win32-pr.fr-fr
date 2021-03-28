---
title: IEQ (SM4-ASM)
description: Comparaison d’égalité des entiers vectoriels au niveau du composant.
ms.assetid: AD010554-80DC-4D2D-B04C-2638276DDC34
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a47ffe38b8322b748f6ba64ce9bbbc26a5bd9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990809"
---
# <a name="ieq-sm4---asm"></a><span data-ttu-id="6a5d5-103">IEQ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6a5d5-103">ieq (sm4 - asm)</span></span>

<span data-ttu-id="6a5d5-104">Comparaison d’égalité des entiers vectoriels au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="6a5d5-104">Component-wise vector integer equality comparison.</span></span>



| <span data-ttu-id="6a5d5-105">dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6a5d5-105">dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|---------------------------------------------------|



 



| <span data-ttu-id="6a5d5-106">Élément</span><span class="sxs-lookup"><span data-stu-id="6a5d5-106">Item</span></span>                                                            | <span data-ttu-id="6a5d5-107">Description</span><span class="sxs-lookup"><span data-stu-id="6a5d5-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="6a5d5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6a5d5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6a5d5-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6a5d5-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="6a5d5-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6a5d5-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6a5d5-111">\[dans \] la valeur à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="6a5d5-111">\[in\] The value to compare with *src1*.</span></span><br/>           |
| <span data-ttu-id="6a5d5-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="6a5d5-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6a5d5-113">\[dans \] la valeur à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="6a5d5-113">\[in\] The value to compare with *src0*.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="6a5d5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6a5d5-114">Remarks</span></span>

<span data-ttu-id="6a5d5-115">Cette instruction effectue une comparaison d’entiers (*src0*  ==  *src1*) pour chaque composant et écrit le résultat dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="6a5d5-115">This instruction performs the integer comparison (*src0* == *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="6a5d5-116">Si la comparaison est true, 0xFFFFFFFF est retourné pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="6a5d5-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="6a5d5-117">Sinon, 0x0000000 est retourné</span><span class="sxs-lookup"><span data-stu-id="6a5d5-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="6a5d5-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="6a5d5-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6a5d5-119">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="6a5d5-119">Vertex Shader</span></span> | <span data-ttu-id="6a5d5-120">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="6a5d5-120">Geometry Shader</span></span> | <span data-ttu-id="6a5d5-121">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="6a5d5-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6a5d5-122">x</span><span class="sxs-lookup"><span data-stu-id="6a5d5-122">x</span></span>             | <span data-ttu-id="6a5d5-123">x</span><span class="sxs-lookup"><span data-stu-id="6a5d5-123">x</span></span>               | <span data-ttu-id="6a5d5-124">x</span><span class="sxs-lookup"><span data-stu-id="6a5d5-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6a5d5-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="6a5d5-125">Minimum Shader Model</span></span>

<span data-ttu-id="6a5d5-126">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="6a5d5-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6a5d5-127">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6a5d5-127">Shader Model</span></span>                                              | <span data-ttu-id="6a5d5-128">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="6a5d5-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6a5d5-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="6a5d5-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6a5d5-130">Oui</span><span class="sxs-lookup"><span data-stu-id="6a5d5-130">yes</span></span>       |
| [<span data-ttu-id="6a5d5-131">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="6a5d5-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6a5d5-132">Oui</span><span class="sxs-lookup"><span data-stu-id="6a5d5-132">yes</span></span>       |
| [<span data-ttu-id="6a5d5-133">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="6a5d5-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6a5d5-134">Oui</span><span class="sxs-lookup"><span data-stu-id="6a5d5-134">yes</span></span>       |
| [<span data-ttu-id="6a5d5-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a5d5-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6a5d5-136">non</span><span class="sxs-lookup"><span data-stu-id="6a5d5-136">no</span></span>        |
| [<span data-ttu-id="6a5d5-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a5d5-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6a5d5-138">non</span><span class="sxs-lookup"><span data-stu-id="6a5d5-138">no</span></span>        |
| [<span data-ttu-id="6a5d5-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a5d5-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6a5d5-140">non</span><span class="sxs-lookup"><span data-stu-id="6a5d5-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6a5d5-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a5d5-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a5d5-142">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a5d5-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





