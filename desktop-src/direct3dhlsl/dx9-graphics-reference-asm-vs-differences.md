---
title: Différences entre vertex shader
description: Différences entre vertex shader
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c74603f9eab4ea91e9220bbaa172c0262aeda99
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031371"
---
# <a name="vertex-shader-differences"></a><span data-ttu-id="4d80d-103">Différences entre vertex shader</span><span class="sxs-lookup"><span data-stu-id="4d80d-103">Vertex Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="4d80d-104">Emplacements des instructions</span><span class="sxs-lookup"><span data-stu-id="4d80d-104">Instruction Slots</span></span>

<span data-ttu-id="4d80d-105">Chaque version prend en charge un nombre différent d’emplacements d’instruction maximum.</span><span class="sxs-lookup"><span data-stu-id="4d80d-105">Each version supports a differing number of maximum instruction slots.</span></span>



| <span data-ttu-id="4d80d-106">Version</span><span class="sxs-lookup"><span data-stu-id="4d80d-106">Version</span></span>  | <span data-ttu-id="4d80d-107">Nombre maximal d’emplacements d’instructions</span><span class="sxs-lookup"><span data-stu-id="4d80d-107">Maximum number of instruction slots</span></span>                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d80d-108">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="4d80d-108">vs\_1\_1</span></span> | <span data-ttu-id="4d80d-109">128</span><span class="sxs-lookup"><span data-stu-id="4d80d-109">128</span></span>                                                                                                                               |
| <span data-ttu-id="4d80d-110">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4d80d-110">vs\_2\_0</span></span> | <span data-ttu-id="4d80d-111">256</span><span class="sxs-lookup"><span data-stu-id="4d80d-111">256</span></span>                                                                                                                               |
| <span data-ttu-id="4d80d-112">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4d80d-112">vs\_2\_x</span></span> | <span data-ttu-id="4d80d-113">256</span><span class="sxs-lookup"><span data-stu-id="4d80d-113">256</span></span>                                                                                                                               |
| <span data-ttu-id="4d80d-114">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4d80d-114">vs\_3\_0</span></span> | <span data-ttu-id="4d80d-115">512 minimum et jusqu’au nombre d’emplacements dans D3DCAPS9. MaxVertexShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="4d80d-115">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots.</span></span> <span data-ttu-id="4d80d-116">Consultez [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="4d80d-116">See [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> |



 

