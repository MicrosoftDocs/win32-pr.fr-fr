---
title: Modificateurs de Registre source du nuanceur de pixels
description: Utilisez les modificateurs de Registre source pour modifier la valeur lue dans un registre avant l’exécution d’une instruction.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12cfee533a71408a445d97a63bbd8b76b281236b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311491"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="17a4d-103">Modificateurs de Registre source du nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="17a4d-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="17a4d-104">Utilisez les modificateurs de Registre source pour modifier la valeur lue dans un registre avant l’exécution d’une instruction.</span><span class="sxs-lookup"><span data-stu-id="17a4d-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="17a4d-105">Le contenu d’un registre source reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="17a4d-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="17a4d-106">Les modificateurs sont utiles pour ajuster la plage de données de registre en vue de la préparation de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="17a4d-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="17a4d-107">Un ensemble de modificateurs appelés sélecteurs copie ou réplique les données à partir d’un seul canal (r, g, b, a) dans les autres canaux.</span><span class="sxs-lookup"><span data-stu-id="17a4d-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="17a4d-108">PS \_ 1 \_ 1-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="17a4d-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="17a4d-109">Ce tableau identifie les versions qui prennent en charge chaque modificateur :</span><span class="sxs-lookup"><span data-stu-id="17a4d-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="17a4d-110">Modificateurs de Registre source</span><span class="sxs-lookup"><span data-stu-id="17a4d-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="17a4d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17a4d-111">Syntax</span></span>         | <span data-ttu-id="17a4d-112">Version</span><span class="sxs-lookup"><span data-stu-id="17a4d-112">Version</span></span> |      |      |      |     |     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|-----|-----|
|                                                                                                              |                | <span data-ttu-id="17a4d-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="17a4d-113">1\_1</span></span>    | <span data-ttu-id="17a4d-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="17a4d-114">1\_2</span></span> | <span data-ttu-id="17a4d-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="17a4d-115">1\_3</span></span> | <span data-ttu-id="17a4d-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="17a4d-116">1\_4</span></span> |     |     |
| [<span data-ttu-id="17a4d-117">biais</span><span class="sxs-lookup"><span data-stu-id="17a4d-117">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="17a4d-118">inscrire un \_ décalage</span><span class="sxs-lookup"><span data-stu-id="17a4d-118">register\_bias</span></span> | <span data-ttu-id="17a4d-119">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-119">X</span></span>       | <span data-ttu-id="17a4d-120">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-120">X</span></span>    | <span data-ttu-id="17a4d-121">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-121">X</span></span>    | <span data-ttu-id="17a4d-122">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-122">X</span></span>    |     |     |
| [<span data-ttu-id="17a4d-123">alternatif</span><span class="sxs-lookup"><span data-stu-id="17a4d-123">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="17a4d-124">1-s’inscrire</span><span class="sxs-lookup"><span data-stu-id="17a4d-124">1 - register</span></span>   | <span data-ttu-id="17a4d-125">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-125">X</span></span>       | <span data-ttu-id="17a4d-126">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-126">X</span></span>    | <span data-ttu-id="17a4d-127">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-127">X</span></span>    | <span data-ttu-id="17a4d-128">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-128">X</span></span>    |     |     |
| [<span data-ttu-id="17a4d-129">negate</span><span class="sxs-lookup"><span data-stu-id="17a4d-129">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="17a4d-130">\- annuler</span><span class="sxs-lookup"><span data-stu-id="17a4d-130">\- register</span></span>    | <span data-ttu-id="17a4d-131">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-131">X</span></span>       | <span data-ttu-id="17a4d-132">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-132">X</span></span>    | <span data-ttu-id="17a4d-133">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-133">X</span></span>    | <span data-ttu-id="17a4d-134">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-134">X</span></span>    |     |     |
| [<span data-ttu-id="17a4d-135">mettre à l’échelle par 2</span><span class="sxs-lookup"><span data-stu-id="17a4d-135">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="17a4d-136">inscrire \_ x2</span><span class="sxs-lookup"><span data-stu-id="17a4d-136">register\_x2</span></span>   |         |      |      | <span data-ttu-id="17a4d-137">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-137">X</span></span>    |     |     |
| [<span data-ttu-id="17a4d-138">mise à l’échelle signée</span><span class="sxs-lookup"><span data-stu-id="17a4d-138">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="17a4d-139">inscrire \_ BX2</span><span class="sxs-lookup"><span data-stu-id="17a4d-139">register\_bx2</span></span>  | <span data-ttu-id="17a4d-140">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-140">X</span></span>       | <span data-ttu-id="17a4d-141">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-141">X</span></span>    | <span data-ttu-id="17a4d-142">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-142">X</span></span>    | <span data-ttu-id="17a4d-143">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-143">X</span></span>    |     |     |
| [<span data-ttu-id="17a4d-144">modificateurs texld et texcrd</span><span class="sxs-lookup"><span data-stu-id="17a4d-144">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="17a4d-145">inscrire \_ d\*</span><span class="sxs-lookup"><span data-stu-id="17a4d-145">register\_d\*</span></span>  | <span data-ttu-id="17a4d-146">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-146">X</span></span>       | <span data-ttu-id="17a4d-147">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-147">X</span></span>    | <span data-ttu-id="17a4d-148">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-148">X</span></span>    | <span data-ttu-id="17a4d-149">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-149">X</span></span>    |     |     |
| [<span data-ttu-id="17a4d-150">Registre source swizzling</span><span class="sxs-lookup"><span data-stu-id="17a4d-150">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="17a4d-151">Register. XYZW</span><span class="sxs-lookup"><span data-stu-id="17a4d-151">register.xyzw</span></span>  | <span data-ttu-id="17a4d-152">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-152">X</span></span>       | <span data-ttu-id="17a4d-153">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-153">X</span></span>    | <span data-ttu-id="17a4d-154">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-154">X</span></span>    | <span data-ttu-id="17a4d-155">X</span><span class="sxs-lookup"><span data-stu-id="17a4d-155">X</span></span>    |     |     |



 

<span data-ttu-id="17a4d-156">Les modificateurs de Registre source ne peuvent être utilisés que sur des instructions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="17a4d-156">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="17a4d-157">Elles ne peuvent pas être utilisées sur des instructions d’adresse de texture.</span><span class="sxs-lookup"><span data-stu-id="17a4d-157">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="17a4d-158">L’exception est le modificateur [Scale de 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) .</span><span class="sxs-lookup"><span data-stu-id="17a4d-158">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="17a4d-159">Pour la version 1 \_ 1, la mise à l’échelle signée peut être utilisée sur l’argument source de toute \* instruction texm.</span><span class="sxs-lookup"><span data-stu-id="17a4d-159">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="17a4d-160">Pour la version 1 \_ 2 ou 1 \_ 3, l’échelle signée peut être utilisée sur l’argument source d’une instruction d’adresse de texture.</span><span class="sxs-lookup"><span data-stu-id="17a4d-160">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="17a4d-161">Restrictions spécifiques aux modificateurs :</span><span class="sxs-lookup"><span data-stu-id="17a4d-161">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="17a4d-162">L’inverse peut être associé à l’écart, à la mise à l’échelle signée ou au modificateur scalex2.</span><span class="sxs-lookup"><span data-stu-id="17a4d-162">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="17a4d-163">En cas de combinaison, la négation est exécutée en dernier.</span><span class="sxs-lookup"><span data-stu-id="17a4d-163">When combined, negate is run last.</span></span>
-   <span data-ttu-id="17a4d-164">Inverser ne peut pas être combiné avec un autre modificateur.</span><span class="sxs-lookup"><span data-stu-id="17a4d-164">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="17a4d-165">Inverser, inverser, écarter, mettre à l’échelle signée et scalex2 peuvent être combinés avec l’un des sélecteurs.</span><span class="sxs-lookup"><span data-stu-id="17a4d-165">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="17a4d-166">Les modificateurs de Registre source ne doivent pas être utilisés sur des registres constants, car ils entraînent des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="17a4d-166">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="17a4d-167">Pour la version 1 \_ 4, les modificateurs sur les constantes ne sont pas autorisés et ne pourront pas être validés.</span><span class="sxs-lookup"><span data-stu-id="17a4d-167">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="17a4d-168">PS \_ 2 \_ 0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="17a4d-168">ps\_2\_0 and Above</span></span>

<span data-ttu-id="17a4d-169">Pour la version PS \_ 2 \_ et les versions, le nombre de modificateurs a été simplifié.</span><span class="sxs-lookup"><span data-stu-id="17a4d-169">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="17a4d-170">Negate</span><span class="sxs-lookup"><span data-stu-id="17a4d-170">Negate</span></span>

<span data-ttu-id="17a4d-171">Nie le contenu du Registre source.</span><span class="sxs-lookup"><span data-stu-id="17a4d-171">Negate the contents of the source register.</span></span>



| <span data-ttu-id="17a4d-172">Modificateur de composant</span><span class="sxs-lookup"><span data-stu-id="17a4d-172">Component modifier</span></span> | <span data-ttu-id="17a4d-173">Description</span><span class="sxs-lookup"><span data-stu-id="17a4d-173">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="17a4d-174">\- r</span><span class="sxs-lookup"><span data-stu-id="17a4d-174">\- r</span></span>               | <span data-ttu-id="17a4d-175">Négation source</span><span class="sxs-lookup"><span data-stu-id="17a4d-175">Source negation</span></span> |



 

<span data-ttu-id="17a4d-176">Le modificateur de négation ne peut pas être utilisé dans le deuxième Registre source de ces instructions : [M3X2-PS](m3x2---ps.md), [M3x3-](m3x3---ps.md)PS, [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)et [M4X4-PS](m4x4---ps.md).</span><span class="sxs-lookup"><span data-stu-id="17a4d-176">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="17a4d-177">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="17a4d-177">Pixel shader versions</span></span> | <span data-ttu-id="17a4d-178">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17a4d-178">2\_0</span></span> | <span data-ttu-id="17a4d-179">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="17a4d-179">2\_x</span></span> | <span data-ttu-id="17a4d-180">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="17a4d-180">2\_sw</span></span> | <span data-ttu-id="17a4d-181">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17a4d-181">3\_0</span></span> | <span data-ttu-id="17a4d-182">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="17a4d-182">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="17a4d-183">x</span><span class="sxs-lookup"><span data-stu-id="17a4d-183">x</span></span>    | <span data-ttu-id="17a4d-184">x</span><span class="sxs-lookup"><span data-stu-id="17a4d-184">x</span></span>    | <span data-ttu-id="17a4d-185">x</span><span class="sxs-lookup"><span data-stu-id="17a4d-185">x</span></span>     | <span data-ttu-id="17a4d-186">x</span><span class="sxs-lookup"><span data-stu-id="17a4d-186">x</span></span>    | <span data-ttu-id="17a4d-187">x</span><span class="sxs-lookup"><span data-stu-id="17a4d-187">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="17a4d-188">Valeur absolue</span><span class="sxs-lookup"><span data-stu-id="17a4d-188">Absolute Value</span></span>

<span data-ttu-id="17a4d-189">Prenez la valeur absolue du Registre.</span><span class="sxs-lookup"><span data-stu-id="17a4d-189">Take the absolute value of the register.</span></span>



| <span data-ttu-id="17a4d-190">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="17a4d-190">Pixel shader versions</span></span> | <span data-ttu-id="17a4d-191">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17a4d-191">2\_0</span></span> | <span data-ttu-id="17a4d-192">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="17a4d-192">2\_x</span></span> | <span data-ttu-id="17a4d-193">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="17a4d-193">2\_sw</span></span> | <span data-ttu-id="17a4d-194">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17a4d-194">3\_0</span></span> | <span data-ttu-id="17a4d-195">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="17a4d-195">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="17a4d-196">abs</span><span class="sxs-lookup"><span data-stu-id="17a4d-196">abs</span></span>                   |      |      |       | <span data-ttu-id="17a4d-197">x</span><span class="sxs-lookup"><span data-stu-id="17a4d-197">x</span></span>    | <span data-ttu-id="17a4d-198">x</span><span class="sxs-lookup"><span data-stu-id="17a4d-198">x</span></span>     |



 

<span data-ttu-id="17a4d-199">Si un nuanceur de version 3 lit à partir d’un ou de plusieurs registres à virgule flottante constants (c \# ), l’une des conditions suivantes doit être vraie.</span><span class="sxs-lookup"><span data-stu-id="17a4d-199">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="17a4d-200">Tous les registres à virgule flottante constantes doivent utiliser le modificateur ABS.</span><span class="sxs-lookup"><span data-stu-id="17a4d-200">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="17a4d-201">Aucun des registres à virgule flottante constantes ne peut utiliser le modificateur ABS.</span><span class="sxs-lookup"><span data-stu-id="17a4d-201">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17a4d-202">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17a4d-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17a4d-203">Modificateurs de registre de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="17a4d-203">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




