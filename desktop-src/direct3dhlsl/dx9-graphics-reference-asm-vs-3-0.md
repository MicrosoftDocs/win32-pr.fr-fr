---
title: vs_3_0
description: En savoir plus sur vs_3_0, un nuanceur de sommet programmable, qui est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 310d64170280053c34766f214969f78d66560ea3
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011072"
---
# <a name="vs_3_0"></a><span data-ttu-id="74204-103">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="74204-103">vs\_3\_0</span></span>

<span data-ttu-id="74204-104">Un nuanceur de sommet programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="74204-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="74204-105">Enregistre les données de transfert dans et en dehors de l’ALU.</span><span class="sxs-lookup"><span data-stu-id="74204-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="74204-106">Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.</span><span class="sxs-lookup"><span data-stu-id="74204-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

<span data-ttu-id="74204-107">La version du nuanceur de sommets et \_ 3 \_ 0 étend l’ensemble des fonctionnalités prises en charge par vs \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="74204-107">Vertex shader version vs\_3\_0 extends the feature set supported by vs\_2\_x.</span></span> <span data-ttu-id="74204-108">Chacune des fonctionnalités de vs \_ 2 X nécessitant \_ une limite définie est disponible dans vs \_ 3 \_ 0 sans nécessiter d’extrémité.</span><span class="sxs-lookup"><span data-stu-id="74204-108">Each of the features in vs\_2\_X that requires a cap to be set, is available in vs\_3\_0 without requiring the cap.</span></span>

