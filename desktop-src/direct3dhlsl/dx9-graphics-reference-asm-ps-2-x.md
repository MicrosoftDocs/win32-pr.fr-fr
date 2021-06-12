---
title: ps_2_x
description: En savoir plus sur ps_2_x, un nuanceur de pixels programmable, qui est constitué d’un ensemble d’instructions qui s’appliquent aux données de pixels.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9efedc6011cb63b6465fd2d3ced4a7807c09f4da
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010872"
---
# <a name="ps_2_x"></a><span data-ttu-id="b2bb7-103">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b2bb7-103">ps\_2\_x</span></span>

<span data-ttu-id="b2bb7-104">Un nuanceur de pixels programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-104">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="b2bb7-105">Enregistre les données de transfert dans et en dehors de l’ALU.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="b2bb7-106">Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="b2bb7-107">[les \_ instructions PS 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contiennent une liste des instructions disponibles.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-107">[ps\_2\_x Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="b2bb7-108">[ \_ registres PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-108">[ps\_2\_x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="b2bb7-109">[Modificateurs](dx9-graphics-reference-asm-ps-registers-modifiers.md) Sont utilisées pour modifier le mode de fonctionnement d’une instruction.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-109">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="b2bb7-110">Le [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) détermine les composants du registre de destination qui sont écrits.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="b2bb7-111">Les [modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-111">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="b2bb7-112">Le [Registre source Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="dynamic-flow-control"></a><span data-ttu-id="b2bb7-113">Contrôle de Flow dynamique</span><span class="sxs-lookup"><span data-stu-id="b2bb7-113">Dynamic Flow Control</span></span>

<span data-ttu-id="b2bb7-114">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) représente la profondeur d’imbrication des instructions de contrôle de Flow [](if-bool---ps.md)dynamique : [si \_ COMP](if-comp---ps.md), [si \_ prédit](if-pred---ps.md), [break-PS](break---ps.md)et [break \_ COMP-PS](break-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-114">[**DynamicFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of dynamic flow control instructions: [if](if-bool---ps.md), [if\_comp](if-comp---ps.md), [if\_pred](if-pred---ps.md), [break - ps](break---ps.md), and [break\_comp - ps](break-comp---ps.md).</span></span> <span data-ttu-id="b2bb7-115">La valeur est égale à la profondeur d’imbrication du bloc if \_ COMP.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-115">The value is equal to the nesting depth of the if\_comp block.</span></span> <span data-ttu-id="b2bb7-116">Si cette limite est égale à zéro, l’appareil ne prend pas en charge les instructions de contrôle de Flow dynamique.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-116">If this cap is zero, the device does not support dynamic flow control instructions.</span></span>

## <a name="number-of-temporary-registers"></a><span data-ttu-id="b2bb7-117">Nombre de registres temporaires</span><span class="sxs-lookup"><span data-stu-id="b2bb7-117">Number of Temporary Registers</span></span>

<span data-ttu-id="b2bb7-118">Nombre de registres temporaires pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-118">The number of temporary registers supported by the device.</span></span> <span data-ttu-id="b2bb7-119">La plage est comprise entre 12 et 32.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-119">The range is from 12 to 32.</span></span>

## <a name="static-flow-control-nesting-depth"></a><span data-ttu-id="b2bb7-120">Profondeur d’imbrication du contrôle de Flow statique</span><span class="sxs-lookup"><span data-stu-id="b2bb7-120">Static Flow Control Nesting Depth</span></span>

<span data-ttu-id="b2bb7-121">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) représente la profondeur d’imbrication de deux types d’instructions de contrôle de Flow statique : le REP de [boucle](loop---ps.md)  / [](rep---ps.md) et l' [appel](call---ps.md)de  / [callnz](callnz-bool---ps.md).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-121">[**StaticFlowControlDepth**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) represents the nesting depth of two types of static flow control instructions: [loop](loop---ps.md) /[rep](rep---ps.md) And [call](call---ps.md) /[callnz](callnz-bool---ps.md).</span></span> <span data-ttu-id="b2bb7-122">les instructions Loop/REP peuvent être imbriquées jusqu’à **StaticFlowControlDepth** Deep.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-122">loop /rep instructions can be nested up to **StaticFlowControlDepth** deep.</span></span> <span data-ttu-id="b2bb7-123">De manière indépendante, les instructions/callnz peuvent être imbriquées jusqu’à **StaticFlowControlDepth** Deep.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-123">Independently, call /callnz instructions can be nested up to **StaticFlowControlDepth** deep.</span></span>

## <a name="number-of-instruction-slots"></a><span data-ttu-id="b2bb7-124">Nombre d’emplacements d’instructions</span><span class="sxs-lookup"><span data-stu-id="b2bb7-124">Number of Instruction Slots</span></span>

<span data-ttu-id="b2bb7-125">Le nombre d’emplacements d’instruction peut être compris entre 96 et 512, et est spécifié par [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-125">The number of instruction slots can range from 96 to a maximum of 512, and is specified by the [**MaxPixelShaderInstructionSlots**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).</span></span> <span data-ttu-id="b2bb7-126">Le nombre total d’instructions pouvant être exécutées est défini par **MaxPixelShaderInstructionsExecuted**.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-126">The total number of instructions that can run is defined by **MaxPixelShaderInstructionsExecuted**.</span></span> <span data-ttu-id="b2bb7-127">Cette valeur peut être supérieure au nombre d’emplacements d’instruction en raison des appels de boucle et de sous-routine.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-127">This can be larger than the number of instruction slots due to looping and subroutine calls.</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="b2bb7-128">Swizzle arbitraire</span><span class="sxs-lookup"><span data-stu-id="b2bb7-128">Arbitrary Swizzle</span></span>

<span data-ttu-id="b2bb7-129">Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini, le Swizzle arbitraire est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-129">If [**D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, arbitrary swizzle is supported.</span></span> <span data-ttu-id="b2bb7-130">Consultez [Registre source Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-130">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="gradient-instructions"></a><span data-ttu-id="b2bb7-131">Instructions de dégradé</span><span class="sxs-lookup"><span data-stu-id="b2bb7-131">Gradient Instructions</span></span>

<span data-ttu-id="b2bb7-132">Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini, les instructions de dégradé sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-132">If [**D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, gradient instructions are supported.</span></span> <span data-ttu-id="b2bb7-133">Consultez [DSX-PS](dsx---ps.md), [DSY-PS](dsy---ps.md)et [texldd-PS](texldd---ps.md).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-133">See [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md), and [texldd - ps](texldd---ps.md).</span></span>

## <a name="predication"></a><span data-ttu-id="b2bb7-134">Prédicat</span><span class="sxs-lookup"><span data-stu-id="b2bb7-134">Predication</span></span>

<span data-ttu-id="b2bb7-135">Si [**le \_ \_ prédicat D3DD3DPSHADERCAPS2 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini, la prédicat d’instruction est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-135">If [**D3DD3DPSHADERCAPS2\_0\_PREDICATION**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, instruction predication is supported.</span></span> <span data-ttu-id="b2bb7-136">Consultez [Registre de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-136">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

## <a name="dependent-read-limit"></a><span data-ttu-id="b2bb7-137">Limite de lecture dépendante</span><span class="sxs-lookup"><span data-stu-id="b2bb7-137">Dependent Read Limit</span></span>

<span data-ttu-id="b2bb7-138">Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini, aucune limite de lecture n’est dépendante.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-138">If [**D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there are no dependent read limits.</span></span>

## <a name="texture-instruction-limit"></a><span data-ttu-id="b2bb7-139">Limite de l’instruction de texture</span><span class="sxs-lookup"><span data-stu-id="b2bb7-139">Texture Instruction Limit</span></span>

<span data-ttu-id="b2bb7-140">Si [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) est défini, aucune limite n’est imposée sur les instructions de texture.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-140">If [**D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) is set, there is no limit on texture instructions.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="b2bb7-141">Nombre d’échantillonneurs</span><span class="sxs-lookup"><span data-stu-id="b2bb7-141">Sampler Count</span></span>

<span data-ttu-id="b2bb7-142">Le nombre d’échantillonneurs de texture disponibles est 16.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-142">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2bb7-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2bb7-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2bb7-144">Nuanceurs de pixels</span><span class="sxs-lookup"><span data-stu-id="b2bb7-144">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 