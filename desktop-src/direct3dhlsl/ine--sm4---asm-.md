---
title: igne (SM4-ASM)
description: Comparaison non égale des entiers vectoriels au niveau du composant.
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b74a68cf4b1b3c7473f8264e8b83910f4cb0677
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990808"
---
# <a name="ine-sm4---asm"></a><span data-ttu-id="0eef6-103">igne (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0eef6-103">ine (sm4 - asm)</span></span>

<span data-ttu-id="0eef6-104">Comparaison non égale des entiers vectoriels au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="0eef6-104">Component-wise vector integer not-equal comparison.</span></span>



| <span data-ttu-id="0eef6-105">igne dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0eef6-105">ine dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="0eef6-106">Élément</span><span class="sxs-lookup"><span data-stu-id="0eef6-106">Item</span></span>                                                            | <span data-ttu-id="0eef6-107">Description</span><span class="sxs-lookup"><span data-stu-id="0eef6-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0eef6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0eef6-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0eef6-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0eef6-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="0eef6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0eef6-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0eef6-111">\[dans \] contient la valeur à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="0eef6-111">\[in\] Contains the value to compare to *src1*.</span></span><br/>    |
| <span data-ttu-id="0eef6-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="0eef6-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="0eef6-113">\[dans \] contient la valeur à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="0eef6-113">\[in\] Contains the value to compare to *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="0eef6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0eef6-114">Remarks</span></span>

<span data-ttu-id="0eef6-115">Effectue une comparaison d’entiers (*src0* ! = *src1*) pour chaque composant et écrit le résultat dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="0eef6-115">Performs the integer comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="0eef6-116">Si la comparaison est true, 0xFFFFFFFF est retourné pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="0eef6-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="0eef6-117">Sinon, 0x0000000 est retourné</span><span class="sxs-lookup"><span data-stu-id="0eef6-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="0eef6-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="0eef6-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0eef6-119">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="0eef6-119">Vertex Shader</span></span> | <span data-ttu-id="0eef6-120">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="0eef6-120">Geometry Shader</span></span> | <span data-ttu-id="0eef6-121">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0eef6-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0eef6-122">x</span><span class="sxs-lookup"><span data-stu-id="0eef6-122">x</span></span>             | <span data-ttu-id="0eef6-123">x</span><span class="sxs-lookup"><span data-stu-id="0eef6-123">x</span></span>               | <span data-ttu-id="0eef6-124">x</span><span class="sxs-lookup"><span data-stu-id="0eef6-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0eef6-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0eef6-125">Minimum Shader Model</span></span>

<span data-ttu-id="0eef6-126">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="0eef6-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0eef6-127">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0eef6-127">Shader Model</span></span>                                              | <span data-ttu-id="0eef6-128">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0eef6-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0eef6-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="0eef6-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0eef6-130">Oui</span><span class="sxs-lookup"><span data-stu-id="0eef6-130">yes</span></span>       |
| [<span data-ttu-id="0eef6-131">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="0eef6-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0eef6-132">Oui</span><span class="sxs-lookup"><span data-stu-id="0eef6-132">yes</span></span>       |
| [<span data-ttu-id="0eef6-133">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="0eef6-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0eef6-134">Oui</span><span class="sxs-lookup"><span data-stu-id="0eef6-134">yes</span></span>       |
| [<span data-ttu-id="0eef6-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0eef6-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0eef6-136">non</span><span class="sxs-lookup"><span data-stu-id="0eef6-136">no</span></span>        |
| [<span data-ttu-id="0eef6-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0eef6-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0eef6-138">non</span><span class="sxs-lookup"><span data-stu-id="0eef6-138">no</span></span>        |
| [<span data-ttu-id="0eef6-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0eef6-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0eef6-140">non</span><span class="sxs-lookup"><span data-stu-id="0eef6-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0eef6-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0eef6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0eef6-142">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0eef6-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





