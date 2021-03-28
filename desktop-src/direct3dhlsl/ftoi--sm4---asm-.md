---
title: 'ftoi (sm4 - asm) '
description: Conversion d’un entier à virgule flottante en valeur signée.
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "104316668"
---
# <a name="ftoi-sm4---asm"></a><span data-ttu-id="5a473-103">ftoi (sm4 - asm) </span><span class="sxs-lookup"><span data-stu-id="5a473-103">ftoi (sm4 - asm)</span></span>

<span data-ttu-id="5a473-104">Conversion d’un entier à virgule flottante en valeur signée.</span><span class="sxs-lookup"><span data-stu-id="5a473-104">Floating point to signed integer conversion.</span></span>

| <span data-ttu-id="5a473-105">ftoi dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5a473-105">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-|

| <span data-ttu-id="5a473-106">Élément</span><span class="sxs-lookup"><span data-stu-id="5a473-106">Item</span></span> | <span data-ttu-id="5a473-107">Description</span><span class="sxs-lookup"><span data-stu-id="5a473-107">Description</span></span> |
|-|-|
| <span data-ttu-id="5a473-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5a473-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5a473-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5a473-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="5a473-110">*dest*  =  . [rond \_ z](round-z--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="5a473-110">*dest* = [round\_z](round-z--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="5a473-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5a473-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5a473-112">\[dans \] le composant à convertir.</span><span class="sxs-lookup"><span data-stu-id="5a473-112">\[in\] The component to convert.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="5a473-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5a473-113">Remarks</span></span>

<span data-ttu-id="5a473-114">La conversion est effectuée par composant.</span><span class="sxs-lookup"><span data-stu-id="5a473-114">The conversion is performed per component.</span></span> <span data-ttu-id="5a473-115">L’arrondi est toujours effectué vers zéro, suivant la Convention C pour les conversions de float en int. Les applications qui requièrent une sémantique d’arrondi différente peuvent appeler les instructions **Round** avant d’effectuer un cast en Integer.</span><span class="sxs-lookup"><span data-stu-id="5a473-115">Rounding is always performed towards zero, following the C convention for casts from float to int. Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="5a473-116">Les entrées sont ancrées dans la plage \[ 2147483648.999 f... 2147483647.999 f \] avant la conversion, et les valeurs NaN d’entrée produisent un résultat zéro.</span><span class="sxs-lookup"><span data-stu-id="5a473-116">Inputs are clamped to the range \[-2147483648.999f ... 2147483647.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="5a473-117">Les modificateurs de valeur absolue et de négation facultatifs sont appliqués aux valeurs sources avant la conversion.</span><span class="sxs-lookup"><span data-stu-id="5a473-117">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="5a473-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="5a473-118">This instruction applies to the following shader stages:</span></span>

| <span data-ttu-id="5a473-119">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="5a473-119">Vertex Shader</span></span> | <span data-ttu-id="5a473-120">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="5a473-120">Geometry Shader</span></span> | <span data-ttu-id="5a473-121">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5a473-121">Pixel Shader</span></span> |
|-|-|-|
| <span data-ttu-id="5a473-122">x</span><span class="sxs-lookup"><span data-stu-id="5a473-122">x</span></span> | <span data-ttu-id="5a473-123">x</span><span class="sxs-lookup"><span data-stu-id="5a473-123">x</span></span> | <span data-ttu-id="5a473-124">x</span><span class="sxs-lookup"><span data-stu-id="5a473-124">x</span></span> |

## <a name="minimum-shader-model"></a><span data-ttu-id="5a473-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5a473-125">Minimum Shader Model</span></span>

<span data-ttu-id="5a473-126">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5a473-126">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="5a473-127">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5a473-127">Shader Model</span></span> | <span data-ttu-id="5a473-128">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5a473-128">Supported</span></span> |
|-|-|
| [<span data-ttu-id="5a473-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="5a473-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="5a473-130">Oui</span><span class="sxs-lookup"><span data-stu-id="5a473-130">yes</span></span> |
| [<span data-ttu-id="5a473-131">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="5a473-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="5a473-132">Oui</span><span class="sxs-lookup"><span data-stu-id="5a473-132">yes</span></span> |
| [<span data-ttu-id="5a473-133">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="5a473-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="5a473-134">Oui</span><span class="sxs-lookup"><span data-stu-id="5a473-134">yes</span></span> |
| [<span data-ttu-id="5a473-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a473-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5a473-136">non</span><span class="sxs-lookup"><span data-stu-id="5a473-136">no</span></span> |
| [<span data-ttu-id="5a473-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a473-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5a473-138">non</span><span class="sxs-lookup"><span data-stu-id="5a473-138">no</span></span> |
| [<span data-ttu-id="5a473-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a473-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5a473-140">non</span><span class="sxs-lookup"><span data-stu-id="5a473-140">no</span></span> |

## <a name="related-topics"></a><span data-ttu-id="5a473-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a473-141">Related topics</span></span>

[<span data-ttu-id="5a473-142">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a473-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
