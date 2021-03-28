---
title: Journal-PS
description: Full Precision log ₂ (x). | Journal-PS
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8face264d5221cf4b39f99260bec476ee5742f0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974387"
---
# <a name="log---ps"></a><span data-ttu-id="fa8d5-104">Journal-PS</span><span class="sxs-lookup"><span data-stu-id="fa8d5-104">log - ps</span></span>

<span data-ttu-id="fa8d5-105">Full Precision log ₂ (x).</span><span class="sxs-lookup"><span data-stu-id="fa8d5-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa8d5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa8d5-106">Syntax</span></span>



| <span data-ttu-id="fa8d5-107">DST du journal, SRC</span><span class="sxs-lookup"><span data-stu-id="fa8d5-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="fa8d5-108">where</span><span class="sxs-lookup"><span data-stu-id="fa8d5-108">where</span></span>

-   <span data-ttu-id="fa8d5-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-109">dst is the destination register.</span></span>
-   <span data-ttu-id="fa8d5-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-110">src is a source register.</span></span> <span data-ttu-id="fa8d5-111">Le registre source nécessite l’utilisation explicite de Swizzle répliqués ; autrement dit, exactement l’un des composants. x,. y,. z et. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa8d5-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fa8d5-112">Remarks</span></span>



| <span data-ttu-id="fa8d5-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="fa8d5-113">Pixel shader versions</span></span> | <span data-ttu-id="fa8d5-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="fa8d5-114">1\_1</span></span> | <span data-ttu-id="fa8d5-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="fa8d5-115">1\_2</span></span> | <span data-ttu-id="fa8d5-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="fa8d5-116">1\_3</span></span> | <span data-ttu-id="fa8d5-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="fa8d5-117">1\_4</span></span> | <span data-ttu-id="fa8d5-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fa8d5-118">2\_0</span></span> | <span data-ttu-id="fa8d5-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fa8d5-119">2\_x</span></span> | <span data-ttu-id="fa8d5-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="fa8d5-120">2\_sw</span></span> | <span data-ttu-id="fa8d5-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fa8d5-121">3\_0</span></span> | <span data-ttu-id="fa8d5-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="fa8d5-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="fa8d5-123">journal</span><span class="sxs-lookup"><span data-stu-id="fa8d5-123">log</span></span>                   |      |      |      |      | <span data-ttu-id="fa8d5-124">x</span><span class="sxs-lookup"><span data-stu-id="fa8d5-124">x</span></span>    | <span data-ttu-id="fa8d5-125">x</span><span class="sxs-lookup"><span data-stu-id="fa8d5-125">x</span></span>    | <span data-ttu-id="fa8d5-126">x</span><span class="sxs-lookup"><span data-stu-id="fa8d5-126">x</span></span>     | <span data-ttu-id="fa8d5-127">x</span><span class="sxs-lookup"><span data-stu-id="fa8d5-127">x</span></span>    | <span data-ttu-id="fa8d5-128">x</span><span class="sxs-lookup"><span data-stu-id="fa8d5-128">x</span></span>     |



 

<span data-ttu-id="fa8d5-129">L’extrait de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-129">The following code snippet shows the operations performed.</span></span>


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



<span data-ttu-id="fa8d5-130">Cette instruction accepte une source scalaire dont le bit de signe est ignoré.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-130">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="fa8d5-131">Le résultat est répliqué sur les quatre canaux.</span><span class="sxs-lookup"><span data-stu-id="fa8d5-131">The result is replicated to all four channels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa8d5-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa8d5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa8d5-133">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="fa8d5-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




