---
title: utof (SM4-ASM)
description: Entier non signé pour la conversion à virgule flottante.
ms.assetid: 5A52C959-7B4C-4FA1-B29C-BCAF448419F8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9283857df12a85819f0d191d13450e0311fdade
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030614"
---
# <a name="utof-sm4---asm"></a><span data-ttu-id="e1fcc-103">utof (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e1fcc-103">utof (sm4 - asm)</span></span>

<span data-ttu-id="e1fcc-104">Entier non signé pour la conversion à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="e1fcc-104">Unsigned integer to floating point conversion.</span></span>



| <span data-ttu-id="e1fcc-105">utof dest \[ . Mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e1fcc-105">utof dest\[.mask\], src0\[.swizzle\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="e1fcc-106">Élément</span><span class="sxs-lookup"><span data-stu-id="e1fcc-106">Item</span></span>                                                            | <span data-ttu-id="e1fcc-107">Description</span><span class="sxs-lookup"><span data-stu-id="e1fcc-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e1fcc-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e1fcc-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e1fcc-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e1fcc-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="e1fcc-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e1fcc-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e1fcc-111">\[dans \] les composants à convertir.</span><span class="sxs-lookup"><span data-stu-id="e1fcc-111">\[in\] The components to convert.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e1fcc-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e1fcc-112">Remarks</span></span>

<span data-ttu-id="e1fcc-113">*src0* doit contenir un entier 4 tuples non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e1fcc-113">*src0* must contain an unsigned 32-bit integer 4-tuple.</span></span> <span data-ttu-id="e1fcc-114">Après l’exécution de l’instruction, *dest* contient un tuple à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="e1fcc-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span> <span data-ttu-id="e1fcc-115">La conversion est effectuée par composant.</span><span class="sxs-lookup"><span data-stu-id="e1fcc-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="e1fcc-116">Lorsqu’une valeur d’entrée d’entier est trop grande pour être représentée exactement au format à virgule flottante, arrondir au mode pair le plus proche.</span><span class="sxs-lookup"><span data-stu-id="e1fcc-116">When an integer input value is too large to be represented exactly in the floating point format, round to nearest even mode.</span></span>

<span data-ttu-id="e1fcc-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="e1fcc-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e1fcc-118">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="e1fcc-118">Vertex Shader</span></span> | <span data-ttu-id="e1fcc-119">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="e1fcc-119">Geometry Shader</span></span> | <span data-ttu-id="e1fcc-120">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="e1fcc-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e1fcc-121">x</span><span class="sxs-lookup"><span data-stu-id="e1fcc-121">x</span></span>             | <span data-ttu-id="e1fcc-122">x</span><span class="sxs-lookup"><span data-stu-id="e1fcc-122">x</span></span>               | <span data-ttu-id="e1fcc-123">x</span><span class="sxs-lookup"><span data-stu-id="e1fcc-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e1fcc-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="e1fcc-124">Minimum Shader Model</span></span>

<span data-ttu-id="e1fcc-125">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="e1fcc-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e1fcc-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="e1fcc-126">Shader Model</span></span>                                              | <span data-ttu-id="e1fcc-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="e1fcc-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e1fcc-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="e1fcc-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e1fcc-129">Oui</span><span class="sxs-lookup"><span data-stu-id="e1fcc-129">yes</span></span>       |
| [<span data-ttu-id="e1fcc-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="e1fcc-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e1fcc-131">Oui</span><span class="sxs-lookup"><span data-stu-id="e1fcc-131">yes</span></span>       |
| [<span data-ttu-id="e1fcc-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="e1fcc-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e1fcc-133">Oui</span><span class="sxs-lookup"><span data-stu-id="e1fcc-133">yes</span></span>       |
| [<span data-ttu-id="e1fcc-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1fcc-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e1fcc-135">non</span><span class="sxs-lookup"><span data-stu-id="e1fcc-135">no</span></span>        |
| [<span data-ttu-id="e1fcc-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1fcc-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e1fcc-137">non</span><span class="sxs-lookup"><span data-stu-id="e1fcc-137">no</span></span>        |
| [<span data-ttu-id="e1fcc-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1fcc-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e1fcc-139">non</span><span class="sxs-lookup"><span data-stu-id="e1fcc-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e1fcc-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1fcc-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1fcc-141">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1fcc-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





