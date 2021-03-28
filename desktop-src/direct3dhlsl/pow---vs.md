---
title: Pow-vs
description: Src0 (Full Precision ABS) src1. | Pow-vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3263fa19015bc32c94ae714891c3bbb2128c9463
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211422"
---
# <a name="pow---vs"></a><span data-ttu-id="161ea-104">Pow-vs</span><span class="sxs-lookup"><span data-stu-id="161ea-104">pow - vs</span></span>

<span data-ttu-id="161ea-105">Src0 (Full Precision ABS)<sup>src1</sup>.</span><span class="sxs-lookup"><span data-stu-id="161ea-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="161ea-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="161ea-106">Syntax</span></span>



| <span data-ttu-id="161ea-107">Pow DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="161ea-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="161ea-108">where</span><span class="sxs-lookup"><span data-stu-id="161ea-108">where</span></span>

-   <span data-ttu-id="161ea-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="161ea-109">dst is the destination register.</span></span>
-   <span data-ttu-id="161ea-110">src0 est un registre de la source d’entrée.</span><span class="sxs-lookup"><span data-stu-id="161ea-110">src0 is an input source register.</span></span> <span data-ttu-id="161ea-111">Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="161ea-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="161ea-112">src1 est un registre de la source d’entrée.</span><span class="sxs-lookup"><span data-stu-id="161ea-112">src1 is an input source register.</span></span> <span data-ttu-id="161ea-113">Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="161ea-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="161ea-114">Notes</span><span class="sxs-lookup"><span data-stu-id="161ea-114">Remarks</span></span>



| <span data-ttu-id="161ea-115">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="161ea-115">Vertex shader versions</span></span> | <span data-ttu-id="161ea-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="161ea-116">1\_1</span></span> | <span data-ttu-id="161ea-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="161ea-117">2\_0</span></span> | <span data-ttu-id="161ea-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="161ea-118">2\_x</span></span> | <span data-ttu-id="161ea-119">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="161ea-119">2\_sw</span></span> | <span data-ttu-id="161ea-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="161ea-120">3\_0</span></span> | <span data-ttu-id="161ea-121">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="161ea-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="161ea-122">pow</span><span class="sxs-lookup"><span data-stu-id="161ea-122">pow</span></span>                    |      | <span data-ttu-id="161ea-123">x</span><span class="sxs-lookup"><span data-stu-id="161ea-123">x</span></span>    | <span data-ttu-id="161ea-124">x</span><span class="sxs-lookup"><span data-stu-id="161ea-124">x</span></span>    | <span data-ttu-id="161ea-125">x</span><span class="sxs-lookup"><span data-stu-id="161ea-125">x</span></span>     | <span data-ttu-id="161ea-126">x</span><span class="sxs-lookup"><span data-stu-id="161ea-126">x</span></span>    | <span data-ttu-id="161ea-127">x</span><span class="sxs-lookup"><span data-stu-id="161ea-127">x</span></span>     |



 

<span data-ttu-id="161ea-128">Cette instruction fonctionne comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="161ea-128">This instruction works as shown here.</span></span>


```
dest = pow(abs(src0), src1);
```



<span data-ttu-id="161ea-129">Il s’agit d’une instruction scalaire. par conséquent, les registres source doivent avoir répliqué Swizzles pour indiquer les canaux qui sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="161ea-129">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="161ea-130">Le résultat scalaire est répliqué sur les quatre canaux de sortie.</span><span class="sxs-lookup"><span data-stu-id="161ea-130">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="161ea-131">Cette instruction peut être développée en tant que exp (src1 \* log (src0)).</span><span class="sxs-lookup"><span data-stu-id="161ea-131">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="161ea-132">La précision n’est pas inférieure à 15 bits.</span><span class="sxs-lookup"><span data-stu-id="161ea-132">Precision is not lower than 15 bits.</span></span>

<span data-ttu-id="161ea-133">Le registre de dest doit être un registre temporaire et ne doit pas être le même que src1.</span><span class="sxs-lookup"><span data-stu-id="161ea-133">The dest register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="161ea-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="161ea-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="161ea-135">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="161ea-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




