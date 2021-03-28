---
title: emitThenCut (SM4-ASM)
description: Équivalent à une commande Emit suivie d’une commande Cut. | emitThenCut (SM4-ASM)
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5b413ca11e22c7cfc17691fc0a39fe96bf7c0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322521"
---
# <a name="emitthencut-sm4---asm"></a><span data-ttu-id="d5c6a-104">emitThenCut (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d5c6a-104">emitThenCut (sm4 - asm)</span></span>

<span data-ttu-id="d5c6a-105">Équivalent à une commande [Emit](emit--sm4---asm-.md) suivie d’une commande [Cut](cut--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="d5c6a-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="d5c6a-106">emitThenCut</span><span class="sxs-lookup"><span data-stu-id="d5c6a-106">emitThenCut</span></span> |
|-------------|



 

## <a name="remarks"></a><span data-ttu-id="d5c6a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d5c6a-107">Remarks</span></span>

<span data-ttu-id="d5c6a-108">Cette commande est utile lorsque vous ne connaissez pas le dernier vertex dans une topologie.</span><span class="sxs-lookup"><span data-stu-id="d5c6a-108">This command is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="d5c6a-109">Si des flux ont été déclarés, vous devez utiliser le [ \_ flux emitthencut](emitthencut-stream--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="d5c6a-109">If streams have been declared, you must use [emitthencut\_stream](emitthencut-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="d5c6a-110">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="d5c6a-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d5c6a-111">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="d5c6a-111">Vertex Shader</span></span> | <span data-ttu-id="d5c6a-112">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="d5c6a-112">Geometry Shader</span></span> | <span data-ttu-id="d5c6a-113">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d5c6a-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="d5c6a-114">x</span><span class="sxs-lookup"><span data-stu-id="d5c6a-114">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d5c6a-115">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d5c6a-115">Minimum Shader Model</span></span>

<span data-ttu-id="d5c6a-116">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d5c6a-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d5c6a-117">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d5c6a-117">Shader Model</span></span>                                              | <span data-ttu-id="d5c6a-118">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d5c6a-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d5c6a-119">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="d5c6a-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d5c6a-120">Oui</span><span class="sxs-lookup"><span data-stu-id="d5c6a-120">yes</span></span>       |
| [<span data-ttu-id="d5c6a-121">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="d5c6a-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d5c6a-122">Oui</span><span class="sxs-lookup"><span data-stu-id="d5c6a-122">yes</span></span>       |
| [<span data-ttu-id="d5c6a-123">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="d5c6a-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d5c6a-124">Oui</span><span class="sxs-lookup"><span data-stu-id="d5c6a-124">yes</span></span>       |
| [<span data-ttu-id="d5c6a-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5c6a-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d5c6a-126">non</span><span class="sxs-lookup"><span data-stu-id="d5c6a-126">no</span></span>        |
| [<span data-ttu-id="d5c6a-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5c6a-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d5c6a-128">non</span><span class="sxs-lookup"><span data-stu-id="d5c6a-128">no</span></span>        |
| [<span data-ttu-id="d5c6a-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5c6a-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d5c6a-130">non</span><span class="sxs-lookup"><span data-stu-id="d5c6a-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d5c6a-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5c6a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5c6a-132">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5c6a-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




