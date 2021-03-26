---
title: Masque d’écriture du registre de destination
description: Un masque d’écriture contrôle les composants d’un registre de destination qui sont écrits après l’achèvement d’une instruction.
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940333"
---
# <a name="destination-register-write-mask"></a><span data-ttu-id="5f806-103">Masque d’écriture du registre de destination</span><span class="sxs-lookup"><span data-stu-id="5f806-103">Destination Register Write Mask</span></span>

<span data-ttu-id="5f806-104">Un masque d’écriture contrôle les composants d’un registre de destination qui sont écrits après l’achèvement d’une instruction.</span><span class="sxs-lookup"><span data-stu-id="5f806-104">A write mask controls which components of a destination register are written after an instruction is completed.</span></span> <span data-ttu-id="5f806-105">Un masque d’écriture de sortie est autorisé tant que les composants sont dans l’ordre de. RVBA ou. XYZW.</span><span class="sxs-lookup"><span data-stu-id="5f806-105">An output write mask is allowed as long as the components are in the order of .rgba or .xyzw.</span></span> <span data-ttu-id="5f806-106">Autrement dit,. RBA et. XW sont des masques valides.</span><span class="sxs-lookup"><span data-stu-id="5f806-106">That is, .rba and .xw are valid masks.</span></span> <span data-ttu-id="5f806-107">Les registres de texture ont un ensemble de règles et les registres de non-texture ont un autre ensemble de règles.</span><span class="sxs-lookup"><span data-stu-id="5f806-107">Texture registers have one set of rules and non-texture registers have another set of rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f806-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f806-108">Syntax</span></span>



| <span data-ttu-id="5f806-109">DST. writemask</span><span class="sxs-lookup"><span data-stu-id="5f806-109">dst.writemask</span></span> |
|---------------|



 

<span data-ttu-id="5f806-110">where</span><span class="sxs-lookup"><span data-stu-id="5f806-110">where</span></span>

-   <span data-ttu-id="5f806-111">l’heure d’été est un registre de destination.</span><span class="sxs-lookup"><span data-stu-id="5f806-111">dst is a destination register.</span></span>
-   <span data-ttu-id="5f806-112">writemask est une séquence de masques de l’un ou l’autre des jeux : (x, y, z, w) ou (rouge, vert, bleu, alpha).</span><span class="sxs-lookup"><span data-stu-id="5f806-112">writemask is a sequence of masks from either set: (x,y,z,w) or (red, green, blue, alpha).</span></span>

## <a name="remarks"></a><span data-ttu-id="5f806-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5f806-113">Remarks</span></span>

<span data-ttu-id="5f806-114">Les masques d’écriture de destination suivants sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="5f806-114">The following destination write masks are available.</span></span>



