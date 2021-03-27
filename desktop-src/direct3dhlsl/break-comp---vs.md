---
title: break_comp-vs
description: Décomposer de manière conditionnelle de la boucle actuelle à l’instruction ENDLOOP-vs ou endrep-vs.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841665"
---
# <a name="break_comp---vs"></a><span data-ttu-id="e1bf8-103">arrêt \_ COMP-vs</span><span class="sxs-lookup"><span data-stu-id="e1bf8-103">break\_comp - vs</span></span>

<span data-ttu-id="e1bf8-104">Décomposer de manière conditionnelle de la boucle actuelle à l’instruction [ENDLOOP-vs](endloop---vs.md) ou [endrep-vs](endrep---vs.md).</span><span class="sxs-lookup"><span data-stu-id="e1bf8-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e1bf8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1bf8-105">Syntax</span></span>



| <span data-ttu-id="e1bf8-106">arrêter \_ COMP src0, src1</span><span class="sxs-lookup"><span data-stu-id="e1bf8-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="e1bf8-107">Où :</span><span class="sxs-lookup"><span data-stu-id="e1bf8-107">Where:</span></span>

-   <span data-ttu-id="e1bf8-108">\_COMP est une comparaison entre les deux registres sources.</span><span class="sxs-lookup"><span data-stu-id="e1bf8-108">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="e1bf8-109">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1bf8-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="e1bf8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1bf8-110">Syntax</span></span> | <span data-ttu-id="e1bf8-111">Comparaison</span><span class="sxs-lookup"><span data-stu-id="e1bf8-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="e1bf8-112">\_TB</span><span class="sxs-lookup"><span data-stu-id="e1bf8-112">\_gt</span></span>   | <span data-ttu-id="e1bf8-113">Supérieur à</span><span class="sxs-lookup"><span data-stu-id="e1bf8-113">Greater than</span></span>          |
    | <span data-ttu-id="e1bf8-114">\_terme</span><span class="sxs-lookup"><span data-stu-id="e1bf8-114">\_lt</span></span>   | <span data-ttu-id="e1bf8-115">Inférieur à</span><span class="sxs-lookup"><span data-stu-id="e1bf8-115">Less than</span></span>             |
    | <span data-ttu-id="e1bf8-116">\_&</span><span class="sxs-lookup"><span data-stu-id="e1bf8-116">\_ge</span></span>   | <span data-ttu-id="e1bf8-117">Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="e1bf8-117">Greater than or equal</span></span> |
    | <span data-ttu-id="e1bf8-118">\_WinINSTALL</span><span class="sxs-lookup"><span data-stu-id="e1bf8-118">\_le</span></span>   | <span data-ttu-id="e1bf8-119">Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="e1bf8-119">Less than or equal</span></span>    |
    | <span data-ttu-id="e1bf8-120">\_EQ</span><span class="sxs-lookup"><span data-stu-id="e1bf8-120">\_eq</span></span>   | <span data-ttu-id="e1bf8-121">Égal à</span><span class="sxs-lookup"><span data-stu-id="e1bf8-121">Equal to</span></span>              |
    | <span data-ttu-id="e1bf8-122">\_ne</span><span class="sxs-lookup"><span data-stu-id="e1bf8-122">\_ne</span></span>   | <span data-ttu-id="e1bf8-123">Différent de</span><span class="sxs-lookup"><span data-stu-id="e1bf8-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="e1bf8-124">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="e1bf8-124">src0 is a source register.</span></span> <span data-ttu-id="e1bf8-125">La réplication de Swizzle est requise pour sélectionner un composant unique.</span><span class="sxs-lookup"><span data-stu-id="e1bf8-125">Replicate swizzle is required to select a single component.</span></span>
-   <span data-ttu-id="e1bf8-126">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="e1bf8-126">src1 is a source register.</span></span> <span data-ttu-id="e1bf8-127">La réplication de Swizzle est requise pour sélectionner un composant unique.</span><span class="sxs-lookup"><span data-stu-id="e1bf8-127">Replicate swizzle is required to select a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1bf8-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e1bf8-128">Remarks</span></span>

<span data-ttu-id="e1bf8-129">Cette instruction est prise en charge dans les versions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1bf8-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="e1bf8-130">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="e1bf8-130">Vertex shader versions</span></span> | <span data-ttu-id="e1bf8-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="e1bf8-131">1\_1</span></span> | <span data-ttu-id="e1bf8-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e1bf8-132">2\_0</span></span> | <span data-ttu-id="e1bf8-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e1bf8-133">2\_x</span></span> | <span data-ttu-id="e1bf8-134">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e1bf8-134">2\_sw</span></span> | <span data-ttu-id="e1bf8-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e1bf8-135">3\_0</span></span> | <span data-ttu-id="e1bf8-136">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="e1bf8-136">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e1bf8-137">arrêter la \_ COMP.</span><span class="sxs-lookup"><span data-stu-id="e1bf8-137">break\_comp</span></span>            |      |      | <span data-ttu-id="e1bf8-138">x</span><span class="sxs-lookup"><span data-stu-id="e1bf8-138">x</span></span>    | <span data-ttu-id="e1bf8-139">x</span><span class="sxs-lookup"><span data-stu-id="e1bf8-139">x</span></span>     | <span data-ttu-id="e1bf8-140">x</span><span class="sxs-lookup"><span data-stu-id="e1bf8-140">x</span></span>    | <span data-ttu-id="e1bf8-141">x</span><span class="sxs-lookup"><span data-stu-id="e1bf8-141">x</span></span>     |



 

<span data-ttu-id="e1bf8-142">Lorsque la comparaison a la valeur true, elle est déverrouillée de la boucle en cours, comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="e1bf8-142">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="e1bf8-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1bf8-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1bf8-144">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="e1bf8-144">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




