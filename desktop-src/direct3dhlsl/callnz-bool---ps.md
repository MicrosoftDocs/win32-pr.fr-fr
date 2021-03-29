---
title: callnz bool-PS
description: Appelez si la valeur n’est pas égale à zéro. Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette. | callnz bool-PS
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0516e62ce07c60866715591bc59123f38dc5c272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992116"
---
# <a name="callnz-bool---ps"></a><span data-ttu-id="5a9d6-105">callnz bool-PS</span><span class="sxs-lookup"><span data-stu-id="5a9d6-105">callnz bool - ps</span></span>

<span data-ttu-id="5a9d6-106">Appelez si la valeur n’est pas égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="5a9d6-106">Call if not zero.</span></span> <span data-ttu-id="5a9d6-107">Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="5a9d6-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a9d6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a9d6-108">Syntax</span></span>



| <span data-ttu-id="5a9d6-109">callnz l \# , \[ ! \] p\#</span><span class="sxs-lookup"><span data-stu-id="5a9d6-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="5a9d6-110">Où :</span><span class="sxs-lookup"><span data-stu-id="5a9d6-110">Where:</span></span>

-   <span data-ttu-id="5a9d6-111">l \# est une [étiquette-PS](label---ps.md) qui marque le début de la sous-routine à appeler.</span><span class="sxs-lookup"><span data-stu-id="5a9d6-111">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="5a9d6-112">\[!\] est un modificateur de négation facultatif.</span><span class="sxs-lookup"><span data-stu-id="5a9d6-112">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="5a9d6-113">b \# identifie un [Registre booléen constant](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="5a9d6-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5a9d6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5a9d6-114">Remarks</span></span>



| <span data-ttu-id="5a9d6-115">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5a9d6-115">Pixel shader versions</span></span> | <span data-ttu-id="5a9d6-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="5a9d6-116">1\_1</span></span> | <span data-ttu-id="5a9d6-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="5a9d6-117">1\_2</span></span> | <span data-ttu-id="5a9d6-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5a9d6-118">1\_3</span></span> | <span data-ttu-id="5a9d6-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="5a9d6-119">1\_4</span></span> | <span data-ttu-id="5a9d6-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a9d6-120">2\_0</span></span> | <span data-ttu-id="5a9d6-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5a9d6-121">2\_x</span></span> | <span data-ttu-id="5a9d6-122">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5a9d6-122">2\_sw</span></span> | <span data-ttu-id="5a9d6-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a9d6-123">3\_0</span></span> | <span data-ttu-id="5a9d6-124">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5a9d6-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5a9d6-125">callnz bool</span><span class="sxs-lookup"><span data-stu-id="5a9d6-125">callnz bool</span></span>           |      |      |      |      |      | <span data-ttu-id="5a9d6-126">x</span><span class="sxs-lookup"><span data-stu-id="5a9d6-126">x</span></span>    | <span data-ttu-id="5a9d6-127">x</span><span class="sxs-lookup"><span data-stu-id="5a9d6-127">x</span></span>     | <span data-ttu-id="5a9d6-128">x</span><span class="sxs-lookup"><span data-stu-id="5a9d6-128">x</span></span>    | <span data-ttu-id="5a9d6-129">x</span><span class="sxs-lookup"><span data-stu-id="5a9d6-129">x</span></span>     |



 

<span data-ttu-id="5a9d6-130">Cette instruction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a9d6-130">This instruction does the following:</span></span>


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="5a9d6-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a9d6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a9d6-132">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5a9d6-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




