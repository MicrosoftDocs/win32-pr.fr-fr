---
title: ubfe (SM5-ASM)
description: À partir d’une plage de bits dans un nombre, décalez ces bits vers le LSB et définissez les bits restants sur 0.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841657"
---
# <a name="ubfe-sm5---asm"></a><span data-ttu-id="ac18f-103">ubfe (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ac18f-103">ubfe (sm5 - asm)</span></span>

<span data-ttu-id="ac18f-104">À partir d’une plage de bits dans un nombre, décalez ces bits vers le LSB et définissez les bits restants sur 0.</span><span class="sxs-lookup"><span data-stu-id="ac18f-104">Given a range of bits in a number, shift those bits to the LSB and set remaining bits to 0.</span></span>



| <span data-ttu-id="ac18f-105">ubfe dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle \] , src2 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ac18f-105">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="ac18f-106">Élément</span><span class="sxs-lookup"><span data-stu-id="ac18f-106">Item</span></span>                                                            | <span data-ttu-id="ac18f-107">Description</span><span class="sxs-lookup"><span data-stu-id="ac18f-107">Description</span></span>                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="ac18f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ac18f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ac18f-109">\[dans \] contient les résultats de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="ac18f-109">\[in\] Contains the results of the instruction.</span></span><br/>                     |
| <span data-ttu-id="ac18f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ac18f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ac18f-111">\[dans, \] LSB 5 bits fournissent la largeur de champ de bits (0-31).</span><span class="sxs-lookup"><span data-stu-id="ac18f-111">\[in\] The LSB 5 bits provide the bitfield width (0-31).</span></span><br/>            |
| <span data-ttu-id="ac18f-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ac18f-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="ac18f-113">\[dans, \] LSB 5 bits de *src1* fournissent l’offset de champ de bits (0-31).</span><span class="sxs-lookup"><span data-stu-id="ac18f-113">\[in\] The LSB 5 bits of *src1* provide the bitfield offset (0-31).</span></span><br/> |
| <span data-ttu-id="ac18f-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="ac18f-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="ac18f-115">\[dans \] le nombre à décaler.</span><span class="sxs-lookup"><span data-stu-id="ac18f-115">\[in\] The number to shift.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="ac18f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ac18f-116">Remarks</span></span>

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

<span data-ttu-id="ac18f-117">Utilisez cette instruction pour décompresser des entiers ou des indicateurs non signés.</span><span class="sxs-lookup"><span data-stu-id="ac18f-117">Use this instruction to unpack unsigned integers or flags.</span></span>

<span data-ttu-id="ac18f-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="ac18f-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ac18f-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="ac18f-119">Vertex</span></span> | <span data-ttu-id="ac18f-120">Forme</span><span class="sxs-lookup"><span data-stu-id="ac18f-120">Hull</span></span> | <span data-ttu-id="ac18f-121">Domain</span><span class="sxs-lookup"><span data-stu-id="ac18f-121">Domain</span></span> | <span data-ttu-id="ac18f-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="ac18f-122">Geometry</span></span> | <span data-ttu-id="ac18f-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="ac18f-123">Pixel</span></span> | <span data-ttu-id="ac18f-124">Compute</span><span class="sxs-lookup"><span data-stu-id="ac18f-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ac18f-125">X</span><span class="sxs-lookup"><span data-stu-id="ac18f-125">X</span></span>      | <span data-ttu-id="ac18f-126">X</span><span class="sxs-lookup"><span data-stu-id="ac18f-126">X</span></span>    | <span data-ttu-id="ac18f-127">X</span><span class="sxs-lookup"><span data-stu-id="ac18f-127">X</span></span>      | <span data-ttu-id="ac18f-128">X</span><span class="sxs-lookup"><span data-stu-id="ac18f-128">X</span></span>        | <span data-ttu-id="ac18f-129">X</span><span class="sxs-lookup"><span data-stu-id="ac18f-129">X</span></span>     | <span data-ttu-id="ac18f-130">X</span><span class="sxs-lookup"><span data-stu-id="ac18f-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ac18f-131">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="ac18f-131">Minimum Shader Model</span></span>

<span data-ttu-id="ac18f-132">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="ac18f-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ac18f-133">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="ac18f-133">Shader Model</span></span>                                              | <span data-ttu-id="ac18f-134">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="ac18f-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ac18f-135">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="ac18f-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ac18f-136">Oui</span><span class="sxs-lookup"><span data-stu-id="ac18f-136">yes</span></span>       |
| [<span data-ttu-id="ac18f-137">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="ac18f-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ac18f-138">non</span><span class="sxs-lookup"><span data-stu-id="ac18f-138">no</span></span>        |
| [<span data-ttu-id="ac18f-139">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="ac18f-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ac18f-140">non</span><span class="sxs-lookup"><span data-stu-id="ac18f-140">no</span></span>        |
| [<span data-ttu-id="ac18f-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac18f-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ac18f-142">non</span><span class="sxs-lookup"><span data-stu-id="ac18f-142">no</span></span>        |
| [<span data-ttu-id="ac18f-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac18f-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ac18f-144">non</span><span class="sxs-lookup"><span data-stu-id="ac18f-144">no</span></span>        |
| [<span data-ttu-id="ac18f-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac18f-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ac18f-146">non</span><span class="sxs-lookup"><span data-stu-id="ac18f-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ac18f-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ac18f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac18f-148">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac18f-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





