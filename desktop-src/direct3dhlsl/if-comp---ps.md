---
title: if_comp-PS
description: Démarrer une si bool-PS... else-PS... endif-bloc PS, avec une condition basée sur les valeurs qui peuvent être calculées dans un nuanceur. Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’une condition.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679101"
---
# <a name="if_comp---ps"></a><span data-ttu-id="3c317-104">Si \_ COMP-PS</span><span class="sxs-lookup"><span data-stu-id="3c317-104">if\_comp - ps</span></span>

<span data-ttu-id="3c317-105">Démarrer une [si bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... [endif-bloc PS](endif---ps.md) , avec une condition basée sur les valeurs qui peuvent être calculées dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3c317-105">Start an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="3c317-106">Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’une condition.</span><span class="sxs-lookup"><span data-stu-id="3c317-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c317-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c317-107">Syntax</span></span>



| <span data-ttu-id="3c317-108">Si \_ COMP src0, src1</span><span class="sxs-lookup"><span data-stu-id="3c317-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="3c317-109">Où :</span><span class="sxs-lookup"><span data-stu-id="3c317-109">Where:</span></span>

-   <span data-ttu-id="3c317-110">\_COMP est une comparaison entre les deux registres sources.</span><span class="sxs-lookup"><span data-stu-id="3c317-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="3c317-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3c317-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="3c317-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c317-112">Syntax</span></span> | <span data-ttu-id="3c317-113">Comparaison</span><span class="sxs-lookup"><span data-stu-id="3c317-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="3c317-114">\_TB</span><span class="sxs-lookup"><span data-stu-id="3c317-114">\_gt</span></span>   | <span data-ttu-id="3c317-115">Supérieur à</span><span class="sxs-lookup"><span data-stu-id="3c317-115">Greater than</span></span>          |
    | <span data-ttu-id="3c317-116">\_terme</span><span class="sxs-lookup"><span data-stu-id="3c317-116">\_lt</span></span>   | <span data-ttu-id="3c317-117">Inférieur à</span><span class="sxs-lookup"><span data-stu-id="3c317-117">Less than</span></span>             |
    | <span data-ttu-id="3c317-118">\_&</span><span class="sxs-lookup"><span data-stu-id="3c317-118">\_ge</span></span>   | <span data-ttu-id="3c317-119">Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="3c317-119">Greater than or equal</span></span> |
    | <span data-ttu-id="3c317-120">\_WinINSTALL</span><span class="sxs-lookup"><span data-stu-id="3c317-120">\_le</span></span>   | <span data-ttu-id="3c317-121">Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="3c317-121">Less than or equal</span></span>    |
    | <span data-ttu-id="3c317-122">\_EQ</span><span class="sxs-lookup"><span data-stu-id="3c317-122">\_eq</span></span>   | <span data-ttu-id="3c317-123">Égal à</span><span class="sxs-lookup"><span data-stu-id="3c317-123">Equal to</span></span>              |
    | <span data-ttu-id="3c317-124">\_ne</span><span class="sxs-lookup"><span data-stu-id="3c317-124">\_ne</span></span>   | <span data-ttu-id="3c317-125">Différent de</span><span class="sxs-lookup"><span data-stu-id="3c317-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="3c317-126">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="3c317-126">src0 is a source register.</span></span> <span data-ttu-id="3c317-127">La réplication de Swizzle est requise pour sélectionner un composant.</span><span class="sxs-lookup"><span data-stu-id="3c317-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="3c317-128">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="3c317-128">src1 is a source register.</span></span> <span data-ttu-id="3c317-129">La réplication de Swizzle est requise pour sélectionner un composant.</span><span class="sxs-lookup"><span data-stu-id="3c317-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c317-130">Notes</span><span class="sxs-lookup"><span data-stu-id="3c317-130">Remarks</span></span>



| <span data-ttu-id="3c317-131">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="3c317-131">Pixel shader versions</span></span> | <span data-ttu-id="3c317-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="3c317-132">1\_1</span></span> | <span data-ttu-id="3c317-133">1\_2</span><span class="sxs-lookup"><span data-stu-id="3c317-133">1\_2</span></span> | <span data-ttu-id="3c317-134">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3c317-134">1\_3</span></span> | <span data-ttu-id="3c317-135">1\_4</span><span class="sxs-lookup"><span data-stu-id="3c317-135">1\_4</span></span> | <span data-ttu-id="3c317-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c317-136">2\_0</span></span> | <span data-ttu-id="3c317-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3c317-137">2\_x</span></span> | <span data-ttu-id="3c317-138">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="3c317-138">2\_sw</span></span> | <span data-ttu-id="3c317-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c317-139">3\_0</span></span> | <span data-ttu-id="3c317-140">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="3c317-140">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3c317-141">Si \_ COMP</span><span class="sxs-lookup"><span data-stu-id="3c317-141">if\_comp</span></span>              |      |      |      |      |      | <span data-ttu-id="3c317-142">x</span><span class="sxs-lookup"><span data-stu-id="3c317-142">x</span></span>    | <span data-ttu-id="3c317-143">x</span><span class="sxs-lookup"><span data-stu-id="3c317-143">x</span></span>     | <span data-ttu-id="3c317-144">x</span><span class="sxs-lookup"><span data-stu-id="3c317-144">x</span></span>    | <span data-ttu-id="3c317-145">x</span><span class="sxs-lookup"><span data-stu-id="3c317-145">x</span></span>     |



 

<span data-ttu-id="3c317-146">Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’une condition.</span><span class="sxs-lookup"><span data-stu-id="3c317-146">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="3c317-147">Veillez à utiliser les modes de comparaison égal à et différent de sur les nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="3c317-147">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="3c317-148">Étant donné que l’arrondi se produit pendant les calculs à virgule flottante, la comparaison peut être effectuée par rapport à une valeur Epsilon (petit nombre différent de zéro) pour éviter les erreurs.</span><span class="sxs-lookup"><span data-stu-id="3c317-148">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="3c317-149">Les restrictions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3c317-149">Restrictions include:</span></span>

-   <span data-ttu-id="3c317-150">Si \_ COMP... [else-PS](else---ps.md)... [endif](endif---ps.md) les blocs PS (ainsi que les blocs [If](if-bool---ps.md) prédicats) peuvent être imbriqués jusqu’à 24 niveaux de profondeur.</span><span class="sxs-lookup"><span data-stu-id="3c317-150">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks (along with the predicated [if](if-bool---ps.md) blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="3c317-151">les registres src0 et src1 requièrent un Swizzle de réplication.</span><span class="sxs-lookup"><span data-stu-id="3c317-151">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="3c317-152">Si \_ les blocs COMP doivent se terminer par une instruction [else-vs](else---vs.md) ou [endif-vs](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="3c317-152">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="3c317-153">Si \_ COMP... [else-PS](else---ps.md)... [endif : les blocs PS](endif---ps.md) ne peuvent pas chevaucher un bloc de boucle.</span><span class="sxs-lookup"><span data-stu-id="3c317-153">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="3c317-154">Le \_ bloc If COMP doit être complètement à l’intérieur ou à l’extérieur du bloc de boucle.</span><span class="sxs-lookup"><span data-stu-id="3c317-154">The if\_comp block must be completely inside or outside the loop block.</span></span>

## <a name="example"></a><span data-ttu-id="3c317-155">Exemple</span><span class="sxs-lookup"><span data-stu-id="3c317-155">Example</span></span>

<span data-ttu-id="3c317-156">Cette instruction fournit un contrôle de workflow dynamique conditionnel.</span><span class="sxs-lookup"><span data-stu-id="3c317-156">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="3c317-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c317-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c317-158">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="3c317-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




