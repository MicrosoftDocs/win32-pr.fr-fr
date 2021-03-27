---
title: DLT (SM5-ASM)
description: Comparaison « inférieur à » pour la double précision au niveau du composant.
ms.assetid: A9DE5007-4ADD-403D-A2B7-EAE475E9DCCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88fd45ebde621ed2c5f5aafc013741d6ee34c318
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971554"
---
# <a name="dlt-sm5---asm"></a><span data-ttu-id="298c3-103">DLT (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="298c3-103">dlt (sm5 - asm)</span></span>

<span data-ttu-id="298c3-104">Comparaison « inférieur à » pour la double précision au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="298c3-104">Component-wise double-precision less-than comparison.</span></span>



| <span data-ttu-id="298c3-105">DLT \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="298c3-105">dlt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="298c3-106">Élément</span><span class="sxs-lookup"><span data-stu-id="298c3-106">Item</span></span>                                                            | <span data-ttu-id="298c3-107">Description</span><span class="sxs-lookup"><span data-stu-id="298c3-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="298c3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="298c3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="298c3-109">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="298c3-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="298c3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="298c3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="298c3-111">\[dans \] les composants à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="298c3-111">\[in\] The components to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="298c3-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="298c3-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="298c3-113">\[dans \] les composants à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="298c3-113">\[in\] The components to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="298c3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="298c3-114">Remarks</span></span>

<span data-ttu-id="298c3-115">Cette instruction effectue la comparaison à virgule flottante double précision (*src0*  <  *src1*) pour chaque composant et écrit le résultat dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="298c3-115">This instruction performs the double-precision floating-point comparison (*src0* < *src1*) for each component and writes the result to *dest*.</span></span>

<span data-ttu-id="298c3-116">Si la comparaison est true, 32-bit 0xFFFFFFFF est retourné pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="298c3-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="298c3-117">Sinon 32-bit 0x00000000 est retourné.</span><span class="sxs-lookup"><span data-stu-id="298c3-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="298c3-118">La comparaison avec NaN retourne false.</span><span class="sxs-lookup"><span data-stu-id="298c3-118">Comparison with NaN returns false.</span></span>

<span data-ttu-id="298c3-119">Les masques de *dest* valides sont un ou deux composants.</span><span class="sxs-lookup"><span data-stu-id="298c3-119">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="298c3-120">C’est-à-dire :. x,. y,. z,. w,. XY,. XZ,. xw,. YZ,. YW,. ZW le premier composant *dest* dans le masque reçoit le résultat 32 bits pour la première comparaison double.</span><span class="sxs-lookup"><span data-stu-id="298c3-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="298c3-121">Le deuxième composant dans le masque (s’il est présent) reçoit le résultat 32 bits pour la deuxième comparaison double.</span><span class="sxs-lookup"><span data-stu-id="298c3-121">The second component in the mask (if present) receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="298c3-122">Les Swizzles valides pour les paramètres sources sont. XYZW,. Xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="298c3-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="298c3-123">Les mappages *src* suivants sont postérieurs à Swizzle :</span><span class="sxs-lookup"><span data-stu-id="298c3-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="298c3-124">*src0* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="298c3-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="298c3-125">*src1* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="298c3-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="298c3-126">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="298c3-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="298c3-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="298c3-127">Vertex</span></span> | <span data-ttu-id="298c3-128">Forme</span><span class="sxs-lookup"><span data-stu-id="298c3-128">Hull</span></span> | <span data-ttu-id="298c3-129">Domain</span><span class="sxs-lookup"><span data-stu-id="298c3-129">Domain</span></span> | <span data-ttu-id="298c3-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="298c3-130">Geometry</span></span> | <span data-ttu-id="298c3-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="298c3-131">Pixel</span></span> | <span data-ttu-id="298c3-132">Compute</span><span class="sxs-lookup"><span data-stu-id="298c3-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="298c3-133">X</span><span class="sxs-lookup"><span data-stu-id="298c3-133">X</span></span>      | <span data-ttu-id="298c3-134">X</span><span class="sxs-lookup"><span data-stu-id="298c3-134">X</span></span>    | <span data-ttu-id="298c3-135">X</span><span class="sxs-lookup"><span data-stu-id="298c3-135">X</span></span>      | <span data-ttu-id="298c3-136">X</span><span class="sxs-lookup"><span data-stu-id="298c3-136">X</span></span>        | <span data-ttu-id="298c3-137">X</span><span class="sxs-lookup"><span data-stu-id="298c3-137">X</span></span>     | <span data-ttu-id="298c3-138">X</span><span class="sxs-lookup"><span data-stu-id="298c3-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="298c3-139">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="298c3-139">Minimum Shader Model</span></span>

<span data-ttu-id="298c3-140">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="298c3-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="298c3-141">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="298c3-141">Shader Model</span></span>                                              | <span data-ttu-id="298c3-142">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="298c3-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="298c3-143">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="298c3-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="298c3-144">Oui</span><span class="sxs-lookup"><span data-stu-id="298c3-144">yes</span></span>       |
| [<span data-ttu-id="298c3-145">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="298c3-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="298c3-146">non</span><span class="sxs-lookup"><span data-stu-id="298c3-146">no</span></span>        |
| [<span data-ttu-id="298c3-147">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="298c3-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="298c3-148">non</span><span class="sxs-lookup"><span data-stu-id="298c3-148">no</span></span>        |
| [<span data-ttu-id="298c3-149">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="298c3-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="298c3-150">non</span><span class="sxs-lookup"><span data-stu-id="298c3-150">no</span></span>        |
| [<span data-ttu-id="298c3-151">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="298c3-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="298c3-152">non</span><span class="sxs-lookup"><span data-stu-id="298c3-152">no</span></span>        |
| [<span data-ttu-id="298c3-153">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="298c3-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="298c3-154">non</span><span class="sxs-lookup"><span data-stu-id="298c3-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="298c3-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="298c3-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="298c3-156">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="298c3-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





