---
title: callnz prédit-vs
description: Appelez si la valeur est différente de zéro, avec un prédicat. Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette. La prédicat utilise une valeur booléenne pour déterminer si l’instruction ne doit pas être exécutée.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3c3de590dfee56013c76402c840a959e8f9306c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030580"
---
# <a name="callnz-pred---vs"></a><span data-ttu-id="e131b-105">callnz prédit-vs</span><span class="sxs-lookup"><span data-stu-id="e131b-105">callnz pred - vs</span></span>

<span data-ttu-id="e131b-106">Appelez si la valeur est différente de zéro, avec un prédicat.</span><span class="sxs-lookup"><span data-stu-id="e131b-106">Call if not zero, with a predicate.</span></span> <span data-ttu-id="e131b-107">Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="e131b-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="e131b-108">La prédicat utilise une valeur booléenne pour déterminer si l’instruction ne doit pas être exécutée.</span><span class="sxs-lookup"><span data-stu-id="e131b-108">Predication uses a boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="e131b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e131b-109">Syntax</span></span>



| <span data-ttu-id="e131b-110">callnz l \# , \[ ! \] P0. x</span><span class="sxs-lookup"><span data-stu-id="e131b-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="e131b-111">y</span><span class="sxs-lookup"><span data-stu-id="e131b-111">y\</span></span>|<span data-ttu-id="e131b-112">Lettre</span><span class="sxs-lookup"><span data-stu-id="e131b-112">z\</span></span>|<span data-ttu-id="e131b-113">s</span><span class="sxs-lookup"><span data-stu-id="e131b-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="e131b-114">où :</span><span class="sxs-lookup"><span data-stu-id="e131b-114">where:</span></span>

-   <span data-ttu-id="e131b-115">l \# est une [étiquette, vs](label---vs.md) marquant le début de la sous-routine à appeler.</span><span class="sxs-lookup"><span data-stu-id="e131b-115">l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="e131b-116">\[!\] est un modificateur de négation facultatif.</span><span class="sxs-lookup"><span data-stu-id="e131b-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="e131b-117">P0 correspond au [Registre de prédicat](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="e131b-117">p0 is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="e131b-118">{x \| y \| z \| w} est le Swizzle de réplication requis sur P0.</span><span class="sxs-lookup"><span data-stu-id="e131b-118">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="e131b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e131b-119">Remarks</span></span>



| <span data-ttu-id="e131b-120">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="e131b-120">Vertex shader versions</span></span> | <span data-ttu-id="e131b-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="e131b-121">1\_1</span></span> | <span data-ttu-id="e131b-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e131b-122">2\_0</span></span> | <span data-ttu-id="e131b-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e131b-123">2\_x</span></span> | <span data-ttu-id="e131b-124">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e131b-124">2\_sw</span></span> | <span data-ttu-id="e131b-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e131b-125">3\_0</span></span> | <span data-ttu-id="e131b-126">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e131b-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e131b-127">callnz prévu</span><span class="sxs-lookup"><span data-stu-id="e131b-127">callnz pred</span></span>            |      |      | <span data-ttu-id="e131b-128">x</span><span class="sxs-lookup"><span data-stu-id="e131b-128">x</span></span>    | <span data-ttu-id="e131b-129">x</span><span class="sxs-lookup"><span data-stu-id="e131b-129">x</span></span>     | <span data-ttu-id="e131b-130">x</span><span class="sxs-lookup"><span data-stu-id="e131b-130">x</span></span>    | <span data-ttu-id="e131b-131">x</span><span class="sxs-lookup"><span data-stu-id="e131b-131">x</span></span>     |



 

<span data-ttu-id="e131b-132">Cette instruction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e131b-132">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="e131b-133">Cette instruction consomme un emplacement d’instruction de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="e131b-133">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e131b-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e131b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e131b-135">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="e131b-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




