---
title: RET (SM4-ASM)
description: Instruction return.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d834cd9f32d6e38f40666ab235f705c0fc80513f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679121"
---
# <a name="ret-sm4---asm"></a><span data-ttu-id="1d1bf-103">RET (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1d1bf-103">ret (sm4 - asm)</span></span>

<span data-ttu-id="1d1bf-104">Instruction return.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-104">Return statement.</span></span>



| <span data-ttu-id="1d1bf-105">Av</span><span class="sxs-lookup"><span data-stu-id="1d1bf-105">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="1d1bf-106">Notes</span><span class="sxs-lookup"><span data-stu-id="1d1bf-106">Remarks</span></span>

<span data-ttu-id="1d1bf-107">Si, dans une sous-routine, retourne à l’instruction après l’appel.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-107">If within a subroutine, return to the instruction after the call.</span></span> <span data-ttu-id="1d1bf-108">Dans le cas contraire à l’intérieur d’une sous-routine, terminez l’exécution du programme.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-108">If not inside a subroutine, terminate program execution.</span></span>

<span data-ttu-id="1d1bf-109">L’exemple suivant montre comment utiliser cette instruction.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-109">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                ret
```

### <a name="restrictions"></a><span data-ttu-id="1d1bf-110">Restrictions</span><span class="sxs-lookup"><span data-stu-id="1d1bf-110">Restrictions</span></span>

-   <span data-ttu-id="1d1bf-111">**RET** peut apparaître n’importe où dans un programme, un nombre quelconque de fois.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-111">**ret** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="1d1bf-112">Si une instruction d' [étiquette](label--sm4---asm-.md) apparaît dans un nuanceur, elle doit être précédée d’une commande **RET** qui n’est imbriquée dans aucune instruction de contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-112">If a [label](label--sm4---asm-.md) instruction appears in a Shader, it must be preceded by a **ret** command that is not nested in any flow control statements.</span></span>
-   <span data-ttu-id="1d1bf-113">S’il existe des sous-routines dans un nuanceur, la dernière instruction du nuanceur doit être un **RET**.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-113">If there are subroutines in a Shader, the last instruction in the Shader must be a **ret**.</span></span>

<span data-ttu-id="1d1bf-114">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="1d1bf-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1d1bf-115">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="1d1bf-115">Vertex Shader</span></span> | <span data-ttu-id="1d1bf-116">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="1d1bf-116">Geometry Shader</span></span> | <span data-ttu-id="1d1bf-117">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="1d1bf-117">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1d1bf-118">x</span><span class="sxs-lookup"><span data-stu-id="1d1bf-118">x</span></span>             | <span data-ttu-id="1d1bf-119">x</span><span class="sxs-lookup"><span data-stu-id="1d1bf-119">x</span></span>               | <span data-ttu-id="1d1bf-120">x</span><span class="sxs-lookup"><span data-stu-id="1d1bf-120">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1d1bf-121">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="1d1bf-121">Minimum Shader Model</span></span>

<span data-ttu-id="1d1bf-122">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="1d1bf-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1d1bf-123">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1d1bf-123">Shader Model</span></span>                                              | <span data-ttu-id="1d1bf-124">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="1d1bf-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1d1bf-125">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1d1bf-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1d1bf-126">Oui</span><span class="sxs-lookup"><span data-stu-id="1d1bf-126">yes</span></span>       |
| [<span data-ttu-id="1d1bf-127">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="1d1bf-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1d1bf-128">Oui</span><span class="sxs-lookup"><span data-stu-id="1d1bf-128">yes</span></span>       |
| [<span data-ttu-id="1d1bf-129">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="1d1bf-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1d1bf-130">Oui</span><span class="sxs-lookup"><span data-stu-id="1d1bf-130">yes</span></span>       |
| [<span data-ttu-id="1d1bf-131">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d1bf-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1d1bf-132">non</span><span class="sxs-lookup"><span data-stu-id="1d1bf-132">no</span></span>        |
| [<span data-ttu-id="1d1bf-133">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d1bf-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1d1bf-134">non</span><span class="sxs-lookup"><span data-stu-id="1d1bf-134">no</span></span>        |
| [<span data-ttu-id="1d1bf-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d1bf-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1d1bf-136">non</span><span class="sxs-lookup"><span data-stu-id="1d1bf-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1d1bf-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d1bf-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d1bf-138">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d1bf-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




