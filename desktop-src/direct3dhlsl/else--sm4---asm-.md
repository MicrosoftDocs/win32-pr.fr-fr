---
title: else (SM4-ASM)
description: Démarre un bloc Else.
ms.assetid: CFF25E78-D986-4EC5-B542-B3396EFF88E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e283a2621c916ac254daab9f055be0ffe1ba67d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971602"
---
# <a name="else-sm4---asm"></a><span data-ttu-id="945c1-103">else (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="945c1-103">else (sm4 - asm)</span></span>

<span data-ttu-id="945c1-104">Démarre un bloc **else** .</span><span class="sxs-lookup"><span data-stu-id="945c1-104">Starts an **else** block.</span></span>



| <span data-ttu-id="945c1-105">else</span><span class="sxs-lookup"><span data-stu-id="945c1-105">else</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="945c1-106">Notes</span><span class="sxs-lookup"><span data-stu-id="945c1-106">Remarks</span></span>

<span data-ttu-id="945c1-107">Le format de jeton contient le décalage de l’instruction [endif](endif--sm4---asm-.md) correspondante dans le nuanceur pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="945c1-107">The token format contains the offset of the corresponding [endif](endif--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="945c1-108">L’exemple suivant montre comment utiliser l’instruction **else** .</span><span class="sxs-lookup"><span data-stu-id="945c1-108">The following example shows how to use the **else** instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="945c1-109">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="945c1-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="945c1-110">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="945c1-110">Vertex Shader</span></span> | <span data-ttu-id="945c1-111">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="945c1-111">Geometry Shader</span></span> | <span data-ttu-id="945c1-112">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="945c1-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="945c1-113">x</span><span class="sxs-lookup"><span data-stu-id="945c1-113">x</span></span>             | <span data-ttu-id="945c1-114">x</span><span class="sxs-lookup"><span data-stu-id="945c1-114">x</span></span>               | <span data-ttu-id="945c1-115">x</span><span class="sxs-lookup"><span data-stu-id="945c1-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="945c1-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="945c1-116">Minimum Shader Model</span></span>

<span data-ttu-id="945c1-117">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="945c1-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="945c1-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="945c1-118">Shader Model</span></span>                                              | <span data-ttu-id="945c1-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="945c1-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="945c1-120">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="945c1-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="945c1-121">Oui</span><span class="sxs-lookup"><span data-stu-id="945c1-121">yes</span></span>       |
| [<span data-ttu-id="945c1-122">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="945c1-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="945c1-123">Oui</span><span class="sxs-lookup"><span data-stu-id="945c1-123">yes</span></span>       |
| [<span data-ttu-id="945c1-124">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="945c1-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="945c1-125">Oui</span><span class="sxs-lookup"><span data-stu-id="945c1-125">yes</span></span>       |
| [<span data-ttu-id="945c1-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="945c1-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="945c1-127">non</span><span class="sxs-lookup"><span data-stu-id="945c1-127">no</span></span>        |
| [<span data-ttu-id="945c1-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="945c1-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="945c1-129">non</span><span class="sxs-lookup"><span data-stu-id="945c1-129">no</span></span>        |
| [<span data-ttu-id="945c1-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="945c1-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="945c1-131">non</span><span class="sxs-lookup"><span data-stu-id="945c1-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="945c1-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="945c1-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="945c1-133">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="945c1-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




