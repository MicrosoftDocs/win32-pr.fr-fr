---
title: Modificateurs pour ps_1_X
description: Les modificateurs d’instruction affectent le résultat de l’instruction avant qu’elle ne soit écrite dans le registre de destination. En savoir plus sur les modificateurs pour ps_1_X.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c97196040a8f5f9888cb2fb354dcc18ca3743c7
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988724"
---
# <a name="modifiers-for-ps_1_x"></a><span data-ttu-id="0e602-104">Modificateurs pour PS \_ 1 \_ X</span><span class="sxs-lookup"><span data-stu-id="0e602-104">Modifiers for ps\_1\_X</span></span>

<span data-ttu-id="0e602-105">Les modificateurs d’instruction affectent le résultat de l’instruction avant qu’elle ne soit écrite dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="0e602-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span> <span data-ttu-id="0e602-106">Par exemple, utilisez-les pour multiplier ou diviser le résultat par un facteur de deux, ou pour fixer le résultat entre zéro et un.</span><span class="sxs-lookup"><span data-stu-id="0e602-106">For instance, use them to multiply or divide the result by a factor of two, or to clamp the result between zero and one.</span></span> <span data-ttu-id="0e602-107">Les modificateurs d’instruction sont appliqués après l’exécution de l’instruction mais avant l’écriture du résultat dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="0e602-107">Instruction modifiers are applied after the instruction runs but before writing the result to the destination register.</span></span>

<span data-ttu-id="0e602-108">La liste des modificateurs est indiquée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0e602-108">A list of the modifiers is shown below.</span></span>



