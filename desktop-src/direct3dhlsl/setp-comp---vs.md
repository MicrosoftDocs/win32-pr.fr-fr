---
title: setp_comp-vs
description: Définissez le registre de prédicat. | setp_comp-vs
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77d9e5f46e9fb8bbcfb96e56d13cd6f7cebfecc2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393979"
---
# <a name="setp_comp---vs"></a><span data-ttu-id="741f5-104">\_COMP setp-vs</span><span class="sxs-lookup"><span data-stu-id="741f5-104">setp\_comp - vs</span></span>

<span data-ttu-id="741f5-105">Définissez le registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="741f5-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="741f5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="741f5-106">Syntax</span></span>



| <span data-ttu-id="741f5-107">SETP \_ COMP DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="741f5-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="741f5-108">Où :</span><span class="sxs-lookup"><span data-stu-id="741f5-108">Where:</span></span>

-   <span data-ttu-id="741f5-109">\_COMP est une comparaison par canal entre les deux registres sources.</span><span class="sxs-lookup"><span data-stu-id="741f5-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="741f5-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="741f5-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="741f5-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="741f5-111">Syntax</span></span> | <span data-ttu-id="741f5-112">Comparaison</span><span class="sxs-lookup"><span data-stu-id="741f5-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="741f5-113">\_TB</span><span class="sxs-lookup"><span data-stu-id="741f5-113">\_gt</span></span>   | <span data-ttu-id="741f5-114">Supérieur à</span><span class="sxs-lookup"><span data-stu-id="741f5-114">Greater than</span></span>          |
    | <span data-ttu-id="741f5-115">\_terme</span><span class="sxs-lookup"><span data-stu-id="741f5-115">\_lt</span></span>   | <span data-ttu-id="741f5-116">Inférieur à</span><span class="sxs-lookup"><span data-stu-id="741f5-116">Less than</span></span>             |
    | <span data-ttu-id="741f5-117">\_&</span><span class="sxs-lookup"><span data-stu-id="741f5-117">\_ge</span></span>   | <span data-ttu-id="741f5-118">Supérieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="741f5-118">Greater than or equal</span></span> |
    | <span data-ttu-id="741f5-119">\_WinINSTALL</span><span class="sxs-lookup"><span data-stu-id="741f5-119">\_le</span></span>   | <span data-ttu-id="741f5-120">Inférieur ou égal à</span><span class="sxs-lookup"><span data-stu-id="741f5-120">Less than or equal</span></span>    |
    | <span data-ttu-id="741f5-121">\_EQ</span><span class="sxs-lookup"><span data-stu-id="741f5-121">\_eq</span></span>   | <span data-ttu-id="741f5-122">Égal à</span><span class="sxs-lookup"><span data-stu-id="741f5-122">Equal to</span></span>              |
    | <span data-ttu-id="741f5-123">\_ne</span><span class="sxs-lookup"><span data-stu-id="741f5-123">\_ne</span></span>   | <span data-ttu-id="741f5-124">Différent de</span><span class="sxs-lookup"><span data-stu-id="741f5-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="741f5-125">DST est le registre de [Registre des prédicats](dx9-graphics-reference-asm-vs-registers-predicate.md) , P0.</span><span class="sxs-lookup"><span data-stu-id="741f5-125">dst is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="741f5-126">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="741f5-126">src0 is a source register.</span></span>
-   <span data-ttu-id="741f5-127">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="741f5-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="741f5-128">Notes</span><span class="sxs-lookup"><span data-stu-id="741f5-128">Remarks</span></span>



| <span data-ttu-id="741f5-129">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="741f5-129">Vertex shader versions</span></span> | <span data-ttu-id="741f5-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="741f5-130">1\_1</span></span> | <span data-ttu-id="741f5-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="741f5-131">2\_0</span></span> | <span data-ttu-id="741f5-132">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="741f5-132">2\_x</span></span> | <span data-ttu-id="741f5-133">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="741f5-133">2\_sw</span></span> | <span data-ttu-id="741f5-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="741f5-134">3\_0</span></span> | <span data-ttu-id="741f5-135">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="741f5-135">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="741f5-136">\_COMP setp</span><span class="sxs-lookup"><span data-stu-id="741f5-136">setp\_comp</span></span>             |      |      | <span data-ttu-id="741f5-137">x</span><span class="sxs-lookup"><span data-stu-id="741f5-137">x</span></span>    | <span data-ttu-id="741f5-138">x</span><span class="sxs-lookup"><span data-stu-id="741f5-138">x</span></span>     | <span data-ttu-id="741f5-139">x</span><span class="sxs-lookup"><span data-stu-id="741f5-139">x</span></span>    | <span data-ttu-id="741f5-140">x</span><span class="sxs-lookup"><span data-stu-id="741f5-140">x</span></span>     |



 