<span data-ttu-id="4d80d-117">Pour plus d’informations sur les limitations des nuanceurs de logiciels, consultez [nuanceurs de logiciels](dx9-graphics-reference-asm-software-shaders.md).</span><span class="sxs-lookup"><span data-stu-id="4d80d-117">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="4d80d-118">Limites d’imbrication du contrôle de Flow</span><span class="sxs-lookup"><span data-stu-id="4d80d-118">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="4d80d-119">Consultez [limites d’imbrication des contrôles de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="4d80d-119">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>

## <a name="vs_1_1-features"></a><span data-ttu-id="4d80d-120">\_fonctionnalités vs 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="4d80d-120">vs\_1\_1 Features</span></span>

<span data-ttu-id="4d80d-121">Nouvelles instructions :</span><span class="sxs-lookup"><span data-stu-id="4d80d-121">New instructions:</span></span>

<span data-ttu-id="4d80d-122">Voir [instructions-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span><span class="sxs-lookup"><span data-stu-id="4d80d-122">See [Instructions - vs\_1\_1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span></span>

<span data-ttu-id="4d80d-123">Nouveaux registres :</span><span class="sxs-lookup"><span data-stu-id="4d80d-123">New registers:</span></span>

<span data-ttu-id="4d80d-124">Consultez [registres-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span><span class="sxs-lookup"><span data-stu-id="4d80d-124">See [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span></span>

## <a name="vs_2_0-features"></a><span data-ttu-id="4d80d-125">\_fonctionnalités vs 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4d80d-125">vs\_2\_0 Features</span></span>

<span data-ttu-id="4d80d-126">Nouvelles fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="4d80d-126">New features:</span></span>

-   <span data-ttu-id="4d80d-127">Contrôle de Flow statique</span><span class="sxs-lookup"><span data-stu-id="4d80d-127">Static flow control</span></span>
-   <span data-ttu-id="4d80d-128">Les quatre composants du [Registre d’adresses](dx9-graphics-reference-asm-vs-registers-address.md) (a0) sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="4d80d-128">All four components of the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md) (a0) are available.</span></span>

<span data-ttu-id="4d80d-129">Nouvelles instructions :</span><span class="sxs-lookup"><span data-stu-id="4d80d-129">New instructions:</span></span>

-   <span data-ttu-id="4d80d-130">Instructions d’installation- [defb-vs](defb---vs.md), [assignatures-vs](defi---vs.md)</span><span class="sxs-lookup"><span data-stu-id="4d80d-130">Setup instructions - [defb - vs](defb---vs.md), [defi - vs](defi---vs.md)</span></span>
-   <span data-ttu-id="4d80d-131">Instructions arithmétiques- [ABS-vs](abs---vs.md), [CRS-vs](crs---vs.md), [LRP-vs](lrp---vs.md), [Mova-](mova---vs.md)vs, [NRM-vs](nrm---vs.md), [Pow-](pow---vs.md)vs, [SGN-vs](sgn---vs.md), [SinCos,-vs](sincos---vs.md)</span><span class="sxs-lookup"><span data-stu-id="4d80d-131">Arithmetic instructions - [abs - vs](abs---vs.md), [crs - vs](crs---vs.md), [lrp - vs](lrp---vs.md), [mova - vs](mova---vs.md), [nrm - vs](nrm---vs.md), [pow - vs](pow---vs.md), [sgn - vs](sgn---vs.md), [sincos - vs](sincos---vs.md)</span></span>
-   <span data-ttu-id="4d80d-132">Instructions de contrôle de workflow statiques- [appel-vs](call---vs.md), [callnz bool-vs](callnz-bool---vs.md), [else-vs](else---vs.md), [endif-vs](endif---vs.md), [ENDLOOP-vs](endloop---vs.md), [endrep-vs](endrep---vs.md), [si bool-vs](if-bool---vs.md), [label-vs](label---vs.md), [Loop](loop---vs.md)-vs, [REP](rep---vs.md)-vs, [RET-vs](ret---vs.md)</span><span class="sxs-lookup"><span data-stu-id="4d80d-132">Static flow control instructions - [call - vs](call---vs.md), [callnz bool - vs](callnz-bool---vs.md), [else - vs](else---vs.md), [endif - vs](endif---vs.md), [endloop - vs](endloop---vs.md), [endrep - vs](endrep---vs.md), [if bool - vs](if-bool---vs.md), [label - vs](label---vs.md), [loop - vs](loop---vs.md), [rep - vs](rep---vs.md), [ret - vs](ret---vs.md)</span></span>

<span data-ttu-id="4d80d-133">Nouveaux registres :</span><span class="sxs-lookup"><span data-stu-id="4d80d-133">New registers:</span></span>

-   <span data-ttu-id="4d80d-134">[Registre booléen constant](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )</span><span class="sxs-lookup"><span data-stu-id="4d80d-134">[Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b\#)</span></span>
-   <span data-ttu-id="4d80d-135">[Registre d’entiers constant](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )</span><span class="sxs-lookup"><span data-stu-id="4d80d-135">[Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i\#)</span></span>
-   <span data-ttu-id="4d80d-136">[Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al)</span><span class="sxs-lookup"><span data-stu-id="4d80d-136">[Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL)</span></span>

## <a name="vs_2_x-features"></a><span data-ttu-id="4d80d-137">Fonctionnalités de vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4d80d-137">vs\_2\_x Features</span></span>

<span data-ttu-id="4d80d-138">Nouvelles fonctionnalités (D3DCAPS9. VS20Caps):</span><span class="sxs-lookup"><span data-stu-id="4d80d-138">New features (D3DCAPS9.VS20Caps):</span></span>

-   <span data-ttu-id="4d80d-139">Contrôle de Flow dynamique</span><span class="sxs-lookup"><span data-stu-id="4d80d-139">Dynamic flow control</span></span>
-   <span data-ttu-id="4d80d-140">Imbrication des instructions de contrôle de workflow dynamique et statique</span><span class="sxs-lookup"><span data-stu-id="4d80d-140">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="4d80d-141">Nombre d' [enregistreurs temporaires](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ) augmentés</span><span class="sxs-lookup"><span data-stu-id="4d80d-141">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="4d80d-142">Prédicat</span><span class="sxs-lookup"><span data-stu-id="4d80d-142">Predication</span></span>

<span data-ttu-id="4d80d-143">Nouvelles instructions :</span><span class="sxs-lookup"><span data-stu-id="4d80d-143">New Instructions:</span></span>

-   <span data-ttu-id="4d80d-144">Instructions de contrôle de workflow dynamique- [break-vs](break---vs.md), [pause \_ COMP-vs](break-comp---vs.md), [breakp-vs](breakp---vs.md), [callnz prédit-vs](callnz-pred---vs.md), [si \_ COMP-vs](if-comp---vs.md), [si prédit-vs](if-pred---vs.md), [setp \_ COMP-vs](setp-comp---vs.md)</span><span class="sxs-lookup"><span data-stu-id="4d80d-144">Dynamic flow control instructions - [break - vs](break---vs.md), [break\_comp - vs](break-comp---vs.md), [breakp - vs](breakp---vs.md), [callnz pred - vs](callnz-pred---vs.md), [if\_comp - vs](if-comp---vs.md), [if pred - vs](if-pred---vs.md), [setp\_comp - vs](setp-comp---vs.md)</span></span>

<span data-ttu-id="4d80d-145">Nouveaux registres :</span><span class="sxs-lookup"><span data-stu-id="4d80d-145">New registers:</span></span>

-   <span data-ttu-id="4d80d-146">[Registre de prédicats](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0)</span><span class="sxs-lookup"><span data-stu-id="4d80d-146">[Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)</span></span>

## <a name="vs_3_0-features"></a><span data-ttu-id="4d80d-147">Fonctionnalités de vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4d80d-147">vs\_3\_0 Features</span></span>

<span data-ttu-id="4d80d-148">Nouvelles fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="4d80d-148">New features :</span></span>

-   <span data-ttu-id="4d80d-149">Recherche de texture</span><span class="sxs-lookup"><span data-stu-id="4d80d-149">Texture lookup</span></span>
-   <span data-ttu-id="4d80d-150">Registres de [sortie](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) indexables (o \# )</span><span class="sxs-lookup"><span data-stu-id="4d80d-150">Indexable [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#)</span></span>
-   <span data-ttu-id="4d80d-151">Nombre de [registres temporaires](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r \# ) augmentés à 32</span><span class="sxs-lookup"><span data-stu-id="4d80d-151">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased to 32</span></span>

<span data-ttu-id="4d80d-152">Nouvelles instructions :</span><span class="sxs-lookup"><span data-stu-id="4d80d-152">New instructions:</span></span>

-   <span data-ttu-id="4d80d-153">Instruction de configuration- [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)</span><span class="sxs-lookup"><span data-stu-id="4d80d-153">Setup instruction - [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)</span></span>
-   <span data-ttu-id="4d80d-154">Instruction de texture- [texldl-vs](texldl---vs.md)</span><span class="sxs-lookup"><span data-stu-id="4d80d-154">Texture instruction - [texldl - vs](texldl---vs.md)</span></span>

<span data-ttu-id="4d80d-155">Nouveaux registres :</span><span class="sxs-lookup"><span data-stu-id="4d80d-155">New registers:</span></span>

-   <span data-ttu-id="4d80d-156">[Échantillonneur (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# )</span><span class="sxs-lookup"><span data-stu-id="4d80d-156">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d80d-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d80d-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d80d-158">Nuanceurs vertex</span><span class="sxs-lookup"><span data-stu-id="4d80d-158">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 