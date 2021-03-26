---
title: setp_comp-PS
description: Définissez le registre de prédicat. | setp_comp-PS
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a68da290ecb04e9cb7ae49c5525997fbf4c112a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211570"
---
# <a name="setp_comp---ps"></a><span data-ttu-id="27653-104">SETP \_ COMP-PS</span><span class="sxs-lookup"><span data-stu-id="27653-104">setp\_comp - ps</span></span>

<span data-ttu-id="27653-105">Définissez le registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="27653-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="27653-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27653-106">Syntax</span></span>



| <span data-ttu-id="27653-107">SETP \_ COMP DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="27653-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="27653-108">Où :</span><span class="sxs-lookup"><span data-stu-id="27653-108">Where:</span></span>

-   <span data-ttu-id="27653-109">\_COMP est une comparaison par canal entre les deux registres sources.</span><span class="sxs-lookup"><span data-stu-id="27653-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="27653-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="27653-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="27653-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27653-111">Syntax</span></span> | <span data-ttu-id="27653-112">Comparaison</span><span class="sxs-lookup"><span data-stu-id="27653-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="27653-113">\_TB</span><span class="sxs-lookup"><span data-stu-id="27653-113">\_gt</span></span>   | <span data-ttu-id="27653-114">Supérieur à</span><span class="sxs-lookup"><span data-stu-id="27653-114">Greater than</span></span>          |
    | <span data-ttu-id="27653-115">\_terme</span><span class="sxs-lookup"><span data-stu-id="27653-115">\_lt</span></span>   | <span data-ttu-id="27653-116">Inférieur à</span><span class="sxs-lookup"><span data-stu-id="27653-116">Less than</span></span>             |
    | <span data-ttu-id="27653-117">\_&</span><span class="sxs-lookup"><span data-stu-id="27653-117">\_ge</span></span>   | <span data-ttu-id="27653-118">Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="27653-118">Greater than or equal</span></span> |
    | <span data-ttu-id="27653-119">\_WinINSTALL</span><span class="sxs-lookup"><span data-stu-id="27653-119">\_le</span></span>   | <span data-ttu-id="27653-120">Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="27653-120">Less than or equal</span></span>    |
    | <span data-ttu-id="27653-121">\_EQ</span><span class="sxs-lookup"><span data-stu-id="27653-121">\_eq</span></span>   | <span data-ttu-id="27653-122">Égal à</span><span class="sxs-lookup"><span data-stu-id="27653-122">Equal to</span></span>              |
    | <span data-ttu-id="27653-123">\_ne</span><span class="sxs-lookup"><span data-stu-id="27653-123">\_ne</span></span>   | <span data-ttu-id="27653-124">Différent de</span><span class="sxs-lookup"><span data-stu-id="27653-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="27653-125">DST est le registre de [Registre des prédicats](dx9-graphics-reference-asm-ps-registers-predicate.md) , P0.</span><span class="sxs-lookup"><span data-stu-id="27653-125">dst is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="27653-126">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="27653-126">src0 is a source register.</span></span>
-   <span data-ttu-id="27653-127">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="27653-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="27653-128">Notes</span><span class="sxs-lookup"><span data-stu-id="27653-128">Remarks</span></span>



| <span data-ttu-id="27653-129">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="27653-129">Pixel shader versions</span></span> | <span data-ttu-id="27653-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="27653-130">1\_1</span></span> | <span data-ttu-id="27653-131">1\_2</span><span class="sxs-lookup"><span data-stu-id="27653-131">1\_2</span></span> | <span data-ttu-id="27653-132">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="27653-132">1\_3</span></span> | <span data-ttu-id="27653-133">1\_4</span><span class="sxs-lookup"><span data-stu-id="27653-133">1\_4</span></span> | <span data-ttu-id="27653-134">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="27653-134">2\_0</span></span> | <span data-ttu-id="27653-135">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="27653-135">2\_x</span></span> | <span data-ttu-id="27653-136">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="27653-136">2\_sw</span></span> | <span data-ttu-id="27653-137">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="27653-137">3\_0</span></span> | <span data-ttu-id="27653-138">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="27653-138">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="27653-139">\_COMP setp</span><span class="sxs-lookup"><span data-stu-id="27653-139">setp\_comp</span></span>            |      |      |      |      |      | <span data-ttu-id="27653-140">x</span><span class="sxs-lookup"><span data-stu-id="27653-140">x</span></span>    | <span data-ttu-id="27653-141">x</span><span class="sxs-lookup"><span data-stu-id="27653-141">x</span></span>     | <span data-ttu-id="27653-142">x</span><span class="sxs-lookup"><span data-stu-id="27653-142">x</span></span>    | <span data-ttu-id="27653-143">x</span><span class="sxs-lookup"><span data-stu-id="27653-143">x</span></span>     |



 