| <span data-ttu-id="0e602-109">Modificateur</span><span class="sxs-lookup"><span data-stu-id="0e602-109">Modifier</span></span> | <span data-ttu-id="0e602-110">Description</span><span class="sxs-lookup"><span data-stu-id="0e602-110">Description</span></span>                   | <span data-ttu-id="0e602-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e602-111">Syntax</span></span>           | <span data-ttu-id="0e602-112">Version</span><span class="sxs-lookup"><span data-stu-id="0e602-112">Version</span></span> |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | <span data-ttu-id="0e602-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="0e602-113">1\_1</span></span>    | <span data-ttu-id="0e602-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="0e602-114">1\_2</span></span> | <span data-ttu-id="0e602-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0e602-115">1\_3</span></span> | <span data-ttu-id="0e602-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="0e602-116">1\_4</span></span> |
| <span data-ttu-id="0e602-117">\_x2</span><span class="sxs-lookup"><span data-stu-id="0e602-117">\_x2</span></span>     | <span data-ttu-id="0e602-118">Multiplier par 2</span><span class="sxs-lookup"><span data-stu-id="0e602-118">Multiply by 2</span></span>                 | <span data-ttu-id="0e602-119">instruction \_ x2</span><span class="sxs-lookup"><span data-stu-id="0e602-119">instruction\_x2</span></span>  | <span data-ttu-id="0e602-120">X</span><span class="sxs-lookup"><span data-stu-id="0e602-120">X</span></span>       | <span data-ttu-id="0e602-121">X</span><span class="sxs-lookup"><span data-stu-id="0e602-121">X</span></span>    | <span data-ttu-id="0e602-122">X</span><span class="sxs-lookup"><span data-stu-id="0e602-122">X</span></span>    | <span data-ttu-id="0e602-123">X</span><span class="sxs-lookup"><span data-stu-id="0e602-123">X</span></span>    |
| <span data-ttu-id="0e602-124">\_x4</span><span class="sxs-lookup"><span data-stu-id="0e602-124">\_x4</span></span>     | <span data-ttu-id="0e602-125">Multiplier par 4</span><span class="sxs-lookup"><span data-stu-id="0e602-125">Multiply by 4</span></span>                 | <span data-ttu-id="0e602-126">instruction \_ X4</span><span class="sxs-lookup"><span data-stu-id="0e602-126">instruction\_x4</span></span>  | <span data-ttu-id="0e602-127">X</span><span class="sxs-lookup"><span data-stu-id="0e602-127">X</span></span>       | <span data-ttu-id="0e602-128">X</span><span class="sxs-lookup"><span data-stu-id="0e602-128">X</span></span>    | <span data-ttu-id="0e602-129">X</span><span class="sxs-lookup"><span data-stu-id="0e602-129">X</span></span>    | <span data-ttu-id="0e602-130">X</span><span class="sxs-lookup"><span data-stu-id="0e602-130">X</span></span>    |
| <span data-ttu-id="0e602-131">\_8</span><span class="sxs-lookup"><span data-stu-id="0e602-131">\_x8</span></span>     | <span data-ttu-id="0e602-132">Multiplier par 8</span><span class="sxs-lookup"><span data-stu-id="0e602-132">Multiply by 8</span></span>                 | <span data-ttu-id="0e602-133">instruction \_ x8</span><span class="sxs-lookup"><span data-stu-id="0e602-133">instruction\_x8</span></span>  |         |      |      | <span data-ttu-id="0e602-134">X</span><span class="sxs-lookup"><span data-stu-id="0e602-134">X</span></span>    |
| <span data-ttu-id="0e602-135">\_D2</span><span class="sxs-lookup"><span data-stu-id="0e602-135">\_d2</span></span>     | <span data-ttu-id="0e602-136">Division par 2</span><span class="sxs-lookup"><span data-stu-id="0e602-136">Divide by 2</span></span>                   | <span data-ttu-id="0e602-137">instruction \_ D2</span><span class="sxs-lookup"><span data-stu-id="0e602-137">instruction\_d2</span></span>  | <span data-ttu-id="0e602-138">X</span><span class="sxs-lookup"><span data-stu-id="0e602-138">X</span></span>       | <span data-ttu-id="0e602-139">X</span><span class="sxs-lookup"><span data-stu-id="0e602-139">X</span></span>    | <span data-ttu-id="0e602-140">X</span><span class="sxs-lookup"><span data-stu-id="0e602-140">X</span></span>    | <span data-ttu-id="0e602-141">X</span><span class="sxs-lookup"><span data-stu-id="0e602-141">X</span></span>    |
| <span data-ttu-id="0e602-142">\_D4</span><span class="sxs-lookup"><span data-stu-id="0e602-142">\_d4</span></span>     | <span data-ttu-id="0e602-143">Division par 4</span><span class="sxs-lookup"><span data-stu-id="0e602-143">Divide by 4</span></span>                   | <span data-ttu-id="0e602-144">instruction \_ D4</span><span class="sxs-lookup"><span data-stu-id="0e602-144">instruction\_d4</span></span>  |         |      |      | <span data-ttu-id="0e602-145">X</span><span class="sxs-lookup"><span data-stu-id="0e602-145">X</span></span>    |
| <span data-ttu-id="0e602-146">\_D8</span><span class="sxs-lookup"><span data-stu-id="0e602-146">\_d8</span></span>     | <span data-ttu-id="0e602-147">Division par 8</span><span class="sxs-lookup"><span data-stu-id="0e602-147">Divide by 8</span></span>                   | <span data-ttu-id="0e602-148">instruction \_ D8</span><span class="sxs-lookup"><span data-stu-id="0e602-148">instruction\_d8</span></span>  |         |      |      | <span data-ttu-id="0e602-149">X</span><span class="sxs-lookup"><span data-stu-id="0e602-149">X</span></span>    |
| <span data-ttu-id="0e602-150">\_sot</span><span class="sxs-lookup"><span data-stu-id="0e602-150">\_sat</span></span>    | <span data-ttu-id="0e602-151">Saturation (Clamp de 0 et 1)</span><span class="sxs-lookup"><span data-stu-id="0e602-151">Saturate (clamp from 0 and 1)</span></span> | <span data-ttu-id="0e602-152">instruction \_ SAT</span><span class="sxs-lookup"><span data-stu-id="0e602-152">instruction\_sat</span></span> | <span data-ttu-id="0e602-153">X</span><span class="sxs-lookup"><span data-stu-id="0e602-153">X</span></span>       | <span data-ttu-id="0e602-154">X</span><span class="sxs-lookup"><span data-stu-id="0e602-154">X</span></span>    | <span data-ttu-id="0e602-155">X</span><span class="sxs-lookup"><span data-stu-id="0e602-155">X</span></span>    | <span data-ttu-id="0e602-156">X</span><span class="sxs-lookup"><span data-stu-id="0e602-156">X</span></span>    |



 

-   <span data-ttu-id="0e602-157">Le modificateur Multiply multiplie les données de Registre par une puissance de deux après leur lecture.</span><span class="sxs-lookup"><span data-stu-id="0e602-157">The multiply modifier multiplies the register data by a power of two after it is read.</span></span> <span data-ttu-id="0e602-158">C’est le même qu’un décalage vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="0e602-158">This is the same as a shift left.</span></span>
-   <span data-ttu-id="0e602-159">Le modificateur de division divise les données de Registre par une puissance de deux après leur lecture.</span><span class="sxs-lookup"><span data-stu-id="0e602-159">The divide modifier divides the register data by a power of two after it is read.</span></span> <span data-ttu-id="0e602-160">C’est le même qu’un décalage vers la droite.</span><span class="sxs-lookup"><span data-stu-id="0e602-160">This is the same as a shift right.</span></span>
-   <span data-ttu-id="0e602-161">Le modificateur de saturation fixe la plage des valeurs de registre de zéro à un.</span><span class="sxs-lookup"><span data-stu-id="0e602-161">The saturate modifier clamps the range of register values from zero to one.</span></span>

