---
title: ou (SM4-ASM)
description: Or au niveau du bit.
ms.assetid: BBC06F8C-4C86-4077-A1F9-383D6A8FBED3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62064189725b246cc48bbde03a9c094d13f8b9a0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990800"
---
# <a name="or-sm4---asm"></a><span data-ttu-id="76f62-103">ou (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="76f62-103">or (sm4 - asm)</span></span>

<span data-ttu-id="76f62-104">Or au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="76f62-104">Bitwise or.</span></span>



| <span data-ttu-id="76f62-105">ou dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="76f62-105">or dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------|



 



| <span data-ttu-id="76f62-106">Élément</span><span class="sxs-lookup"><span data-stu-id="76f62-106">Item</span></span>                                                            | <span data-ttu-id="76f62-107">Description</span><span class="sxs-lookup"><span data-stu-id="76f62-107">Description</span></span>                                         |
|-----------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="76f62-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="76f62-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="76f62-109">\[dans \] le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="76f62-109">\[in\] The result of the operation.</span></span><br/>      |
| <span data-ttu-id="76f62-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="76f62-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="76f62-111">\[dans \] les composants de ou avec *src1*.</span><span class="sxs-lookup"><span data-stu-id="76f62-111">\[in\] The components to OR with *src1*.</span></span><br/> |
| <span data-ttu-id="76f62-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="76f62-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="76f62-113">\[dans \] les composants de ou avec *src0*.</span><span class="sxs-lookup"><span data-stu-id="76f62-113">\[in\] The components to OR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="76f62-114">Notes</span><span class="sxs-lookup"><span data-stu-id="76f62-114">Remarks</span></span>

<span data-ttu-id="76f62-115">Cette instruction effectue une ou logique au niveau du composant de chaque paire de valeurs 32 bits à partir de *src0* et *src1*.</span><span class="sxs-lookup"><span data-stu-id="76f62-115">This instruction performs a component-wise logical OR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="76f62-116">Les résultats 32 bits sont placés dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="76f62-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="76f62-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="76f62-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="76f62-118">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="76f62-118">Vertex Shader</span></span> | <span data-ttu-id="76f62-119">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="76f62-119">Geometry Shader</span></span> | <span data-ttu-id="76f62-120">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="76f62-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="76f62-121">x</span><span class="sxs-lookup"><span data-stu-id="76f62-121">x</span></span>             | <span data-ttu-id="76f62-122">x</span><span class="sxs-lookup"><span data-stu-id="76f62-122">x</span></span>               | <span data-ttu-id="76f62-123">x</span><span class="sxs-lookup"><span data-stu-id="76f62-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="76f62-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="76f62-124">Minimum Shader Model</span></span>

<span data-ttu-id="76f62-125">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="76f62-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="76f62-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="76f62-126">Shader Model</span></span>                                              | <span data-ttu-id="76f62-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="76f62-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="76f62-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="76f62-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="76f62-129">Oui</span><span class="sxs-lookup"><span data-stu-id="76f62-129">yes</span></span>       |
| [<span data-ttu-id="76f62-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="76f62-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="76f62-131">Oui</span><span class="sxs-lookup"><span data-stu-id="76f62-131">yes</span></span>       |
| [<span data-ttu-id="76f62-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="76f62-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="76f62-133">Oui</span><span class="sxs-lookup"><span data-stu-id="76f62-133">yes</span></span>       |
| [<span data-ttu-id="76f62-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76f62-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="76f62-135">non</span><span class="sxs-lookup"><span data-stu-id="76f62-135">no</span></span>        |
| [<span data-ttu-id="76f62-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76f62-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="76f62-137">non</span><span class="sxs-lookup"><span data-stu-id="76f62-137">no</span></span>        |
| [<span data-ttu-id="76f62-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76f62-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="76f62-139">non</span><span class="sxs-lookup"><span data-stu-id="76f62-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="76f62-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76f62-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76f62-141">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76f62-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





