---
title: ISHR (SM5-ASM)
description: Décalage arithmétique vers la droite (extension de signe). | ISHR (SM5-ASM)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df958b2e5c6e9cdd2a4dfb3d35c8112453ce9f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992092"
---
# <a name="ishr-sm5---asm"></a><span data-ttu-id="a66b4-104">ISHR (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a66b4-104">ishr (sm5 - asm)</span></span>

<span data-ttu-id="a66b4-105">Décalage arithmétique vers la droite (extension de signe).</span><span class="sxs-lookup"><span data-stu-id="a66b4-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="a66b4-106">ishl dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="a66b4-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="a66b4-107">Élément</span><span class="sxs-lookup"><span data-stu-id="a66b4-107">Item</span></span>                                                            | <span data-ttu-id="a66b4-108">Description</span><span class="sxs-lookup"><span data-stu-id="a66b4-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a66b4-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a66b4-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a66b4-110">\[dans \] contient les résultats de l’équipe de travail.</span><span class="sxs-lookup"><span data-stu-id="a66b4-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="a66b4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a66b4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a66b4-112">\[dans \] le nombre de bits à décaler.</span><span class="sxs-lookup"><span data-stu-id="a66b4-112">\[in\] The number of bits to shift.</span></span><br/>       |
| <span data-ttu-id="a66b4-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a66b4-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a66b4-114">\[dans \] les valeurs 32 bits à décaler.</span><span class="sxs-lookup"><span data-stu-id="a66b4-114">\[in\] The 32-bit values to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="a66b4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a66b4-115">Remarks</span></span>

<span data-ttu-id="a66b4-116">Cette instruction effectue un décalage arithmétique au niveau du composant de chaque valeur 32 bits dans *src0* avec un nombre de bits entier non signé fourni par LSB 5 bits (plage 0-31) dans *src1*, en répliquant la valeur de bit 31.</span><span class="sxs-lookup"><span data-stu-id="a66b4-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, replicating the value of bit 31.</span></span> <span data-ttu-id="a66b4-117">Le résultat 32 bits par composant est placé dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="a66b4-117">The 32-bit per component result is placed in *dest*.</span></span>

<span data-ttu-id="a66b4-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="a66b4-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a66b4-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="a66b4-119">Vertex</span></span> | <span data-ttu-id="a66b4-120">Forme</span><span class="sxs-lookup"><span data-stu-id="a66b4-120">Hull</span></span> | <span data-ttu-id="a66b4-121">Domain</span><span class="sxs-lookup"><span data-stu-id="a66b4-121">Domain</span></span> | <span data-ttu-id="a66b4-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="a66b4-122">Geometry</span></span> | <span data-ttu-id="a66b4-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="a66b4-123">Pixel</span></span> | <span data-ttu-id="a66b4-124">Compute</span><span class="sxs-lookup"><span data-stu-id="a66b4-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a66b4-125">X</span><span class="sxs-lookup"><span data-stu-id="a66b4-125">X</span></span>      | <span data-ttu-id="a66b4-126">X</span><span class="sxs-lookup"><span data-stu-id="a66b4-126">X</span></span>    | <span data-ttu-id="a66b4-127">X</span><span class="sxs-lookup"><span data-stu-id="a66b4-127">X</span></span>      | <span data-ttu-id="a66b4-128">X</span><span class="sxs-lookup"><span data-stu-id="a66b4-128">X</span></span>        | <span data-ttu-id="a66b4-129">X</span><span class="sxs-lookup"><span data-stu-id="a66b4-129">X</span></span>     | <span data-ttu-id="a66b4-130">X</span><span class="sxs-lookup"><span data-stu-id="a66b4-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a66b4-131">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="a66b4-131">Minimum Shader Model</span></span>

<span data-ttu-id="a66b4-132">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="a66b4-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a66b4-133">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a66b4-133">Shader Model</span></span>                                              | <span data-ttu-id="a66b4-134">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="a66b4-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a66b4-135">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="a66b4-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a66b4-136">Oui</span><span class="sxs-lookup"><span data-stu-id="a66b4-136">yes</span></span>       |
| [<span data-ttu-id="a66b4-137">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="a66b4-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a66b4-138">non</span><span class="sxs-lookup"><span data-stu-id="a66b4-138">no</span></span>        |
| [<span data-ttu-id="a66b4-139">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="a66b4-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a66b4-140">non</span><span class="sxs-lookup"><span data-stu-id="a66b4-140">no</span></span>        |
| [<span data-ttu-id="a66b4-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a66b4-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a66b4-142">non</span><span class="sxs-lookup"><span data-stu-id="a66b4-142">no</span></span>        |
| [<span data-ttu-id="a66b4-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a66b4-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a66b4-144">non</span><span class="sxs-lookup"><span data-stu-id="a66b4-144">no</span></span>        |
| [<span data-ttu-id="a66b4-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a66b4-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a66b4-146">non</span><span class="sxs-lookup"><span data-stu-id="a66b4-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a66b4-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a66b4-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a66b4-148">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a66b4-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





