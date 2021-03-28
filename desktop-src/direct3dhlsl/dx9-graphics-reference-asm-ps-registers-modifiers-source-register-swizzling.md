---
title: Registre source swizzling (référence du PS HLSL)
description: Swizzling fait référence à la capacité de copier n’importe quel composant Registre source vers un composant de registre temporaire. Swizzling n’affecte pas les données du Registre source. Avant l’exécution d’une instruction, les données d’un registre source sont copiées dans un registre temporaire.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313792"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a><span data-ttu-id="efb3b-105">Registre source swizzling (référence du PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="efb3b-105">Source register swizzling (HLSL PS reference)</span></span>

<span data-ttu-id="efb3b-106">Swizzling fait référence à la capacité de copier n’importe quel composant Registre source vers un composant de registre temporaire.</span><span class="sxs-lookup"><span data-stu-id="efb3b-106">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="efb3b-107">Swizzling n’affecte pas les données du Registre source.</span><span class="sxs-lookup"><span data-stu-id="efb3b-107">Swizzling does not affect the source register data.</span></span> <span data-ttu-id="efb3b-108">Avant l’exécution d’une instruction, les données d’un registre source sont copiées dans un registre temporaire.</span><span class="sxs-lookup"><span data-stu-id="efb3b-108">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span>

## <a name="source-swizzling"></a><span data-ttu-id="efb3b-109">Swizzling source</span><span class="sxs-lookup"><span data-stu-id="efb3b-109">Source Swizzling</span></span>

<span data-ttu-id="efb3b-110">La source Swizzle permet à un composant individuel d’un registre source de prendre la valeur de l’un des quatre composants du même registre source avant que le registre ne soit lu pour le calcul.</span><span class="sxs-lookup"><span data-stu-id="efb3b-110">Source swizzle allows individual component of a source register to take on the value of any of the four components of the same source register before the register is read for computation.</span></span>

<span data-ttu-id="efb3b-111">Par exemple, le Swizzle. zxxy signifie :</span><span class="sxs-lookup"><span data-stu-id="efb3b-111">For example, the .zxxy swizzle means:</span></span>

-   <span data-ttu-id="efb3b-112">le composant. x prendra la valeur du composant. z</span><span class="sxs-lookup"><span data-stu-id="efb3b-112">.x component will take on the value of .z component</span></span>
-   <span data-ttu-id="efb3b-113">le composant. y prendra la valeur du composant. x</span><span class="sxs-lookup"><span data-stu-id="efb3b-113">.y component will take on the value of .x component</span></span>
-   <span data-ttu-id="efb3b-114">le composant. z prendra la valeur du composant. x</span><span class="sxs-lookup"><span data-stu-id="efb3b-114">.z component will take on the value of .x component</span></span>
-   <span data-ttu-id="efb3b-115">. w le composant prendra la valeur du composant. y</span><span class="sxs-lookup"><span data-stu-id="efb3b-115">.w component will take on the value of .y component</span></span>

<span data-ttu-id="efb3b-116">Les composants peuvent apparaître dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="efb3b-116">The components can appear in any order.</span></span> <span data-ttu-id="efb3b-117">Si moins de quatre composants sont spécifiés, le dernier composant est répété.</span><span class="sxs-lookup"><span data-stu-id="efb3b-117">If fewer than four components are specified, the last component is repeated.</span></span> <span data-ttu-id="efb3b-118">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="efb3b-118">For example:</span></span>


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



<span data-ttu-id="efb3b-119">Si aucun composant n’est spécifié, aucun swizzling n’est appliqué.</span><span class="sxs-lookup"><span data-stu-id="efb3b-119">If no component is specified, no swizzling is applied.</span></span>

<span data-ttu-id="efb3b-120">Certaines instructions présentent des restrictions pour les Swizzle sources.</span><span class="sxs-lookup"><span data-stu-id="efb3b-120">Some instructions have restrictions for source swizzle.</span></span> <span data-ttu-id="efb3b-121">Ils sont répertoriés dans les pages de référence des instructions respectées.</span><span class="sxs-lookup"><span data-stu-id="efb3b-121">They are listed in the respected instruction reference pages.</span></span>



