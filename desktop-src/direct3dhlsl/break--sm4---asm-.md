---
title: Break (SM4-ASM)
description: Déplace le point d’exécution vers l’instruction après le prochain ENDLOOP ou endswitch.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06396d062e9126091052126737e3e05c58dbdb16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313663"
---
# <a name="break-sm4---asm"></a><span data-ttu-id="96d1f-103">Break (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="96d1f-103">break (sm4 - asm)</span></span>

<span data-ttu-id="96d1f-104">Déplace le point d’exécution vers l’instruction après le prochain [ENDLOOP](endloop--sm4---asm-.md) ou [endswitch](endswitch--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="96d1f-104">Moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="96d1f-105">break</span><span class="sxs-lookup"><span data-stu-id="96d1f-105">break</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="96d1f-106">Notes</span><span class="sxs-lookup"><span data-stu-id="96d1f-106">Remarks</span></span>

<span data-ttu-id="96d1f-107">Le format de jeton contient le décalage de l’instruction **ENDLOOP** ou **endswitch** correspondante dans le nuanceur pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="96d1f-107">The token format contains the offset of the corresponding **endloop** or **endswitch** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="96d1f-108">L’exemple suivant illustre l’instruction **break** .</span><span class="sxs-lookup"><span data-stu-id="96d1f-108">The following example shows the **break** instruction.</span></span>


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



<span data-ttu-id="96d1f-109">Cette instruction doit apparaître dans une **boucle** / **ENDLOOP** ou dans un **cas** d’un **commutateur** / **endswitch**.</span><span class="sxs-lookup"><span data-stu-id="96d1f-109">This instruction must appear within a **loop**/**endloop** or in a **case** in a **switch**/**endswitch**.</span></span>

<span data-ttu-id="96d1f-110">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="96d1f-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="96d1f-111">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="96d1f-111">Vertex Shader</span></span> | <span data-ttu-id="96d1f-112">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="96d1f-112">Geometry Shader</span></span> | <span data-ttu-id="96d1f-113">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="96d1f-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="96d1f-114">x</span><span class="sxs-lookup"><span data-stu-id="96d1f-114">x</span></span>             | <span data-ttu-id="96d1f-115">x</span><span class="sxs-lookup"><span data-stu-id="96d1f-115">x</span></span>               | <span data-ttu-id="96d1f-116">x</span><span class="sxs-lookup"><span data-stu-id="96d1f-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="96d1f-117">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="96d1f-117">Minimum Shader Model</span></span>

<span data-ttu-id="96d1f-118">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="96d1f-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="96d1f-119">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="96d1f-119">Shader Model</span></span>                                              | <span data-ttu-id="96d1f-120">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="96d1f-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="96d1f-121">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="96d1f-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="96d1f-122">Oui</span><span class="sxs-lookup"><span data-stu-id="96d1f-122">yes</span></span>       |
| [<span data-ttu-id="96d1f-123">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="96d1f-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="96d1f-124">Oui</span><span class="sxs-lookup"><span data-stu-id="96d1f-124">yes</span></span>       |
| [<span data-ttu-id="96d1f-125">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="96d1f-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="96d1f-126">Oui</span><span class="sxs-lookup"><span data-stu-id="96d1f-126">yes</span></span>       |
| [<span data-ttu-id="96d1f-127">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96d1f-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="96d1f-128">non</span><span class="sxs-lookup"><span data-stu-id="96d1f-128">no</span></span>        |
| [<span data-ttu-id="96d1f-129">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96d1f-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="96d1f-130">non</span><span class="sxs-lookup"><span data-stu-id="96d1f-130">no</span></span>        |
| [<span data-ttu-id="96d1f-131">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96d1f-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="96d1f-132">non</span><span class="sxs-lookup"><span data-stu-id="96d1f-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="96d1f-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96d1f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96d1f-134">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96d1f-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




