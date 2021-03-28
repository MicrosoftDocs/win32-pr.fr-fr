---
title: logP-vs
description: Précision partielle logP ₂ (x).
ms.assetid: 8547ca8a-7bde-4e41-9e65-f7fcd65454c1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a261d63ad47dcf12728b8bcd0025ec578ede0b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030589"
---
# <a name="logp---vs"></a><span data-ttu-id="4af59-103">logP-vs</span><span class="sxs-lookup"><span data-stu-id="4af59-103">logp - vs</span></span>

<span data-ttu-id="4af59-104">Précision partielle logP ₂ (x).</span><span class="sxs-lookup"><span data-stu-id="4af59-104">Partial precision logp₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="4af59-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4af59-105">Syntax</span></span>



| <span data-ttu-id="4af59-106">logP DST, SRC</span><span class="sxs-lookup"><span data-stu-id="4af59-106">logp dst, src</span></span> |
|---------------|



 

<span data-ttu-id="4af59-107">where</span><span class="sxs-lookup"><span data-stu-id="4af59-107">where</span></span>

-   <span data-ttu-id="4af59-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="4af59-108">dst is the destination register.</span></span>
-   <span data-ttu-id="4af59-109">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="4af59-109">src is a source register.</span></span> <span data-ttu-id="4af59-110">Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="4af59-110">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="4af59-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4af59-111">Remarks</span></span>



| <span data-ttu-id="4af59-112">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="4af59-112">Vertex shader versions</span></span> | <span data-ttu-id="4af59-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="4af59-113">1\_1</span></span> | <span data-ttu-id="4af59-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4af59-114">2\_0</span></span> | <span data-ttu-id="4af59-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4af59-115">2\_x</span></span> | <span data-ttu-id="4af59-116">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="4af59-116">2\_sw</span></span> | <span data-ttu-id="4af59-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4af59-117">3\_0</span></span> | <span data-ttu-id="4af59-118">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="4af59-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4af59-119">logp</span><span class="sxs-lookup"><span data-stu-id="4af59-119">logp</span></span>                   | <span data-ttu-id="4af59-120">x</span><span class="sxs-lookup"><span data-stu-id="4af59-120">x</span></span>    | <span data-ttu-id="4af59-121">x</span><span class="sxs-lookup"><span data-stu-id="4af59-121">x</span></span>    | <span data-ttu-id="4af59-122">x</span><span class="sxs-lookup"><span data-stu-id="4af59-122">x</span></span>    | <span data-ttu-id="4af59-123">x</span><span class="sxs-lookup"><span data-stu-id="4af59-123">x</span></span>     | <span data-ttu-id="4af59-124">x</span><span class="sxs-lookup"><span data-stu-id="4af59-124">x</span></span>    | <span data-ttu-id="4af59-125">x</span><span class="sxs-lookup"><span data-stu-id="4af59-125">x</span></span>     |



 

<span data-ttu-id="4af59-126">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="4af59-126">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src);
if (f != 0)
    dest.x = dest.y = dest.z = dest.w = (float)(log(f)/log(2));
else
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;   
```



<span data-ttu-id="4af59-127">Cette instruction fournit un logarithme de base 2 de précision partielle, jusqu’à 10 bits.</span><span class="sxs-lookup"><span data-stu-id="4af59-127">This instruction provides logarithm base 2 partial precision, up to 10 bits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4af59-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4af59-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4af59-129">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="4af59-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