| <span data-ttu-id="5f806-115">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5f806-115">Pixel shader versions</span></span> | <span data-ttu-id="5f806-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="5f806-116">1\_1</span></span> | <span data-ttu-id="5f806-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="5f806-117">1\_2</span></span> | <span data-ttu-id="5f806-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5f806-118">1\_3</span></span> | <span data-ttu-id="5f806-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="5f806-119">1\_4</span></span> | <span data-ttu-id="5f806-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5f806-120">2\_0</span></span> | <span data-ttu-id="5f806-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5f806-121">2\_x</span></span> | <span data-ttu-id="5f806-122">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5f806-122">2\_sw</span></span> | <span data-ttu-id="5f806-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5f806-123">3\_0</span></span> | <span data-ttu-id="5f806-124">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="5f806-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5f806-125">. XYZW (par défaut)</span><span class="sxs-lookup"><span data-stu-id="5f806-125">.xyzw (default)</span></span>       | <span data-ttu-id="5f806-126">x</span><span class="sxs-lookup"><span data-stu-id="5f806-126">x</span></span>    | <span data-ttu-id="5f806-127">x</span><span class="sxs-lookup"><span data-stu-id="5f806-127">x</span></span>    | <span data-ttu-id="5f806-128">x</span><span class="sxs-lookup"><span data-stu-id="5f806-128">x</span></span>    | <span data-ttu-id="5f806-129">x</span><span class="sxs-lookup"><span data-stu-id="5f806-129">x</span></span>    | <span data-ttu-id="5f806-130">x</span><span class="sxs-lookup"><span data-stu-id="5f806-130">x</span></span>    | <span data-ttu-id="5f806-131">x</span><span class="sxs-lookup"><span data-stu-id="5f806-131">x</span></span>    | <span data-ttu-id="5f806-132">x</span><span class="sxs-lookup"><span data-stu-id="5f806-132">x</span></span>     | <span data-ttu-id="5f806-133">x</span><span class="sxs-lookup"><span data-stu-id="5f806-133">x</span></span>    | <span data-ttu-id="5f806-134">x</span><span class="sxs-lookup"><span data-stu-id="5f806-134">x</span></span>     |
| <span data-ttu-id="5f806-135">. xyz</span><span class="sxs-lookup"><span data-stu-id="5f806-135">.xyz</span></span>                  | <span data-ttu-id="5f806-136">x</span><span class="sxs-lookup"><span data-stu-id="5f806-136">x</span></span>    | <span data-ttu-id="5f806-137">x</span><span class="sxs-lookup"><span data-stu-id="5f806-137">x</span></span>    | <span data-ttu-id="5f806-138">x</span><span class="sxs-lookup"><span data-stu-id="5f806-138">x</span></span>    | <span data-ttu-id="5f806-139">x</span><span class="sxs-lookup"><span data-stu-id="5f806-139">x</span></span>    | <span data-ttu-id="5f806-140">x</span><span class="sxs-lookup"><span data-stu-id="5f806-140">x</span></span>    | <span data-ttu-id="5f806-141">x</span><span class="sxs-lookup"><span data-stu-id="5f806-141">x</span></span>    | <span data-ttu-id="5f806-142">x</span><span class="sxs-lookup"><span data-stu-id="5f806-142">x</span></span>     | <span data-ttu-id="5f806-143">x</span><span class="sxs-lookup"><span data-stu-id="5f806-143">x</span></span>    | <span data-ttu-id="5f806-144">x</span><span class="sxs-lookup"><span data-stu-id="5f806-144">x</span></span>     |
| <span data-ttu-id="5f806-145">. w</span><span class="sxs-lookup"><span data-stu-id="5f806-145">.w</span></span>                    | <span data-ttu-id="5f806-146">x</span><span class="sxs-lookup"><span data-stu-id="5f806-146">x</span></span>    | <span data-ttu-id="5f806-147">x</span><span class="sxs-lookup"><span data-stu-id="5f806-147">x</span></span>    | <span data-ttu-id="5f806-148">x</span><span class="sxs-lookup"><span data-stu-id="5f806-148">x</span></span>    | <span data-ttu-id="5f806-149">x</span><span class="sxs-lookup"><span data-stu-id="5f806-149">x</span></span>    | <span data-ttu-id="5f806-150">x</span><span class="sxs-lookup"><span data-stu-id="5f806-150">x</span></span>    | <span data-ttu-id="5f806-151">x</span><span class="sxs-lookup"><span data-stu-id="5f806-151">x</span></span>    | <span data-ttu-id="5f806-152">x</span><span class="sxs-lookup"><span data-stu-id="5f806-152">x</span></span>     | <span data-ttu-id="5f806-153">x</span><span class="sxs-lookup"><span data-stu-id="5f806-153">x</span></span>    | <span data-ttu-id="5f806-154">x</span><span class="sxs-lookup"><span data-stu-id="5f806-154">x</span></span>     |
| <span data-ttu-id="5f806-155">masque arbitraire</span><span class="sxs-lookup"><span data-stu-id="5f806-155">arbitrary mask</span></span>        |      |      |      | <span data-ttu-id="5f806-156">x</span><span class="sxs-lookup"><span data-stu-id="5f806-156">x</span></span>    | <span data-ttu-id="5f806-157">x</span><span class="sxs-lookup"><span data-stu-id="5f806-157">x</span></span>    | <span data-ttu-id="5f806-158">x</span><span class="sxs-lookup"><span data-stu-id="5f806-158">x</span></span>    | <span data-ttu-id="5f806-159">x</span><span class="sxs-lookup"><span data-stu-id="5f806-159">x</span></span>     | <span data-ttu-id="5f806-160">x</span><span class="sxs-lookup"><span data-stu-id="5f806-160">x</span></span>    | <span data-ttu-id="5f806-161">x</span><span class="sxs-lookup"><span data-stu-id="5f806-161">x</span></span>     |



 

