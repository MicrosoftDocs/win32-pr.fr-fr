---
title: vs_2_x
description: En savoir plus sur vs_2_x, un nuanceur de sommet programmable, qui est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex.
ms.assetid: 64b07597-1e16-4803-b991-e78eabc2c060
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3449ae4c1e1eb3b977916f6fb1d19303e9d21a4e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010713"
---
# <a name="vs_2_x"></a><span data-ttu-id="e95f5-103">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e95f5-103">vs\_2\_x</span></span>

<span data-ttu-id="e95f5-104">Un nuanceur de sommet programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="e95f5-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="e95f5-105">Enregistre les données de transfert dans et en dehors de l’ALU.</span><span class="sxs-lookup"><span data-stu-id="e95f5-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="e95f5-106">Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.</span><span class="sxs-lookup"><span data-stu-id="e95f5-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="e95f5-107">La version du nuanceur de sommets vs \_ 2 \_ x étend l’ensemble des fonctionnalités prises en charge par vs \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="e95f5-107">Vertex shader version vs\_2\_x extends the feature set supported by vs\_2\_0.</span></span> <span data-ttu-id="e95f5-108">Chaque fonctionnalité supplémentaire est représentée par une extrémité correspondante dans la structure [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) dans [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span><span class="sxs-lookup"><span data-stu-id="e95f5-108">Each additional feature is represented by a corresponding cap in the [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure within [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps).</span></span> <span data-ttu-id="e95f5-109">Pour utiliser l’une des fonctionnalités améliorées représentées par ces majuscules, la version du nuanceur de sommets doit être spécifiée sous la forme vs \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="e95f5-109">To use any of the enhanced features represented by these caps, the vertex shader version must be specified as vs\_2\_x.</span></span>

