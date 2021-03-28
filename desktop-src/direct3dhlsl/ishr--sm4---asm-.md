---
title: ISHR (SM4-ASM)
description: Décalage arithmétique vers la droite (extension de signe). | ISHR (SM4-ASM)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516543c5501ed886c5c1fa98d093062e3099a0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992093"
---
# <a name="ishr-sm4---asm"></a><span data-ttu-id="4beaf-104">ISHR (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4beaf-104">ishr (sm4 - asm)</span></span>

<span data-ttu-id="4beaf-105">Décalage arithmétique vers la droite (extension de signe).</span><span class="sxs-lookup"><span data-stu-id="4beaf-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="4beaf-106">ISHR dest \[ . Mask \] , src0 \[ . Swizzle \] , src1. Select, \_ composant</span><span class="sxs-lookup"><span data-stu-id="4beaf-106">ishr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="4beaf-107">Élément</span><span class="sxs-lookup"><span data-stu-id="4beaf-107">Item</span></span>                                                            | <span data-ttu-id="4beaf-108">Description</span><span class="sxs-lookup"><span data-stu-id="4beaf-108">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4beaf-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4beaf-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4beaf-110">\[dans \] contient le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="4beaf-110">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="4beaf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4beaf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4beaf-112">\[dans \] contient la valeur à décaler.</span><span class="sxs-lookup"><span data-stu-id="4beaf-112">\[in\] Contains the value to be shifted.</span></span><br/>     |
| <span data-ttu-id="4beaf-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="4beaf-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="4beaf-114">\[dans \] contient le nombre de décalages.</span><span class="sxs-lookup"><span data-stu-id="4beaf-114">\[in\] Contains the shift amount.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="4beaf-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4beaf-115">Remarks</span></span>

<span data-ttu-id="4beaf-116">Cette instruction effectue un décalage arithmétique au niveau du composant de chaque valeur 32 bits dans *src0* avec un nombre de bits entier non signé fourni par LSB 5 bits (plage 0-31) dans *src1. Sélectionnez le \_ composant*, en répliquant la valeur de bit 31.</span><span class="sxs-lookup"><span data-stu-id="4beaf-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, replicating the value of bit 31.</span></span> <span data-ttu-id="4beaf-117">Le résultat 32 bits par composant est placé dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="4beaf-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="4beaf-118">Le nombre est une valeur scalaire appliquée à tous les composants.</span><span class="sxs-lookup"><span data-stu-id="4beaf-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="4beaf-119">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="4beaf-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4beaf-120">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="4beaf-120">Vertex Shader</span></span> | <span data-ttu-id="4beaf-121">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="4beaf-121">Geometry Shader</span></span> | <span data-ttu-id="4beaf-122">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="4beaf-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4beaf-123">x</span><span class="sxs-lookup"><span data-stu-id="4beaf-123">x</span></span>             | <span data-ttu-id="4beaf-124">x</span><span class="sxs-lookup"><span data-stu-id="4beaf-124">x</span></span>               | <span data-ttu-id="4beaf-125">x</span><span class="sxs-lookup"><span data-stu-id="4beaf-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4beaf-126">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4beaf-126">Minimum Shader Model</span></span>

<span data-ttu-id="4beaf-127">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="4beaf-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4beaf-128">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4beaf-128">Shader Model</span></span>                                              | <span data-ttu-id="4beaf-129">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="4beaf-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4beaf-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4beaf-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4beaf-131">Oui</span><span class="sxs-lookup"><span data-stu-id="4beaf-131">yes</span></span>       |
| [<span data-ttu-id="4beaf-132">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="4beaf-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4beaf-133">Oui</span><span class="sxs-lookup"><span data-stu-id="4beaf-133">yes</span></span>       |
| [<span data-ttu-id="4beaf-134">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="4beaf-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4beaf-135">Oui</span><span class="sxs-lookup"><span data-stu-id="4beaf-135">yes</span></span>       |
| [<span data-ttu-id="4beaf-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4beaf-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4beaf-137">non</span><span class="sxs-lookup"><span data-stu-id="4beaf-137">no</span></span>        |
| [<span data-ttu-id="4beaf-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4beaf-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4beaf-139">non</span><span class="sxs-lookup"><span data-stu-id="4beaf-139">no</span></span>        |
| [<span data-ttu-id="4beaf-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4beaf-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4beaf-141">non</span><span class="sxs-lookup"><span data-stu-id="4beaf-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4beaf-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4beaf-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4beaf-143">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4beaf-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





