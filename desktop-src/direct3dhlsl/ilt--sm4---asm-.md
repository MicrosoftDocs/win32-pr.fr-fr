---
title: ILT (SM4-ASM)
description: Comparaison des entiers vectoriels au niveau du composant inférieur à.
ms.assetid: 5F06E568-6234-4778-8169-D8352FAB5297
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c2e5e47272412bb483e4782e9a6c35e971293c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313633"
---
# <a name="ilt-sm4---asm"></a><span data-ttu-id="01ae7-103">ILT (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="01ae7-103">ilt (sm4 - asm)</span></span>

<span data-ttu-id="01ae7-104">Comparaison des entiers vectoriels au niveau du composant inférieur à.</span><span class="sxs-lookup"><span data-stu-id="01ae7-104">Component-wise vector integer less-than comparison.</span></span>



| <span data-ttu-id="01ae7-105">ILT dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="01ae7-105">ilt dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="01ae7-106">Élément</span><span class="sxs-lookup"><span data-stu-id="01ae7-106">Item</span></span>                                                            | <span data-ttu-id="01ae7-107">Description</span><span class="sxs-lookup"><span data-stu-id="01ae7-107">Description</span></span>                                       |
|-----------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="01ae7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="01ae7-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="01ae7-109">Résultat de l'opération.</span><span class="sxs-lookup"><span data-stu-id="01ae7-109">The result of the operation.</span></span><br/>           |
| <span data-ttu-id="01ae7-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="01ae7-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="01ae7-111">\[dans \] la valeur à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="01ae7-111">\[in\] The value to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="01ae7-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="01ae7-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="01ae7-113">\[dans \] la valeur à comparer à *src0*.</span><span class="sxs-lookup"><span data-stu-id="01ae7-113">\[in\] The value to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="01ae7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="01ae7-114">Remarks</span></span>

<span data-ttu-id="01ae7-115">Effectue une comparaison d’entiers *(src0*  <  *src1*) pour chaque composant et écrit le résultat dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="01ae7-115">Performs the integer comparison *(src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="01ae7-116">Si la comparaison est true, 0xFFFFFFFF est retourné pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="01ae7-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="01ae7-117">Sinon, 0x0000000 est retourné.</span><span class="sxs-lookup"><span data-stu-id="01ae7-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="01ae7-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="01ae7-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="01ae7-119">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="01ae7-119">Vertex Shader</span></span> | <span data-ttu-id="01ae7-120">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="01ae7-120">Geometry Shader</span></span> | <span data-ttu-id="01ae7-121">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="01ae7-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="01ae7-122">x</span><span class="sxs-lookup"><span data-stu-id="01ae7-122">x</span></span>             | <span data-ttu-id="01ae7-123">x</span><span class="sxs-lookup"><span data-stu-id="01ae7-123">x</span></span>               | <span data-ttu-id="01ae7-124">x</span><span class="sxs-lookup"><span data-stu-id="01ae7-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="01ae7-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="01ae7-125">Minimum Shader Model</span></span>



| <span data-ttu-id="01ae7-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="01ae7-126">Shader Model</span></span>                                              | <span data-ttu-id="01ae7-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="01ae7-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="01ae7-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="01ae7-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="01ae7-129">Oui</span><span class="sxs-lookup"><span data-stu-id="01ae7-129">yes</span></span>       |
| [<span data-ttu-id="01ae7-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="01ae7-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="01ae7-131">Oui</span><span class="sxs-lookup"><span data-stu-id="01ae7-131">yes</span></span>       |
| [<span data-ttu-id="01ae7-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="01ae7-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="01ae7-133">Oui</span><span class="sxs-lookup"><span data-stu-id="01ae7-133">yes</span></span>       |
| [<span data-ttu-id="01ae7-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01ae7-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="01ae7-135">non</span><span class="sxs-lookup"><span data-stu-id="01ae7-135">no</span></span>        |
| [<span data-ttu-id="01ae7-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01ae7-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="01ae7-137">non</span><span class="sxs-lookup"><span data-stu-id="01ae7-137">no</span></span>        |
| [<span data-ttu-id="01ae7-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01ae7-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="01ae7-139">non</span><span class="sxs-lookup"><span data-stu-id="01ae7-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="01ae7-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01ae7-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01ae7-141">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="01ae7-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





