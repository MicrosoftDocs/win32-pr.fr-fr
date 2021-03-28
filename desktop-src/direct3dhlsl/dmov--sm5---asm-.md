---
title: dmov (SM5-ASM)
description: Déplacement au niveau du composant. | dmov (SM5-ASM)
ms.assetid: 05DBB9E2-10EC-4324-BB8F-1A9E315DE90C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b7d9c5ca0da1671ddf30fb9746333617f7688a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953774"
---
# <a name="dmov-sm5---asm"></a><span data-ttu-id="9e33a-104">dmov (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9e33a-104">dmov (sm5 - asm)</span></span>

<span data-ttu-id="9e33a-105">Déplacement au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="9e33a-105">Component-wise move.</span></span>



| <span data-ttu-id="9e33a-106">dmov \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9e33a-106">dmov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="9e33a-107">Élément</span><span class="sxs-lookup"><span data-stu-id="9e33a-107">Item</span></span>                                                            | <span data-ttu-id="9e33a-108">Description</span><span class="sxs-lookup"><span data-stu-id="9e33a-108">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="9e33a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9e33a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9e33a-110">\[dans \] la destination de déplacement.</span><span class="sxs-lookup"><span data-stu-id="9e33a-110">\[in\] The move destination.</span></span> <span data-ttu-id="9e33a-111">*dest*  =  . *src0*.</span><span class="sxs-lookup"><span data-stu-id="9e33a-111">*dest* = *src0*.</span></span><br/> |
| <span data-ttu-id="9e33a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9e33a-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9e33a-113">\[dans \] les composants à déplacer.</span><span class="sxs-lookup"><span data-stu-id="9e33a-113">\[in\] The components to be moved.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="9e33a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9e33a-114">Remarks</span></span>

<span data-ttu-id="9e33a-115">Les modificateurs, autres que Swizzle, supposent que les données sont à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="9e33a-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="9e33a-116">L’absence de modificateurs déplace les données sans modifier les bits.</span><span class="sxs-lookup"><span data-stu-id="9e33a-116">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="9e33a-117">Les Swizzles valides pour les paramètres sources sont. XYZW,. Xyxy,. zwxy,. zwzw.</span><span class="sxs-lookup"><span data-stu-id="9e33a-117">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="9e33a-118">Les mappages *src* suivants sont postérieurs à Swizzle :</span><span class="sxs-lookup"><span data-stu-id="9e33a-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="9e33a-119">*src0* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="9e33a-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="9e33a-120">*src1* est un double vec2 entre (x 32LSB, y 32MSB) et (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="9e33a-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="9e33a-121">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="9e33a-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9e33a-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="9e33a-122">Vertex</span></span> | <span data-ttu-id="9e33a-123">Forme</span><span class="sxs-lookup"><span data-stu-id="9e33a-123">Hull</span></span> | <span data-ttu-id="9e33a-124">Domain</span><span class="sxs-lookup"><span data-stu-id="9e33a-124">Domain</span></span> | <span data-ttu-id="9e33a-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="9e33a-125">Geometry</span></span> | <span data-ttu-id="9e33a-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="9e33a-126">Pixel</span></span> | <span data-ttu-id="9e33a-127">Compute</span><span class="sxs-lookup"><span data-stu-id="9e33a-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9e33a-128">X</span><span class="sxs-lookup"><span data-stu-id="9e33a-128">X</span></span>      | <span data-ttu-id="9e33a-129">X</span><span class="sxs-lookup"><span data-stu-id="9e33a-129">X</span></span>    | <span data-ttu-id="9e33a-130">X</span><span class="sxs-lookup"><span data-stu-id="9e33a-130">X</span></span>      | <span data-ttu-id="9e33a-131">X</span><span class="sxs-lookup"><span data-stu-id="9e33a-131">X</span></span>        | <span data-ttu-id="9e33a-132">X</span><span class="sxs-lookup"><span data-stu-id="9e33a-132">X</span></span>     | <span data-ttu-id="9e33a-133">X</span><span class="sxs-lookup"><span data-stu-id="9e33a-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9e33a-134">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9e33a-134">Minimum Shader Model</span></span>

<span data-ttu-id="9e33a-135">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="9e33a-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9e33a-136">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9e33a-136">Shader Model</span></span>                                              | <span data-ttu-id="9e33a-137">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="9e33a-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9e33a-138">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9e33a-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9e33a-139">Oui</span><span class="sxs-lookup"><span data-stu-id="9e33a-139">yes</span></span>       |
| [<span data-ttu-id="9e33a-140">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="9e33a-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9e33a-141">non</span><span class="sxs-lookup"><span data-stu-id="9e33a-141">no</span></span>        |
| [<span data-ttu-id="9e33a-142">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="9e33a-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9e33a-143">non</span><span class="sxs-lookup"><span data-stu-id="9e33a-143">no</span></span>        |
| [<span data-ttu-id="9e33a-144">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e33a-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9e33a-145">non</span><span class="sxs-lookup"><span data-stu-id="9e33a-145">no</span></span>        |
| [<span data-ttu-id="9e33a-146">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e33a-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9e33a-147">non</span><span class="sxs-lookup"><span data-stu-id="9e33a-147">no</span></span>        |
| [<span data-ttu-id="9e33a-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e33a-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9e33a-149">non</span><span class="sxs-lookup"><span data-stu-id="9e33a-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9e33a-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e33a-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e33a-151">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9e33a-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





