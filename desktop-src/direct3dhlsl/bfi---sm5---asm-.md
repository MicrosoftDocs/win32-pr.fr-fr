---
title: BFI (SM5-ASM)
description: En fonction d’une plage de bits du LSB d’un nombre, placez ce nombre de bits dans un autre nombre à tout décalage.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030594"
---
# <a name="bfi-sm5---asm"></a><span data-ttu-id="6f2da-103">BFI (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6f2da-103">bfi (sm5 - asm)</span></span>

<span data-ttu-id="6f2da-104">En fonction d’une plage de bits du LSB d’un nombre, placez ce nombre de bits dans un autre nombre à tout décalage.</span><span class="sxs-lookup"><span data-stu-id="6f2da-104">Given a bit range from the LSB of a number, place that number of bits in another number at any offset.</span></span>



| <span data-ttu-id="6f2da-105">BFI dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle \] , src3 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6f2da-105">bfi dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\], src3\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="6f2da-106">Élément</span><span class="sxs-lookup"><span data-stu-id="6f2da-106">Item</span></span>                                                            | <span data-ttu-id="6f2da-107">Description</span><span class="sxs-lookup"><span data-stu-id="6f2da-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="6f2da-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6f2da-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6f2da-109">\[dans \] l’adresse des résultats.</span><span class="sxs-lookup"><span data-stu-id="6f2da-109">\[in\] The address of the results.</span></span><br/>                       |
| <span data-ttu-id="6f2da-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6f2da-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6f2da-111">\[dans \] la largeur de champ de champ à prendre de *src2*.</span><span class="sxs-lookup"><span data-stu-id="6f2da-111">\[in\] The bitfield width to take from *src2*.</span></span><br/>           |
| <span data-ttu-id="6f2da-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="6f2da-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6f2da-113">\[dans \] l’offset de champ de bits pour le remplacement de bits dans *src3*.</span><span class="sxs-lookup"><span data-stu-id="6f2da-113">\[in\] The bitfield offset for replacing bits in *src3*.</span></span><br/> |
| <span data-ttu-id="6f2da-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="6f2da-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="6f2da-115">\[dans \] le numéro à partir duquel les bits sont extraits.</span><span class="sxs-lookup"><span data-stu-id="6f2da-115">\[in\] The number the bits are taken from.</span></span> <br/>              |
| <span data-ttu-id="6f2da-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span><span class="sxs-lookup"><span data-stu-id="6f2da-116"><span id="src3"></span><span id="SRC3"></span>*src3*</span></span><br/> | <span data-ttu-id="6f2da-117">\[dans \] le nombre avec bits à remplacer.</span><span class="sxs-lookup"><span data-stu-id="6f2da-117">\[in\] The number with bits to be replaced.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="6f2da-118">Notes</span><span class="sxs-lookup"><span data-stu-id="6f2da-118">Remarks</span></span>

<span data-ttu-id="6f2da-119">Les LSB 5 bits de *src0* fournissent la largeur de champ de bits (0-31) à prendre de *src2*.</span><span class="sxs-lookup"><span data-stu-id="6f2da-119">The LSB 5 bits of *src0* provide the bitfield width (0-31) to take from *src2*.</span></span>

<span data-ttu-id="6f2da-120">Les LSB 5 bits de *src1* fournissent l’offset de champ de bits (0-31) pour commencer à remplacer des bits dans le nombre lu à partir de *src3*.</span><span class="sxs-lookup"><span data-stu-id="6f2da-120">The LSB 5 bits of *src1* provide the bitfield offset (0-31) to start replacing bits in the number read from *src3*.</span></span>

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

<span data-ttu-id="6f2da-121">Cette instruction est utilisée pour compresser des entiers ou des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="6f2da-121">This instruction is used for packing integers or flags.</span></span>

<span data-ttu-id="6f2da-122">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="6f2da-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6f2da-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="6f2da-123">Vertex</span></span> | <span data-ttu-id="6f2da-124">Forme</span><span class="sxs-lookup"><span data-stu-id="6f2da-124">Hull</span></span> | <span data-ttu-id="6f2da-125">Domain</span><span class="sxs-lookup"><span data-stu-id="6f2da-125">Domain</span></span> | <span data-ttu-id="6f2da-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="6f2da-126">Geometry</span></span> | <span data-ttu-id="6f2da-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="6f2da-127">Pixel</span></span> | <span data-ttu-id="6f2da-128">Compute</span><span class="sxs-lookup"><span data-stu-id="6f2da-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6f2da-129">X</span><span class="sxs-lookup"><span data-stu-id="6f2da-129">X</span></span>      | <span data-ttu-id="6f2da-130">X</span><span class="sxs-lookup"><span data-stu-id="6f2da-130">X</span></span>    | <span data-ttu-id="6f2da-131">X</span><span class="sxs-lookup"><span data-stu-id="6f2da-131">X</span></span>      | <span data-ttu-id="6f2da-132">X</span><span class="sxs-lookup"><span data-stu-id="6f2da-132">X</span></span>        | <span data-ttu-id="6f2da-133">X</span><span class="sxs-lookup"><span data-stu-id="6f2da-133">X</span></span>     | <span data-ttu-id="6f2da-134">X</span><span class="sxs-lookup"><span data-stu-id="6f2da-134">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6f2da-135">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="6f2da-135">Minimum Shader Model</span></span>

<span data-ttu-id="6f2da-136">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="6f2da-136">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6f2da-137">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6f2da-137">Shader Model</span></span>                                              | <span data-ttu-id="6f2da-138">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="6f2da-138">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6f2da-139">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="6f2da-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6f2da-140">Oui</span><span class="sxs-lookup"><span data-stu-id="6f2da-140">yes</span></span>       |
| [<span data-ttu-id="6f2da-141">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="6f2da-141">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6f2da-142">non</span><span class="sxs-lookup"><span data-stu-id="6f2da-142">no</span></span>        |
| [<span data-ttu-id="6f2da-143">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="6f2da-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6f2da-144">non</span><span class="sxs-lookup"><span data-stu-id="6f2da-144">no</span></span>        |
| [<span data-ttu-id="6f2da-145">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f2da-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6f2da-146">non</span><span class="sxs-lookup"><span data-stu-id="6f2da-146">no</span></span>        |
| [<span data-ttu-id="6f2da-147">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f2da-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6f2da-148">non</span><span class="sxs-lookup"><span data-stu-id="6f2da-148">no</span></span>        |
| [<span data-ttu-id="6f2da-149">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f2da-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6f2da-150">non</span><span class="sxs-lookup"><span data-stu-id="6f2da-150">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6f2da-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f2da-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f2da-152">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6f2da-152">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





