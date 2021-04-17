---
title: vs_2_x
description: Un nuanceur de sommet programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex. Enregistre les données de transfert dans et en dehors de l’ALU. Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d09af016ca4fd399de0f2aeec1267343b9d11574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463463"
---
# <a name="vs_2_x"></a><span data-ttu-id="cabbb-105">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cabbb-105">vs\_2\_x</span></span>

<span data-ttu-id="cabbb-106">Un nuanceur de sommet programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="cabbb-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="cabbb-107">Enregistre les données de transfert dans et en dehors de l’ALU.</span><span class="sxs-lookup"><span data-stu-id="cabbb-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="cabbb-108">Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.</span><span class="sxs-lookup"><span data-stu-id="cabbb-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="cabbb-109">La version du nuanceur de sommets vs \_ 2 \_ x étend l’ensemble des fonctionnalités prises en charge par vs \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="cabbb-109">Vertex shader version vs\_2\_x extends the feature set supported by vs\_2\_0.</span></span> <span data-ttu-id="cabbb-110">Chaque fonctionnalité supplémentaire est représentée par une extrémité correspondante dans la structure [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) dans [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span><span class="sxs-lookup"><span data-stu-id="cabbb-110">Each additional feature is represented by a corresponding cap in the [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure within [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span></span> <span data-ttu-id="cabbb-111">Pour utiliser l’une des fonctionnalités améliorées représentées par ces majuscules, la version du nuanceur de sommets doit être spécifiée sous la forme vs \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="cabbb-111">To use any of the enhanced features represented by these caps, the vertex shader version must be specified as vs\_2\_x.</span></span>

