---
title: ushr (SM4-ASM)
description: Déplacer vers la droite. | ushr (SM4-ASM)
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c48b706afb1223a5289f93b5ca393a89c36e915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211420"
---
# <a name="ushr-sm4---asm"></a><span data-ttu-id="3a70f-104">ushr (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3a70f-104">ushr (sm4 - asm)</span></span>

<span data-ttu-id="3a70f-105">Déplacer vers la droite.</span><span class="sxs-lookup"><span data-stu-id="3a70f-105">Shift right.</span></span>



| <span data-ttu-id="3a70f-106">ushr dest \[ . Mask \] , src0 \[ . Swizzle \] , src1. Select, \_ composant</span><span class="sxs-lookup"><span data-stu-id="3a70f-106">ushr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="3a70f-107">Élément</span><span class="sxs-lookup"><span data-stu-id="3a70f-107">Item</span></span>                                                            | <span data-ttu-id="3a70f-108">Description</span><span class="sxs-lookup"><span data-stu-id="3a70f-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3a70f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3a70f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3a70f-110">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3a70f-110">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="3a70f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3a70f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3a70f-112">\[dans \] les composants à décaler.</span><span class="sxs-lookup"><span data-stu-id="3a70f-112">\[in\] The components to shift.</span></span><br/>                    |
| <span data-ttu-id="3a70f-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="3a70f-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="3a70f-114">\[dans \] la quantité de décalage de *src0*.</span><span class="sxs-lookup"><span data-stu-id="3a70f-114">\[in\] The amount to shift *src0*.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="3a70f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3a70f-115">Remarks</span></span>

<span data-ttu-id="3a70f-116">Cette instruction effectue un décalage au niveau du composant de chaque valeur 32 bits dans *src0* avec un nombre de bits entier non signé fourni par LSB 5 bits (plage 0-31) dans *src1. Sélectionnez le \_ composant*, en insérant 0.</span><span class="sxs-lookup"><span data-stu-id="3a70f-116">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, inserting 0.</span></span> <span data-ttu-id="3a70f-117">Le résultat 32 bits par composant est placé dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="3a70f-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="3a70f-118">Le nombre est une valeur scalaire appliquée à tous les composants.</span><span class="sxs-lookup"><span data-stu-id="3a70f-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="3a70f-119">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="3a70f-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3a70f-120">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="3a70f-120">Vertex Shader</span></span> | <span data-ttu-id="3a70f-121">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="3a70f-121">Geometry Shader</span></span> | <span data-ttu-id="3a70f-122">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="3a70f-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3a70f-123">x</span><span class="sxs-lookup"><span data-stu-id="3a70f-123">x</span></span>             | <span data-ttu-id="3a70f-124">x</span><span class="sxs-lookup"><span data-stu-id="3a70f-124">x</span></span>               | <span data-ttu-id="3a70f-125">x</span><span class="sxs-lookup"><span data-stu-id="3a70f-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3a70f-126">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3a70f-126">Minimum Shader Model</span></span>

<span data-ttu-id="3a70f-127">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="3a70f-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3a70f-128">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3a70f-128">Shader Model</span></span>                                              | <span data-ttu-id="3a70f-129">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3a70f-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3a70f-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3a70f-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3a70f-131">Oui</span><span class="sxs-lookup"><span data-stu-id="3a70f-131">yes</span></span>       |
| [<span data-ttu-id="3a70f-132">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="3a70f-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3a70f-133">Oui</span><span class="sxs-lookup"><span data-stu-id="3a70f-133">yes</span></span>       |
| [<span data-ttu-id="3a70f-134">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="3a70f-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3a70f-135">Oui</span><span class="sxs-lookup"><span data-stu-id="3a70f-135">yes</span></span>       |
| [<span data-ttu-id="3a70f-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a70f-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3a70f-137">non</span><span class="sxs-lookup"><span data-stu-id="3a70f-137">no</span></span>        |
| [<span data-ttu-id="3a70f-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a70f-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3a70f-139">non</span><span class="sxs-lookup"><span data-stu-id="3a70f-139">no</span></span>        |
| [<span data-ttu-id="3a70f-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a70f-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3a70f-141">non</span><span class="sxs-lookup"><span data-stu-id="3a70f-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3a70f-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a70f-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a70f-143">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3a70f-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





