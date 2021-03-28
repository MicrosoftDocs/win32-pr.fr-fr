---
title: if_comp-vs
description: Démarrer une si bool-vs... else-vs... endif-bloc vs, avec une condition basée sur les valeurs qui peuvent être calculées dans un nuanceur. Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’une condition.
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadbe9620367efc75f821a711de89eb3498d247f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990704"
---
# <a name="if_comp---vs"></a><span data-ttu-id="d9e06-104">Si \_ COMP-vs</span><span class="sxs-lookup"><span data-stu-id="d9e06-104">if\_comp - vs</span></span>

<span data-ttu-id="d9e06-105">Démarrer une [si bool-vs](if-bool---vs.md)... [else-vs](else---vs.md)... [endif-bloc vs](endif---vs.md) , avec une condition basée sur les valeurs qui peuvent être calculées dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="d9e06-105">Start an [if bool - vs](if-bool---vs.md)...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="d9e06-106">Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’une condition.</span><span class="sxs-lookup"><span data-stu-id="d9e06-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9e06-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9e06-107">Syntax</span></span>



| <span data-ttu-id="d9e06-108">Si \_ COMP src0, src1</span><span class="sxs-lookup"><span data-stu-id="d9e06-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="d9e06-109">Où :</span><span class="sxs-lookup"><span data-stu-id="d9e06-109">Where:</span></span>

-   <span data-ttu-id="d9e06-110">\_COMP est une comparaison entre les deux registres sources.</span><span class="sxs-lookup"><span data-stu-id="d9e06-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="d9e06-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d9e06-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="d9e06-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9e06-112">Syntax</span></span> | <span data-ttu-id="d9e06-113">Comparaison</span><span class="sxs-lookup"><span data-stu-id="d9e06-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="d9e06-114">\_TB</span><span class="sxs-lookup"><span data-stu-id="d9e06-114">\_gt</span></span>   | <span data-ttu-id="d9e06-115">Supérieur à</span><span class="sxs-lookup"><span data-stu-id="d9e06-115">Greater than</span></span>          |
    | <span data-ttu-id="d9e06-116">\_terme</span><span class="sxs-lookup"><span data-stu-id="d9e06-116">\_lt</span></span>   | <span data-ttu-id="d9e06-117">Inférieur à</span><span class="sxs-lookup"><span data-stu-id="d9e06-117">Less than</span></span>             |
    | <span data-ttu-id="d9e06-118">\_&</span><span class="sxs-lookup"><span data-stu-id="d9e06-118">\_ge</span></span>   | <span data-ttu-id="d9e06-119">Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="d9e06-119">Greater than or equal</span></span> |
    | <span data-ttu-id="d9e06-120">\_WinINSTALL</span><span class="sxs-lookup"><span data-stu-id="d9e06-120">\_le</span></span>   | <span data-ttu-id="d9e06-121">Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="d9e06-121">Less than or equal</span></span>    |
    | <span data-ttu-id="d9e06-122">\_EQ</span><span class="sxs-lookup"><span data-stu-id="d9e06-122">\_eq</span></span>   | <span data-ttu-id="d9e06-123">Égal à</span><span class="sxs-lookup"><span data-stu-id="d9e06-123">Equal to</span></span>              |
    | <span data-ttu-id="d9e06-124">\_ne</span><span class="sxs-lookup"><span data-stu-id="d9e06-124">\_ne</span></span>   | <span data-ttu-id="d9e06-125">Différent de</span><span class="sxs-lookup"><span data-stu-id="d9e06-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="d9e06-126">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="d9e06-126">src0 is a source register.</span></span> <span data-ttu-id="d9e06-127">La réplication de Swizzle est requise pour sélectionner un composant.</span><span class="sxs-lookup"><span data-stu-id="d9e06-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="d9e06-128">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="d9e06-128">src1 is a source register.</span></span> <span data-ttu-id="d9e06-129">La réplication de Swizzle est requise pour sélectionner un composant.</span><span class="sxs-lookup"><span data-stu-id="d9e06-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9e06-130">Notes</span><span class="sxs-lookup"><span data-stu-id="d9e06-130">Remarks</span></span>



| <span data-ttu-id="d9e06-131">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="d9e06-131">Vertex shader versions</span></span> | <span data-ttu-id="d9e06-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="d9e06-132">1\_1</span></span> | <span data-ttu-id="d9e06-133">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d9e06-133">2\_0</span></span> | <span data-ttu-id="d9e06-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d9e06-134">2\_x</span></span> | <span data-ttu-id="d9e06-135">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d9e06-135">2\_sw</span></span> | <span data-ttu-id="d9e06-136">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d9e06-136">3\_0</span></span> | <span data-ttu-id="d9e06-137">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d9e06-137">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d9e06-138">Si \_ COMP</span><span class="sxs-lookup"><span data-stu-id="d9e06-138">if\_comp</span></span>               |      |      | <span data-ttu-id="d9e06-139">x</span><span class="sxs-lookup"><span data-stu-id="d9e06-139">x</span></span>    | <span data-ttu-id="d9e06-140">x</span><span class="sxs-lookup"><span data-stu-id="d9e06-140">x</span></span>     | <span data-ttu-id="d9e06-141">x</span><span class="sxs-lookup"><span data-stu-id="d9e06-141">x</span></span>    | <span data-ttu-id="d9e06-142">x</span><span class="sxs-lookup"><span data-stu-id="d9e06-142">x</span></span>     |



 

<span data-ttu-id="d9e06-143">Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’une condition.</span><span class="sxs-lookup"><span data-stu-id="d9e06-143">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="d9e06-144">Veillez à utiliser les modes de comparaison égal à et différent de sur les nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d9e06-144">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="d9e06-145">Étant donné que l’arrondi se produit pendant les calculs à virgule flottante, la comparaison peut être effectuée par rapport à une valeur Epsilon (petit nombre différent de zéro) pour éviter les erreurs.</span><span class="sxs-lookup"><span data-stu-id="d9e06-145">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="d9e06-146">Les restrictions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d9e06-146">Restrictions include:</span></span>

-   <span data-ttu-id="d9e06-147">Si \_ COMP... [else-vs](else---vs.md)... [endif-](endif---vs.md) les blocs vs (avec les blocs if prédicats) peuvent être imbriqués jusqu’à 24 couches.</span><span class="sxs-lookup"><span data-stu-id="d9e06-147">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks (along with the predicated if blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="d9e06-148">les registres src0 et src1 requièrent un Swizzle de réplication.</span><span class="sxs-lookup"><span data-stu-id="d9e06-148">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="d9e06-149">Si \_ les blocs COMP doivent se terminer par une instruction [else-vs](else---vs.md) ou [endif-vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e06-149">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="d9e06-150">Si \_ COMP... [else-vs](else---vs.md)... [endif-les blocs vs](endif---vs.md) ne peuvent pas chevaucher un bloc de boucle.</span><span class="sxs-lookup"><span data-stu-id="d9e06-150">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="d9e06-151">Le \_ bloc If COMP doit être complètement à l’intérieur ou à l’extérieur du bloc [Loop-vs](loop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e06-151">The if\_comp block must be completely inside, or outside the [loop - vs](loop---vs.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="d9e06-152">Exemple</span><span class="sxs-lookup"><span data-stu-id="d9e06-152">Example</span></span>

<span data-ttu-id="d9e06-153">Cette instruction fournit un contrôle de workflow dynamique conditionnel.</span><span class="sxs-lookup"><span data-stu-id="d9e06-153">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="d9e06-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9e06-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9e06-155">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="d9e06-155">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




