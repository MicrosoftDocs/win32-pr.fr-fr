---
title: ftod (SM5-ASM)
description: Conversion au niveau du composant des données à virgule flottante simple précision en données à virgule flottante double précision.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6790735745805426d32aefcc5d5d771ade644e43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313705"
---
# <a name="ftod-sm5---asm"></a><span data-ttu-id="a0b7d-103">ftod (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a0b7d-103">ftod (sm5 - asm)</span></span>

<span data-ttu-id="a0b7d-104">Conversion au niveau du composant des données à virgule flottante simple précision en données à virgule flottante double précision.</span><span class="sxs-lookup"><span data-stu-id="a0b7d-104">Component-wise conversion from single-precision floating-point data to double-precision floating-point data.</span></span>



| <span data-ttu-id="a0b7d-105">ftod dest \[ . Mask \] , \[ - \] src \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="a0b7d-105">ftod dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="a0b7d-106">Élément</span><span class="sxs-lookup"><span data-stu-id="a0b7d-106">Item</span></span>                                                            | <span data-ttu-id="a0b7d-107">Description</span><span class="sxs-lookup"><span data-stu-id="a0b7d-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a0b7d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a0b7d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a0b7d-109">\[dans \] l’adresse des données converties.</span><span class="sxs-lookup"><span data-stu-id="a0b7d-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="a0b7d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a0b7d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a0b7d-111">\[dans \] les données à convertir.</span><span class="sxs-lookup"><span data-stu-id="a0b7d-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="a0b7d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a0b7d-112">Remarks</span></span>

<span data-ttu-id="a0b7d-113">Chaque composant de la source est converti à partir de la représentation à simple précision en représentation à double précision.</span><span class="sxs-lookup"><span data-stu-id="a0b7d-113">Each component of the source is converted from the single-precision representation to the double-precision representation.</span></span>

<span data-ttu-id="a0b7d-114">Les masques de *dest* valides sont. XY,. ZW et. XYZW.</span><span class="sxs-lookup"><span data-stu-id="a0b7d-114">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="a0b7d-115">. XY reçoit le résultat de la première conversion, et. ZW reçoit le résultat de la deuxième conversion.</span><span class="sxs-lookup"><span data-stu-id="a0b7d-115">.xy receives the result of the first conversion, and .zw receives the result of the second conversion.</span></span>

<span data-ttu-id="a0b7d-116">*dest* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="a0b7d-116">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="a0b7d-117">*src* est un vec2 flottant sur x et y (ZW ignoré) (Swizzle).</span><span class="sxs-lookup"><span data-stu-id="a0b7d-117">*src* is a float vec2 across x and y (zw ignored) (post swizzle).</span></span>

<span data-ttu-id="a0b7d-118">Pour les conversions de type float32<->, les implémentations peuvent honorer des dénormes float32 ou peuvent les vider.</span><span class="sxs-lookup"><span data-stu-id="a0b7d-118">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="a0b7d-119">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="a0b7d-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a0b7d-120">Sommet</span><span class="sxs-lookup"><span data-stu-id="a0b7d-120">Vertex</span></span> | <span data-ttu-id="a0b7d-121">Forme</span><span class="sxs-lookup"><span data-stu-id="a0b7d-121">Hull</span></span> | <span data-ttu-id="a0b7d-122">Domain</span><span class="sxs-lookup"><span data-stu-id="a0b7d-122">Domain</span></span> | <span data-ttu-id="a0b7d-123">Géométrie</span><span class="sxs-lookup"><span data-stu-id="a0b7d-123">Geometry</span></span> | <span data-ttu-id="a0b7d-124">Pixel</span><span class="sxs-lookup"><span data-stu-id="a0b7d-124">Pixel</span></span> | <span data-ttu-id="a0b7d-125">Compute</span><span class="sxs-lookup"><span data-stu-id="a0b7d-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a0b7d-126">X</span><span class="sxs-lookup"><span data-stu-id="a0b7d-126">X</span></span>      | <span data-ttu-id="a0b7d-127">X</span><span class="sxs-lookup"><span data-stu-id="a0b7d-127">X</span></span>    | <span data-ttu-id="a0b7d-128">X</span><span class="sxs-lookup"><span data-stu-id="a0b7d-128">X</span></span>      | <span data-ttu-id="a0b7d-129">X</span><span class="sxs-lookup"><span data-stu-id="a0b7d-129">X</span></span>        | <span data-ttu-id="a0b7d-130">X</span><span class="sxs-lookup"><span data-stu-id="a0b7d-130">X</span></span>     | <span data-ttu-id="a0b7d-131">X</span><span class="sxs-lookup"><span data-stu-id="a0b7d-131">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a0b7d-132">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="a0b7d-132">Minimum Shader Model</span></span>

<span data-ttu-id="a0b7d-133">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="a0b7d-133">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a0b7d-134">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a0b7d-134">Shader Model</span></span>                                              | <span data-ttu-id="a0b7d-135">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="a0b7d-135">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a0b7d-136">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="a0b7d-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a0b7d-137">Oui</span><span class="sxs-lookup"><span data-stu-id="a0b7d-137">yes</span></span>       |
| [<span data-ttu-id="a0b7d-138">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="a0b7d-138">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a0b7d-139">non</span><span class="sxs-lookup"><span data-stu-id="a0b7d-139">no</span></span>        |
| [<span data-ttu-id="a0b7d-140">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="a0b7d-140">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a0b7d-141">non</span><span class="sxs-lookup"><span data-stu-id="a0b7d-141">no</span></span>        |
| [<span data-ttu-id="a0b7d-142">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0b7d-142">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a0b7d-143">non</span><span class="sxs-lookup"><span data-stu-id="a0b7d-143">no</span></span>        |
| [<span data-ttu-id="a0b7d-144">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0b7d-144">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a0b7d-145">non</span><span class="sxs-lookup"><span data-stu-id="a0b7d-145">no</span></span>        |
| [<span data-ttu-id="a0b7d-146">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0b7d-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a0b7d-147">non</span><span class="sxs-lookup"><span data-stu-id="a0b7d-147">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a0b7d-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0b7d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0b7d-149">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0b7d-149">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