<span data-ttu-id="5f806-162">Le masque arbitraire permet de combiner tout ensemble de canaux pour produire un masque.</span><span class="sxs-lookup"><span data-stu-id="5f806-162">The arbitrary mask allows any set of channels to be combined to produce a mask.</span></span> <span data-ttu-id="5f806-163">Les canaux doivent être listés dans l’ordre r, g, b, a, par exemple, Register. RBA, qui met à jour les canaux rouge, bleu et alpha de la destination.</span><span class="sxs-lookup"><span data-stu-id="5f806-163">The channels must be listed in the order r, g, b, a - for example, register.rba, which updates the red, blue, and alpha channels of the destination.</span></span> <span data-ttu-id="5f806-164">Le masque arbitraire est disponible dans la version 1 \_ 4 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5f806-164">The arbitrary mask is available in version 1\_4 or higher.</span></span>

<span data-ttu-id="5f806-165">Si aucun masque d’écriture de destination n’est spécifié, le masque d’écriture de destination est défini par défaut sur le cas RVBA.</span><span class="sxs-lookup"><span data-stu-id="5f806-165">If no destination write mask is specified, the destination write mask defaults to the rgba case.</span></span> <span data-ttu-id="5f806-166">En d’autres termes, tous les canaux du registre de destination sont mis à jour.</span><span class="sxs-lookup"><span data-stu-id="5f806-166">In other words, all channels in the destination register are updated.</span></span>

<span data-ttu-id="5f806-167">Pour les versions 1 \_ 0 à 1 \_ 3, l’instruction arithmétique [DP3-PS](dp3---ps.md) DP3 peut utiliser uniquement les masques d’écriture de sortie. RGB ou. RVBA.</span><span class="sxs-lookup"><span data-stu-id="5f806-167">For versions 1\_0 to 1\_3, the [dp3 - ps](dp3---ps.md) dp3 arithmetic instruction can use only the .rgb or .rgba output write masks.</span></span>

