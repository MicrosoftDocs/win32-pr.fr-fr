---
title: emitThenCut_stream (SM5-ASM)
description: Équivalent à une commande Emit suivie d’une commande Cut. | emitThenCut_stream (SM5-ASM)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae3129f2a3fb50664a5dbf070c7a1dae9bf5d6e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973978"
---
# <a name="emitthencut_stream-sm5---asm"></a><span data-ttu-id="4dff5-104">emitThenCut \_ Stream (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4dff5-104">emitThenCut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="4dff5-105">Équivalent à une commande [Emit](emit--sm4---asm-.md) suivie d’une commande [Cut](cut--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="4dff5-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="4dff5-106">emitThenCut \_ flux de streamIndex</span><span class="sxs-lookup"><span data-stu-id="4dff5-106">emitThenCut\_stream streamIndex</span></span> |
|---------------------------------|



 



| <span data-ttu-id="4dff5-107">Élément</span><span class="sxs-lookup"><span data-stu-id="4dff5-107">Item</span></span>                                                                                                               | <span data-ttu-id="4dff5-108">Description</span><span class="sxs-lookup"><span data-stu-id="4dff5-108">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="4dff5-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="4dff5-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="4dff5-110">\[dans \] l’index de flux.</span><span class="sxs-lookup"><span data-stu-id="4dff5-110">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4dff5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4dff5-111">Remarks</span></span>

<span data-ttu-id="4dff5-112">Cette opération est utile lorsque vous ne connaissez pas le dernier vertex dans une topologie.</span><span class="sxs-lookup"><span data-stu-id="4dff5-112">This operation is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="4dff5-113">Si les flux n’ont pas été déclarés, vous devez utiliser [emitThenCut](emitthencut--sm4---asm-.md) au lieu de **emitThenCut \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="4dff5-113">If streams have not been declared, then you must use [emitThenCut](emitthencut--sm4---asm-.md) instead of **emitThenCut\_stream**.</span></span>

<span data-ttu-id="4dff5-114">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="4dff5-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4dff5-115">Sommet</span><span class="sxs-lookup"><span data-stu-id="4dff5-115">Vertex</span></span> | <span data-ttu-id="4dff5-116">Forme</span><span class="sxs-lookup"><span data-stu-id="4dff5-116">Hull</span></span> | <span data-ttu-id="4dff5-117">Domain</span><span class="sxs-lookup"><span data-stu-id="4dff5-117">Domain</span></span> | <span data-ttu-id="4dff5-118">Géométrie</span><span class="sxs-lookup"><span data-stu-id="4dff5-118">Geometry</span></span> | <span data-ttu-id="4dff5-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="4dff5-119">Pixel</span></span> | <span data-ttu-id="4dff5-120">Compute</span><span class="sxs-lookup"><span data-stu-id="4dff5-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="4dff5-121">X</span><span class="sxs-lookup"><span data-stu-id="4dff5-121">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4dff5-122">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4dff5-122">Minimum Shader Model</span></span>

<span data-ttu-id="4dff5-123">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="4dff5-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4dff5-124">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4dff5-124">Shader Model</span></span>                                              | <span data-ttu-id="4dff5-125">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="4dff5-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4dff5-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4dff5-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4dff5-127">Oui</span><span class="sxs-lookup"><span data-stu-id="4dff5-127">yes</span></span>       |
| [<span data-ttu-id="4dff5-128">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="4dff5-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4dff5-129">non</span><span class="sxs-lookup"><span data-stu-id="4dff5-129">no</span></span>        |
| [<span data-ttu-id="4dff5-130">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="4dff5-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4dff5-131">non</span><span class="sxs-lookup"><span data-stu-id="4dff5-131">no</span></span>        |
| [<span data-ttu-id="4dff5-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4dff5-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4dff5-133">non</span><span class="sxs-lookup"><span data-stu-id="4dff5-133">no</span></span>        |
| [<span data-ttu-id="4dff5-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4dff5-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4dff5-135">non</span><span class="sxs-lookup"><span data-stu-id="4dff5-135">no</span></span>        |
| [<span data-ttu-id="4dff5-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4dff5-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4dff5-137">non</span><span class="sxs-lookup"><span data-stu-id="4dff5-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4dff5-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4dff5-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dff5-139">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4dff5-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





