---
title: endif (SM4-ASM)
description: Met fin à une instruction if.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3fa6cf0efd395843212f6bacac478285e496c2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030552"
---
# <a name="endif-sm4---asm"></a><span data-ttu-id="929d8-103">endif (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="929d8-103">endif (sm4 - asm)</span></span>

<span data-ttu-id="929d8-104">Met fin à une instruction [If](if--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="929d8-104">Ends an [if](if--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="929d8-105">endif</span><span class="sxs-lookup"><span data-stu-id="929d8-105">endif</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="929d8-106">Notes</span><span class="sxs-lookup"><span data-stu-id="929d8-106">Remarks</span></span>

<span data-ttu-id="929d8-107">L’exemple suivant montre comment utiliser l’instruction ENDIF.</span><span class="sxs-lookup"><span data-stu-id="929d8-107">The following example shows how to use the endif instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="929d8-108">Le format de jeton contient le décalage de l’instruction **If** correspondante dans le nuanceur pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="929d8-108">The token format contains the offset of the corresponding **if** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="929d8-109">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="929d8-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="929d8-110">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="929d8-110">Vertex Shader</span></span> | <span data-ttu-id="929d8-111">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="929d8-111">Geometry Shader</span></span> | <span data-ttu-id="929d8-112">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="929d8-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="929d8-113">x</span><span class="sxs-lookup"><span data-stu-id="929d8-113">x</span></span>             | <span data-ttu-id="929d8-114">x</span><span class="sxs-lookup"><span data-stu-id="929d8-114">x</span></span>               | <span data-ttu-id="929d8-115">x</span><span class="sxs-lookup"><span data-stu-id="929d8-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="929d8-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="929d8-116">Minimum Shader Model</span></span>

<span data-ttu-id="929d8-117">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="929d8-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="929d8-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="929d8-118">Shader Model</span></span>                                              | <span data-ttu-id="929d8-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="929d8-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="929d8-120">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="929d8-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="929d8-121">Oui</span><span class="sxs-lookup"><span data-stu-id="929d8-121">yes</span></span>       |
| [<span data-ttu-id="929d8-122">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="929d8-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="929d8-123">Oui</span><span class="sxs-lookup"><span data-stu-id="929d8-123">yes</span></span>       |
| [<span data-ttu-id="929d8-124">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="929d8-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="929d8-125">Oui</span><span class="sxs-lookup"><span data-stu-id="929d8-125">yes</span></span>       |
| [<span data-ttu-id="929d8-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="929d8-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="929d8-127">non</span><span class="sxs-lookup"><span data-stu-id="929d8-127">no</span></span>        |
| [<span data-ttu-id="929d8-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="929d8-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="929d8-129">non</span><span class="sxs-lookup"><span data-stu-id="929d8-129">no</span></span>        |
| [<span data-ttu-id="929d8-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="929d8-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="929d8-131">non</span><span class="sxs-lookup"><span data-stu-id="929d8-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="929d8-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="929d8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="929d8-133">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="929d8-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




