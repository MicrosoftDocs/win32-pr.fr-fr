---
title: Pow-PS
description: Src0 (Full Precision ABS) src1. | Pow-PS
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974007"
---
# <a name="pow---ps"></a><span data-ttu-id="0990f-104">Pow-PS</span><span class="sxs-lookup"><span data-stu-id="0990f-104">pow - ps</span></span>

<span data-ttu-id="0990f-105">Src0 (Full Precision ABS)<sup>src1</sup>.</span><span class="sxs-lookup"><span data-stu-id="0990f-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="0990f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0990f-106">Syntax</span></span>



| <span data-ttu-id="0990f-107">Pow DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="0990f-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="0990f-108">where</span><span class="sxs-lookup"><span data-stu-id="0990f-108">where</span></span>

-   <span data-ttu-id="0990f-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="0990f-109">dst is the destination register.</span></span>
-   <span data-ttu-id="0990f-110">src0 est un registre de la source d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0990f-110">src0 is an input source register.</span></span> <span data-ttu-id="0990f-111">Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="0990f-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="0990f-112">src1 est un registre de la source d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0990f-112">src1 is an input source register.</span></span> <span data-ttu-id="0990f-113">Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="0990f-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="0990f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0990f-114">Remarks</span></span>



| <span data-ttu-id="0990f-115">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0990f-115">Pixel shader versions</span></span> | <span data-ttu-id="0990f-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="0990f-116">1\_1</span></span> | <span data-ttu-id="0990f-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="0990f-117">1\_2</span></span> | <span data-ttu-id="0990f-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0990f-118">1\_3</span></span> | <span data-ttu-id="0990f-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="0990f-119">1\_4</span></span> | <span data-ttu-id="0990f-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0990f-120">2\_0</span></span> | <span data-ttu-id="0990f-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0990f-121">2\_x</span></span> | <span data-ttu-id="0990f-122">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="0990f-122">2\_sw</span></span> | <span data-ttu-id="0990f-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0990f-123">3\_0</span></span> | <span data-ttu-id="0990f-124">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="0990f-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0990f-125">pow</span><span class="sxs-lookup"><span data-stu-id="0990f-125">pow</span></span>                   |      |      |      |      | <span data-ttu-id="0990f-126">x</span><span class="sxs-lookup"><span data-stu-id="0990f-126">x</span></span>    | <span data-ttu-id="0990f-127">x</span><span class="sxs-lookup"><span data-stu-id="0990f-127">x</span></span>    | <span data-ttu-id="0990f-128">x</span><span class="sxs-lookup"><span data-stu-id="0990f-128">x</span></span>     | <span data-ttu-id="0990f-129">x</span><span class="sxs-lookup"><span data-stu-id="0990f-129">x</span></span>    | <span data-ttu-id="0990f-130">x</span><span class="sxs-lookup"><span data-stu-id="0990f-130">x</span></span>     |



 

<span data-ttu-id="0990f-131">Cette instruction fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="0990f-131">This instruction works as follows:</span></span>

<span data-ttu-id="0990f-132">dest. x = dest. y = dest. z = dest. w = \[ ABS (src0) \] <sup>src1</sup>;</span><span class="sxs-lookup"><span data-stu-id="0990f-132">dest.x = dest.y = dest.z = dest.w = \[abs(src0)\]<sup>src1</sup>;</span></span>

<span data-ttu-id="0990f-133">Il s’agit d’une instruction scalaire. par conséquent, les registres source doivent avoir répliqué Swizzles pour indiquer les canaux qui sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="0990f-133">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="0990f-134">La puissance d’entrée (src1) doit être une scalaire.</span><span class="sxs-lookup"><span data-stu-id="0990f-134">The input power (src1) must be a scalar.</span></span>

<span data-ttu-id="0990f-135">Le résultat scalaire est répliqué sur les quatre canaux de sortie.</span><span class="sxs-lookup"><span data-stu-id="0990f-135">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="0990f-136">Cette instruction peut être développée en tant que exp (src1 \* log (src0)).</span><span class="sxs-lookup"><span data-stu-id="0990f-136">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="0990f-137">Le registre de l’heure d’été doit être un registre temporaire et ne doit pas être le même que src1.</span><span class="sxs-lookup"><span data-stu-id="0990f-137">The dst register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0990f-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0990f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0990f-139">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0990f-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




