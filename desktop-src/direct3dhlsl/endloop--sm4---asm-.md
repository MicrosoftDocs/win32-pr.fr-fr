---
title: ENDLOOP (SM4-ASM)
description: Termine une instruction de boucle.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655fa6addd19a6ce9f6f6b20a2677ef43cb8b751
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381120"
---
# <a name="endloop-sm4---asm"></a><span data-ttu-id="5a472-103">ENDLOOP (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5a472-103">endloop (sm4 - asm)</span></span>

<span data-ttu-id="5a472-104">Termine une instruction de boucle.</span><span class="sxs-lookup"><span data-stu-id="5a472-104">Ends a loop statement.</span></span>



| <span data-ttu-id="5a472-105">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="5a472-105">endloop</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="5a472-106">Notes</span><span class="sxs-lookup"><span data-stu-id="5a472-106">Remarks</span></span>

<span data-ttu-id="5a472-107">L’exemple suivant montre comment utiliser cette instruction.</span><span class="sxs-lookup"><span data-stu-id="5a472-107">The following example shows how to use this instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="5a472-108">Le format de jeton contient le décalage de l’instruction de boucle correspondante dans le nuanceur pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="5a472-108">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="5a472-109">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="5a472-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5a472-110">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="5a472-110">Vertex Shader</span></span> | <span data-ttu-id="5a472-111">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="5a472-111">Geometry Shader</span></span> | <span data-ttu-id="5a472-112">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5a472-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5a472-113">x</span><span class="sxs-lookup"><span data-stu-id="5a472-113">x</span></span>             | <span data-ttu-id="5a472-114">x</span><span class="sxs-lookup"><span data-stu-id="5a472-114">x</span></span>               | <span data-ttu-id="5a472-115">x</span><span class="sxs-lookup"><span data-stu-id="5a472-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5a472-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5a472-116">Minimum Shader Model</span></span>

<span data-ttu-id="5a472-117">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5a472-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5a472-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5a472-118">Shader Model</span></span>                                              | <span data-ttu-id="5a472-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5a472-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5a472-120">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="5a472-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5a472-121">Oui</span><span class="sxs-lookup"><span data-stu-id="5a472-121">yes</span></span>       |
| [<span data-ttu-id="5a472-122">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="5a472-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5a472-123">Oui</span><span class="sxs-lookup"><span data-stu-id="5a472-123">yes</span></span>       |
| [<span data-ttu-id="5a472-124">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="5a472-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5a472-125">Oui</span><span class="sxs-lookup"><span data-stu-id="5a472-125">yes</span></span>       |
| [<span data-ttu-id="5a472-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a472-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5a472-127">non</span><span class="sxs-lookup"><span data-stu-id="5a472-127">no</span></span>        |
| [<span data-ttu-id="5a472-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a472-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5a472-129">non</span><span class="sxs-lookup"><span data-stu-id="5a472-129">no</span></span>        |
| [<span data-ttu-id="5a472-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a472-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5a472-131">non</span><span class="sxs-lookup"><span data-stu-id="5a472-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5a472-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a472-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a472-133">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a472-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