-   <span data-ttu-id="cabbb-112">[Instructions-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contient une liste des instructions disponibles.</span><span class="sxs-lookup"><span data-stu-id="cabbb-112">[Instructions - vs\_2\_x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="cabbb-113">[Registres-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.</span><span class="sxs-lookup"><span data-stu-id="cabbb-113">[Registers - vs\_2\_x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="cabbb-114">Les [modificateurs de Registre du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers.md) permettent de modifier la façon dont une instruction fonctionne.</span><span class="sxs-lookup"><span data-stu-id="cabbb-114">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="cabbb-115">Les [modificateurs de Registre source du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="cabbb-115">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="cabbb-116">Le [Registre source Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.</span><span class="sxs-lookup"><span data-stu-id="cabbb-116">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="cabbb-117">Le [masquage du registre de destination](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) détermine les composants du registre de destination qui sont écrits.</span><span class="sxs-lookup"><span data-stu-id="cabbb-117">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="cabbb-118">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="cabbb-118">New Features</span></span>

<span data-ttu-id="cabbb-119">Les nouvelles fonctionnalités sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cabbb-119">New features are as follows:</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="cabbb-120">Contrôle de Flow dynamique</span><span class="sxs-lookup"><span data-stu-id="cabbb-120">Dynamic Flow Control</span></span>

<span data-ttu-id="cabbb-121">Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, les instructions de contrôle de workflow dynamique suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="cabbb-121">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, then the following dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="cabbb-122">Si \_ COMP-vs</span><span class="sxs-lookup"><span data-stu-id="cabbb-122">if\_comp - vs</span></span>](if-comp---vs.md)
-   [<span data-ttu-id="cabbb-123">Break-vs</span><span class="sxs-lookup"><span data-stu-id="cabbb-123">break - vs</span></span>](break---vs.md)
-   [<span data-ttu-id="cabbb-124">arrêt \_ COMP-vs</span><span class="sxs-lookup"><span data-stu-id="cabbb-124">break\_comp - vs</span></span>](break-comp---vs.md)

<span data-ttu-id="cabbb-125">Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) est également défini, les instructions de contrôle de Flow supplémentaires suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="cabbb-125">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is also set, the following additional flow control instructions are supported:</span></span>

-   [<span data-ttu-id="cabbb-126">\_COMP setp-vs</span><span class="sxs-lookup"><span data-stu-id="cabbb-126">setp\_comp - vs</span></span>](setp-comp---vs.md)
-   [<span data-ttu-id="cabbb-127">Si prédit-vs</span><span class="sxs-lookup"><span data-stu-id="cabbb-127">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="cabbb-128">callnz prédit-vs</span><span class="sxs-lookup"><span data-stu-id="cabbb-128">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="cabbb-129">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="cabbb-129">breakp - vs</span></span>](breakp---vs.md)

<span data-ttu-id="cabbb-130">La plage de valeurs pour la profondeur du contrôle de transmission dynamique est comprise entre 0 et 24 et est égale à la profondeur d’imbrication des instructions de contrôle de Flow dynamique (voir [limites d’imbrication du contrôle de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md) pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="cabbb-130">The range of values for dynamic flow control depth is 0 to 24 and is equal to the nesting depth of the dynamic flow control instructions (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span> <span data-ttu-id="cabbb-131">Si cette limite est égale à zéro, l’appareil ne prend pas en charge les instructions de contrôle de Flow dynamique.</span><span class="sxs-lookup"><span data-stu-id="cabbb-131">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

### <a name="number-of-temporary-registers"></a><span data-ttu-id="cabbb-132">Nombre de registres temporaires</span><span class="sxs-lookup"><span data-stu-id="cabbb-132">Number of Temporary Registers</span></span>

<span data-ttu-id="cabbb-133">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) représente le nombre de [registres temporaires](dx9-graphics-reference-asm-vs-registers-temporary.md)pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cabbb-133">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s supported by the device.</span></span> <span data-ttu-id="cabbb-134">La plage de valeurs de cette limite est comprise entre 12 et 32.</span><span class="sxs-lookup"><span data-stu-id="cabbb-134">The range of values for this cap is 12 to 32.</span></span>

### <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="cabbb-135">Profondeur d’imbrication du contrôle de Flow statique</span><span class="sxs-lookup"><span data-stu-id="cabbb-135">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="cabbb-136">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) représente la profondeur d’imbrication de deux types d’instructions de contrôle de Flow statique : [Loop-vs](loop---vs.md) / [REP-vs](rep---vs.md) et [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [If bool-vs](if-bool---vs.md). les instructions Loop-vs/REP-VS peuvent être imbriquées jusqu’à D3DVS20CAPS Deep.</span><span class="sxs-lookup"><span data-stu-id="cabbb-136">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the nesting depth of two types of static flow control instructions: [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) and [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[if bool - vs](if-bool---vs.md). loop - vs/rep - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="cabbb-137">De manière indépendante, les instructions Call-vs/callnz bool-VS peuvent être imbriquées jusqu’à D3DVS20CAPS Deep.</span><span class="sxs-lookup"><span data-stu-id="cabbb-137">Independently, call - vs/callnz bool - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="cabbb-138">Si D3DVS20CAPS est également défini, [callnz prédit-vs](callnz-pred---vs.md) est compté vers la profondeur d’imbrication de l’appel-vs/callnz bool-vs/if bool-vs (voir [limites d’imbrication du contrôle de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md) pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="cabbb-138">If D3DVS20CAPS is also set, then [callnz pred - vs](callnz-pred---vs.md) is counted toward the nesting depth of call - vs/callnz bool - vs/if bool - vs (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span>

### <a name="predication"></a><span data-ttu-id="cabbb-139">Prédicat</span><span class="sxs-lookup"><span data-stu-id="cabbb-139">Predication</span></span>

<span data-ttu-id="cabbb-140">Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) est défini, l’appareil prend en charge [setp \_ COMP-vs](setp-comp---vs.md) et la prédicat d’instruction.</span><span class="sxs-lookup"><span data-stu-id="cabbb-140">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is set, the device supports [setp\_comp - vs](setp-comp---vs.md) and instruction predication.</span></span> <span data-ttu-id="cabbb-141">Si D3DVS20CAPS est également supérieur à 0, les instructions de contrôle de workflow dynamique supplémentaires suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="cabbb-141">If D3DVS20CAPS is also greater than 0, then the following additional dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="cabbb-142">Si prédit-vs</span><span class="sxs-lookup"><span data-stu-id="cabbb-142">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="cabbb-143">callnz prédit-vs</span><span class="sxs-lookup"><span data-stu-id="cabbb-143">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="cabbb-144">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="cabbb-144">breakp - vs</span></span>](breakp---vs.md)

### <a name="instruction-count"></a><span data-ttu-id="cabbb-145">Nombre d’instructions</span><span class="sxs-lookup"><span data-stu-id="cabbb-145">Instruction Count</span></span>

<span data-ttu-id="cabbb-146">Chaque nuanceur de sommets peut avoir jusqu’à 256 instructions stockées.</span><span class="sxs-lookup"><span data-stu-id="cabbb-146">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="cabbb-147">Le nombre d’instructions exécutées peut être bien plus élevé (en raison de la prise en charge de la boucle/REP) et est limité par [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), qui doit être au moins 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="cabbb-147">The number of instructions run can be much higher (because of the loop/rep support), and is capped by [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cabbb-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cabbb-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cabbb-149">Nuanceurs vertex</span><span class="sxs-lookup"><span data-stu-id="cabbb-149">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 