<span data-ttu-id="0e602-162">Les modificateurs d’instruction peuvent être utilisés sur des instructions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="0e602-162">Instruction modifiers can be used on arithmetic instructions.</span></span> <span data-ttu-id="0e602-163">Elles ne peuvent pas être utilisées dans les instructions d’adresse de texture.</span><span class="sxs-lookup"><span data-stu-id="0e602-163">They may not be used on texture address instructions.</span></span>

<span data-ttu-id="0e602-164">Multiplier (modificateur)</span><span class="sxs-lookup"><span data-stu-id="0e602-164">Multiply modifier</span></span>

<span data-ttu-id="0e602-165">Cet exemple charge le registre de destination (dest) avec la somme des deux couleurs dans les opérandes sources (src0 et src1) et multiplie le résultat par deux.</span><span class="sxs-lookup"><span data-stu-id="0e602-165">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and multiplies the result by two.</span></span>


```
add_x2 dest, src0, src1
```



<span data-ttu-id="0e602-166">Cet exemple combine deux modificateurs d’instruction.</span><span class="sxs-lookup"><span data-stu-id="0e602-166">This example combines two instruction modifiers.</span></span> <span data-ttu-id="0e602-167">En premier lieu, deux couleurs dans les opérandes sources (src0 et src1) sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="0e602-167">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="0e602-168">Le résultat est ensuite multiplié par deux et placé entre 0,0 et 1,0 pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="0e602-168">The result is then multiplied by two, and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="0e602-169">Le résultat est enregistré dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="0e602-169">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



<span data-ttu-id="0e602-170">Diviser (modificateur)</span><span class="sxs-lookup"><span data-stu-id="0e602-170">Divide modifier</span></span>

<span data-ttu-id="0e602-171">Cet exemple charge le registre de destination (dest) avec la somme des deux couleurs dans les opérandes sources (src0 et src1) et divise le résultat par deux.</span><span class="sxs-lookup"><span data-stu-id="0e602-171">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1) and divides the result by two.</span></span>


```
add_d2 dest, src0, src1
```



<span data-ttu-id="0e602-172">Saturation (modificateur)</span><span class="sxs-lookup"><span data-stu-id="0e602-172">Saturate modifier</span></span>

<span data-ttu-id="0e602-173">Pour les instructions arithmétiques, le modificateur de saturation fixe le résultat de cette instruction dans la plage 0,0 à 1,0 pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="0e602-173">For arithmetic instructions, the saturation modifier clamps the result of this instruction into the range 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="0e602-174">L’exemple suivant montre comment utiliser ce modificateur d’instruction.</span><span class="sxs-lookup"><span data-stu-id="0e602-174">The following example shows how to use this instruction modifier.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



<span data-ttu-id="0e602-175">Cette opération se produit après n’importe quel modificateur d’instruction Multiply ou de division.</span><span class="sxs-lookup"><span data-stu-id="0e602-175">This operation occurs after any multiply or divide instruction modifier.</span></span> <span data-ttu-id="0e602-176">\_la SAT est le plus souvent utilisé pour brider les résultats du produit scalaire.</span><span class="sxs-lookup"><span data-stu-id="0e602-176">\_sat is most often used to clamp dot product results.</span></span> <span data-ttu-id="0e602-177">Toutefois, elle permet également une émulation cohérente des méthodes multipasses dans lesquelles la mémoire tampon de trame est toujours comprise entre 0 et 1, et de la syntaxe de multitexture DirectX 6 et 7,0, dans laquelle la saturation est définie pour se produire à chaque étape.</span><span class="sxs-lookup"><span data-stu-id="0e602-177">However, it also enables consistent emulation of multipass methods where the frame buffer is always in the range 0 to 1, and of DirectX 6 and 7.0 multitexture syntax, in which saturation is defined to occur at every stage.</span></span>

<span data-ttu-id="0e602-178">Cet exemple charge le registre de destination (dest) avec la somme des deux couleurs dans les opérandes sources (src0 et src1) et fixe le résultat dans la plage 0,0 à 1,0 pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="0e602-178">This example loads the destination register (dest) with the sum of the two colors in the source operands (src0 and src1), and clamps the result into the range 0.0 to 1.0 for each component.</span></span>


```
add_sat dest, src0, src1
```



<span data-ttu-id="0e602-179">Cet exemple combine deux modificateurs d’instruction.</span><span class="sxs-lookup"><span data-stu-id="0e602-179">This example combines two instruction modifiers.</span></span> <span data-ttu-id="0e602-180">En premier lieu, deux couleurs dans les opérandes sources (src0 et src1) sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="0e602-180">First, two colors in the source operands (src0 and src1) are added.</span></span> <span data-ttu-id="0e602-181">Le résultat est multiplié par deux et est ancré entre 0,0 et 1,0 pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="0e602-181">The result is multiplied by two and clamped between 0.0 to 1.0 for each component.</span></span> <span data-ttu-id="0e602-182">Le résultat est enregistré dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="0e602-182">The result is saved in the destination register.</span></span>


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a><span data-ttu-id="0e602-183">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e602-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e602-184">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0e602-184">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




