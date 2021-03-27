---
title: itof (SM4-ASM)
description: Entier signé dans la conversion à virgule flottante.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d262f65801cd2caa0e6432b335ce32fff0d4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841669"
---
# <a name="itof-sm4---asm"></a><span data-ttu-id="9aff9-103">itof (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9aff9-103">itof (sm4 - asm)</span></span>

<span data-ttu-id="9aff9-104">Entier signé dans la conversion à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="9aff9-104">Signed integer to floating point conversion.</span></span>



| <span data-ttu-id="9aff9-105">itof dest \[ . Mask \] , \[ - \] src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9aff9-105">itof dest\[.mask\], \[-\]src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="9aff9-106">Élément</span><span class="sxs-lookup"><span data-stu-id="9aff9-106">Item</span></span>                                                            | <span data-ttu-id="9aff9-107">Description</span><span class="sxs-lookup"><span data-stu-id="9aff9-107">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9aff9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9aff9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9aff9-109">\[dans \] contient le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9aff9-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="9aff9-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9aff9-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9aff9-111">\[dans \] contient la valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="9aff9-111">\[in\] Contains the value to convert.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="9aff9-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9aff9-112">Remarks</span></span>

<span data-ttu-id="9aff9-113">Cette instruction de conversion de type entier à virgule flottante suppose que *src0* contient un entier 32 bits signé de 4 tuples.</span><span class="sxs-lookup"><span data-stu-id="9aff9-113">This signed integer-to-float conversion instruction assumes that *src0* contains a signed 32-bit integer 4-tuple.</span></span> <span data-ttu-id="9aff9-114">Après l’exécution de l’instruction, *dest* contient un tuple à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="9aff9-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span>

<span data-ttu-id="9aff9-115">La conversion est effectuée par composant.</span><span class="sxs-lookup"><span data-stu-id="9aff9-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="9aff9-116">Lorsqu’une valeur d’entrée d’entier est trop grande pour être représentée exactement au format à virgule flottante, l’arrondi au mode pair le plus proche est fortement recommandé, mais pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9aff9-116">When an integer input value is too large in magnitude to be represented exactly in the floating point format, rounding to nearest even mode is strongly recommended but not required.</span></span>

<span data-ttu-id="9aff9-117">Le modificateur de négation facultatif sur l’opérande source prend le complément à 2 avant d’effectuer une opération arithmétique.</span><span class="sxs-lookup"><span data-stu-id="9aff9-117">The optional negate modifier on source operand takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="9aff9-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="9aff9-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9aff9-119">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="9aff9-119">Vertex Shader</span></span> | <span data-ttu-id="9aff9-120">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="9aff9-120">Geometry Shader</span></span> | <span data-ttu-id="9aff9-121">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="9aff9-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9aff9-122">x</span><span class="sxs-lookup"><span data-stu-id="9aff9-122">x</span></span>             | <span data-ttu-id="9aff9-123">x</span><span class="sxs-lookup"><span data-stu-id="9aff9-123">x</span></span>               | <span data-ttu-id="9aff9-124">x</span><span class="sxs-lookup"><span data-stu-id="9aff9-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9aff9-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9aff9-125">Minimum Shader Model</span></span>

<span data-ttu-id="9aff9-126">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="9aff9-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9aff9-127">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9aff9-127">Shader Model</span></span>                                              | <span data-ttu-id="9aff9-128">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="9aff9-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9aff9-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9aff9-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9aff9-130">Oui</span><span class="sxs-lookup"><span data-stu-id="9aff9-130">yes</span></span>       |
| [<span data-ttu-id="9aff9-131">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="9aff9-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9aff9-132">Oui</span><span class="sxs-lookup"><span data-stu-id="9aff9-132">yes</span></span>       |
| [<span data-ttu-id="9aff9-133">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="9aff9-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9aff9-134">Oui</span><span class="sxs-lookup"><span data-stu-id="9aff9-134">yes</span></span>       |
| [<span data-ttu-id="9aff9-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9aff9-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9aff9-136">non</span><span class="sxs-lookup"><span data-stu-id="9aff9-136">no</span></span>        |
| [<span data-ttu-id="9aff9-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9aff9-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9aff9-138">non</span><span class="sxs-lookup"><span data-stu-id="9aff9-138">no</span></span>        |
| [<span data-ttu-id="9aff9-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9aff9-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9aff9-140">non</span><span class="sxs-lookup"><span data-stu-id="9aff9-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9aff9-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9aff9-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aff9-142">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9aff9-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





