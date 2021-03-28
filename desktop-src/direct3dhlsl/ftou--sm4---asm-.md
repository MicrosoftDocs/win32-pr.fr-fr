---
title: ftou (SM4-ASM)
description: Conversion d’un entier non signé en virgule flottante.
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313645"
---
# <a name="ftou-sm4---asm"></a><span data-ttu-id="9ff1b-103">ftou (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9ff1b-103">ftou (sm4 - asm)</span></span>

<span data-ttu-id="9ff1b-104">Conversion d’un entier non signé en virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-104">Floating point to unsigned integer conversion.</span></span>



| <span data-ttu-id="9ff1b-105">ftou dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9ff1b-105">ftou dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="9ff1b-106">ftoi dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9ff1b-106">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="9ff1b-107">Élément</span><span class="sxs-lookup"><span data-stu-id="9ff1b-107">Item</span></span>                                                            | <span data-ttu-id="9ff1b-108">Description</span><span class="sxs-lookup"><span data-stu-id="9ff1b-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9ff1b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9ff1b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9ff1b-110">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-110">\[in\] The address of the result of the operation.</span></span> <br/> |
| <span data-ttu-id="9ff1b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9ff1b-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9ff1b-112">\[dans \] la valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-112">\[in\] The value to convert.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="9ff1b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9ff1b-113">Remarks</span></span>

<span data-ttu-id="9ff1b-114">La conversion est effectuée par composant.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-114">The conversion is performed per-component.</span></span> <span data-ttu-id="9ff1b-115">L’arrondi est toujours effectué vers zéro, suivant la Convention C pour les conversions de float en int.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-115">Rounding is always performed towards zero, following the C convention for casts from float to int.</span></span>

<span data-ttu-id="9ff1b-116">Les applications qui requièrent une sémantique d’arrondi différente peuvent appeler les instructions **Round** avant d’effectuer un cast en Integer.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-116">Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="9ff1b-117">Les entrées sont ancrées à la plage \[ 0.0 f... 4294967295.999 f \] avant la conversion, et les valeurs NaN d’entrée produisent un résultat zéro.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-117">Inputs are clamped to the range \[0.0f ... 4294967295.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="9ff1b-118">Les modificateurs de valeur absolue et de négation facultatifs sont appliqués aux valeurs sources avant la conversion.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-118">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="9ff1b-119">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="9ff1b-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9ff1b-120">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="9ff1b-120">Vertex Shader</span></span> | <span data-ttu-id="9ff1b-121">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="9ff1b-121">Geometry Shader</span></span> | <span data-ttu-id="9ff1b-122">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="9ff1b-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9ff1b-123">x</span><span class="sxs-lookup"><span data-stu-id="9ff1b-123">x</span></span>             | <span data-ttu-id="9ff1b-124">x</span><span class="sxs-lookup"><span data-stu-id="9ff1b-124">x</span></span>               | <span data-ttu-id="9ff1b-125">x</span><span class="sxs-lookup"><span data-stu-id="9ff1b-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9ff1b-126">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9ff1b-126">Minimum Shader Model</span></span>

<span data-ttu-id="9ff1b-127">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9ff1b-128">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9ff1b-128">Shader Model</span></span>                                              | <span data-ttu-id="9ff1b-129">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="9ff1b-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9ff1b-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9ff1b-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9ff1b-131">Oui</span><span class="sxs-lookup"><span data-stu-id="9ff1b-131">yes</span></span>       |
| [<span data-ttu-id="9ff1b-132">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="9ff1b-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9ff1b-133">Oui</span><span class="sxs-lookup"><span data-stu-id="9ff1b-133">yes</span></span>       |
| [<span data-ttu-id="9ff1b-134">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="9ff1b-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9ff1b-135">Oui</span><span class="sxs-lookup"><span data-stu-id="9ff1b-135">yes</span></span>       |
| [<span data-ttu-id="9ff1b-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ff1b-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9ff1b-137">non</span><span class="sxs-lookup"><span data-stu-id="9ff1b-137">no</span></span>        |
| [<span data-ttu-id="9ff1b-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ff1b-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9ff1b-139">non</span><span class="sxs-lookup"><span data-stu-id="9ff1b-139">no</span></span>        |
| [<span data-ttu-id="9ff1b-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ff1b-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9ff1b-141">non</span><span class="sxs-lookup"><span data-stu-id="9ff1b-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9ff1b-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ff1b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ff1b-143">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ff1b-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





