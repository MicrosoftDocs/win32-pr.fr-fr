---
title: ibfe (SM5-ASM)
description: À partir d’une plage de bits dans un nombre, décalez ces bits vers le LSB et signez étendre le MSB de la plage.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805d5c1137e25d8b8fa560588b9e876ccc5c8748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679113"
---
# <a name="ibfe-sm5---asm"></a><span data-ttu-id="9afad-103">ibfe (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9afad-103">ibfe (sm5 - asm)</span></span>

<span data-ttu-id="9afad-104">À partir d’une plage de bits dans un nombre, décalez ces bits vers le LSB et signez étendre le MSB de la plage.</span><span class="sxs-lookup"><span data-stu-id="9afad-104">Given a range of bits in a number, shift those bits to the LSB and sign extend the MSB of the range.</span></span>



| <span data-ttu-id="9afad-105">ibfe dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9afad-105">ibfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="9afad-106">Élément</span><span class="sxs-lookup"><span data-stu-id="9afad-106">Item</span></span>                                                            | <span data-ttu-id="9afad-107">Description</span><span class="sxs-lookup"><span data-stu-id="9afad-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9afad-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9afad-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9afad-109">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9afad-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="9afad-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9afad-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9afad-111">\[dans \] la largeur du champ de binaire.</span><span class="sxs-lookup"><span data-stu-id="9afad-111">\[in\] The bitfield width.</span></span><br/>                          |
| <span data-ttu-id="9afad-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="9afad-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="9afad-113">\[dans \] l’offset de champ de binaire.</span><span class="sxs-lookup"><span data-stu-id="9afad-113">\[in\] The bitfield offset.</span></span><br/>                         |
| <span data-ttu-id="9afad-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="9afad-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="9afad-115">\[dans \] la valeur à décaler.</span><span class="sxs-lookup"><span data-stu-id="9afad-115">\[in\] The value to shift.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="9afad-116">Notes</span><span class="sxs-lookup"><span data-stu-id="9afad-116">Remarks</span></span>

<span data-ttu-id="9afad-117">Les LSB 5 bits de src0 fournissent la largeur de champ de bits (0-31).</span><span class="sxs-lookup"><span data-stu-id="9afad-117">The LSB 5 bits of src0 provide the bitfield width (0-31).</span></span>

<span data-ttu-id="9afad-118">Les LSB 5 bits de src1 fournissent l’offset de champ de bits (0-31).</span><span class="sxs-lookup"><span data-stu-id="9afad-118">The LSB 5 bits of src1 provide the bitfield offset (0-31).</span></span>

<span data-ttu-id="9afad-119">L’exemple suivant montre comment utiliser cette instruction.</span><span class="sxs-lookup"><span data-stu-id="9afad-119">The following example shows how to use this instruction.</span></span>

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

<span data-ttu-id="9afad-120">Utilisez cette instruction pour décompresser des entiers ou des indicateurs signés.</span><span class="sxs-lookup"><span data-stu-id="9afad-120">Use this instruction to unpack signed integers or flags.</span></span>

<span data-ttu-id="9afad-121">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="9afad-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9afad-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="9afad-122">Vertex</span></span> | <span data-ttu-id="9afad-123">Forme</span><span class="sxs-lookup"><span data-stu-id="9afad-123">Hull</span></span> | <span data-ttu-id="9afad-124">Domain</span><span class="sxs-lookup"><span data-stu-id="9afad-124">Domain</span></span> | <span data-ttu-id="9afad-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="9afad-125">Geometry</span></span> | <span data-ttu-id="9afad-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="9afad-126">Pixel</span></span> | <span data-ttu-id="9afad-127">Compute</span><span class="sxs-lookup"><span data-stu-id="9afad-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9afad-128">X</span><span class="sxs-lookup"><span data-stu-id="9afad-128">X</span></span>      | <span data-ttu-id="9afad-129">X</span><span class="sxs-lookup"><span data-stu-id="9afad-129">X</span></span>    | <span data-ttu-id="9afad-130">X</span><span class="sxs-lookup"><span data-stu-id="9afad-130">X</span></span>      | <span data-ttu-id="9afad-131">X</span><span class="sxs-lookup"><span data-stu-id="9afad-131">X</span></span>        | <span data-ttu-id="9afad-132">X</span><span class="sxs-lookup"><span data-stu-id="9afad-132">X</span></span>     | <span data-ttu-id="9afad-133">X</span><span class="sxs-lookup"><span data-stu-id="9afad-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9afad-134">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9afad-134">Minimum Shader Model</span></span>

<span data-ttu-id="9afad-135">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="9afad-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9afad-136">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9afad-136">Shader Model</span></span>                                              | <span data-ttu-id="9afad-137">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="9afad-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9afad-138">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9afad-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9afad-139">Oui</span><span class="sxs-lookup"><span data-stu-id="9afad-139">yes</span></span>       |
| [<span data-ttu-id="9afad-140">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="9afad-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9afad-141">non</span><span class="sxs-lookup"><span data-stu-id="9afad-141">no</span></span>        |
| [<span data-ttu-id="9afad-142">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="9afad-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9afad-143">non</span><span class="sxs-lookup"><span data-stu-id="9afad-143">no</span></span>        |
| [<span data-ttu-id="9afad-144">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9afad-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9afad-145">non</span><span class="sxs-lookup"><span data-stu-id="9afad-145">no</span></span>        |
| [<span data-ttu-id="9afad-146">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9afad-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9afad-147">non</span><span class="sxs-lookup"><span data-stu-id="9afad-147">no</span></span>        |
| [<span data-ttu-id="9afad-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9afad-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9afad-149">non</span><span class="sxs-lookup"><span data-stu-id="9afad-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9afad-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9afad-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9afad-151">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9afad-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





