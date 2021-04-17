---
title: continue (SM4-ASM)
description: Poursuit l’exécution au début de la boucle en cours.
ms.assetid: 3F0021B2-50D1-407C-9EE4-1CB679E184BF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53b023e998fcf131a387fc009cfc8cb133ff6a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990756"
---
# <a name="continue-sm4---asm"></a><span data-ttu-id="d966f-103">continue (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d966f-103">continue (sm4 - asm)</span></span>

<span data-ttu-id="d966f-104">Poursuit l’exécution au début de la boucle en cours.</span><span class="sxs-lookup"><span data-stu-id="d966f-104">Continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="d966f-105">continue</span><span class="sxs-lookup"><span data-stu-id="d966f-105">continue</span></span> |
|----------|



 

## <a name="remarks"></a><span data-ttu-id="d966f-106">Notes</span><span class="sxs-lookup"><span data-stu-id="d966f-106">Remarks</span></span>

<span data-ttu-id="d966f-107">**continue** ne peut être utilisé qu’à l’intérieur d’une [boucle](loop--sm4---asm-.md) ou d’un [ENDLOOP](endloop--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="d966f-107">**continue** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="d966f-108">L’exemple suivant montre comment utiliser l’instruction **continue** .</span><span class="sxs-lookup"><span data-stu-id="d966f-108">The following example shows how to use the **continue** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    if_z r1.x
                        ...
                        continue
                    endif
                    ...
                endloop
```



<span data-ttu-id="d966f-109">Le format de jeton contient le décalage de l’instruction de boucle correspondante dans le nuanceur pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="d966f-109">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="d966f-110">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="d966f-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d966f-111">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="d966f-111">Vertex Shader</span></span> | <span data-ttu-id="d966f-112">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="d966f-112">Geometry Shader</span></span> | <span data-ttu-id="d966f-113">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d966f-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d966f-114">x</span><span class="sxs-lookup"><span data-stu-id="d966f-114">x</span></span>             | <span data-ttu-id="d966f-115">x</span><span class="sxs-lookup"><span data-stu-id="d966f-115">x</span></span>               | <span data-ttu-id="d966f-116">x</span><span class="sxs-lookup"><span data-stu-id="d966f-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d966f-117">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d966f-117">Minimum Shader Model</span></span>

<span data-ttu-id="d966f-118">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d966f-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d966f-119">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d966f-119">Shader Model</span></span>                                              | <span data-ttu-id="d966f-120">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d966f-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d966f-121">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="d966f-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d966f-122">Oui</span><span class="sxs-lookup"><span data-stu-id="d966f-122">yes</span></span>       |
| [<span data-ttu-id="d966f-123">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="d966f-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d966f-124">Oui</span><span class="sxs-lookup"><span data-stu-id="d966f-124">yes</span></span>       |
| [<span data-ttu-id="d966f-125">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="d966f-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d966f-126">Oui</span><span class="sxs-lookup"><span data-stu-id="d966f-126">yes</span></span>       |
| [<span data-ttu-id="d966f-127">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d966f-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d966f-128">non</span><span class="sxs-lookup"><span data-stu-id="d966f-128">no</span></span>        |
| [<span data-ttu-id="d966f-129">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d966f-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d966f-130">non</span><span class="sxs-lookup"><span data-stu-id="d966f-130">no</span></span>        |
| [<span data-ttu-id="d966f-131">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d966f-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d966f-132">non</span><span class="sxs-lookup"><span data-stu-id="d966f-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d966f-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d966f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d966f-134">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d966f-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




