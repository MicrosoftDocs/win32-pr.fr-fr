---
title: exp-PS
description: Fournit une valeur double exponentielle de précision complète. | exp-PS
ms.assetid: 09e4446f-4149-4ec8-b3e3-2045b55bd591
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acd7c50c1f0d6ff08ee5d66e50fdd3e56939f0d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043004"
---
# <a name="exp---ps"></a><span data-ttu-id="a07c2-104">exp-PS</span><span class="sxs-lookup"><span data-stu-id="a07c2-104">exp - ps</span></span>

<span data-ttu-id="a07c2-105">Fournit une précision complète de 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="a07c2-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="a07c2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a07c2-106">Syntax</span></span>



| <span data-ttu-id="a07c2-107">exp heure d’été, SRC</span><span class="sxs-lookup"><span data-stu-id="a07c2-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="a07c2-108">where</span><span class="sxs-lookup"><span data-stu-id="a07c2-108">where</span></span>

-   <span data-ttu-id="a07c2-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="a07c2-109">dst is the destination register.</span></span>
-   <span data-ttu-id="a07c2-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="a07c2-110">src is a source register.</span></span> <span data-ttu-id="a07c2-111">Le registre source nécessite l’utilisation explicite de Swizzle répliqués ; autrement dit, exactement l’un des composants. x,. y,. z et. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="a07c2-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="a07c2-112">Consultez [Registre source Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="a07c2-112">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a07c2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a07c2-113">Remarks</span></span>



| <span data-ttu-id="a07c2-114">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="a07c2-114">Pixel shader versions</span></span> | <span data-ttu-id="a07c2-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="a07c2-115">1\_1</span></span> | <span data-ttu-id="a07c2-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="a07c2-116">1\_2</span></span> | <span data-ttu-id="a07c2-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a07c2-117">1\_3</span></span> | <span data-ttu-id="a07c2-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="a07c2-118">1\_4</span></span> | <span data-ttu-id="a07c2-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a07c2-119">2\_0</span></span> | <span data-ttu-id="a07c2-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a07c2-120">2\_x</span></span> | <span data-ttu-id="a07c2-121">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="a07c2-121">2\_sw</span></span> | <span data-ttu-id="a07c2-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a07c2-122">3\_0</span></span> | <span data-ttu-id="a07c2-123">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="a07c2-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a07c2-124">exp</span><span class="sxs-lookup"><span data-stu-id="a07c2-124">exp</span></span>                   |      |      |      |      | <span data-ttu-id="a07c2-125">x</span><span class="sxs-lookup"><span data-stu-id="a07c2-125">x</span></span>    | <span data-ttu-id="a07c2-126">x</span><span class="sxs-lookup"><span data-stu-id="a07c2-126">x</span></span>    | <span data-ttu-id="a07c2-127">x</span><span class="sxs-lookup"><span data-stu-id="a07c2-127">x</span></span>     | <span data-ttu-id="a07c2-128">x</span><span class="sxs-lookup"><span data-stu-id="a07c2-128">x</span></span>    | <span data-ttu-id="a07c2-129">x</span><span class="sxs-lookup"><span data-stu-id="a07c2-129">x</span></span>     |



 

<span data-ttu-id="a07c2-130">L’extrait de code suivant montre les opérations effectuées :</span><span class="sxs-lookup"><span data-stu-id="a07c2-130">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="a07c2-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a07c2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a07c2-132">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="a07c2-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




