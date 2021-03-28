---
title: ineg (SM4-ASM)
description: complément à 2.
ms.assetid: 20C1EEC8-E349-4398-8EE3-EDD01EBCD4B1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4da3e0cbb08bee7bd732a4da8175705d1e1a0f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381199"
---
# <a name="ineg-sm4---asm"></a><span data-ttu-id="989fb-103">ineg (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="989fb-103">ineg (sm4 - asm)</span></span>

<span data-ttu-id="989fb-104">complément à 2.</span><span class="sxs-lookup"><span data-stu-id="989fb-104">2's complement.</span></span>



| <span data-ttu-id="989fb-105">ineg dest \[ . Mask \] , src0 \[ . Swizzle</span><span class="sxs-lookup"><span data-stu-id="989fb-105">ineg dest\[.mask\], src0\[.swizzle</span></span> |
|------------------------------------|



 



| <span data-ttu-id="989fb-106">Élément</span><span class="sxs-lookup"><span data-stu-id="989fb-106">Item</span></span>                                                            | <span data-ttu-id="989fb-107">Description</span><span class="sxs-lookup"><span data-stu-id="989fb-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="989fb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="989fb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="989fb-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="989fb-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="989fb-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="989fb-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="989fb-111">\[dans \] contient les valeurs de l’opération.</span><span class="sxs-lookup"><span data-stu-id="989fb-111">\[in\] Contains the values for the operation.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="989fb-112">Notes</span><span class="sxs-lookup"><span data-stu-id="989fb-112">Remarks</span></span>

<span data-ttu-id="989fb-113">Cette instruction effectue le complément composant-Wise 2 de chaque valeur 32 bits dans *src0*.</span><span class="sxs-lookup"><span data-stu-id="989fb-113">This instruction performs component-wise 2's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="989fb-114">Les résultats 32 bits sont stockés dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="989fb-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="989fb-115">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="989fb-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="989fb-116">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="989fb-116">Vertex Shader</span></span> | <span data-ttu-id="989fb-117">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="989fb-117">Geometry Shader</span></span> | <span data-ttu-id="989fb-118">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="989fb-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="989fb-119">x</span><span class="sxs-lookup"><span data-stu-id="989fb-119">x</span></span>             | <span data-ttu-id="989fb-120">x</span><span class="sxs-lookup"><span data-stu-id="989fb-120">x</span></span>               | <span data-ttu-id="989fb-121">x</span><span class="sxs-lookup"><span data-stu-id="989fb-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="989fb-122">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="989fb-122">Minimum Shader Model</span></span>

<span data-ttu-id="989fb-123">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="989fb-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="989fb-124">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="989fb-124">Shader Model</span></span>                                              | <span data-ttu-id="989fb-125">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="989fb-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="989fb-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="989fb-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="989fb-127">Oui</span><span class="sxs-lookup"><span data-stu-id="989fb-127">yes</span></span>       |
| [<span data-ttu-id="989fb-128">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="989fb-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="989fb-129">Oui</span><span class="sxs-lookup"><span data-stu-id="989fb-129">yes</span></span>       |
| [<span data-ttu-id="989fb-130">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="989fb-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="989fb-131">Oui</span><span class="sxs-lookup"><span data-stu-id="989fb-131">yes</span></span>       |
| [<span data-ttu-id="989fb-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="989fb-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="989fb-133">non</span><span class="sxs-lookup"><span data-stu-id="989fb-133">no</span></span>        |
| [<span data-ttu-id="989fb-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="989fb-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="989fb-135">non</span><span class="sxs-lookup"><span data-stu-id="989fb-135">no</span></span>        |
| [<span data-ttu-id="989fb-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="989fb-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="989fb-137">non</span><span class="sxs-lookup"><span data-stu-id="989fb-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="989fb-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="989fb-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="989fb-139">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="989fb-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