-   <span data-ttu-id="e95f5-110">[Instructions-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contient une liste des instructions disponibles.</span><span class="sxs-lookup"><span data-stu-id="e95f5-110">[Instructions - vs\_2\_x](dx9-graphics-reference-asm-vs-instructions-vs-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="e95f5-111">[Registres-vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.</span><span class="sxs-lookup"><span data-stu-id="e95f5-111">[Registers - vs\_2\_x](dx9-graphics-reference-asm-vs-registers-vs-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="e95f5-112">Les [modificateurs de Registre du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers.md) permettent de modifier la façon dont une instruction fonctionne.</span><span class="sxs-lookup"><span data-stu-id="e95f5-112">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="e95f5-113">Les [modificateurs de Registre source du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="e95f5-113">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="e95f5-114">Le [Registre source Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.</span><span class="sxs-lookup"><span data-stu-id="e95f5-114">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="e95f5-115">Le [masquage du registre de destination](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) détermine les composants du registre de destination qui sont écrits.</span><span class="sxs-lookup"><span data-stu-id="e95f5-115">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="e95f5-116">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="e95f5-116">New Features</span></span>

<span data-ttu-id="e95f5-117">Les nouvelles fonctionnalités sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e95f5-117">New features are as follows:</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="e95f5-118">Contrôle de Flow dynamique</span><span class="sxs-lookup"><span data-stu-id="e95f5-118">Dynamic Flow Control</span></span>

<span data-ttu-id="e95f5-119">Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, les instructions de contrôle de workflow dynamique suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="e95f5-119">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) > 0, then the following dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="e95f5-120">Si \_ COMP-vs</span><span class="sxs-lookup"><span data-stu-id="e95f5-120">if\_comp - vs</span></span>](if-comp---vs.md)
-   [<span data-ttu-id="e95f5-121">Break-vs</span><span class="sxs-lookup"><span data-stu-id="e95f5-121">break - vs</span></span>](break---vs.md)
-   [<span data-ttu-id="e95f5-122">arrêt \_ COMP-vs</span><span class="sxs-lookup"><span data-stu-id="e95f5-122">break\_comp - vs</span></span>](break-comp---vs.md)

<span data-ttu-id="e95f5-123">Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) est également défini, les instructions de contrôle de Flow supplémentaires suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="e95f5-123">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is also set, the following additional flow control instructions are supported:</span></span>

-   [<span data-ttu-id="e95f5-124">\_COMP setp-vs</span><span class="sxs-lookup"><span data-stu-id="e95f5-124">setp\_comp - vs</span></span>](setp-comp---vs.md)
-   [<span data-ttu-id="e95f5-125">Si prédit-vs</span><span class="sxs-lookup"><span data-stu-id="e95f5-125">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="e95f5-126">callnz prédit-vs</span><span class="sxs-lookup"><span data-stu-id="e95f5-126">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="e95f5-127">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="e95f5-127">breakp - vs</span></span>](breakp---vs.md)

<span data-ttu-id="e95f5-128">La plage de valeurs pour la profondeur du contrôle de transmission dynamique est comprise entre 0 et 24 et est égale à la profondeur d’imbrication des instructions de contrôle de Flow dynamique (voir [limites d’imbrication du contrôle de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md) pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="e95f5-128">The range of values for dynamic flow control depth is 0 to 24 and is equal to the nesting depth of the dynamic flow control instructions (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span> <span data-ttu-id="e95f5-129">Si cette limite est égale à zéro, l’appareil ne prend pas en charge les instructions de contrôle de Flow dynamique.</span><span class="sxs-lookup"><span data-stu-id="e95f5-129">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

### <a name="number-of-temporary-registers"></a><span data-ttu-id="e95f5-130">Nombre de registres temporaires</span><span class="sxs-lookup"><span data-stu-id="e95f5-130">Number of Temporary Registers</span></span>

<span data-ttu-id="e95f5-131">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) représente le nombre de [registres temporaires](dx9-graphics-reference-asm-vs-registers-temporary.md)pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e95f5-131">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s supported by the device.</span></span> <span data-ttu-id="e95f5-132">La plage de valeurs de cette limite est comprise entre 12 et 32.</span><span class="sxs-lookup"><span data-stu-id="e95f5-132">The range of values for this cap is 12 to 32.</span></span>

### <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="e95f5-133">Profondeur d’imbrication du contrôle de Flow statique</span><span class="sxs-lookup"><span data-stu-id="e95f5-133">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="e95f5-134">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) représente la profondeur d’imbrication de deux types d’instructions de contrôle de Flow statique : [Loop-vs](loop---vs.md) / [REP-vs](rep---vs.md) et [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [If bool-vs](if-bool---vs.md). les instructions Loop-vs/REP-VS peuvent être imbriquées jusqu’à D3DVS20CAPS Deep.</span><span class="sxs-lookup"><span data-stu-id="e95f5-134">[D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) represents the nesting depth of two types of static flow control instructions: [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) and [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[if bool - vs](if-bool---vs.md). loop - vs/rep - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="e95f5-135">De manière indépendante, les instructions Call-vs/callnz bool-VS peuvent être imbriquées jusqu’à D3DVS20CAPS Deep.</span><span class="sxs-lookup"><span data-stu-id="e95f5-135">Independently, call - vs/callnz bool - vs instructions can be nested up to D3DVS20CAPS deep.</span></span> <span data-ttu-id="e95f5-136">Si D3DVS20CAPS est également défini, [callnz prédit-vs](callnz-pred---vs.md) est compté vers la profondeur d’imbrication de l’appel-vs/callnz bool-vs/if bool-vs (voir [limites d’imbrication du contrôle de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md) pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="e95f5-136">If D3DVS20CAPS is also set, then [callnz pred - vs](callnz-pred---vs.md) is counted toward the nesting depth of call - vs/callnz bool - vs/if bool - vs (see [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details).</span></span>

### <a name="predication"></a><span data-ttu-id="e95f5-137">Prédicat</span><span class="sxs-lookup"><span data-stu-id="e95f5-137">Predication</span></span>

<span data-ttu-id="e95f5-138">Si [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) est défini, l’appareil prend en charge [setp \_ COMP-vs](setp-comp---vs.md) et la prédicat d’instruction.</span><span class="sxs-lookup"><span data-stu-id="e95f5-138">If [D3DVS20CAPS](/windows/desktop/direct3d9/d3dvs20caps) is set, the device supports [setp\_comp - vs](setp-comp---vs.md) and instruction predication.</span></span> <span data-ttu-id="e95f5-139">Si D3DVS20CAPS est également supérieur à 0, les instructions de contrôle de workflow dynamique supplémentaires suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="e95f5-139">If D3DVS20CAPS is also greater than 0, then the following additional dynamic flow control instructions are supported:</span></span>

-   [<span data-ttu-id="e95f5-140">Si prédit-vs</span><span class="sxs-lookup"><span data-stu-id="e95f5-140">if pred - vs</span></span>](if-pred---vs.md)
-   [<span data-ttu-id="e95f5-141">callnz prédit-vs</span><span class="sxs-lookup"><span data-stu-id="e95f5-141">callnz pred - vs</span></span>](callnz-pred---vs.md)
-   [<span data-ttu-id="e95f5-142">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="e95f5-142">breakp - vs</span></span>](breakp---vs.md)

### <a name="instruction-count"></a><span data-ttu-id="e95f5-143">Nombre d’instructions</span><span class="sxs-lookup"><span data-stu-id="e95f5-143">Instruction Count</span></span>

<span data-ttu-id="e95f5-144">Chaque nuanceur de sommets peut avoir jusqu’à 256 instructions stockées.</span><span class="sxs-lookup"><span data-stu-id="e95f5-144">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="e95f5-145">Le nombre d’instructions exécutées peut être bien plus élevé (en raison de la prise en charge de la boucle/REP) et est limité par [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), qui doit être au moins 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="e95f5-145">The number of instructions run can be much higher (because of the loop/rep support), and is capped by [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9), which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e95f5-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e95f5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e95f5-147">Nuanceurs vertex</span><span class="sxs-lookup"><span data-stu-id="e95f5-147">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 