<span data-ttu-id="27653-144">Cette instruction fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="27653-144">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="27653-145">Pour chaque canal qui peut être écrit selon le masque d’écriture de destination, enregistrez le résultat booléen de l’opération de comparaison entre les canaux correspondants de src0 et src1 (une fois que le modificateur de source Swizzles a été résolu).</span><span class="sxs-lookup"><span data-stu-id="27653-145">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="27653-146">Les registres sources permettent de spécifier des Swizzles de composant arbitraires.</span><span class="sxs-lookup"><span data-stu-id="27653-146">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="27653-147">Le registre de destination autorise des masques d’écriture arbitraires.</span><span class="sxs-lookup"><span data-stu-id="27653-147">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="27653-148">Le registre de l’heure d’été doit être un registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="27653-148">The dst register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="27653-149">Application du registre de prédicat</span><span class="sxs-lookup"><span data-stu-id="27653-149">Applying the Predicate Register</span></span>

<span data-ttu-id="27653-150">Une fois que le registre de prédicat a été initialisé avec setp \_ COMP, il peut être utilisé pour contrôler une instruction par composant.</span><span class="sxs-lookup"><span data-stu-id="27653-150">Once the predicate register has been initialized with setp\_comp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="27653-151">Voici la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="27653-151">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



<span data-ttu-id="27653-152">Où :</span><span class="sxs-lookup"><span data-stu-id="27653-152">Where:</span></span>

-   <span data-ttu-id="27653-153">\[!\] est un booléen facultatif NOT</span><span class="sxs-lookup"><span data-stu-id="27653-153">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="27653-154">P0 correspond au registre de prédicat</span><span class="sxs-lookup"><span data-stu-id="27653-154">p0 is the predicate register</span></span>
-   <span data-ttu-id="27653-155">\[. Swizzle \] est un Swizzle facultatif à appliquer au contenu du registre de prédicat avant de l’utiliser pour masquer l’instruction.</span><span class="sxs-lookup"><span data-stu-id="27653-155">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="27653-156">Les Swizzles disponibles sont :. XYZW (valeur par défaut si aucune valeur n’est spécifiée) ou n’importe quel Swizzle de réplication :. x/. r,. y/. g,. z/. b ou. a/. w.</span><span class="sxs-lookup"><span data-stu-id="27653-156">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="27653-157">instruction est une aritmetic ou une instruction de texture.</span><span class="sxs-lookup"><span data-stu-id="27653-157">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="27653-158">Il ne peut pas s’agir d’une instruction de contrôle de workflow statique ou dynamique.</span><span class="sxs-lookup"><span data-stu-id="27653-158">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="27653-159">dest, src0,... registres requis par l’instruction</span><span class="sxs-lookup"><span data-stu-id="27653-159">dest, src0, ... are the registers required by the instruction</span></span>

<span data-ttu-id="27653-160">En supposant que le registre de prédicat a été configuré avec des valeurs de composant (true, true, false, false), il peut être appliqué à cette instruction :</span><span class="sxs-lookup"><span data-stu-id="27653-160">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
(p0) add r1, r2, r3
```



<span data-ttu-id="27653-161">pour effectuer un ajout de 2 composants.</span><span class="sxs-lookup"><span data-stu-id="27653-161">to perform a 2 component add.</span></span>


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



<span data-ttu-id="27653-162">Les composants z et w de R1 ne seront pas écrits puisque le registre de prédicat contenait la valeur false dans les composants z et w.</span><span class="sxs-lookup"><span data-stu-id="27653-162">The z and w components of r1 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="27653-163">L’application du registre de prédicat à une instruction arithmétique ou de texture augmente son nombre d’emplacements d’instructions de 1.</span><span class="sxs-lookup"><span data-stu-id="27653-163">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="27653-164">Le registre de prédicat peut également être appliqué aux instructions [If prédit-PS](if-pred---ps.md), [callnz prédit-PS](callnz-pred---ps.md) et [breakp-PS](break-p---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="27653-164">The predicate register can also be applied to [if pred - ps](if-pred---ps.md), [callnz pred - ps](callnz-pred---ps.md) and [breakp - ps](break-p---ps.md) instructions.</span></span> <span data-ttu-id="27653-165">Ces instructions de contrôle de Flow n’ont pas d’augmentation du nombre d’emplacements d’instruction lors de l’utilisation du registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="27653-165">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27653-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27653-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27653-167">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="27653-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




