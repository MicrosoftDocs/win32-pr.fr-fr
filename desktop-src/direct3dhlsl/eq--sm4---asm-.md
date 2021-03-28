---
title: EQ (SM4-ASM)
description: Comparaison d’égalité des points à virgule flottante vectorielle.
ms.assetid: 925578E4-0161-45A9-840F-14AA65FF4F33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f47dc7bda7b1c61c251ace061fc75897788b968
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381117"
---
# <a name="eq-sm4---asm"></a><span data-ttu-id="c6f43-103">EQ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c6f43-103">eq (sm4 - asm)</span></span>

<span data-ttu-id="c6f43-104">Comparaison d’égalité des points à virgule flottante vectorielle.</span><span class="sxs-lookup"><span data-stu-id="c6f43-104">Component-wise vector floating point equality comparison.</span></span>



| <span data-ttu-id="c6f43-105">EQ dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c6f43-105">eq dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="c6f43-106">Élément</span><span class="sxs-lookup"><span data-stu-id="c6f43-106">Item</span></span>                                                            | <span data-ttu-id="c6f43-107">Description</span><span class="sxs-lookup"><span data-stu-id="c6f43-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c6f43-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c6f43-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c6f43-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c6f43-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="c6f43-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c6f43-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c6f43-111">\[dans \] le composant à comapre à *src1*.</span><span class="sxs-lookup"><span data-stu-id="c6f43-111">\[in\] The component to comapre to *src1*.</span></span><br/>         |
| <span data-ttu-id="c6f43-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c6f43-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c6f43-113">\[dans \] le composant à comapre à *src0*.</span><span class="sxs-lookup"><span data-stu-id="c6f43-113">\[in\] The component to comapre to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="c6f43-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c6f43-114">Remarks</span></span>

<span data-ttu-id="c6f43-115">Effectue la comparaison float (*src0*  ==  *src1*) pour chaque composant et écrit le résultat dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="c6f43-115">Performs the float comparison (*src0* == *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="c6f43-116">Si la comparaison est true, 0xFFFFFFFF est retourné pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="c6f43-116">If the comparison is true, 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="c6f43-117">Sinon, 0x0000000 est retourné.</span><span class="sxs-lookup"><span data-stu-id="c6f43-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="c6f43-118">Les dénormes sont vidées avant la comparaison (les registres source d’origine ne sont pas touchés).</span><span class="sxs-lookup"><span data-stu-id="c6f43-118">Denorms are flushed before comparison (original source registers untouched).</span></span> <span data-ttu-id="c6f43-119">+ 0 est égal à-0.</span><span class="sxs-lookup"><span data-stu-id="c6f43-119">+0 equals -0.</span></span> <span data-ttu-id="c6f43-120">La comparaison avec NaN retourne false.</span><span class="sxs-lookup"><span data-stu-id="c6f43-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="c6f43-121">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="c6f43-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c6f43-122">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="c6f43-122">Vertex Shader</span></span> | <span data-ttu-id="c6f43-123">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="c6f43-123">Geometry Shader</span></span> | <span data-ttu-id="c6f43-124">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c6f43-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c6f43-125">x</span><span class="sxs-lookup"><span data-stu-id="c6f43-125">x</span></span>             | <span data-ttu-id="c6f43-126">x</span><span class="sxs-lookup"><span data-stu-id="c6f43-126">x</span></span>               | <span data-ttu-id="c6f43-127">x</span><span class="sxs-lookup"><span data-stu-id="c6f43-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c6f43-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c6f43-128">Minimum Shader Model</span></span>

<span data-ttu-id="c6f43-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="c6f43-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c6f43-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c6f43-130">Shader Model</span></span>                                              | <span data-ttu-id="c6f43-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="c6f43-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c6f43-132">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="c6f43-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c6f43-133">Oui</span><span class="sxs-lookup"><span data-stu-id="c6f43-133">yes</span></span>       |
| [<span data-ttu-id="c6f43-134">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="c6f43-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c6f43-135">Oui</span><span class="sxs-lookup"><span data-stu-id="c6f43-135">yes</span></span>       |
| [<span data-ttu-id="c6f43-136">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="c6f43-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c6f43-137">Oui</span><span class="sxs-lookup"><span data-stu-id="c6f43-137">yes</span></span>       |
| [<span data-ttu-id="c6f43-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6f43-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c6f43-139">non</span><span class="sxs-lookup"><span data-stu-id="c6f43-139">no</span></span>        |
| [<span data-ttu-id="c6f43-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6f43-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c6f43-141">non</span><span class="sxs-lookup"><span data-stu-id="c6f43-141">no</span></span>        |
| [<span data-ttu-id="c6f43-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6f43-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c6f43-143">non</span><span class="sxs-lookup"><span data-stu-id="c6f43-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c6f43-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c6f43-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6f43-145">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c6f43-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