<span data-ttu-id="5f806-168">Les masques d’écriture de registre de destination sont pris en charge uniquement pour les opérations arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="5f806-168">Destination register write masks are supported for arithmetic operations only.</span></span> <span data-ttu-id="5f806-169">Ils ne peuvent pas être utilisés sur les instructions d’adressage de texture, à l’exception des instructions de la version 1 \_ 4, [texcrd-PS](texcrd---ps.md) et [texld-PS \_ 2 \_ 0 et up](texld---ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="5f806-169">They cannot be used on texture addressing instructions, with the exception of the version 1\_4 instructions, [texcrd - ps](texcrd---ps.md) and [texld - ps\_2\_0 and up](texld---ps-2-0.md).</span></span>

<span data-ttu-id="5f806-170">La valeur par défaut consiste à écrire les quatre canaux de couleurs.</span><span class="sxs-lookup"><span data-stu-id="5f806-170">The default is to write all four color channels.</span></span>


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



<span data-ttu-id="5f806-171">Le masque d’écriture alpha est également appelé masque d’écriture scalaire, car il utilise le pipeline scalaire.</span><span class="sxs-lookup"><span data-stu-id="5f806-171">The alpha write mask is also referred to as the scalar write mask, because it uses the scalar pipeline.</span></span>


```
add r0.a, t1, v1
```



<span data-ttu-id="5f806-172">Par conséquent, cette instruction place efficacement la somme du composant alpha de T1 et le composant alpha de V1 dans R0. a.</span><span class="sxs-lookup"><span data-stu-id="5f806-172">So this instruction effectively puts the sum of the alpha component of t1 and the alpha component of v1 into r0.a.</span></span>

<span data-ttu-id="5f806-173">Le masque d’écriture de couleur est utilisé pour contrôler l’écriture des canaux de couleurs.</span><span class="sxs-lookup"><span data-stu-id="5f806-173">The color write mask is used to control writing to the color channels.</span></span>


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



<span data-ttu-id="5f806-174">Pour la version 1 \_ 4, les masques d’écriture de destination peuvent être utilisés dans n’importe quelle combinaison, à condition que les masques soient triés r, g, b, a.</span><span class="sxs-lookup"><span data-stu-id="5f806-174">For version 1\_4, destination write masks can be used in any combination as long as the masks are ordered r,g,b,a.</span></span>


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



<span data-ttu-id="5f806-175">Une instruction co-émises permet d’émettre simultanément deux instructions potentiellement différentes.</span><span class="sxs-lookup"><span data-stu-id="5f806-175">A co-issued instruction allows two potentially different instructions to be issued simultaneously.</span></span> <span data-ttu-id="5f806-176">Pour ce faire, vous devez exécuter les instructions dans le pipeline alpha et le pipeline RGB.</span><span class="sxs-lookup"><span data-stu-id="5f806-176">This is accomplished by executing the instructions in the alpha pipeline and the RGB pipeline.</span></span>


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



<span data-ttu-id="5f806-177">L’avantage des instructions de couplage de cette façon est qu’il permet d’effectuer différentes opérations dans le pipeline Vector et le pipeline scalaire en parallèle.</span><span class="sxs-lookup"><span data-stu-id="5f806-177">The advantage of pairing instructions this way is that it allows different operations to be performed in the vector and scalar pipeline in parallel.</span></span>

<span data-ttu-id="5f806-178">Ces registres de sortie du nuanceur de sommets sont limités aux masques d’écriture suivants :</span><span class="sxs-lookup"><span data-stu-id="5f806-178">These vertex shader output registers are restricted to the following write masks:</span></span>



| <span data-ttu-id="5f806-179">Type de Registre</span><span class="sxs-lookup"><span data-stu-id="5f806-179">Register Type</span></span> | <span data-ttu-id="5f806-180">Masque d’écriture requis</span><span class="sxs-lookup"><span data-stu-id="5f806-180">Required Write Mask</span></span>                                              |
|---------------|------------------------------------------------------------------|
| <span data-ttu-id="5f806-181">oFog</span><span class="sxs-lookup"><span data-stu-id="5f806-181">oFog</span></span>          | <span data-ttu-id="5f806-182">aucun masque d’écriture explicite n’est autorisé sur ce registre scalaire</span><span class="sxs-lookup"><span data-stu-id="5f806-182">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="5f806-183">Décide</span><span class="sxs-lookup"><span data-stu-id="5f806-183">oPts</span></span>          | <span data-ttu-id="5f806-184">aucun masque d’écriture explicite n’est autorisé sur ce registre scalaire</span><span class="sxs-lookup"><span data-stu-id="5f806-184">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="5f806-185">oPos</span><span class="sxs-lookup"><span data-stu-id="5f806-185">oPos</span></span>          | <span data-ttu-id="5f806-186">. XYZW (qui est la valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="5f806-186">.xyzw(which is the default)</span></span>                                      |
| <span data-ttu-id="5f806-187">oT\#</span><span class="sxs-lookup"><span data-stu-id="5f806-187">oT\#</span></span>          | <span data-ttu-id="5f806-188">Mask combiné :. x \| . XY. \| xyz \| . XYZW (qui est la valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="5f806-188">combined mask: .x \| .xy \| .xyz \| .xyzw (which is the default)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5f806-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f806-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f806-190">Modificateurs de registre de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5f806-190">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




