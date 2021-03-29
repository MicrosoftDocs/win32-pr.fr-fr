---
title: ushr (SM5-ASM)
description: Déplacer vers la droite. | ushr (SM5-ASM)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33c627ec4aa985b5ac8a27cf0babd6219c9247c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974215"
---
# <a name="ushr-sm5---asm"></a><span data-ttu-id="c43e3-104">ushr (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c43e3-104">ushr (sm5 - asm)</span></span>

<span data-ttu-id="c43e3-105">Déplacer vers la droite.</span><span class="sxs-lookup"><span data-stu-id="c43e3-105">Shift right.</span></span>



| <span data-ttu-id="c43e3-106">ubfe dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c43e3-106">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="c43e3-107">Élément</span><span class="sxs-lookup"><span data-stu-id="c43e3-107">Item</span></span>                                                            | <span data-ttu-id="c43e3-108">Description</span><span class="sxs-lookup"><span data-stu-id="c43e3-108">Description</span></span>                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c43e3-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c43e3-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c43e3-110">\[dans \] contient les résultats de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="c43e3-110">\[in\] Contains the results of the instruction.</span></span><br/>                   |
| <span data-ttu-id="c43e3-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c43e3-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c43e3-112">\[dans \] les valeurs 32 bits à décaler.</span><span class="sxs-lookup"><span data-stu-id="c43e3-112">\[in\] The 32-bit values to shift.</span></span><br/>                                |
| <span data-ttu-id="c43e3-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c43e3-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c43e3-114">\[dans, \] les LSB 5 bits fournissent le nombre de bits à décaler (0-31).</span><span class="sxs-lookup"><span data-stu-id="c43e3-114">\[in\] The LSB 5 bits provide the number of bits to shift (0-31).</span></span><br/> |



 

<span data-ttu-id="c43e3-115">Cette instruction effectue un décalage au niveau du composant de chaque valeur 32 bits dans *src0* avec un nombre de bits entier non signé fourni par LSB 5 bits (plage 0-31) dans *src1*, en insérant 0.</span><span class="sxs-lookup"><span data-stu-id="c43e3-115">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="c43e3-116">Les résultats de 32 bits par composant sont placés dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="c43e3-116">The 32-bit per component results is placed in *dest*.</span></span>

<span data-ttu-id="c43e3-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="c43e3-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c43e3-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="c43e3-118">Vertex</span></span> | <span data-ttu-id="c43e3-119">Forme</span><span class="sxs-lookup"><span data-stu-id="c43e3-119">Hull</span></span> | <span data-ttu-id="c43e3-120">Domain</span><span class="sxs-lookup"><span data-stu-id="c43e3-120">Domain</span></span> | <span data-ttu-id="c43e3-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="c43e3-121">Geometry</span></span> | <span data-ttu-id="c43e3-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="c43e3-122">Pixel</span></span> | <span data-ttu-id="c43e3-123">Compute</span><span class="sxs-lookup"><span data-stu-id="c43e3-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c43e3-124">X</span><span class="sxs-lookup"><span data-stu-id="c43e3-124">X</span></span>      | <span data-ttu-id="c43e3-125">X</span><span class="sxs-lookup"><span data-stu-id="c43e3-125">X</span></span>    | <span data-ttu-id="c43e3-126">X</span><span class="sxs-lookup"><span data-stu-id="c43e3-126">X</span></span>      | <span data-ttu-id="c43e3-127">X</span><span class="sxs-lookup"><span data-stu-id="c43e3-127">X</span></span>        | <span data-ttu-id="c43e3-128">X</span><span class="sxs-lookup"><span data-stu-id="c43e3-128">X</span></span>     | <span data-ttu-id="c43e3-129">X</span><span class="sxs-lookup"><span data-stu-id="c43e3-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c43e3-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c43e3-130">Minimum Shader Model</span></span>

<span data-ttu-id="c43e3-131">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="c43e3-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c43e3-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c43e3-132">Shader Model</span></span>                                              | <span data-ttu-id="c43e3-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="c43e3-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c43e3-134">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="c43e3-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c43e3-135">Oui</span><span class="sxs-lookup"><span data-stu-id="c43e3-135">yes</span></span>       |
| [<span data-ttu-id="c43e3-136">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="c43e3-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c43e3-137">non</span><span class="sxs-lookup"><span data-stu-id="c43e3-137">no</span></span>        |
| [<span data-ttu-id="c43e3-138">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="c43e3-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c43e3-139">non</span><span class="sxs-lookup"><span data-stu-id="c43e3-139">no</span></span>        |
| [<span data-ttu-id="c43e3-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c43e3-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c43e3-141">non</span><span class="sxs-lookup"><span data-stu-id="c43e3-141">no</span></span>        |
| [<span data-ttu-id="c43e3-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c43e3-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c43e3-143">non</span><span class="sxs-lookup"><span data-stu-id="c43e3-143">no</span></span>        |
| [<span data-ttu-id="c43e3-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c43e3-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c43e3-145">non</span><span class="sxs-lookup"><span data-stu-id="c43e3-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c43e3-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c43e3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c43e3-147">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c43e3-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





