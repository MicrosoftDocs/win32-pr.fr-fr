---
title: Différences de nuanceur de pixels
description: Différences de nuanceur de pixels
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382143"
---
# <a name="pixel-shader-differences"></a><span data-ttu-id="4405c-103">Différences de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="4405c-103">Pixel Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="4405c-104">Emplacements des instructions</span><span class="sxs-lookup"><span data-stu-id="4405c-104">Instruction Slots</span></span>

<span data-ttu-id="4405c-105">Chaque version prend en charge un nombre différent d’emplacements d’instruction maximum.</span><span class="sxs-lookup"><span data-stu-id="4405c-105">Each version supports a different number of maximum instruction slots.</span></span>



| <span data-ttu-id="4405c-106">Version</span><span class="sxs-lookup"><span data-stu-id="4405c-106">Version</span></span>  | <span data-ttu-id="4405c-107">Nombre maximal d’emplacements d’instructions</span><span class="sxs-lookup"><span data-stu-id="4405c-107">Maximum number of instruction slots</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4405c-108">PS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="4405c-108">ps\_1\_1</span></span> | <span data-ttu-id="4405c-109">4 texture + 8 arithmétiques</span><span class="sxs-lookup"><span data-stu-id="4405c-109">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="4405c-110">PS \_ 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="4405c-110">ps\_1\_2</span></span> | <span data-ttu-id="4405c-111">4 texture + 8 arithmétiques</span><span class="sxs-lookup"><span data-stu-id="4405c-111">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="4405c-112">PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4405c-112">ps\_1\_3</span></span> | <span data-ttu-id="4405c-113">4 texture + 8 arithmétiques</span><span class="sxs-lookup"><span data-stu-id="4405c-113">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="4405c-114">PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="4405c-114">ps\_1\_4</span></span> | <span data-ttu-id="4405c-115">6 texture + 8 arithmétiques par phase</span><span class="sxs-lookup"><span data-stu-id="4405c-115">6 texture + 8 arithmetic per phase</span></span>                                                                                    |
| <span data-ttu-id="4405c-116">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4405c-116">ps\_2\_0</span></span> | <span data-ttu-id="4405c-117">32 texture + 64 arithmétique</span><span class="sxs-lookup"><span data-stu-id="4405c-117">32 texture + 64 arithmetic</span></span>                                                                                            |
| <span data-ttu-id="4405c-118">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4405c-118">ps\_2\_x</span></span> | <span data-ttu-id="4405c-119">96 minimum et jusqu’au nombre d’emplacements dans D3DCAPS9. D3DPSHADERCAPS2 \_ 0. NumInstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="4405c-119">96 minimum, and up to the number of slots in D3DCAPS9.D3DPSHADERCAPS2\_0.NumInstructionSlots.</span></span> <span data-ttu-id="4405c-120">Consultez D3DPSHADERCAPS2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="4405c-120">See D3DPSHADERCAPS2\_0.</span></span> |
| <span data-ttu-id="4405c-121">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4405c-121">ps\_3\_0</span></span> | <span data-ttu-id="4405c-122">512 minimum et jusqu’au nombre d’emplacements dans D3DCAPS9. MaxPixelShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="4405c-122">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots.</span></span> <span data-ttu-id="4405c-123">Consultez D3DPSHADERCAPS2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="4405c-123">See D3DPSHADERCAPS2\_0.</span></span>      |



 

