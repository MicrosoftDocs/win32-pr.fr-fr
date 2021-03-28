---
title: endswitch (SM4-ASM)
description: Termine une instruction switch.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523a4008ab976ee299758349d57c6e32a3f336b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381119"
---
# <a name="endswitch-sm4---asm"></a><span data-ttu-id="23ca4-103">endswitch (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="23ca4-103">endswitch (sm4 - asm)</span></span>

<span data-ttu-id="23ca4-104">Termine une instruction [switch](switch--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="23ca4-104">Ends a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="23ca4-105">endswitch</span><span class="sxs-lookup"><span data-stu-id="23ca4-105">endswitch</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="23ca4-106">Notes</span><span class="sxs-lookup"><span data-stu-id="23ca4-106">Remarks</span></span>

<span data-ttu-id="23ca4-107">Le format de jeton contient le décalage de l’instruction switch correspondante dans le nuanceur pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="23ca4-107">The token format contains the offset of the corresponding switch instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="23ca4-108">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="23ca4-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="23ca4-109">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="23ca4-109">Vertex Shader</span></span> | <span data-ttu-id="23ca4-110">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="23ca4-110">Geometry Shader</span></span> | <span data-ttu-id="23ca4-111">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="23ca4-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="23ca4-112">x</span><span class="sxs-lookup"><span data-stu-id="23ca4-112">x</span></span>             | <span data-ttu-id="23ca4-113">x</span><span class="sxs-lookup"><span data-stu-id="23ca4-113">x</span></span>               | <span data-ttu-id="23ca4-114">x</span><span class="sxs-lookup"><span data-stu-id="23ca4-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="23ca4-115">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="23ca4-115">Minimum Shader Model</span></span>

<span data-ttu-id="23ca4-116">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="23ca4-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="23ca4-117">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="23ca4-117">Shader Model</span></span>                                              | <span data-ttu-id="23ca4-118">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="23ca4-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="23ca4-119">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="23ca4-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="23ca4-120">Oui</span><span class="sxs-lookup"><span data-stu-id="23ca4-120">yes</span></span>       |
| [<span data-ttu-id="23ca4-121">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="23ca4-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="23ca4-122">Oui</span><span class="sxs-lookup"><span data-stu-id="23ca4-122">yes</span></span>       |
| [<span data-ttu-id="23ca4-123">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="23ca4-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="23ca4-124">Oui</span><span class="sxs-lookup"><span data-stu-id="23ca4-124">yes</span></span>       |
| [<span data-ttu-id="23ca4-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23ca4-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="23ca4-126">non</span><span class="sxs-lookup"><span data-stu-id="23ca4-126">no</span></span>        |
| [<span data-ttu-id="23ca4-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23ca4-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="23ca4-128">non</span><span class="sxs-lookup"><span data-stu-id="23ca4-128">no</span></span>        |
| [<span data-ttu-id="23ca4-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23ca4-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="23ca4-130">non</span><span class="sxs-lookup"><span data-stu-id="23ca4-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="23ca4-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23ca4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23ca4-132">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23ca4-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




