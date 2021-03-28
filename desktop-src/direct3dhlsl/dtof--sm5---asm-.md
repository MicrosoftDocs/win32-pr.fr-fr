---
title: dtof (SM5-ASM)
description: Conversion au niveau du composant des données à virgule flottante double précision en données à virgule flottante simple précision.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a66e72cf4c2cb1ac49adc492a586b4cbb9eef3b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313627"
---
# <a name="dtof-sm5---asm"></a><span data-ttu-id="0cc20-103">dtof (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0cc20-103">dtof (sm5 - asm)</span></span>

<span data-ttu-id="0cc20-104">Conversion au niveau du composant des données à virgule flottante double précision en données à virgule flottante simple précision.</span><span class="sxs-lookup"><span data-stu-id="0cc20-104">Component-wise conversion from double-precision floating-point data to single-precision floating-point data.</span></span>



| <span data-ttu-id="0cc20-105">dtof dest \[ . Mask \] , \[ - \] src \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="0cc20-105">dtof dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="0cc20-106">Élément</span><span class="sxs-lookup"><span data-stu-id="0cc20-106">Item</span></span>                                                            | <span data-ttu-id="0cc20-107">Description</span><span class="sxs-lookup"><span data-stu-id="0cc20-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0cc20-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0cc20-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0cc20-109">\[dans \] l’adresse des données converties.</span><span class="sxs-lookup"><span data-stu-id="0cc20-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="0cc20-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0cc20-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0cc20-111">\[dans \] les données à convertir.</span><span class="sxs-lookup"><span data-stu-id="0cc20-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="0cc20-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0cc20-112">Remarks</span></span>

<span data-ttu-id="0cc20-113">Chaque composant de la source est converti à partir de la représentation à double précision en une représentation à simple précision à l’aide de l’arrondi à la valeur la plus proche.</span><span class="sxs-lookup"><span data-stu-id="0cc20-113">Each component of the source is converted from the double-precision representation to the single-precision representation using round-to-nearest-even rounding.</span></span>

<span data-ttu-id="0cc20-114">Le Swizzles valide pour le paramètre source est. XYZW,. Xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="0cc20-114">The valid swizzles for the source parameter are .xyzw, .xyxy, .zwxy, .zwzw.</span></span>

<span data-ttu-id="0cc20-115">Les masques de *dest* valides sont un ou deux composants.</span><span class="sxs-lookup"><span data-stu-id="0cc20-115">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="0cc20-116">C’est-à-dire :. x,. y,. z,. w,. XY,. XZ,. xw,. YZ,. YW,. ZW le résultat de la première conversion est dirigé vers le premier composant du masque, et le résultat du deuxième composant est placé dans le deuxième composant du masque, s’il est présent.</span><span class="sxs-lookup"><span data-stu-id="0cc20-116">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The result of the first conversion goes to the first component in the mask, and the result of the second component goes in the second component in the mask, if present.</span></span>

<span data-ttu-id="0cc20-117">les composants *dest* sont float32.</span><span class="sxs-lookup"><span data-stu-id="0cc20-117">*dest* components are float32.</span></span>

<span data-ttu-id="0cc20-118">*src* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB) poster Swizzle.</span><span class="sxs-lookup"><span data-stu-id="0cc20-118">*src* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB) post swizzle.</span></span>

<span data-ttu-id="0cc20-119">Pour les conversions de type float32<->, les implémentations peuvent honorer des dénormes float32 ou peuvent les vider.</span><span class="sxs-lookup"><span data-stu-id="0cc20-119">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="0cc20-120">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="0cc20-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0cc20-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="0cc20-121">Vertex</span></span> | <span data-ttu-id="0cc20-122">Forme</span><span class="sxs-lookup"><span data-stu-id="0cc20-122">Hull</span></span> | <span data-ttu-id="0cc20-123">Domain</span><span class="sxs-lookup"><span data-stu-id="0cc20-123">Domain</span></span> | <span data-ttu-id="0cc20-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="0cc20-124">Geometry</span></span> | <span data-ttu-id="0cc20-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="0cc20-125">Pixel</span></span> | <span data-ttu-id="0cc20-126">Compute</span><span class="sxs-lookup"><span data-stu-id="0cc20-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0cc20-127">X</span><span class="sxs-lookup"><span data-stu-id="0cc20-127">X</span></span>      | <span data-ttu-id="0cc20-128">X</span><span class="sxs-lookup"><span data-stu-id="0cc20-128">X</span></span>    | <span data-ttu-id="0cc20-129">X</span><span class="sxs-lookup"><span data-stu-id="0cc20-129">X</span></span>      | <span data-ttu-id="0cc20-130">X</span><span class="sxs-lookup"><span data-stu-id="0cc20-130">X</span></span>        | <span data-ttu-id="0cc20-131">X</span><span class="sxs-lookup"><span data-stu-id="0cc20-131">X</span></span>     | <span data-ttu-id="0cc20-132">X</span><span class="sxs-lookup"><span data-stu-id="0cc20-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0cc20-133">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0cc20-133">Minimum Shader Model</span></span>

<span data-ttu-id="0cc20-134">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="0cc20-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0cc20-135">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0cc20-135">Shader Model</span></span>                                              | <span data-ttu-id="0cc20-136">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0cc20-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0cc20-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="0cc20-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0cc20-138">Oui</span><span class="sxs-lookup"><span data-stu-id="0cc20-138">yes</span></span>       |
| [<span data-ttu-id="0cc20-139">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="0cc20-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0cc20-140">non</span><span class="sxs-lookup"><span data-stu-id="0cc20-140">no</span></span>        |
| [<span data-ttu-id="0cc20-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="0cc20-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0cc20-142">non</span><span class="sxs-lookup"><span data-stu-id="0cc20-142">no</span></span>        |
| [<span data-ttu-id="0cc20-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0cc20-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0cc20-144">non</span><span class="sxs-lookup"><span data-stu-id="0cc20-144">no</span></span>        |
| [<span data-ttu-id="0cc20-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0cc20-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0cc20-146">non</span><span class="sxs-lookup"><span data-stu-id="0cc20-146">no</span></span>        |
| [<span data-ttu-id="0cc20-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0cc20-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0cc20-148">non</span><span class="sxs-lookup"><span data-stu-id="0cc20-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0cc20-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0cc20-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cc20-150">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0cc20-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





