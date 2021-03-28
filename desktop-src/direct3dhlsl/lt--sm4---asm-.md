---
title: lt (SM4-ASM)
description: Comparaison « inférieur à virgule flottante » à virgule flottante au niveau du composant.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a727987e4eaee017137d62dbe12f8581540876
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313675"
---
# <a name="lt-sm4---asm"></a><span data-ttu-id="73d8d-103">lt (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="73d8d-103">lt (sm4 - asm)</span></span>

<span data-ttu-id="73d8d-104">Comparaison « inférieur à virgule flottante » à virgule flottante au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="73d8d-104">Component-wise vector floating point less-than comparison.</span></span>



| <span data-ttu-id="73d8d-105">lt dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="73d8d-105">lt dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="73d8d-106">Élément</span><span class="sxs-lookup"><span data-stu-id="73d8d-106">Item</span></span>                                                            | <span data-ttu-id="73d8d-107">Description</span><span class="sxs-lookup"><span data-stu-id="73d8d-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="73d8d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="73d8d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="73d8d-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="73d8d-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="73d8d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="73d8d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="73d8d-111">\[dans \] la valeur à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="73d8d-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="73d8d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="73d8d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="73d8d-113">\[dans \] la valeur à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="73d8d-113">\[in\] The value to compare to *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="73d8d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="73d8d-114">Remarks</span></span>

<span data-ttu-id="73d8d-115">Cette instruction effectue la comparaison float (*src0*  <  *src1*) pour chaque composant et écrit le résultat dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="73d8d-115">This instruction performs the float comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="73d8d-116">Si la comparaison est true, 0xFFFFFFFF est retourné pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="73d8d-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="73d8d-117">Sinon, 0x0000000 est retourné</span><span class="sxs-lookup"><span data-stu-id="73d8d-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="73d8d-118">Les dénormes sont vidées avant la comparaison ; les registres source d’origine ne sont pas touchés.</span><span class="sxs-lookup"><span data-stu-id="73d8d-118">Denorms are flushed before comparison; original source registers are untouched.</span></span>

<span data-ttu-id="73d8d-119">+ 0 est égal à-0.</span><span class="sxs-lookup"><span data-stu-id="73d8d-119">+0 equals -0.</span></span>

<span data-ttu-id="73d8d-120">La comparaison avec NaN retourne false.</span><span class="sxs-lookup"><span data-stu-id="73d8d-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="73d8d-121">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="73d8d-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="73d8d-122">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="73d8d-122">Vertex Shader</span></span> | <span data-ttu-id="73d8d-123">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="73d8d-123">Geometry Shader</span></span> | <span data-ttu-id="73d8d-124">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="73d8d-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="73d8d-125">x</span><span class="sxs-lookup"><span data-stu-id="73d8d-125">x</span></span>             | <span data-ttu-id="73d8d-126">x</span><span class="sxs-lookup"><span data-stu-id="73d8d-126">x</span></span>               | <span data-ttu-id="73d8d-127">x</span><span class="sxs-lookup"><span data-stu-id="73d8d-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="73d8d-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="73d8d-128">Minimum Shader Model</span></span>

<span data-ttu-id="73d8d-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="73d8d-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="73d8d-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="73d8d-130">Shader Model</span></span>                                              | <span data-ttu-id="73d8d-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="73d8d-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="73d8d-132">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="73d8d-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="73d8d-133">Oui</span><span class="sxs-lookup"><span data-stu-id="73d8d-133">yes</span></span>       |
| [<span data-ttu-id="73d8d-134">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="73d8d-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="73d8d-135">Oui</span><span class="sxs-lookup"><span data-stu-id="73d8d-135">yes</span></span>       |
| [<span data-ttu-id="73d8d-136">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="73d8d-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="73d8d-137">Oui</span><span class="sxs-lookup"><span data-stu-id="73d8d-137">yes</span></span>       |
| [<span data-ttu-id="73d8d-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="73d8d-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="73d8d-139">non</span><span class="sxs-lookup"><span data-stu-id="73d8d-139">no</span></span>        |
| [<span data-ttu-id="73d8d-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="73d8d-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="73d8d-141">non</span><span class="sxs-lookup"><span data-stu-id="73d8d-141">no</span></span>        |
| [<span data-ttu-id="73d8d-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="73d8d-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="73d8d-143">non</span><span class="sxs-lookup"><span data-stu-id="73d8d-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="73d8d-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73d8d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73d8d-145">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="73d8d-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





