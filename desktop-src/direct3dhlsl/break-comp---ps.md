---
title: break_comp-PS
description: Sortir de la boucle actuelle au ENDLOOP-PS ou endrep-PS le plus proche, en fonction d’une comparaison par composant.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5088312a16102153ad78afffdcd9ea1275d34e0d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101085"
---
# <a name="break_comp---ps"></a><span data-ttu-id="8889d-103">arrêter \_ COMP-PS</span><span class="sxs-lookup"><span data-stu-id="8889d-103">break\_comp - ps</span></span>

<span data-ttu-id="8889d-104">Sortir de la boucle actuelle au [ENDLOOP-PS](endloop---ps.md) ou [endrep-PS](endrep---ps.md)le plus proche, en fonction d’une comparaison par composant.</span><span class="sxs-lookup"><span data-stu-id="8889d-104">Break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md), based on a per-component comparison.</span></span>

## <a name="syntax"></a><span data-ttu-id="8889d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8889d-105">Syntax</span></span>



| <span data-ttu-id="8889d-106">arrêter \_ COMP src0, src1</span><span class="sxs-lookup"><span data-stu-id="8889d-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="8889d-107">Où :</span><span class="sxs-lookup"><span data-stu-id="8889d-107">Where:</span></span>

-   <span data-ttu-id="8889d-108">\_COMP est une comparaison scalaire (ou unique) entre les deux registres sources.</span><span class="sxs-lookup"><span data-stu-id="8889d-108">\_comp is a scalar (or single) comparison between the two source registers.</span></span> <span data-ttu-id="8889d-109">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8889d-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="8889d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8889d-110">Syntax</span></span> | <span data-ttu-id="8889d-111">Comparaison</span><span class="sxs-lookup"><span data-stu-id="8889d-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="8889d-112">\_TB</span><span class="sxs-lookup"><span data-stu-id="8889d-112">\_gt</span></span>   | <span data-ttu-id="8889d-113">Supérieur à</span><span class="sxs-lookup"><span data-stu-id="8889d-113">Greater than</span></span>          |
    | <span data-ttu-id="8889d-114">\_terme</span><span class="sxs-lookup"><span data-stu-id="8889d-114">\_lt</span></span>   | <span data-ttu-id="8889d-115">Inférieur à</span><span class="sxs-lookup"><span data-stu-id="8889d-115">Less than</span></span>             |
    | <span data-ttu-id="8889d-116">\_&</span><span class="sxs-lookup"><span data-stu-id="8889d-116">\_ge</span></span>   | <span data-ttu-id="8889d-117">Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="8889d-117">Greater than or equal</span></span> |
    | <span data-ttu-id="8889d-118">\_WinINSTALL</span><span class="sxs-lookup"><span data-stu-id="8889d-118">\_le</span></span>   | <span data-ttu-id="8889d-119">Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="8889d-119">Less than or equal</span></span>    |
    | <span data-ttu-id="8889d-120">\_EQ</span><span class="sxs-lookup"><span data-stu-id="8889d-120">\_eq</span></span>   | <span data-ttu-id="8889d-121">Égal à</span><span class="sxs-lookup"><span data-stu-id="8889d-121">Equal to</span></span>              |
    | <span data-ttu-id="8889d-122">\_ne</span><span class="sxs-lookup"><span data-stu-id="8889d-122">\_ne</span></span>   | <span data-ttu-id="8889d-123">Différent de</span><span class="sxs-lookup"><span data-stu-id="8889d-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="8889d-124">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="8889d-124">src0 is a source register.</span></span> <span data-ttu-id="8889d-125">La réplication de Swizzle est requise si vous sélectionnez un seul composant.</span><span class="sxs-lookup"><span data-stu-id="8889d-125">Replicate swizzle is required if selecting a single component.</span></span>
-   <span data-ttu-id="8889d-126">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="8889d-126">src1 is a source register.</span></span> <span data-ttu-id="8889d-127">La réplication de Swizzle est requise si vous sélectionnez un seul composant.</span><span class="sxs-lookup"><span data-stu-id="8889d-127">Replicate swizzle is required if selecting a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="8889d-128">Notes</span><span class="sxs-lookup"><span data-stu-id="8889d-128">Remarks</span></span>

<span data-ttu-id="8889d-129">Cette instruction est prise en charge dans les versions suivantes.</span><span class="sxs-lookup"><span data-stu-id="8889d-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="8889d-130">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="8889d-130">Pixel shader versions</span></span> | <span data-ttu-id="8889d-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="8889d-131">1\_1</span></span> | <span data-ttu-id="8889d-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="8889d-132">1\_2</span></span> | <span data-ttu-id="8889d-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8889d-133">1\_3</span></span> | <span data-ttu-id="8889d-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="8889d-134">1\_4</span></span> | <span data-ttu-id="8889d-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8889d-135">2\_0</span></span> | <span data-ttu-id="8889d-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8889d-136">2\_x</span></span> | <span data-ttu-id="8889d-137">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8889d-137">2\_sw</span></span> | <span data-ttu-id="8889d-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8889d-138">3\_0</span></span> | <span data-ttu-id="8889d-139">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8889d-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8889d-140">arrêter la \_ COMP.</span><span class="sxs-lookup"><span data-stu-id="8889d-140">break\_comp</span></span>           |      |      |      |      |      | <span data-ttu-id="8889d-141">x</span><span class="sxs-lookup"><span data-stu-id="8889d-141">x</span></span>    | <span data-ttu-id="8889d-142">x</span><span class="sxs-lookup"><span data-stu-id="8889d-142">x</span></span>     | <span data-ttu-id="8889d-143">x</span><span class="sxs-lookup"><span data-stu-id="8889d-143">x</span></span>    | <span data-ttu-id="8889d-144">x</span><span class="sxs-lookup"><span data-stu-id="8889d-144">x</span></span>     |



 

<span data-ttu-id="8889d-145">Lorsque la comparaison a la valeur true, elle est déverrouillée de la boucle en cours, comme indiqué.</span><span class="sxs-lookup"><span data-stu-id="8889d-145">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="8889d-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8889d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8889d-147">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="8889d-147">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