| <span data-ttu-id="efb3b-122">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="efb3b-122">Pixel shader versions</span></span> | <span data-ttu-id="efb3b-123">1\_1</span><span class="sxs-lookup"><span data-stu-id="efb3b-123">1\_1</span></span> | <span data-ttu-id="efb3b-124">1\_2</span><span class="sxs-lookup"><span data-stu-id="efb3b-124">1\_2</span></span> | <span data-ttu-id="efb3b-125">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="efb3b-125">1\_3</span></span> | <span data-ttu-id="efb3b-126">1\_4</span><span class="sxs-lookup"><span data-stu-id="efb3b-126">1\_4</span></span> | <span data-ttu-id="efb3b-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="efb3b-127">2\_0</span></span> | <span data-ttu-id="efb3b-128">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="efb3b-128">2\_x</span></span> | <span data-ttu-id="efb3b-129">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="efb3b-129">2\_sw</span></span> | <span data-ttu-id="efb3b-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="efb3b-130">3\_0</span></span> | <span data-ttu-id="efb3b-131">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="efb3b-131">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="efb3b-132">.x</span><span class="sxs-lookup"><span data-stu-id="efb3b-132">.x</span></span>                    |      |      |      | <span data-ttu-id="efb3b-133">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-133">x</span></span>    | <span data-ttu-id="efb3b-134">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-134">x</span></span>    | <span data-ttu-id="efb3b-135">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-135">x</span></span>    | <span data-ttu-id="efb3b-136">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-136">x</span></span>     | <span data-ttu-id="efb3b-137">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-137">x</span></span>    | <span data-ttu-id="efb3b-138">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-138">x</span></span>     |
| <span data-ttu-id="efb3b-139">. y</span><span class="sxs-lookup"><span data-stu-id="efb3b-139">.y</span></span>                    |      |      |      | <span data-ttu-id="efb3b-140">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-140">x</span></span>    | <span data-ttu-id="efb3b-141">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-141">x</span></span>    | <span data-ttu-id="efb3b-142">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-142">x</span></span>    | <span data-ttu-id="efb3b-143">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-143">x</span></span>     | <span data-ttu-id="efb3b-144">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-144">x</span></span>    | <span data-ttu-id="efb3b-145">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-145">x</span></span>     |
| <span data-ttu-id="efb3b-146">. z</span><span class="sxs-lookup"><span data-stu-id="efb3b-146">.z</span></span>                    | <span data-ttu-id="efb3b-147">x\*</span><span class="sxs-lookup"><span data-stu-id="efb3b-147">x\*</span></span>  | <span data-ttu-id="efb3b-148">x\*</span><span class="sxs-lookup"><span data-stu-id="efb3b-148">x\*</span></span>  | <span data-ttu-id="efb3b-149">x\*</span><span class="sxs-lookup"><span data-stu-id="efb3b-149">x\*</span></span>  | <span data-ttu-id="efb3b-150">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-150">x</span></span>    | <span data-ttu-id="efb3b-151">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-151">x</span></span>    | <span data-ttu-id="efb3b-152">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-152">x</span></span>    | <span data-ttu-id="efb3b-153">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-153">x</span></span>     | <span data-ttu-id="efb3b-154">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-154">x</span></span>    | <span data-ttu-id="efb3b-155">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-155">x</span></span>     |
| <span data-ttu-id="efb3b-156">. w</span><span class="sxs-lookup"><span data-stu-id="efb3b-156">.w</span></span>                    | <span data-ttu-id="efb3b-157">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-157">x</span></span>    | <span data-ttu-id="efb3b-158">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-158">x</span></span>    | <span data-ttu-id="efb3b-159">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-159">x</span></span>    | <span data-ttu-id="efb3b-160">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-160">x</span></span>    | <span data-ttu-id="efb3b-161">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-161">x</span></span>    | <span data-ttu-id="efb3b-162">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-162">x</span></span>    | <span data-ttu-id="efb3b-163">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-163">x</span></span>     | <span data-ttu-id="efb3b-164">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-164">x</span></span>    | <span data-ttu-id="efb3b-165">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-165">x</span></span>     |
| <span data-ttu-id="efb3b-166">. XYZW (par défaut)</span><span class="sxs-lookup"><span data-stu-id="efb3b-166">.xyzw (default)</span></span>       | <span data-ttu-id="efb3b-167">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-167">x</span></span>    | <span data-ttu-id="efb3b-168">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-168">x</span></span>    | <span data-ttu-id="efb3b-169">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-169">x</span></span>    | <span data-ttu-id="efb3b-170">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-170">x</span></span>    | <span data-ttu-id="efb3b-171">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-171">x</span></span>    | <span data-ttu-id="efb3b-172">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-172">x</span></span>    | <span data-ttu-id="efb3b-173">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-173">x</span></span>     | <span data-ttu-id="efb3b-174">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-174">x</span></span>    | <span data-ttu-id="efb3b-175">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-175">x</span></span>     |
| <span data-ttu-id="efb3b-176">.yzxw</span><span class="sxs-lookup"><span data-stu-id="efb3b-176">.yzxw</span></span>                 |      |      |      |      | <span data-ttu-id="efb3b-177">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-177">x</span></span>    | <span data-ttu-id="efb3b-178">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-178">x</span></span>    | <span data-ttu-id="efb3b-179">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-179">x</span></span>     | <span data-ttu-id="efb3b-180">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-180">x</span></span>    | <span data-ttu-id="efb3b-181">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-181">x</span></span>     |
| <span data-ttu-id="efb3b-182">.zxyw</span><span class="sxs-lookup"><span data-stu-id="efb3b-182">.zxyw</span></span>                 |      |      |      |      | <span data-ttu-id="efb3b-183">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-183">x</span></span>    | <span data-ttu-id="efb3b-184">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-184">x</span></span>    | <span data-ttu-id="efb3b-185">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-185">x</span></span>     | <span data-ttu-id="efb3b-186">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-186">x</span></span>    | <span data-ttu-id="efb3b-187">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-187">x</span></span>     |
| <span data-ttu-id="efb3b-188">.wzyx</span><span class="sxs-lookup"><span data-stu-id="efb3b-188">.wzyx</span></span>                 |      |      |      |      | <span data-ttu-id="efb3b-189">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-189">x</span></span>    | <span data-ttu-id="efb3b-190">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-190">x</span></span>    | <span data-ttu-id="efb3b-191">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-191">x</span></span>     | <span data-ttu-id="efb3b-192">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-192">x</span></span>    | <span data-ttu-id="efb3b-193">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-193">x</span></span>     |
| <span data-ttu-id="efb3b-194">Swizzle arbitraire</span><span class="sxs-lookup"><span data-stu-id="efb3b-194">arbitrary swizzle</span></span>     |      |      |      |      |      | <span data-ttu-id="efb3b-195">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-195">x</span></span>    | <span data-ttu-id="efb3b-196">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-196">x</span></span>     | <span data-ttu-id="efb3b-197">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-197">x</span></span>    | <span data-ttu-id="efb3b-198">x</span><span class="sxs-lookup"><span data-stu-id="efb3b-198">x</span></span>     |



 

