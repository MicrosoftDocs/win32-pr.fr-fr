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
ms.openlocfilehash: a9dd4476dd7a1a885edb2e62a29b5127f5ff0a14
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129676"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="2955a-103">Modificateurs de Registre source du nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="2955a-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="2955a-104">Utilisez les modificateurs de Registre source pour modifier la valeur lue dans un registre avant l’exécution d’une instruction.</span><span class="sxs-lookup"><span data-stu-id="2955a-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="2955a-105">Le contenu d’un registre source reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="2955a-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="2955a-106">Les modificateurs sont utiles pour ajuster la plage de données de registre en vue de la préparation de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="2955a-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="2955a-107">Un ensemble de modificateurs appelés sélecteurs copie ou réplique les données à partir d’un seul canal (r, g, b, a) dans les autres canaux.</span><span class="sxs-lookup"><span data-stu-id="2955a-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="2955a-108">PS \_ 1 \_ 1-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="2955a-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="2955a-109">Ce tableau identifie les versions qui prennent en charge chaque modificateur :</span><span class="sxs-lookup"><span data-stu-id="2955a-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="2955a-110">Modificateurs de Registre source</span><span class="sxs-lookup"><span data-stu-id="2955a-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="2955a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2955a-111">Syntax</span></span>         | <span data-ttu-id="2955a-112">Version 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="2955a-112">Version 1\_1</span></span> | <span data-ttu-id="2955a-113">Version 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="2955a-113">Version 1\_2</span></span>     | <span data-ttu-id="2955a-114">Version 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2955a-114">Version 1\_3</span></span>     | <span data-ttu-id="2955a-115">Version 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="2955a-115">Version 1\_4</span></span>     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|
| [<span data-ttu-id="2955a-116">biais</span><span class="sxs-lookup"><span data-stu-id="2955a-116">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="2955a-117">inscrire un \_ décalage</span><span class="sxs-lookup"><span data-stu-id="2955a-117">register\_bias</span></span> | <span data-ttu-id="2955a-118">X</span><span class="sxs-lookup"><span data-stu-id="2955a-118">X</span></span>       | <span data-ttu-id="2955a-119">X</span><span class="sxs-lookup"><span data-stu-id="2955a-119">X</span></span>    | <span data-ttu-id="2955a-120">X</span><span class="sxs-lookup"><span data-stu-id="2955a-120">X</span></span>    | <span data-ttu-id="2955a-121">X</span><span class="sxs-lookup"><span data-stu-id="2955a-121">X</span></span>    |
| [<span data-ttu-id="2955a-122">alternatif</span><span class="sxs-lookup"><span data-stu-id="2955a-122">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="2955a-123">1-s’inscrire</span><span class="sxs-lookup"><span data-stu-id="2955a-123">1 - register</span></span>   | <span data-ttu-id="2955a-124">X</span><span class="sxs-lookup"><span data-stu-id="2955a-124">X</span></span>       | <span data-ttu-id="2955a-125">X</span><span class="sxs-lookup"><span data-stu-id="2955a-125">X</span></span>    | <span data-ttu-id="2955a-126">X</span><span class="sxs-lookup"><span data-stu-id="2955a-126">X</span></span>    | <span data-ttu-id="2955a-127">X</span><span class="sxs-lookup"><span data-stu-id="2955a-127">X</span></span>    |
| [<span data-ttu-id="2955a-128">negate</span><span class="sxs-lookup"><span data-stu-id="2955a-128">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="2955a-129">\- annuler</span><span class="sxs-lookup"><span data-stu-id="2955a-129">\- register</span></span>    | <span data-ttu-id="2955a-130">X</span><span class="sxs-lookup"><span data-stu-id="2955a-130">X</span></span>       | <span data-ttu-id="2955a-131">X</span><span class="sxs-lookup"><span data-stu-id="2955a-131">X</span></span>    | <span data-ttu-id="2955a-132">X</span><span class="sxs-lookup"><span data-stu-id="2955a-132">X</span></span>    | <span data-ttu-id="2955a-133">X</span><span class="sxs-lookup"><span data-stu-id="2955a-133">X</span></span>    |
| [<span data-ttu-id="2955a-134">mettre à l’échelle par 2</span><span class="sxs-lookup"><span data-stu-id="2955a-134">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="2955a-135">inscrire \_ x2</span><span class="sxs-lookup"><span data-stu-id="2955a-135">register\_x2</span></span>   |         |      |      | <span data-ttu-id="2955a-136">X</span><span class="sxs-lookup"><span data-stu-id="2955a-136">X</span></span>    |
| [<span data-ttu-id="2955a-137">mise à l’échelle signée</span><span class="sxs-lookup"><span data-stu-id="2955a-137">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="2955a-138">inscrire \_ BX2</span><span class="sxs-lookup"><span data-stu-id="2955a-138">register\_bx2</span></span>  | <span data-ttu-id="2955a-139">X</span><span class="sxs-lookup"><span data-stu-id="2955a-139">X</span></span>       | <span data-ttu-id="2955a-140">X</span><span class="sxs-lookup"><span data-stu-id="2955a-140">X</span></span>    | <span data-ttu-id="2955a-141">X</span><span class="sxs-lookup"><span data-stu-id="2955a-141">X</span></span>    | <span data-ttu-id="2955a-142">X</span><span class="sxs-lookup"><span data-stu-id="2955a-142">X</span></span>    |
| [<span data-ttu-id="2955a-143">modificateurs texld et texcrd</span><span class="sxs-lookup"><span data-stu-id="2955a-143">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="2955a-144">inscrire \_ d\*</span><span class="sxs-lookup"><span data-stu-id="2955a-144">register\_d\*</span></span>  | <span data-ttu-id="2955a-145">X</span><span class="sxs-lookup"><span data-stu-id="2955a-145">X</span></span>       | <span data-ttu-id="2955a-146">X</span><span class="sxs-lookup"><span data-stu-id="2955a-146">X</span></span>    | <span data-ttu-id="2955a-147">X</span><span class="sxs-lookup"><span data-stu-id="2955a-147">X</span></span>    | <span data-ttu-id="2955a-148">X</span><span class="sxs-lookup"><span data-stu-id="2955a-148">X</span></span>    |
| [<span data-ttu-id="2955a-149">Registre source swizzling</span><span class="sxs-lookup"><span data-stu-id="2955a-149">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="2955a-150">Register. XYZW</span><span class="sxs-lookup"><span data-stu-id="2955a-150">register.xyzw</span></span>  | <span data-ttu-id="2955a-151">X</span><span class="sxs-lookup"><span data-stu-id="2955a-151">X</span></span>       | <span data-ttu-id="2955a-152">X</span><span class="sxs-lookup"><span data-stu-id="2955a-152">X</span></span>    | <span data-ttu-id="2955a-153">X</span><span class="sxs-lookup"><span data-stu-id="2955a-153">X</span></span>    | <span data-ttu-id="2955a-154">X</span><span class="sxs-lookup"><span data-stu-id="2955a-154">X</span></span>    |



 

<span data-ttu-id="2955a-155">Les modificateurs de Registre source ne peuvent être utilisés que sur des instructions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="2955a-155">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="2955a-156">Elles ne peuvent pas être utilisées sur des instructions d’adresse de texture.</span><span class="sxs-lookup"><span data-stu-id="2955a-156">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="2955a-157">L’exception est le modificateur [Scale de 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) .</span><span class="sxs-lookup"><span data-stu-id="2955a-157">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="2955a-158">Pour la version 1 \_ 1, la mise à l’échelle signée peut être utilisée sur l’argument source de toute \* instruction texm.</span><span class="sxs-lookup"><span data-stu-id="2955a-158">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="2955a-159">Pour la version 1 \_ 2 ou 1 \_ 3, l’échelle signée peut être utilisée sur l’argument source d’une instruction d’adresse de texture.</span><span class="sxs-lookup"><span data-stu-id="2955a-159">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="2955a-160">Restrictions spécifiques aux modificateurs :</span><span class="sxs-lookup"><span data-stu-id="2955a-160">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="2955a-161">L’inverse peut être associé à l’écart, à la mise à l’échelle signée ou au modificateur scalex2.</span><span class="sxs-lookup"><span data-stu-id="2955a-161">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="2955a-162">En cas de combinaison, la négation est exécutée en dernier.</span><span class="sxs-lookup"><span data-stu-id="2955a-162">When combined, negate is run last.</span></span>
-   <span data-ttu-id="2955a-163">Inverser ne peut pas être combiné avec un autre modificateur.</span><span class="sxs-lookup"><span data-stu-id="2955a-163">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="2955a-164">Inverser, inverser, écarter, mettre à l’échelle signée et scalex2 peuvent être combinés avec l’un des sélecteurs.</span><span class="sxs-lookup"><span data-stu-id="2955a-164">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="2955a-165">Les modificateurs de Registre source ne doivent pas être utilisés sur des registres constants, car ils entraînent des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="2955a-165">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="2955a-166">Pour la version 1 \_ 4, les modificateurs sur les constantes ne sont pas autorisés et ne pourront pas être validés.</span><span class="sxs-lookup"><span data-stu-id="2955a-166">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="2955a-167">PS \_ 2 \_ 0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="2955a-167">ps\_2\_0 and Above</span></span>

<span data-ttu-id="2955a-168">Pour la version PS \_ 2 \_ et les versions, le nombre de modificateurs a été simplifié.</span><span class="sxs-lookup"><span data-stu-id="2955a-168">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="2955a-169">Negate</span><span class="sxs-lookup"><span data-stu-id="2955a-169">Negate</span></span>

<span data-ttu-id="2955a-170">Nie le contenu du Registre source.</span><span class="sxs-lookup"><span data-stu-id="2955a-170">Negate the contents of the source register.</span></span>



| <span data-ttu-id="2955a-171">Modificateur de composant</span><span class="sxs-lookup"><span data-stu-id="2955a-171">Component modifier</span></span> | <span data-ttu-id="2955a-172">Description</span><span class="sxs-lookup"><span data-stu-id="2955a-172">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="2955a-173">\- r</span><span class="sxs-lookup"><span data-stu-id="2955a-173">\- r</span></span>               | <span data-ttu-id="2955a-174">Négation source</span><span class="sxs-lookup"><span data-stu-id="2955a-174">Source negation</span></span> |



 

<span data-ttu-id="2955a-175">Le modificateur de négation ne peut pas être utilisé dans le deuxième Registre source de ces instructions : [M3X2-PS](m3x2---ps.md), [M3x3-](m3x3---ps.md)PS, [M3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)et [M4X4-PS](m4x4---ps.md).</span><span class="sxs-lookup"><span data-stu-id="2955a-175">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="2955a-176">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="2955a-176">Pixel shader versions</span></span> | <span data-ttu-id="2955a-177">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2955a-177">2\_0</span></span> | <span data-ttu-id="2955a-178">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2955a-178">2\_x</span></span> | <span data-ttu-id="2955a-179">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2955a-179">2\_sw</span></span> | <span data-ttu-id="2955a-180">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2955a-180">3\_0</span></span> | <span data-ttu-id="2955a-181">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2955a-181">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="2955a-182">x</span><span class="sxs-lookup"><span data-stu-id="2955a-182">x</span></span>    | <span data-ttu-id="2955a-183">x</span><span class="sxs-lookup"><span data-stu-id="2955a-183">x</span></span>    | <span data-ttu-id="2955a-184">x</span><span class="sxs-lookup"><span data-stu-id="2955a-184">x</span></span>     | <span data-ttu-id="2955a-185">x</span><span class="sxs-lookup"><span data-stu-id="2955a-185">x</span></span>    | <span data-ttu-id="2955a-186">x</span><span class="sxs-lookup"><span data-stu-id="2955a-186">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="2955a-187">Valeur absolue</span><span class="sxs-lookup"><span data-stu-id="2955a-187">Absolute Value</span></span>

<span data-ttu-id="2955a-188">Prenez la valeur absolue du Registre.</span><span class="sxs-lookup"><span data-stu-id="2955a-188">Take the absolute value of the register.</span></span>



| <span data-ttu-id="2955a-189">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="2955a-189">Pixel shader versions</span></span> | <span data-ttu-id="2955a-190">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2955a-190">2\_0</span></span> | <span data-ttu-id="2955a-191">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2955a-191">2\_x</span></span> | <span data-ttu-id="2955a-192">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2955a-192">2\_sw</span></span> | <span data-ttu-id="2955a-193">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2955a-193">3\_0</span></span> | <span data-ttu-id="2955a-194">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2955a-194">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="2955a-195">abs</span><span class="sxs-lookup"><span data-stu-id="2955a-195">abs</span></span>                   |      |      |       | <span data-ttu-id="2955a-196">x</span><span class="sxs-lookup"><span data-stu-id="2955a-196">x</span></span>    | <span data-ttu-id="2955a-197">x</span><span class="sxs-lookup"><span data-stu-id="2955a-197">x</span></span>     |



 

<span data-ttu-id="2955a-198">Si un nuanceur de version 3 lit à partir d’un ou de plusieurs registres à virgule flottante constants (c \# ), l’une des conditions suivantes doit être vraie.</span><span class="sxs-lookup"><span data-stu-id="2955a-198">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="2955a-199">Tous les registres à virgule flottante constantes doivent utiliser le modificateur ABS.</span><span class="sxs-lookup"><span data-stu-id="2955a-199">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="2955a-200">Aucun des registres à virgule flottante constantes ne peut utiliser le modificateur ABS.</span><span class="sxs-lookup"><span data-stu-id="2955a-200">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2955a-201">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2955a-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2955a-202">Modificateurs de registre de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="2955a-202">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




