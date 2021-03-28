---
title: ishl (sm5 - asm)
description: Décalage vers la gauche. | ishl (SM5-ASM)
ms.assetid: 3EE669BA-252D-4617-85B0-AEBB7F7E4C5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230034e66ca9adfbd6c94cc99351b485c6577fdf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322226"
---
# <a name="ishl-sm5---asm"></a><span data-ttu-id="2a0be-104">ishl (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="2a0be-104">ishl (sm5 - asm)</span></span>

<span data-ttu-id="2a0be-105">Décalage vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="2a0be-105">Shift left.</span></span>



| <span data-ttu-id="2a0be-106">ishl dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2a0be-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="2a0be-107">Élément</span><span class="sxs-lookup"><span data-stu-id="2a0be-107">Item</span></span>                                                            | <span data-ttu-id="2a0be-108">Description</span><span class="sxs-lookup"><span data-stu-id="2a0be-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2a0be-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2a0be-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2a0be-110">\[dans \] contient les résultats de l’équipe de travail.</span><span class="sxs-lookup"><span data-stu-id="2a0be-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="2a0be-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2a0be-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2a0be-112">\[dans \] les valeurs 32 bits à décaler.</span><span class="sxs-lookup"><span data-stu-id="2a0be-112">\[in\] The 32-bit values to shift.</span></span><br/>       |
| <span data-ttu-id="2a0be-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="2a0be-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2a0be-114">\[dans \] le nombre de bits à décaler.</span><span class="sxs-lookup"><span data-stu-id="2a0be-114">\[in\] The number of bits to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="2a0be-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2a0be-115">Remarks</span></span>

<span data-ttu-id="2a0be-116">Cette instruction effectue un décalage au niveau du composant de chaque valeur 32 bits dans *src0* à gauche d’un nombre de bits entier non signé fourni par LSB 5 bits (plage 0-31) dans *src1*, en insérant 0.</span><span class="sxs-lookup"><span data-stu-id="2a0be-116">This instruction performs a component-wise shift of each 32-bit value in *src0* left by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="2a0be-117">Les résultats de 32 bits par composant sont placés dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="2a0be-117">The 32-bit per component results are placed in *dest*.</span></span>

<span data-ttu-id="2a0be-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="2a0be-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2a0be-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="2a0be-119">Vertex</span></span> | <span data-ttu-id="2a0be-120">Forme</span><span class="sxs-lookup"><span data-stu-id="2a0be-120">Hull</span></span> | <span data-ttu-id="2a0be-121">Domain</span><span class="sxs-lookup"><span data-stu-id="2a0be-121">Domain</span></span> | <span data-ttu-id="2a0be-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="2a0be-122">Geometry</span></span> | <span data-ttu-id="2a0be-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="2a0be-123">Pixel</span></span> | <span data-ttu-id="2a0be-124">Compute</span><span class="sxs-lookup"><span data-stu-id="2a0be-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2a0be-125">X</span><span class="sxs-lookup"><span data-stu-id="2a0be-125">X</span></span>      | <span data-ttu-id="2a0be-126">X</span><span class="sxs-lookup"><span data-stu-id="2a0be-126">X</span></span>    | <span data-ttu-id="2a0be-127">X</span><span class="sxs-lookup"><span data-stu-id="2a0be-127">X</span></span>      | <span data-ttu-id="2a0be-128">X</span><span class="sxs-lookup"><span data-stu-id="2a0be-128">X</span></span>        | <span data-ttu-id="2a0be-129">X</span><span class="sxs-lookup"><span data-stu-id="2a0be-129">X</span></span>     | <span data-ttu-id="2a0be-130">X</span><span class="sxs-lookup"><span data-stu-id="2a0be-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2a0be-131">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="2a0be-131">Minimum Shader Model</span></span>

<span data-ttu-id="2a0be-132">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="2a0be-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2a0be-133">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="2a0be-133">Shader Model</span></span>                                              | <span data-ttu-id="2a0be-134">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="2a0be-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2a0be-135">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="2a0be-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2a0be-136">Oui</span><span class="sxs-lookup"><span data-stu-id="2a0be-136">yes</span></span>       |
| [<span data-ttu-id="2a0be-137">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="2a0be-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2a0be-138">non</span><span class="sxs-lookup"><span data-stu-id="2a0be-138">no</span></span>        |
| [<span data-ttu-id="2a0be-139">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="2a0be-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2a0be-140">non</span><span class="sxs-lookup"><span data-stu-id="2a0be-140">no</span></span>        |
| [<span data-ttu-id="2a0be-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a0be-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2a0be-142">non</span><span class="sxs-lookup"><span data-stu-id="2a0be-142">no</span></span>        |
| [<span data-ttu-id="2a0be-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a0be-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2a0be-144">non</span><span class="sxs-lookup"><span data-stu-id="2a0be-144">no</span></span>        |
| [<span data-ttu-id="2a0be-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a0be-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2a0be-146">non</span><span class="sxs-lookup"><span data-stu-id="2a0be-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2a0be-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a0be-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a0be-148">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2a0be-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