-   <span data-ttu-id="74204-109">[Instructions-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contient une liste des instructions disponibles.</span><span class="sxs-lookup"><span data-stu-id="74204-109">[Instructions - vs\_3\_0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="74204-110">[Registres-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.</span><span class="sxs-lookup"><span data-stu-id="74204-110">[Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="74204-111">Les [modificateurs de Registre du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers.md) permettent de modifier la façon dont une instruction fonctionne.</span><span class="sxs-lookup"><span data-stu-id="74204-111">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="74204-112">Les [modificateurs de Registre source du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="74204-112">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="74204-113">Le [Registre source Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.</span><span class="sxs-lookup"><span data-stu-id="74204-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="74204-114">Le [masquage du registre de destination](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) détermine les composants du registre de destination qui sont écrits.</span><span class="sxs-lookup"><span data-stu-id="74204-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="new-features"></a><span data-ttu-id="74204-115">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="74204-115">New Features</span></span>

<span data-ttu-id="74204-116">Les nouvelles fonctionnalités de la version de nuanceur de sommets et \_ 3 \_ 0 sont répertoriées dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="74204-116">New features of vertex shader version vs\_3\_0 are listed in the following sections.</span></span>

### <a name="indexing-registers"></a><span data-ttu-id="74204-117">Indexation des registres</span><span class="sxs-lookup"><span data-stu-id="74204-117">Indexing Registers</span></span>

<span data-ttu-id="74204-118">Dans les modèles de nuanceur précédents, seule la Banque de registres constantes peut être indexée.</span><span class="sxs-lookup"><span data-stu-id="74204-118">In the earlier shader models, only the constant register bank could be indexed.</span></span> <span data-ttu-id="74204-119">Dans ce modèle, les banques de registres suivantes peuvent être indexées à l’aide du registre de compteur de boucle (aL) :</span><span class="sxs-lookup"><span data-stu-id="74204-119">In this model, the following register banks can be indexed, using the loop counter register (aL):</span></span>

-   <span data-ttu-id="74204-120">Registre d’entrée (v \# )</span><span class="sxs-lookup"><span data-stu-id="74204-120">Input register (v\#)</span></span>
-   <span data-ttu-id="74204-121">Registre de sortie (o \# )</span><span class="sxs-lookup"><span data-stu-id="74204-121">Output register (o\#)</span></span>

### <a name="vertex-textures"></a><span data-ttu-id="74204-122">Textures de vertex</span><span class="sxs-lookup"><span data-stu-id="74204-122">Vertex Textures</span></span>

<span data-ttu-id="74204-123">Ce modèle de nuanceur prend en charge la recherche de texture dans le nuanceur vertex à l’aide de texldl.</span><span class="sxs-lookup"><span data-stu-id="74204-123">This shader model supports texture lookup in the vertex shader using texldl.</span></span> <span data-ttu-id="74204-124">Le moteur de vertex a quatre étapes d’échantillonnage de texture (distinctes de l’échantillonneur de mappage de déplacement et les échantillonneurs de texture dans le moteur de pixels) qui peuvent être utilisés pour échantillonner des textures définies à ces étapes.</span><span class="sxs-lookup"><span data-stu-id="74204-124">The vertex engine has four texture sampler stages (distinct from the displacement map sampler and the texture samplers in the pixel engine) that can be used to sample textures set at those stages.</span></span> <span data-ttu-id="74204-125">Consultez [textures de vertex dans vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span><span class="sxs-lookup"><span data-stu-id="74204-125">See [Vertex Textures in vs\_3\_0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).</span></span>

### <a name="vertex-stream-frequency"></a><span data-ttu-id="74204-126">Fréquence du flux de vertex</span><span class="sxs-lookup"><span data-stu-id="74204-126">Vertex Stream Frequency</span></span>

<span data-ttu-id="74204-127">Cette fonctionnalité permet à un sous-ensemble des registres d’entrée d’être initialisés à un taux différent d’une fois par vertex.</span><span class="sxs-lookup"><span data-stu-id="74204-127">This feature allows a subset of the input registers to be initialized at a rate different from once per vertex.</span></span> <span data-ttu-id="74204-128">Consultez [dessin de géométrie non indexée](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span><span class="sxs-lookup"><span data-stu-id="74204-128">See [Drawing Non-Indexed Geometry](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).</span></span>

### <a name="shader-output"></a><span data-ttu-id="74204-129">Sortie du nuanceur</span><span class="sxs-lookup"><span data-stu-id="74204-129">Shader Output</span></span>

<span data-ttu-id="74204-130">Comme pour vs \_ 2 \_ 0, la sortie du nuanceur peut varier en fonction du contrôle de Flow statique.</span><span class="sxs-lookup"><span data-stu-id="74204-130">Similar to vs\_2\_0, the output of the shader can vary with static flow control.</span></span> <span data-ttu-id="74204-131">Soyez vigilant avec la branche dynamique, car cela peut entraîner une variation des sorties de nuanceur par vertex.</span><span class="sxs-lookup"><span data-stu-id="74204-131">Be careful with dynamic branching as this can cause shader outputs to vary per vertex.</span></span> <span data-ttu-id="74204-132">Cela produira des résultats imprévisibles sur un matériel différent.</span><span class="sxs-lookup"><span data-stu-id="74204-132">This will produce unpredictable results on different hardware.</span></span>

### <a name="dynamic-flow-control"></a><span data-ttu-id="74204-133">Contrôle de Flow dynamique</span><span class="sxs-lookup"><span data-stu-id="74204-133">Dynamic flow control</span></span>

<span data-ttu-id="74204-134">Toutes les instructions de contrôle de Flow dynamique sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="74204-134">All dynamic flow control instructions are supported.</span></span> <span data-ttu-id="74204-135">La valeur de profondeur d’imbrication maximale autorisée est 24.</span><span class="sxs-lookup"><span data-stu-id="74204-135">The maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="74204-136">(Pour plus d’informations, consultez [limites d’imbrication du contrôle de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md) .)</span><span class="sxs-lookup"><span data-stu-id="74204-136">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="temporary-registers"></a><span data-ttu-id="74204-137">Registres temporaires</span><span class="sxs-lookup"><span data-stu-id="74204-137">Temporary Registers</span></span>

<span data-ttu-id="74204-138">Un total de 32 registres temporaires (r \# ) est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="74204-138">A total of 32 temporary registers (r\#) is supported.</span></span>

### <a name="static-flow-control"></a><span data-ttu-id="74204-139">Contrôle de Flow statique</span><span class="sxs-lookup"><span data-stu-id="74204-139">Static Flow Control</span></span>

<span data-ttu-id="74204-140">La profondeur d’imbrication maximale pour [Loop-vs](loop---vs.md) / [REP-vs](rep---vs.md) est 4.</span><span class="sxs-lookup"><span data-stu-id="74204-140">The maximum nesting depth for [loop - vs](loop---vs.md)/[rep - vs](rep---vs.md) is 4.</span></span> <span data-ttu-id="74204-141">La profondeur d’imbrication maximale pour [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [callnz prédit-vs](callnz-pred---vs.md) est 4.</span><span class="sxs-lookup"><span data-stu-id="74204-141">The maximum nesting depth for [call - vs](call---vs.md)/[callnz bool - vs](callnz-bool---vs.md)/[callnz pred - vs](callnz-pred---vs.md) is 4.</span></span> <span data-ttu-id="74204-142">Pour [si bool-vs](if-bool---vs.md), la valeur de profondeur d’imbrication maximale autorisée est 24.</span><span class="sxs-lookup"><span data-stu-id="74204-142">For [if bool - vs](if-bool---vs.md), the maximum nesting depth value allowed is 24.</span></span> <span data-ttu-id="74204-143">(Pour plus d’informations, consultez [limites d’imbrication du contrôle de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md) .)</span><span class="sxs-lookup"><span data-stu-id="74204-143">(See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md) for details.)</span></span>

### <a name="predication"></a><span data-ttu-id="74204-144">Prédicat</span><span class="sxs-lookup"><span data-stu-id="74204-144">Predication</span></span>

<span data-ttu-id="74204-145">Le prédicat d’instruction est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="74204-145">Instruction predication is supported.</span></span> <span data-ttu-id="74204-146">Utilisez [setp \_ COMP-vs](setp-comp---vs.md) pour définir le registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="74204-146">Use [setp\_comp - vs](setp-comp---vs.md) to set the predicate register.</span></span>

### <a name="instruction-count"></a><span data-ttu-id="74204-147">Nombre d’instructions</span><span class="sxs-lookup"><span data-stu-id="74204-147">Instruction Count</span></span>

<span data-ttu-id="74204-148">Chaque nuanceur vertex est autorisé à partir de 512 jusqu’au nombre d’emplacements dans MaxVertexShader30InstructionSlots dans [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="74204-148">Each vertex shader is allowed anywhere from 512 up to the number of slots in MaxVertexShader30InstructionSlots in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> <span data-ttu-id="74204-149">Le nombre d’instructions exécutées peut être bien plus élevé en raison de la prise en charge de la boucle/REP ; Toutefois, cela est limité par MaxVShaderInstructionsExecuted dans D3DCAPS9, qui doit être au moins 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="74204-149">The number of instructions run can be much higher because of the loop/rep support; however, this is capped by MaxVShaderInstructionsExecuted in D3DCAPS9 which should be at least 0xFFFF.</span></span>

### <a name="device-caps"></a><span data-ttu-id="74204-150">Cap de l’appareil</span><span class="sxs-lookup"><span data-stu-id="74204-150">Device Caps</span></span>

<span data-ttu-id="74204-151">Si le nuanceur de sommets 3 \_ 0 est pris en charge, les limites suivantes sont prises en charge dans le matériel (au minimum) :</span><span class="sxs-lookup"><span data-stu-id="74204-151">If Vertex Shader 3\_0 is supported, the following caps are supported in hardware (at a minimum):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74204-152">Encapsul</span><span class="sxs-lookup"><span data-stu-id="74204-152">Cap</span></span></th>
<th><span data-ttu-id="74204-153">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="74204-153">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74204-154">Bouchons de nuanceur</span><span class="sxs-lookup"><span data-stu-id="74204-154">Shader caps</span></span></td>
<td><ul>
<li><span data-ttu-id="74204-155">DynamicFlowControlDepth est 24</span><span class="sxs-lookup"><span data-stu-id="74204-155">DynamicFlowControlDepth is 24</span></span></li>
<li><span data-ttu-id="74204-156">NumTemps est 32</span><span class="sxs-lookup"><span data-stu-id="74204-156">NumTemps is 32</span></span></li>
<li><span data-ttu-id="74204-157">StaticFlowControlDepth est 4</span><span class="sxs-lookup"><span data-stu-id="74204-157">StaticFlowControlDepth is 4</span></span></li>
<li><span data-ttu-id="74204-158">Le prédicat est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="74204-158">Predication is supported.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74204-159">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span><span class="sxs-lookup"><span data-stu-id="74204-159">GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</span></span></td>
<td><span data-ttu-id="74204-160">8 Ko</span><span class="sxs-lookup"><span data-stu-id="74204-160">8K</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74204-161">VertexShaderVersion</span><span class="sxs-lookup"><span data-stu-id="74204-161">VertexShaderVersion</span></span></td>
<td><span data-ttu-id="74204-162">3_0</span><span class="sxs-lookup"><span data-stu-id="74204-162">3_0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74204-163">MaxVertexShaderConst</span><span class="sxs-lookup"><span data-stu-id="74204-163">MaxVertexShaderConst</span></span></td>
<td><span data-ttu-id="74204-164">256</span><span class="sxs-lookup"><span data-stu-id="74204-164">256</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74204-165">MaxVertexShader30InstructionSlots</span><span class="sxs-lookup"><span data-stu-id="74204-165">MaxVertexShader30InstructionSlots</span></span></td>
<td><span data-ttu-id="74204-166">512</span><span class="sxs-lookup"><span data-stu-id="74204-166">512</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74204-167">Prise en charge du brouillard</span><span class="sxs-lookup"><span data-stu-id="74204-167">Fog support</span></span></td>
<td><span data-ttu-id="74204-168">D3DPRASTERCAPS_FOGVERTEX</span><span class="sxs-lookup"><span data-stu-id="74204-168">D3DPRASTERCAPS_FOGVERTEX</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74204-169">VertexTextureFilterCaps</span><span class="sxs-lookup"><span data-stu-id="74204-169">VertexTextureFilterCaps</span></span></td>
<td><ul>
<li><span data-ttu-id="74204-170"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="74204-170"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></span></span></li>
<li><span data-ttu-id="74204-171"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span><span class="sxs-lookup"><span data-stu-id="74204-171"><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74204-172"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span><span class="sxs-lookup"><span data-stu-id="74204-172"><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></span></span></td>
<td><span data-ttu-id="74204-173">Les éléments vertex dans une déclaration de vertex peuvent partager le même décalage de flux.</span><span class="sxs-lookup"><span data-stu-id="74204-173">Vertex elements in a vertex declaration can share the same stream offset.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74204-174">Formats de vertex</span><span class="sxs-lookup"><span data-stu-id="74204-174">Vertex formats</span></span></td>
<td><ul>
<li><span data-ttu-id="74204-175">D3DDECLTYPE_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="74204-175">D3DDECLTYPE_UBYTE4</span></span></li>
<li><span data-ttu-id="74204-176">D3DDECLTYPE_UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="74204-176">D3DDECLTYPE_UBYTE4N</span></span></li>
<li><span data-ttu-id="74204-177">D3DDECLTYPE_SHORT2N</span><span class="sxs-lookup"><span data-stu-id="74204-177">D3DDECLTYPE_SHORT2N</span></span></li>
<li><span data-ttu-id="74204-178">D3DDECLTYPE_SHORT4N</span><span class="sxs-lookup"><span data-stu-id="74204-178">D3DDECLTYPE_SHORT4N</span></span></li>
<li><span data-ttu-id="74204-179">D3DDECLTYPE_FLOAT16_2</span><span class="sxs-lookup"><span data-stu-id="74204-179">D3DDECLTYPE_FLOAT16_2</span></span></li>
<li><span data-ttu-id="74204-180">D3DDECLTYPE_FLOAT16_4</span><span class="sxs-lookup"><span data-stu-id="74204-180">D3DDECLTYPE_FLOAT16_4</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="74204-181">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="74204-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74204-182">Nuanceurs vertex</span><span class="sxs-lookup"><span data-stu-id="74204-182">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 