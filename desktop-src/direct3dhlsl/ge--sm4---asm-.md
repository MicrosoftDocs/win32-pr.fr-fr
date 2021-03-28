---
title: GE (SM4-ASM)
description: Comparaison de points à virgule flottante de type Vector à valeur supérieure ou égale au niveau du composant.
ms.assetid: 658AF249-4935-41AF-972A-D8CDEABA76AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93d21d9ac044e2ad4d63e954a4732a15794b123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381155"
---
# <a name="ge-sm4---asm"></a><span data-ttu-id="baf5a-103">GE (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="baf5a-103">ge (sm4 - asm)</span></span>

<span data-ttu-id="baf5a-104">Comparaison de points à virgule flottante de type Vector à valeur supérieure ou égale au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="baf5a-104">Component-wise vector floating point greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="baf5a-105">GE dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="baf5a-105">ge dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="baf5a-106">Élément</span><span class="sxs-lookup"><span data-stu-id="baf5a-106">Item</span></span>                                                            | <span data-ttu-id="baf5a-107">Description</span><span class="sxs-lookup"><span data-stu-id="baf5a-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="baf5a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="baf5a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="baf5a-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="baf5a-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="baf5a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="baf5a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="baf5a-111">\[dans \] le composant à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="baf5a-111">\[in\] The component to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="baf5a-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="baf5a-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="baf5a-113">\[dans \] le composant à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="baf5a-113">\[in\] The component to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="baf5a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="baf5a-114">Remarks</span></span>

<span data-ttu-id="baf5a-115">Effectue la comparaison float (*src0*  >=  *src1*) pour chaque composant et écrit le résultat dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="baf5a-115">Performs the float comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="baf5a-116">Si la comparaison est true, 0xFFFFFFFF est retourné pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="baf5a-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="baf5a-117">Sinon, 0x0000000 est retourné.</span><span class="sxs-lookup"><span data-stu-id="baf5a-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="baf5a-118">Les dénormes sont vidées avant la comparaison et les registres source d’origine ne sont pas touchés.</span><span class="sxs-lookup"><span data-stu-id="baf5a-118">Denorms are flushed before comparison, and original source registers are untouched.</span></span> <span data-ttu-id="baf5a-119">+ 0 est égal à-0.</span><span class="sxs-lookup"><span data-stu-id="baf5a-119">+0 equals -0.</span></span> <span data-ttu-id="baf5a-120">La comparaison avec NaN retourne false.</span><span class="sxs-lookup"><span data-stu-id="baf5a-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="baf5a-121">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="baf5a-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="baf5a-122">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="baf5a-122">Vertex Shader</span></span> | <span data-ttu-id="baf5a-123">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="baf5a-123">Geometry Shader</span></span> | <span data-ttu-id="baf5a-124">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="baf5a-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="baf5a-125">x</span><span class="sxs-lookup"><span data-stu-id="baf5a-125">x</span></span>             | <span data-ttu-id="baf5a-126">x</span><span class="sxs-lookup"><span data-stu-id="baf5a-126">x</span></span>               | <span data-ttu-id="baf5a-127">x</span><span class="sxs-lookup"><span data-stu-id="baf5a-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="baf5a-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="baf5a-128">Minimum Shader Model</span></span>

<span data-ttu-id="baf5a-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="baf5a-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="baf5a-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="baf5a-130">Shader Model</span></span>                                              | <span data-ttu-id="baf5a-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="baf5a-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="baf5a-132">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="baf5a-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="baf5a-133">Oui</span><span class="sxs-lookup"><span data-stu-id="baf5a-133">yes</span></span>       |
| [<span data-ttu-id="baf5a-134">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="baf5a-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="baf5a-135">Oui</span><span class="sxs-lookup"><span data-stu-id="baf5a-135">yes</span></span>       |
| [<span data-ttu-id="baf5a-136">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="baf5a-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="baf5a-137">Oui</span><span class="sxs-lookup"><span data-stu-id="baf5a-137">yes</span></span>       |
| [<span data-ttu-id="baf5a-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="baf5a-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="baf5a-139">non</span><span class="sxs-lookup"><span data-stu-id="baf5a-139">no</span></span>        |
| [<span data-ttu-id="baf5a-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="baf5a-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="baf5a-141">non</span><span class="sxs-lookup"><span data-stu-id="baf5a-141">no</span></span>        |
| [<span data-ttu-id="baf5a-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="baf5a-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="baf5a-143">non</span><span class="sxs-lookup"><span data-stu-id="baf5a-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="baf5a-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="baf5a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baf5a-145">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="baf5a-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





