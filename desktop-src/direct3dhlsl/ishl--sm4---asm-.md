---
title: ishl (SM4-ASM)
description: Décalage vers la gauche. | ishl (SM4-ASM)
ms.assetid: FA0213B8-8A76-4916-8B2F-0983C404A838
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e14225f8c8b0e46cf0ba6eda61f96e4563a904e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992013"
---
# <a name="ishl-sm4---asm"></a><span data-ttu-id="573f1-104">ishl (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="573f1-104">ishl (sm4 - asm)</span></span>

<span data-ttu-id="573f1-105">Décalage vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="573f1-105">Shift left.</span></span>



| <span data-ttu-id="573f1-106">dest \[ . Mask \] , src0 \[ . Swizzle \] , src1. Select ( \_ composant)</span><span class="sxs-lookup"><span data-stu-id="573f1-106">dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="573f1-107">Élément</span><span class="sxs-lookup"><span data-stu-id="573f1-107">Item</span></span>                                                            | <span data-ttu-id="573f1-108">Description</span><span class="sxs-lookup"><span data-stu-id="573f1-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="573f1-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="573f1-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="573f1-110">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="573f1-110">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="573f1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="573f1-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="573f1-112">\[dans \] contient les valeurs à décaler.</span><span class="sxs-lookup"><span data-stu-id="573f1-112">\[in\] Contains the values to be shifted.</span></span><br/>          |
| <span data-ttu-id="573f1-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="573f1-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="573f1-114">\[dans \] contient le nombre de décalages.</span><span class="sxs-lookup"><span data-stu-id="573f1-114">\[in\] Contains the shift amount.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="573f1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="573f1-115">Remarks</span></span>

<span data-ttu-id="573f1-116">Cette instruction effectue un décalage au niveau du composant de chaque valeur 32 bits dans *src0* à gauche d’un nombre de bits entier non signé fourni par LSB 5 bits (plage 0-31) dans *src1. Sélectionnez le \_ composant*, en insérant 0.</span><span class="sxs-lookup"><span data-stu-id="573f1-116">This instruction performs a component-wise shift of each 32-bit value in *src0* left by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, inserting 0.</span></span> <span data-ttu-id="573f1-117">Les résultats de 32 bits par composant sont placés dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="573f1-117">The 32-bit per component results are placed in *dest*.</span></span> <span data-ttu-id="573f1-118">Le nombre est une valeur scalaire appliquée à tous les composants.</span><span class="sxs-lookup"><span data-stu-id="573f1-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="573f1-119">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="573f1-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="573f1-120">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="573f1-120">Vertex Shader</span></span> | <span data-ttu-id="573f1-121">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="573f1-121">Geometry Shader</span></span> | <span data-ttu-id="573f1-122">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="573f1-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="573f1-123">x</span><span class="sxs-lookup"><span data-stu-id="573f1-123">x</span></span>             | <span data-ttu-id="573f1-124">x</span><span class="sxs-lookup"><span data-stu-id="573f1-124">x</span></span>               | <span data-ttu-id="573f1-125">x</span><span class="sxs-lookup"><span data-stu-id="573f1-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="573f1-126">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="573f1-126">Minimum Shader Model</span></span>

<span data-ttu-id="573f1-127">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="573f1-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="573f1-128">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="573f1-128">Shader Model</span></span>                                              | <span data-ttu-id="573f1-129">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="573f1-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="573f1-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="573f1-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="573f1-131">Oui</span><span class="sxs-lookup"><span data-stu-id="573f1-131">yes</span></span>       |
| [<span data-ttu-id="573f1-132">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="573f1-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="573f1-133">Oui</span><span class="sxs-lookup"><span data-stu-id="573f1-133">yes</span></span>       |
| [<span data-ttu-id="573f1-134">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="573f1-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="573f1-135">Oui</span><span class="sxs-lookup"><span data-stu-id="573f1-135">yes</span></span>       |
| [<span data-ttu-id="573f1-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="573f1-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="573f1-137">non</span><span class="sxs-lookup"><span data-stu-id="573f1-137">no</span></span>        |
| [<span data-ttu-id="573f1-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="573f1-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="573f1-139">non</span><span class="sxs-lookup"><span data-stu-id="573f1-139">no</span></span>        |
| [<span data-ttu-id="573f1-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="573f1-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="573f1-141">non</span><span class="sxs-lookup"><span data-stu-id="573f1-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="573f1-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="573f1-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="573f1-143">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="573f1-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





