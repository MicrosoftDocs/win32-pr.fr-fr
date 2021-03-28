---
title: exp-vs
description: Fournit une valeur double exponentielle de précision complète. | exp-vs
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5b49b69e1270075aef4368dedca5791c2784657
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992077"
---
# <a name="exp---vs"></a><span data-ttu-id="d7757-104">exp-vs</span><span class="sxs-lookup"><span data-stu-id="d7757-104">exp - vs</span></span>

<span data-ttu-id="d7757-105">Fournit une précision complète de 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="d7757-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7757-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7757-106">Syntax</span></span>



| <span data-ttu-id="d7757-107">exp heure d’été, SRC</span><span class="sxs-lookup"><span data-stu-id="d7757-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="d7757-108">where</span><span class="sxs-lookup"><span data-stu-id="d7757-108">where</span></span>

-   <span data-ttu-id="d7757-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="d7757-109">dst is the destination register.</span></span>
-   <span data-ttu-id="d7757-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="d7757-110">src is a source register.</span></span> <span data-ttu-id="d7757-111">Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="d7757-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="d7757-112">Consultez [Registre source Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="d7757-112">See [Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7757-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d7757-113">Remarks</span></span>



| <span data-ttu-id="d7757-114">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="d7757-114">Vertex shader versions</span></span> | <span data-ttu-id="d7757-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="d7757-115">1\_1</span></span> | <span data-ttu-id="d7757-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d7757-116">2\_0</span></span> | <span data-ttu-id="d7757-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d7757-117">2\_x</span></span> | <span data-ttu-id="d7757-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d7757-118">2\_sw</span></span> | <span data-ttu-id="d7757-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d7757-119">3\_0</span></span> | <span data-ttu-id="d7757-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d7757-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d7757-121">exp</span><span class="sxs-lookup"><span data-stu-id="d7757-121">exp</span></span>                    | <span data-ttu-id="d7757-122">x</span><span class="sxs-lookup"><span data-stu-id="d7757-122">x</span></span>    | <span data-ttu-id="d7757-123">x</span><span class="sxs-lookup"><span data-stu-id="d7757-123">x</span></span>    | <span data-ttu-id="d7757-124">x</span><span class="sxs-lookup"><span data-stu-id="d7757-124">x</span></span>    | <span data-ttu-id="d7757-125">x</span><span class="sxs-lookup"><span data-stu-id="d7757-125">x</span></span>     | <span data-ttu-id="d7757-126">x</span><span class="sxs-lookup"><span data-stu-id="d7757-126">x</span></span>    | <span data-ttu-id="d7757-127">x</span><span class="sxs-lookup"><span data-stu-id="d7757-127">x</span></span>     |



 

<span data-ttu-id="d7757-128">Cette instruction fournit au moins 21 bits de précision.</span><span class="sxs-lookup"><span data-stu-id="d7757-128">This instruction provides at least 21 bits of precision.</span></span>

<span data-ttu-id="d7757-129">Le fragment de code suivant montre les opérations effectuées :</span><span class="sxs-lookup"><span data-stu-id="d7757-129">The following code fragment shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="d7757-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d7757-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7757-131">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="d7757-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




