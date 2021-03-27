---
title: journalisation-vs
description: Full Precision log ₂ (x). | journalisation-vs
ms.assetid: 53c91825-ec54-4b04-bf08-52d4b1c5122d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9e0564ab5b38943017e61bde171d0db3060ca0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211524"
---
# <a name="log---vs"></a><span data-ttu-id="43298-104">journalisation-vs</span><span class="sxs-lookup"><span data-stu-id="43298-104">log - vs</span></span>

<span data-ttu-id="43298-105">Full Precision log ₂ (x).</span><span class="sxs-lookup"><span data-stu-id="43298-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="43298-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43298-106">Syntax</span></span>



| <span data-ttu-id="43298-107">DST du journal, SRC</span><span class="sxs-lookup"><span data-stu-id="43298-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="43298-108">where</span><span class="sxs-lookup"><span data-stu-id="43298-108">where</span></span>

-   <span data-ttu-id="43298-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="43298-109">dst is the destination register.</span></span>
-   <span data-ttu-id="43298-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="43298-110">src is a source register.</span></span> <span data-ttu-id="43298-111">Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="43298-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="43298-112">Notes</span><span class="sxs-lookup"><span data-stu-id="43298-112">Remarks</span></span>



| <span data-ttu-id="43298-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="43298-113">Vertex shader versions</span></span> | <span data-ttu-id="43298-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="43298-114">1\_1</span></span> | <span data-ttu-id="43298-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="43298-115">2\_0</span></span> | <span data-ttu-id="43298-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="43298-116">2\_x</span></span> | <span data-ttu-id="43298-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="43298-117">2\_sw</span></span> | <span data-ttu-id="43298-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="43298-118">3\_0</span></span> | <span data-ttu-id="43298-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="43298-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="43298-120">journal</span><span class="sxs-lookup"><span data-stu-id="43298-120">log</span></span>                    | <span data-ttu-id="43298-121">x</span><span class="sxs-lookup"><span data-stu-id="43298-121">x</span></span>    | <span data-ttu-id="43298-122">x</span><span class="sxs-lookup"><span data-stu-id="43298-122">x</span></span>    | <span data-ttu-id="43298-123">x</span><span class="sxs-lookup"><span data-stu-id="43298-123">x</span></span>    | <span data-ttu-id="43298-124">x</span><span class="sxs-lookup"><span data-stu-id="43298-124">x</span></span>     | <span data-ttu-id="43298-125">x</span><span class="sxs-lookup"><span data-stu-id="43298-125">x</span></span>    | <span data-ttu-id="43298-126">x</span><span class="sxs-lookup"><span data-stu-id="43298-126">x</span></span>     |



 

<span data-ttu-id="43298-127">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="43298-127">The following code fragment shows the operations performed.</span></span>


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



<span data-ttu-id="43298-128">Cette instruction accepte une source scalaire dont le bit de signe est ignoré.</span><span class="sxs-lookup"><span data-stu-id="43298-128">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="43298-129">Le résultat est répliqué sur les quatre canaux.</span><span class="sxs-lookup"><span data-stu-id="43298-129">The result is replicated to all four channels.</span></span>

<span data-ttu-id="43298-130">Cette instruction fournit 21 bits de précision.</span><span class="sxs-lookup"><span data-stu-id="43298-130">This instruction provides 21 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43298-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="43298-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43298-132">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="43298-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




