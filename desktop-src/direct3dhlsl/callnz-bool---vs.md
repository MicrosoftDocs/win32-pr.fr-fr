---
title: callnz bool-vs
description: Appelez si la valeur n’est pas égale à zéro. Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette. | callnz bool-vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3932f4c5d50445b3220a0460a5c434a1ff8aae4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992113"
---
# <a name="callnz-bool---vs"></a><span data-ttu-id="ea3da-105">callnz bool-vs</span><span class="sxs-lookup"><span data-stu-id="ea3da-105">callnz bool - vs</span></span>

<span data-ttu-id="ea3da-106">Appelez si la valeur n’est pas égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ea3da-106">Call if not zero.</span></span> <span data-ttu-id="ea3da-107">Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="ea3da-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea3da-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea3da-108">Syntax</span></span>



| <span data-ttu-id="ea3da-109">callnz l \# , \[ ! \] p\#</span><span class="sxs-lookup"><span data-stu-id="ea3da-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="ea3da-110">où :</span><span class="sxs-lookup"><span data-stu-id="ea3da-110">where:</span></span>

-   <span data-ttu-id="ea3da-111">où l \# est une [étiquette, et](label---vs.md) qui marque le début de la sous-routine à appeler.</span><span class="sxs-lookup"><span data-stu-id="ea3da-111">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="ea3da-112">\[!\] est le modificateur Boolean facultatif facultatif.</span><span class="sxs-lookup"><span data-stu-id="ea3da-112">\[!\] is the optional boolean NOT modifier.</span></span>
-   <span data-ttu-id="ea3da-113">b \# identifie un [Registre booléen constant](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="ea3da-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea3da-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ea3da-114">Remarks</span></span>



| <span data-ttu-id="ea3da-115">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="ea3da-115">Vertex shader versions</span></span> | <span data-ttu-id="ea3da-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="ea3da-116">1\_1</span></span> | <span data-ttu-id="ea3da-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ea3da-117">2\_0</span></span> | <span data-ttu-id="ea3da-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ea3da-118">2\_x</span></span> | <span data-ttu-id="ea3da-119">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="ea3da-119">2\_sw</span></span> | <span data-ttu-id="ea3da-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ea3da-120">3\_0</span></span> | <span data-ttu-id="ea3da-121">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="ea3da-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="ea3da-122">callnz bool</span><span class="sxs-lookup"><span data-stu-id="ea3da-122">callnz bool</span></span>            |      | <span data-ttu-id="ea3da-123">x</span><span class="sxs-lookup"><span data-stu-id="ea3da-123">x</span></span>    | <span data-ttu-id="ea3da-124">x</span><span class="sxs-lookup"><span data-stu-id="ea3da-124">x</span></span>    | <span data-ttu-id="ea3da-125">x</span><span class="sxs-lookup"><span data-stu-id="ea3da-125">x</span></span>     | <span data-ttu-id="ea3da-126">x</span><span class="sxs-lookup"><span data-stu-id="ea3da-126">x</span></span>    | <span data-ttu-id="ea3da-127">x</span><span class="sxs-lookup"><span data-stu-id="ea3da-127">x</span></span>     |



 

<span data-ttu-id="ea3da-128">Cette instruction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea3da-128">This instruction does the following:</span></span>


```
if (specified boolean register is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="ea3da-129">Cette instruction consomme un emplacement d’instruction de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="ea3da-129">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea3da-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea3da-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea3da-131">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="ea3da-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




