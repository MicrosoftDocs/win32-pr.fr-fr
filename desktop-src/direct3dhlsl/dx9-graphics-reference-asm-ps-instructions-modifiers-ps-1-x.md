---
title: Modificateurs pour ps_1_X
description: Les modificateurs d’instruction affectent le résultat de l’instruction avant qu’elle ne soit écrite dans le registre de destination.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbc8a9b13f7ffc29cf84bc839409f29bea6c8c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840842"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="49f8d-103">Modificateurs pour PS \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="49f8d-103">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="49f8d-104">Les modificateurs d’instruction affectent le résultat de l’instruction avant qu’elle ne soit écrite dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="49f8d-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="49f8d-105">Par exemple, utilisez-les pour multiplier ou diviser le résultat par un facteur de deux, ou pour fixer le résultat entre zéro et un.</span><span class="sxs-lookup"><span data-stu-id="49f8d-105">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="49f8d-106">Les modificateurs d’instruction sont appliqués après l’exécution de l’instruction mais avant l’écriture du résultat dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="49f8d-106">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="49f8d-107">La liste des modificateurs est indiquée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="49f8d-107">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="49f8d-108">Modificateur</span><span class="sxs-lookup"><span data-stu-id="49f8d-108">Modifier</span></span> | <span data-ttu-id="49f8d-109">Description</span><span class="sxs-lookup"><span data-stu-id="49f8d-109">Description</span></span>                   | <span data-ttu-id="49f8d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49f8d-110">Syntax</span></span>           | <span data-ttu-id="49f8d-111">Version</span><span class="sxs-lookup"><span data-stu-id="49f8d-111">Version</span></span> |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | <span data-ttu-id="49f8d-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="49f8d-112">1\_1</span></span>    | <span data-ttu-id="49f8d-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="49f8d-113">1\_2</span></span> | <span data-ttu-id="49f8d-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="49f8d-114">1\_3</span></span> | <span data-ttu-id="49f8d-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="49f8d-115">1\_4</span></span> |
| <span data-ttu-id="49f8d-116">\_x2</span><span class="sxs-lookup"><span data-stu-id="49f8d-116">\_x2</span></span>     | <span data-ttu-id="49f8d-117">Multiplier par 2</span><span class="sxs-lookup"><span data-stu-id="49f8d-117">Multiply by 2</span></span>                 | <span data-ttu-id="49f8d-118">instruction \_ x2</span><span class="sxs-lookup"><span data-stu-id="49f8d-118">instruction\_x2</span></span>  | <span data-ttu-id="49f8d-119">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-119">X</span></span>       | <span data-ttu-id="49f8d-120">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-120">X</span></span>    | <span data-ttu-id="49f8d-121">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-121">X</span></span>    | <span data-ttu-id="49f8d-122">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-122">X</span></span>    |
| <span data-ttu-id="49f8d-123">\_x4</span><span class="sxs-lookup"><span data-stu-id="49f8d-123">\_x4</span></span>     | <span data-ttu-id="49f8d-124">Multiplier par 4</span><span class="sxs-lookup"><span data-stu-id="49f8d-124">Multiply by 4</span></span>                 | <span data-ttu-id="49f8d-125">instruction \_ X4</span><span class="sxs-lookup"><span data-stu-id="49f8d-125">instruction\_x4</span></span>  | <span data-ttu-id="49f8d-126">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-126">X</span></span>       | <span data-ttu-id="49f8d-127">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-127">X</span></span>    | <span data-ttu-id="49f8d-128">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-128">X</span></span>    | <span data-ttu-id="49f8d-129">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-129">X</span></span>    |
| <span data-ttu-id="49f8d-130">\_8</span><span class="sxs-lookup"><span data-stu-id="49f8d-130">\_x8</span></span>     | <span data-ttu-id="49f8d-131">Multiplier par 8</span><span class="sxs-lookup"><span data-stu-id="49f8d-131">Multiply by 8</span></span>                 | <span data-ttu-id="49f8d-132">instruction \_ x8</span><span class="sxs-lookup"><span data-stu-id="49f8d-132">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="49f8d-133">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-133">X</span></span>    |
| <span data-ttu-id="49f8d-134">\_D2</span><span class="sxs-lookup"><span data-stu-id="49f8d-134">\_d2</span></span>     | <span data-ttu-id="49f8d-135">Division par 2</span><span class="sxs-lookup"><span data-stu-id="49f8d-135">Divide by 2</span></span>                   | <span data-ttu-id="49f8d-136">instruction \_ D2</span><span class="sxs-lookup"><span data-stu-id="49f8d-136">instruction\_d2</span></span>  | <span data-ttu-id="49f8d-137">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-137">X</span></span>       | <span data-ttu-id="49f8d-138">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-138">X</span></span>    | <span data-ttu-id="49f8d-139">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-139">X</span></span>    | <span data-ttu-id="49f8d-140">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-140">X</span></span>    |
| <span data-ttu-id="49f8d-141">\_D4</span><span class="sxs-lookup"><span data-stu-id="49f8d-141">\_d4</span></span>     | <span data-ttu-id="49f8d-142">Division par 4</span><span class="sxs-lookup"><span data-stu-id="49f8d-142">Divide by 4</span></span>                   | <span data-ttu-id="49f8d-143">instruction \_ D4</span><span class="sxs-lookup"><span data-stu-id="49f8d-143">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="49f8d-144">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-144">X</span></span>    |
| <span data-ttu-id="49f8d-145">\_D8</span><span class="sxs-lookup"><span data-stu-id="49f8d-145">\_d8</span></span>     | <span data-ttu-id="49f8d-146">Division par 8</span><span class="sxs-lookup"><span data-stu-id="49f8d-146">Divide by 8</span></span>                   | <span data-ttu-id="49f8d-147">instruction \_ D8</span><span class="sxs-lookup"><span data-stu-id="49f8d-147">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="49f8d-148">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-148">X</span></span>    |
| <span data-ttu-id="49f8d-149">\_sot</span><span class="sxs-lookup"><span data-stu-id="49f8d-149">\_sat</span></span>    | <span data-ttu-id="49f8d-150">Saturation (Clamp de 0 et 1)</span><span class="sxs-lookup"><span data-stu-id="49f8d-150">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="49f8d-151">instruction \_ SAT</span><span class="sxs-lookup"><span data-stu-id="49f8d-151">instruction\_sat</span></span> | <span data-ttu-id="49f8d-152">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-152">X</span></span>       | <span data-ttu-id="49f8d-153">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-153">X</span></span>    | <span data-ttu-id="49f8d-154">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-154">X</span></span>    | <span data-ttu-id="49f8d-155">X</span><span class="sxs-lookup"><span data-stu-id="49f8d-155">X</span></span>    |



 

