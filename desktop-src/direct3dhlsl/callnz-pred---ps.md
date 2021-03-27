---
title: callnz prédit-PS
description: Appelez avec un prédicat, si différent de zéro. Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette. La prédicat utilise une valeur booléenne pour déterminer si l’instruction ne doit pas être exécutée.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a04bd4b1bfa16d965a90b66e3956674ecb112590
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940565"
---
# <a name="callnz-pred---ps"></a><span data-ttu-id="2d0ce-105">callnz prédit-PS</span><span class="sxs-lookup"><span data-stu-id="2d0ce-105">callnz pred - ps</span></span>

<span data-ttu-id="2d0ce-106">Appelez avec un prédicat, si différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="2d0ce-106">Call with a predicate, if not zero.</span></span> <span data-ttu-id="2d0ce-107">Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="2d0ce-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="2d0ce-108">La prédicat utilise une valeur booléenne pour déterminer si l’instruction ne doit pas être exécutée.</span><span class="sxs-lookup"><span data-stu-id="2d0ce-108">Predication uses a Boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d0ce-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d0ce-109">Syntax</span></span>



| <span data-ttu-id="2d0ce-110">callnz l \# , \[ ! \] P0. x</span><span class="sxs-lookup"><span data-stu-id="2d0ce-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="2d0ce-111">y</span><span class="sxs-lookup"><span data-stu-id="2d0ce-111">y\</span></span>|<span data-ttu-id="2d0ce-112">Lettre</span><span class="sxs-lookup"><span data-stu-id="2d0ce-112">z\</span></span>|<span data-ttu-id="2d0ce-113">s</span><span class="sxs-lookup"><span data-stu-id="2d0ce-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="2d0ce-114">Où :</span><span class="sxs-lookup"><span data-stu-id="2d0ce-114">Where:</span></span>

-   <span data-ttu-id="2d0ce-115">où l \# est une [étiquette-PS](label---ps.md) marque le début de la sous-routine à appeler.</span><span class="sxs-lookup"><span data-stu-id="2d0ce-115">where l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="2d0ce-116">\[!\] est un modificateur de négation facultatif.</span><span class="sxs-lookup"><span data-stu-id="2d0ce-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="2d0ce-117">P0 correspond au registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="2d0ce-117">p0 is the predicate register.</span></span> <span data-ttu-id="2d0ce-118">Consultez [Registre de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="2d0ce-118">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="2d0ce-119">{x \| y \| z \| w} est le Swizzle de réplication requis sur P0.</span><span class="sxs-lookup"><span data-stu-id="2d0ce-119">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d0ce-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2d0ce-120">Remarks</span></span>



| <span data-ttu-id="2d0ce-121">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="2d0ce-121">Pixel shader versions</span></span> | <span data-ttu-id="2d0ce-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="2d0ce-122">1\_1</span></span> | <span data-ttu-id="2d0ce-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="2d0ce-123">1\_2</span></span> | <span data-ttu-id="2d0ce-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2d0ce-124">1\_3</span></span> | <span data-ttu-id="2d0ce-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="2d0ce-125">1\_4</span></span> | <span data-ttu-id="2d0ce-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2d0ce-126">2\_0</span></span> | <span data-ttu-id="2d0ce-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2d0ce-127">2\_x</span></span> | <span data-ttu-id="2d0ce-128">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2d0ce-128">2\_sw</span></span> | <span data-ttu-id="2d0ce-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2d0ce-129">3\_0</span></span> | <span data-ttu-id="2d0ce-130">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2d0ce-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2d0ce-131">callnz prévu</span><span class="sxs-lookup"><span data-stu-id="2d0ce-131">callnz pred</span></span>           |      |      |      |      |      | <span data-ttu-id="2d0ce-132">x</span><span class="sxs-lookup"><span data-stu-id="2d0ce-132">x</span></span>    | <span data-ttu-id="2d0ce-133">x</span><span class="sxs-lookup"><span data-stu-id="2d0ce-133">x</span></span>     | <span data-ttu-id="2d0ce-134">x</span><span class="sxs-lookup"><span data-stu-id="2d0ce-134">x</span></span>    | <span data-ttu-id="2d0ce-135">x</span><span class="sxs-lookup"><span data-stu-id="2d0ce-135">x</span></span>     |



 

<span data-ttu-id="2d0ce-136">Cette instruction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2d0ce-136">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="2d0ce-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2d0ce-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d0ce-138">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="2d0ce-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