<span data-ttu-id="efb3b-199">\* Disponible uniquement si le masque d’écriture de destination est. w (. a).</span><span class="sxs-lookup"><span data-stu-id="efb3b-199">\* Only available if destination write mask is .w (.a).</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="efb3b-200">Swizzle arbitraire</span><span class="sxs-lookup"><span data-stu-id="efb3b-200">Arbitrary Swizzle</span></span>

<span data-ttu-id="efb3b-201">Les Swizzles peuvent être appliqués aux registres sources dans un ordre arbitraire. autrement dit, tout registre source peut prendre n’importe quel masque de composant, dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="efb3b-201">Swizzles can be applied to source registers in an arbitrary order; that is, any source register can take any component mask, in any order.</span></span>

## <a name="replicate-swizzle"></a><span data-ttu-id="efb3b-202">Répliquer Swizzle</span><span class="sxs-lookup"><span data-stu-id="efb3b-202">Replicate Swizzle</span></span>

<span data-ttu-id="efb3b-203">Répliquer Swizzle copie un composant vers un autre.</span><span class="sxs-lookup"><span data-stu-id="efb3b-203">Replicate swizzle copies one component to another.</span></span> <span data-ttu-id="efb3b-204">Il s’agit d’un seul des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalent) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="efb3b-204">This is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efb3b-205">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="efb3b-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efb3b-206">Modificateurs de Registre source du nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="efb3b-206">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[<span data-ttu-id="efb3b-207">registres PS 1 \_ \_ 1 PS 1 2 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ 3 PS 1 \_ \_ \_ \_ 4</span><span class="sxs-lookup"><span data-stu-id="efb3b-207">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="efb3b-208">\_registres PS 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="efb3b-208">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="efb3b-209">\_registres PS 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="efb3b-209">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="efb3b-210">\_registres PS 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="efb3b-210">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