-   <span data-ttu-id="49f8d-156">Le modificateur Multiply multiplie les données de Registre par une puissance de deux après leur lecture.</span><span class="sxs-lookup"><span data-stu-id="49f8d-156">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="49f8d-157">C’est le même qu’un décalage vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="49f8d-157">This is the same as a shift left.</span></span>
-   <span data-ttu-id="49f8d-158">Le modificateur de division divise les données de Registre par une puissance de deux après leur lecture.</span><span class="sxs-lookup"><span data-stu-id="49f8d-158">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="49f8d-159">C’est le même qu’un décalage vers la droite.</span><span class="sxs-lookup"><span data-stu-id="49f8d-159">This is the same as a shift right.</span></span>
-   <span data-ttu-id="49f8d-160">Le modificateur de saturation fixe la plage des valeurs de registre de zéro à un.</span><span class="sxs-lookup"><span data-stu-id="49f8d-160">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="49f8d-161">Les modificateurs d’instruction peuvent être utilisés sur des instructions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="49f8d-161">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="49f8d-162">Elles ne peuvent pas être utilisées dans les instructions d’adresse de texture.</span><span class="sxs-lookup"><span data-stu-id="49f8d-162">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="49f8d-163">Multiplier (modificateur)</span><span class="sxs-lookup"><span data-stu-id="49f8d-163">Multiply modifier</span></span>

<span data-ttu-id="49f8d-164">Cet exemple charge le registre de destination (dest) avec la somme des deux couleurs dans les opérandes sources (src0 et src1) et multiplie le résultat par deux.</span><span class="sxs-lookup"><span data-stu-id="49f8d-164">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="49f8d-165">Cet exemple combine deux modificateurs d’instruction.</span><span class="sxs-lookup"><span data-stu-id="49f8d-165">This example combines two instruction modifiers.</span></span> <span data-ttu-id="49f8d-166">En premier lieu, deux couleurs dans les opérandes sources (src0 et src1) sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="49f8d-166">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="49f8d-167">Le résultat est ensuite multiplié par deux et placé entre 0,0 et 1,0 pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="49f8d-167">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="49f8d-168">Le résultat est enregistré dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="49f8d-168">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="49f8d-169">Diviser (modificateur)</span><span class="sxs-lookup"><span data-stu-id="49f8d-169">Divide modifier</span></span>

<span data-ttu-id="49f8d-170">Cet exemple charge le registre de destination (dest) avec la somme des deux couleurs dans les opérandes sources (src0 et src1) et divise le résultat par deux.</span><span class="sxs-lookup"><span data-stu-id="49f8d-170">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="49f8d-171">Saturation (modificateur)</span><span class="sxs-lookup"><span data-stu-id="49f8d-171">Saturate modifier</span></span>

<span data-ttu-id="49f8d-172">Pour les instructions arithmétiques, le modificateur de saturation fixe le résultat de cette instruction dans la plage 0,0 à 1,0 pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="49f8d-172">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="49f8d-173">L’exemple suivant montre comment utiliser ce modificateur d’instruction.</span><span class="sxs-lookup"><span data-stu-id="49f8d-173">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="49f8d-174">Cette opération se produit après n’importe quel modificateur d’instruction Multiply ou de division.</span><span class="sxs-lookup"><span data-stu-id="49f8d-174">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="49f8d-175">\_la SAT est le plus souvent utilisé pour brider les résultats du produit scalaire.</span><span class="sxs-lookup"><span data-stu-id="49f8d-175">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="49f8d-176">Toutefois, elle permet également une émulation cohérente des méthodes multipasses dans lesquelles la mémoire tampon de trame est toujours comprise entre 0 et 1, et de la syntaxe de multitexture DirectX 6 et 7,0, dans laquelle la saturation est définie pour se produire à chaque étape.</span><span class="sxs-lookup"><span data-stu-id="49f8d-176">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="49f8d-177">Cet exemple charge le registre de destination (dest) avec la somme des deux couleurs dans les opérandes sources (src0 et src1) et fixe le résultat dans la plage 0,0 à 1,0 pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="49f8d-177">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="49f8d-178">Cet exemple combine deux modificateurs d’instruction.</span><span class="sxs-lookup"><span data-stu-id="49f8d-178">This example combines two instruction modifiers.</span></span> <span data-ttu-id="49f8d-179">En premier lieu, deux couleurs dans les opérandes sources (src0 et src1) sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="49f8d-179">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="49f8d-180">Le résultat est multiplié par deux et est ancré entre 0,0 et 1,0 pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="49f8d-180">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="49f8d-181">Le résultat est enregistré dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="49f8d-181">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="49f8d-182">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49f8d-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49f8d-183">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="49f8d-183">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




