---
title: Dmax (SM5-ASM)
description: Valeur maximale à double précision au niveau du composant.
ms.assetid: 34ED8B34-2592-4BBB-BCF0-F2222E4D51D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703b277a98b16570de6f5ab7e0e7643ddfdcc705
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381145"
---
# <a name="dmax-sm5---asm"></a><span data-ttu-id="50208-103">Dmax (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="50208-103">dmax (sm5 - asm)</span></span>

<span data-ttu-id="50208-104">Valeur maximale à double précision au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="50208-104">Component-wise double-precision maximum.</span></span>



| <span data-ttu-id="50208-105">Dmax \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="50208-105">dmax\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="50208-106">Élément</span><span class="sxs-lookup"><span data-stu-id="50208-106">Item</span></span>                                                            | <span data-ttu-id="50208-107">Description</span><span class="sxs-lookup"><span data-stu-id="50208-107">Description</span></span>                                                                                                                                                                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50208-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="50208-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="50208-109">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="50208-109">\[in\] The address of the results of the operation.</span></span><br/> <span data-ttu-id="50208-110">*dest*  =  . *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="50208-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="50208-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="50208-111">*src0* : *src1*</span></span><br/> <span data-ttu-id="50208-112">>= est utilisé à la place de > afin que si min (x, y) = x, alors Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="50208-112">>= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span> <br/> |
| <span data-ttu-id="50208-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="50208-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="50208-114">\[dans \] la valeur à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="50208-114">\[in\] The value to compare with *src1*.</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="50208-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="50208-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="50208-116">\[dans \] la valeur à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="50208-116">\[in\] The value to compare with *src0*.</span></span><br/>                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="50208-117">Notes</span><span class="sxs-lookup"><span data-stu-id="50208-117">Remarks</span></span>

<span data-ttu-id="50208-118">NaN a une gestion spéciale.</span><span class="sxs-lookup"><span data-stu-id="50208-118">NaN has special handling.</span></span> <span data-ttu-id="50208-119">Si un opérande source est NaN, l’autre opérande source est retourné.</span><span class="sxs-lookup"><span data-stu-id="50208-119">If one source operand is NaN, then the other source operand is returned.</span></span> <span data-ttu-id="50208-120">Le choix est effectué par composant.</span><span class="sxs-lookup"><span data-stu-id="50208-120">The choice is made per-component.</span></span> <span data-ttu-id="50208-121">Si les deux sont NaN, toute représentation NaN est retournée.</span><span class="sxs-lookup"><span data-stu-id="50208-121">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="50208-122">Les Swizzles valides pour les paramètres sources sont. XYZW,. Xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="50208-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="50208-123">Les masques de *dest* valides sont. XY,. ZW et. XYZW.</span><span class="sxs-lookup"><span data-stu-id="50208-123">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="50208-124">Les mappages *src* suivants sont postérieurs à Swizzle :</span><span class="sxs-lookup"><span data-stu-id="50208-124">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="50208-125">*dest* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="50208-125">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="50208-126">*src0* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="50208-126">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="50208-127">*src1* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="50208-127">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="50208-128">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="50208-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="50208-129">Sommet</span><span class="sxs-lookup"><span data-stu-id="50208-129">Vertex</span></span> | <span data-ttu-id="50208-130">Forme</span><span class="sxs-lookup"><span data-stu-id="50208-130">Hull</span></span> | <span data-ttu-id="50208-131">Domain</span><span class="sxs-lookup"><span data-stu-id="50208-131">Domain</span></span> | <span data-ttu-id="50208-132">Géométrie</span><span class="sxs-lookup"><span data-stu-id="50208-132">Geometry</span></span> | <span data-ttu-id="50208-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="50208-133">Pixel</span></span> | <span data-ttu-id="50208-134">Compute</span><span class="sxs-lookup"><span data-stu-id="50208-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="50208-135">X</span><span class="sxs-lookup"><span data-stu-id="50208-135">X</span></span>      | <span data-ttu-id="50208-136">X</span><span class="sxs-lookup"><span data-stu-id="50208-136">X</span></span>    | <span data-ttu-id="50208-137">X</span><span class="sxs-lookup"><span data-stu-id="50208-137">X</span></span>      | <span data-ttu-id="50208-138">X</span><span class="sxs-lookup"><span data-stu-id="50208-138">X</span></span>        | <span data-ttu-id="50208-139">X</span><span class="sxs-lookup"><span data-stu-id="50208-139">X</span></span>     | <span data-ttu-id="50208-140">X</span><span class="sxs-lookup"><span data-stu-id="50208-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="50208-141">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="50208-141">Minimum Shader Model</span></span>

<span data-ttu-id="50208-142">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="50208-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="50208-143">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="50208-143">Shader Model</span></span>                                              | <span data-ttu-id="50208-144">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="50208-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="50208-145">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="50208-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="50208-146">Oui</span><span class="sxs-lookup"><span data-stu-id="50208-146">yes</span></span>       |
| [<span data-ttu-id="50208-147">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="50208-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="50208-148">non</span><span class="sxs-lookup"><span data-stu-id="50208-148">no</span></span>        |
| [<span data-ttu-id="50208-149">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="50208-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="50208-150">non</span><span class="sxs-lookup"><span data-stu-id="50208-150">no</span></span>        |
| [<span data-ttu-id="50208-151">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="50208-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="50208-152">non</span><span class="sxs-lookup"><span data-stu-id="50208-152">no</span></span>        |
| [<span data-ttu-id="50208-153">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="50208-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="50208-154">non</span><span class="sxs-lookup"><span data-stu-id="50208-154">no</span></span>        |
| [<span data-ttu-id="50208-155">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="50208-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="50208-156">non</span><span class="sxs-lookup"><span data-stu-id="50208-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="50208-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50208-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50208-158">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="50208-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