<span data-ttu-id="4405c-124">Pour plus d’informations sur les limitations des nuanceurs de logiciels, consultez [nuanceurs de logiciels](dx9-graphics-reference-asm-software-shaders.md).</span><span class="sxs-lookup"><span data-stu-id="4405c-124">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="4405c-125">Limites d’imbrication du contrôle de Flow</span><span class="sxs-lookup"><span data-stu-id="4405c-125">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="4405c-126">Consultez [limitations du contrôle de workflow](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="4405c-126">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>

## <a name="ps_1_x-features"></a><span data-ttu-id="4405c-127">Fonctionnalités de PS \_ 1 \_ x</span><span class="sxs-lookup"><span data-stu-id="4405c-127">ps\_1\_x Features</span></span>

<span data-ttu-id="4405c-128">Nouvelles instructions :</span><span class="sxs-lookup"><span data-stu-id="4405c-128">New instructions:</span></span>

<span data-ttu-id="4405c-129">Consultez les instructions PS 1 [ \_ \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="4405c-129">See [ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).</span></span>

<span data-ttu-id="4405c-130">Nouveaux registres :</span><span class="sxs-lookup"><span data-stu-id="4405c-130">New registers:</span></span>

<span data-ttu-id="4405c-131">Consultez [les \_ registres PS 1 \_ 1 PS 1 \_ \_ \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="4405c-131">See [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="ps_2_0-features"></a><span data-ttu-id="4405c-132">Fonctionnalités de PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4405c-132">ps\_2\_0 Features</span></span>

<span data-ttu-id="4405c-133">Nouvelles fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="4405c-133">New features:</span></span>

-   <span data-ttu-id="4405c-134">Trois nouveaux Swizzles-. yzxw,. zxyw,. wzyx</span><span class="sxs-lookup"><span data-stu-id="4405c-134">Three new swizzles - .yzxw, .zxyw, .wzyx</span></span>
-   <span data-ttu-id="4405c-135">Nombre de [registres temporaires](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) passé à 12</span><span class="sxs-lookup"><span data-stu-id="4405c-135">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) increased to 12</span></span>
-   <span data-ttu-id="4405c-136">Nombre de registres de [registres à virgule flottante constants](dx9-graphics-reference-asm-ps-registers-constant-float.md) (c \# ) passés à 32</span><span class="sxs-lookup"><span data-stu-id="4405c-136">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md) registers (c\#) increased to 32</span></span>
-   <span data-ttu-id="4405c-137">Nombre de [registres de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)(t \# ) augmentés à 8</span><span class="sxs-lookup"><span data-stu-id="4405c-137">Number of [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t\#) increased to 8</span></span>

<span data-ttu-id="4405c-138">Nouvelles instructions :</span><span class="sxs-lookup"><span data-stu-id="4405c-138">New instructions:</span></span>

-   <span data-ttu-id="4405c-139">Instructions d’installation- [DCL-(SM2, SM3-PS ASM)](dcl---ps.md), [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)</span><span class="sxs-lookup"><span data-stu-id="4405c-139">Setup instructions - [dcl - (sm2, sm3 - ps asm)](dcl---ps.md), [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)</span></span>
-   <span data-ttu-id="4405c-140">Instructions arithmétiques [-ABS-PS](abs---ps.md), [CRS-PS](crs---ps.md), [dp2add-PS](dp2add---ps.md), [exp-PS](exp---ps.md), [FRC-](frc---ps.md)PS [, log-PS](log---ps.md), [M3X2-PS](m3x2---ps.md), [M3x3-](m3x3---ps.md)PS [, M3x4-](m3x4---ps.md)PS, [m4x3-PS](m4x3---ps.md), [M4X4-](m4x4---ps.md)PS, [Max-](max---ps.md)PS, [min-PS](min---ps.md), [NRM](nrm---ps.md)-PS [, Pow-PS](pow---ps.md), [RCP-PS](rcp---ps.md), [rsq-](rsq---ps.md)PS, [SinCos,-PS](sincos---ps.md)</span><span class="sxs-lookup"><span data-stu-id="4405c-140">Arithmetic instructions - [abs - ps](abs---ps.md), [crs - ps](crs---ps.md), [dp2add - ps](dp2add---ps.md), [exp - ps](exp---ps.md), [frc - ps](frc---ps.md), [log - ps](log---ps.md), [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), [m4x4 - ps](m4x4---ps.md), [max - ps](max---ps.md), [min - ps](min---ps.md), [nrm - ps](nrm---ps.md), [pow - ps](pow---ps.md), [rcp - ps](rcp---ps.md), [rsq - ps](rsq---ps.md), [sincos - ps](sincos---ps.md)</span></span>
-   <span data-ttu-id="4405c-141">Instructions de texture- [texld-PS \_ 2 \_ 0 et up](texld---ps-2-0.md) (syntaxe différente), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="4405c-141">Texture instructions - [texld - ps\_2\_0 and up](texld---ps-2-0.md) (different syntax), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)</span></span>

<span data-ttu-id="4405c-142">Nouveaux registres :</span><span class="sxs-lookup"><span data-stu-id="4405c-142">New registers:</span></span>

-   <span data-ttu-id="4405c-143">[Échantillonneur (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# )</span><span class="sxs-lookup"><span data-stu-id="4405c-143">[Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#)</span></span>

## <a name="ps_2_x-features"></a><span data-ttu-id="4405c-144">Fonctionnalités de PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4405c-144">ps\_2\_x Features</span></span>

<span data-ttu-id="4405c-145">Nouvelles fonctionnalités (voir [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).) :</span><span class="sxs-lookup"><span data-stu-id="4405c-145">New features (See [**D3DPSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).):</span></span>

-   <span data-ttu-id="4405c-146">Contrôle de Flow dynamique</span><span class="sxs-lookup"><span data-stu-id="4405c-146">Dynamic flow control</span></span>
-   <span data-ttu-id="4405c-147">Contrôle de Flow statique</span><span class="sxs-lookup"><span data-stu-id="4405c-147">Static flow control</span></span>
-   <span data-ttu-id="4405c-148">Imbrication des instructions de contrôle de workflow dynamique et statique</span><span class="sxs-lookup"><span data-stu-id="4405c-148">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="4405c-149">Nombre d' [enregistreurs temporaires](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ) augmentés</span><span class="sxs-lookup"><span data-stu-id="4405c-149">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="4405c-150">Swizzle source arbitraire</span><span class="sxs-lookup"><span data-stu-id="4405c-150">Arbitrary source swizzle</span></span>
-   <span data-ttu-id="4405c-151">Instructions de dégradé</span><span class="sxs-lookup"><span data-stu-id="4405c-151">Gradient instructions</span></span>
-   <span data-ttu-id="4405c-152">Prédicat</span><span class="sxs-lookup"><span data-stu-id="4405c-152">Predication</span></span>
-   <span data-ttu-id="4405c-153">Aucune limite de lecture de texture dépendante</span><span class="sxs-lookup"><span data-stu-id="4405c-153">No dependent texture read limit</span></span>
-   <span data-ttu-id="4405c-154">Aucune limite d’instruction de texture</span><span class="sxs-lookup"><span data-stu-id="4405c-154">No texture instruction limit</span></span>

<span data-ttu-id="4405c-155">Nouvelles instructions :</span><span class="sxs-lookup"><span data-stu-id="4405c-155">New instructions:</span></span>

-   <span data-ttu-id="4405c-156">Instructions de contrôle de Flow statique- [si bool-PS](if-bool---ps.md), [Call-PS](call---ps.md), [callnz bool-PS](callnz-bool---ps.md), [else-PS](else---ps.md), [endif-PS](endif---ps.md), [REP-PS](rep---ps.md), [endrep-PS](endrep---ps.md), [label-PS](label---ps.md), [RET-PS](ret---ps.md)</span><span class="sxs-lookup"><span data-stu-id="4405c-156">Static flow control instructions - [if bool - ps](if-bool---ps.md), [call - ps](call---ps.md), [callnz bool - ps](callnz-bool---ps.md), [else - ps](else---ps.md), [endif - ps](endif---ps.md), [rep - ps](rep---ps.md), [endrep - ps](endrep---ps.md), [label - ps](label---ps.md), [ret - ps](ret---ps.md)</span></span>
-   <span data-ttu-id="4405c-157">Instructions de contrôle de workflow dynamique- [break-PS](break---ps.md), [break \_ COMP-PS](break-comp---ps.md), [breakp-PS](break-p---ps.md), [callnz prédit-PS](callnz-pred---ps.md), [si \_ COMP-PS](if-comp---ps.md), [si prédit-PS](if-pred---ps.md), [setp \_ COMP-PS](setp-comp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="4405c-157">Dynamic flow control instructions - [break - ps](break---ps.md), [break\_comp - ps](break-comp---ps.md), [breakp - ps](break-p---ps.md), [callnz pred - ps](callnz-pred---ps.md), [if\_comp - ps](if-comp---ps.md), [if pred - ps](if-pred---ps.md), [setp\_comp - ps](setp-comp---ps.md)</span></span>
-   <span data-ttu-id="4405c-158">Instructions arithmétiques- [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)</span><span class="sxs-lookup"><span data-stu-id="4405c-158">Arithmetic instructions - [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)</span></span>
-   <span data-ttu-id="4405c-159">Instruction de texture- [texldd-PS](texldd---ps.md)</span><span class="sxs-lookup"><span data-stu-id="4405c-159">Texture instruction - [texldd - ps](texldd---ps.md)</span></span>

<span data-ttu-id="4405c-160">Nouveaux registres :</span><span class="sxs-lookup"><span data-stu-id="4405c-160">New registers:</span></span>

-   <span data-ttu-id="4405c-161">[Registre de prédicats](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0)</span><span class="sxs-lookup"><span data-stu-id="4405c-161">[Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0)</span></span>

## <a name="ps_3_0-features"></a><span data-ttu-id="4405c-162">Fonctionnalités de PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4405c-162">ps\_3\_0 Features</span></span>

<span data-ttu-id="4405c-163">Nouvelles fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="4405c-163">New features:</span></span>

-   <span data-ttu-id="4405c-164">10 [registres d’entrée](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)consolidés s (v \# )</span><span class="sxs-lookup"><span data-stu-id="4405c-164">Consolidated 10 [Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)s (v\#)</span></span>
-   <span data-ttu-id="4405c-165">Registre de [couleur d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md) indexable (v \# ) avec le [Registre de compteur de boucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al)</span><span class="sxs-lookup"><span data-stu-id="4405c-165">Indexable [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) with the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL)</span></span>
-   <span data-ttu-id="4405c-166">Nombre de [registres temporaires](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r \# ) augmentés à 32</span><span class="sxs-lookup"><span data-stu-id="4405c-166">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased to 32</span></span>
-   <span data-ttu-id="4405c-167">Nombre de [registres de type flottant](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c \# ) augmentés à 224</span><span class="sxs-lookup"><span data-stu-id="4405c-167">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#) increased to 224</span></span>

<span data-ttu-id="4405c-168">Nouvelles instructions :</span><span class="sxs-lookup"><span data-stu-id="4405c-168">New instructions:</span></span>

-   <span data-ttu-id="4405c-169">Instruction de configuration [- \_ sémantique DCL (SM3-PS ASM)](dcl-usage---ps.md)</span><span class="sxs-lookup"><span data-stu-id="4405c-169">Setup instruction - [dcl\_semantics (sm3 - ps asm)](dcl-usage---ps.md)</span></span>
-   <span data-ttu-id="4405c-170">Instructions de Flow statique- [Loop-PS](loop---ps.md), [ENDLOOP-PS](endloop---ps.md)</span><span class="sxs-lookup"><span data-stu-id="4405c-170">Static flow instructions - [loop - ps](loop---ps.md), [endloop - ps](endloop---ps.md)</span></span>
-   <span data-ttu-id="4405c-171">Instruction arithmétique- [SinCos,-PS](sincos---ps.md) (nouvelle syntaxe)</span><span class="sxs-lookup"><span data-stu-id="4405c-171">Arithmetic instruction - [sincos - ps](sincos---ps.md) (new syntax)</span></span>
-   <span data-ttu-id="4405c-172">Instruction de texture- [texldl-PS](texldl---ps.md)</span><span class="sxs-lookup"><span data-stu-id="4405c-172">Texture instruction - [texldl - ps](texldl---ps.md)</span></span>

<span data-ttu-id="4405c-173">Nouveaux registres :</span><span class="sxs-lookup"><span data-stu-id="4405c-173">New registers:</span></span>

-   <span data-ttu-id="4405c-174">[Registre d’entrée](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )</span><span class="sxs-lookup"><span data-stu-id="4405c-174">[Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#)</span></span>
-   <span data-ttu-id="4405c-175">[Registre de position](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPOS)</span><span class="sxs-lookup"><span data-stu-id="4405c-175">[Position Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)</span></span>
-   <span data-ttu-id="4405c-176">[Inscription faciale](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)</span><span class="sxs-lookup"><span data-stu-id="4405c-176">[Face Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4405c-177">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4405c-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4405c-178">Nuanceurs de pixels</span><span class="sxs-lookup"><span data-stu-id="4405c-178">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 