<span data-ttu-id="741f5-141">Cette instruction fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="741f5-141">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="741f5-142">Pour chaque canal qui peut être écrit selon le masque d’écriture de destination, enregistrez le résultat booléen de l’opération de comparaison entre les canaux correspondants de src0 et src1 (une fois que le modificateur de source Swizzles a été résolu).</span><span class="sxs-lookup"><span data-stu-id="741f5-142">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="741f5-143">Les registres sources permettent de spécifier des Swizzles de composant arbitraires.</span><span class="sxs-lookup"><span data-stu-id="741f5-143">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="741f5-144">Le registre de destination autorise des masques d’écriture arbitraires.</span><span class="sxs-lookup"><span data-stu-id="741f5-144">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="741f5-145">Le registre de dest doit être le registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="741f5-145">The dest register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="741f5-146">Application du registre de prédicat</span><span class="sxs-lookup"><span data-stu-id="741f5-146">Applying the Predicate Register</span></span>

<span data-ttu-id="741f5-147">Une fois que le registre de prédicat a été initialisé avec setp, il peut être utilisé pour contrôler une instruction par composant.</span><span class="sxs-lookup"><span data-stu-id="741f5-147">Once the predicate register has been initialized with setp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="741f5-148">Voici la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="741f5-148">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



<span data-ttu-id="741f5-149">Où :</span><span class="sxs-lookup"><span data-stu-id="741f5-149">Where:</span></span>

-   <span data-ttu-id="741f5-150">\[!\] est un booléen facultatif NOT</span><span class="sxs-lookup"><span data-stu-id="741f5-150">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="741f5-151">P0 correspond au registre de prédicat</span><span class="sxs-lookup"><span data-stu-id="741f5-151">p0 is the predicate register</span></span>
-   <span data-ttu-id="741f5-152">\[. Swizzle \] est un Swizzle facultatif à appliquer au contenu du registre de prédicat avant de l’utiliser pour masquer l’instruction.</span><span class="sxs-lookup"><span data-stu-id="741f5-152">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="741f5-153">Les Swizzles disponibles sont :. XYZW (valeur par défaut si aucune valeur n’est spécifiée) ou n’importe quel Swizzle de réplication :. x/. r,. y/. g,. z/. b ou. a/. w.</span><span class="sxs-lookup"><span data-stu-id="741f5-153">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="741f5-154">instruction est une aritmetic ou une instruction de texture.</span><span class="sxs-lookup"><span data-stu-id="741f5-154">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="741f5-155">Il ne peut pas s’agir d’une instruction de contrôle de workflow statique ou dynamique.</span><span class="sxs-lookup"><span data-stu-id="741f5-155">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="741f5-156">dest, srcReg,... registres requis par l’instruction</span><span class="sxs-lookup"><span data-stu-id="741f5-156">dest, srcReg, ... are the registers required by the instruction</span></span>

<span data-ttu-id="741f5-157">En supposant que le registre de prédicat a été configuré avec des valeurs de composant (true, true, false, false), il peut être appliqué à cette instruction :</span><span class="sxs-lookup"><span data-stu-id="741f5-157">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



<span data-ttu-id="741f5-158">pour effectuer un ajout de 2 composants.</span><span class="sxs-lookup"><span data-stu-id="741f5-158">to perform a 2 component add.</span></span>


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



<span data-ttu-id="741f5-159">Les composants x et y de R2 ne seront pas écrits puisque le registre de prédicat contenait la valeur false dans les composants z et w.</span><span class="sxs-lookup"><span data-stu-id="741f5-159">The x and y components of r2 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="741f5-160">L’application du registre de prédicat à une instruction arithmétique ou de texture augmente son nombre d’emplacements d’instructions de 1.</span><span class="sxs-lookup"><span data-stu-id="741f5-160">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="741f5-161">Le registre de prédicat peut également être appliqué à [If prédit-vs](if-pred---vs.md), [callnz prédit-vs](callnz-pred---vs.md) et [breakp-vs](breakp---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="741f5-161">The predicate register can also be applied to [if pred - vs](if-pred---vs.md), [callnz pred - vs](callnz-pred---vs.md) and [breakp - vs](breakp---vs.md) instructions.</span></span> <span data-ttu-id="741f5-162">Ces instructions de contrôle de Flow n’ont pas d’augmentation du nombre d’emplacements d’instruction lors de l’utilisation du registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="741f5-162">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="741f5-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="741f5-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="741f5-164">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="741f5-164">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




