---
title: Assembly modèle 4 du nuanceur
description: Assembly modèle 4 du nuanceur
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029247"
---
# <a name="shader-model-4-assembly"></a><span data-ttu-id="59be0-103">Assembly modèle 4 du nuanceur</span><span class="sxs-lookup"><span data-stu-id="59be0-103">Shader Model 4 Assembly</span></span>

<span data-ttu-id="59be0-104">Le modèle de nuanceur 4 vous oblige à programmer des nuanceurs en HLSL.</span><span class="sxs-lookup"><span data-stu-id="59be0-104">Shader Model 4 requires you to program shaders in HLSL.</span></span> <span data-ttu-id="59be0-105">Toutefois, le compilateur du nuanceur compile le code HLSL dans un assembly qui s’exécute sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="59be0-105">However, the shader compiler compiles the HLSL code into assembly that runs on the device.</span></span> <span data-ttu-id="59be0-106">Si vous utilisez PIX pour Windows pour déboguer vos nuanceurs, vous pouvez choisir d’afficher le code du nuanceur en HLSL ou en assembly.</span><span class="sxs-lookup"><span data-stu-id="59be0-106">If you are using PIX for Windows to debug your shaders, you can choose to display shader code in either HLSL or assembly.</span></span> <span data-ttu-id="59be0-107">Cette section répertorie les instructions de l’assembly Shader Model 4 et Shader Model 4,1 que vous pouvez rencontrer lors du débogage d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="59be0-107">This section lists the Shader Model 4 and Shader Model 4.1 assembly instructions that you may encounter when debugging a shader.</span></span>

<dl>

[<span data-ttu-id="59be0-108">Modificateurs d’instruction</span><span class="sxs-lookup"><span data-stu-id="59be0-108">Instruction Modifiers</span></span>](instruction-modifiers.md)  
[<span data-ttu-id="59be0-109">add</span><span class="sxs-lookup"><span data-stu-id="59be0-109">add</span></span>](add--sm4---asm-.md)  
[<span data-ttu-id="59be0-110">and</span><span class="sxs-lookup"><span data-stu-id="59be0-110">and</span></span>](and--sm4---asm-.md)  
[<span data-ttu-id="59be0-111">break</span><span class="sxs-lookup"><span data-stu-id="59be0-111">break</span></span>](break--sm4---asm-.md)  
[<span data-ttu-id="59be0-112">breakc</span><span class="sxs-lookup"><span data-stu-id="59be0-112">breakc</span></span>](breakc--sm4---asm-.md)  
[<span data-ttu-id="59be0-113">call</span><span class="sxs-lookup"><span data-stu-id="59be0-113">call</span></span>](call--sm4---asm-.md)  
[<span data-ttu-id="59be0-114">callc</span><span class="sxs-lookup"><span data-stu-id="59be0-114">callc</span></span>](callc--sm4---asm-.md)  
[<span data-ttu-id="59be0-115">case</span><span class="sxs-lookup"><span data-stu-id="59be0-115">case</span></span>](case--sm4---asm-.md)  
[<span data-ttu-id="59be0-116">pouvoir</span><span class="sxs-lookup"><span data-stu-id="59be0-116">continue</span></span>](continue--sm4---asm-.md)  
[<span data-ttu-id="59be0-117">continuec</span><span class="sxs-lookup"><span data-stu-id="59be0-117">continuec</span></span>](continuec--sm4---asm-.md)  
[<span data-ttu-id="59be0-118">réduis</span><span class="sxs-lookup"><span data-stu-id="59be0-118">cut</span></span>](cut--sm4---asm-.md)  
[<span data-ttu-id="59be0-119">\_constantBuffer DCL</span><span class="sxs-lookup"><span data-stu-id="59be0-119">dcl\_constantBuffer</span></span>](dcl-constantbuffer.md)  
[<span data-ttu-id="59be0-120">DCL \_ globalFlags</span><span class="sxs-lookup"><span data-stu-id="59be0-120">dcl\_globalFlags</span></span>](dcl-globalflags.md)  
[<span data-ttu-id="59be0-121">\_immediateConstantBuffer DCL</span><span class="sxs-lookup"><span data-stu-id="59be0-121">dcl\_immediateConstantBuffer</span></span>](dcl-immediateconstantbuffer.md)  
[<span data-ttu-id="59be0-122">\_indexableTemp DCL</span><span class="sxs-lookup"><span data-stu-id="59be0-122">dcl\_indexableTemp</span></span>](dcl-indexabletemp.md)  
[<span data-ttu-id="59be0-123">\_indexRange DCL</span><span class="sxs-lookup"><span data-stu-id="59be0-123">dcl\_indexRange</span></span>](dcl-indexrange.md)  
[<span data-ttu-id="59be0-124">\_entrée DCL</span><span class="sxs-lookup"><span data-stu-id="59be0-124">dcl\_input</span></span>](dcl-input.md)  
[<span data-ttu-id="59be0-125">\_SV d’entrée DCL \_</span><span class="sxs-lookup"><span data-stu-id="59be0-125">dcl\_input\_sv</span></span>](dcl-input-sv.md)  
[<span data-ttu-id="59be0-126">\_vPrim d’entrée DCL</span><span class="sxs-lookup"><span data-stu-id="59be0-126">dcl\_input vPrim</span></span>](dcl-input-vprim.md)  
[<span data-ttu-id="59be0-127">\_maxOutputVertexCount DCL</span><span class="sxs-lookup"><span data-stu-id="59be0-127">dcl\_maxOutputVertexCount</span></span>](dcl-maxoutputvertexcount.md)  
[<span data-ttu-id="59be0-128">\_sortie DCL</span><span class="sxs-lookup"><span data-stu-id="59be0-128">dcl\_output</span></span>](dcl-output.md)  
[<span data-ttu-id="59be0-129">\_oDepth de sortie DCL \_</span><span class="sxs-lookup"><span data-stu-id="59be0-129">dcl\_output\_oDepth</span></span>](dcl-output-odepth.md)  
[<span data-ttu-id="59be0-130">copie DCL, \_ \_ SGV</span><span class="sxs-lookup"><span data-stu-id="59be0-130">dcl\_output\_sgv</span></span>](dcl-output-sgv.md)  
[<span data-ttu-id="59be0-131">\_SIV de sortie DCL \_</span><span class="sxs-lookup"><span data-stu-id="59be0-131">dcl\_output\_siv</span></span>](dcl-output-siv.md)  
[<span data-ttu-id="59be0-132">\_outputTopology DCL</span><span class="sxs-lookup"><span data-stu-id="59be0-132">dcl\_outputTopology</span></span>](dcl-outputtopology.md)  
[<span data-ttu-id="59be0-133">\_ressource DCL</span><span class="sxs-lookup"><span data-stu-id="59be0-133">dcl\_resource</span></span>](dcl-resource.md)  
[<span data-ttu-id="59be0-134">exemple de DCL \_</span><span class="sxs-lookup"><span data-stu-id="59be0-134">dcl\_sampler</span></span>](dcl-sampler.md)  
[<span data-ttu-id="59be0-135">temps de la DCL \_</span><span class="sxs-lookup"><span data-stu-id="59be0-135">dcl\_temps</span></span>](dcl-temps.md)  
[<span data-ttu-id="59be0-136">default</span><span class="sxs-lookup"><span data-stu-id="59be0-136">default</span></span>](default--sm4---asm-.md)  
[<span data-ttu-id="59be0-137">Deriv \_ RTX</span><span class="sxs-lookup"><span data-stu-id="59be0-137">deriv\_rtx</span></span>](deriv-rtx--sm4---asm-.md)  
[<span data-ttu-id="59be0-138">Deriv \_ propriété</span><span class="sxs-lookup"><span data-stu-id="59be0-138">deriv\_rty</span></span>](deriv-rty--sm4---asm-.md)  
[<span data-ttu-id="59be0-139">refuser</span><span class="sxs-lookup"><span data-stu-id="59be0-139">discard</span></span>](discard--sm4---asm-.md)  
[<span data-ttu-id="59be0-140">div</span><span class="sxs-lookup"><span data-stu-id="59be0-140">div</span></span>](div--sm4---asm-.md)  
[<span data-ttu-id="59be0-141">dp2</span><span class="sxs-lookup"><span data-stu-id="59be0-141">dp2</span></span>](dp2--sm4---asm-.md)  
[<span data-ttu-id="59be0-142">dp3</span><span class="sxs-lookup"><span data-stu-id="59be0-142">dp3</span></span>](dp3--sm4---asm-.md)  
[<span data-ttu-id="59be0-143">dp4</span><span class="sxs-lookup"><span data-stu-id="59be0-143">dp4</span></span>](dp4--sm4---asm-.md)  
[<span data-ttu-id="59be0-144">else</span><span class="sxs-lookup"><span data-stu-id="59be0-144">else</span></span>](else--sm4---asm-.md)  
[<span data-ttu-id="59be0-145">émettra</span><span class="sxs-lookup"><span data-stu-id="59be0-145">emit</span></span>](emit--sm4---asm-.md)  
[<span data-ttu-id="59be0-146">emitThenCut</span><span class="sxs-lookup"><span data-stu-id="59be0-146">emitThenCut</span></span>](emitthencut--sm4---asm-.md)  
[<span data-ttu-id="59be0-147">endif</span><span class="sxs-lookup"><span data-stu-id="59be0-147">endif</span></span>](endif--sm4---asm-.md)  
[<span data-ttu-id="59be0-148">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="59be0-148">endloop</span></span>](endloop--sm4---asm-.md)  
[<span data-ttu-id="59be0-149">endswitch</span><span class="sxs-lookup"><span data-stu-id="59be0-149">endswitch</span></span>](endswitch--sm4---asm-.md)  
[<span data-ttu-id="59be0-150">eq</span><span class="sxs-lookup"><span data-stu-id="59be0-150">eq</span></span>](eq--sm4---asm-.md)  
[<span data-ttu-id="59be0-151">exp</span><span class="sxs-lookup"><span data-stu-id="59be0-151">exp</span></span>](exp--sm4---asm-.md)  
[<span data-ttu-id="59be0-152">frc</span><span class="sxs-lookup"><span data-stu-id="59be0-152">frc</span></span>](frc--sm4---asm-.md)  
[<span data-ttu-id="59be0-153">ftoi</span><span class="sxs-lookup"><span data-stu-id="59be0-153">ftoi</span></span>](ftoi--sm4---asm-.md)  
[<span data-ttu-id="59be0-154">ftou</span><span class="sxs-lookup"><span data-stu-id="59be0-154">ftou</span></span>](ftou--sm4---asm-.md)  
[<span data-ttu-id="59be0-155">ge</span><span class="sxs-lookup"><span data-stu-id="59be0-155">ge</span></span>](ge--sm4---asm-.md)  
[<span data-ttu-id="59be0-156">IAdd</span><span class="sxs-lookup"><span data-stu-id="59be0-156">iadd</span></span>](iadd--sm4---asm-.md)  
[<span data-ttu-id="59be0-157">ibfe</span><span class="sxs-lookup"><span data-stu-id="59be0-157">ibfe</span></span>](dne--sm5---asm-.md)  
[<span data-ttu-id="59be0-158">ieq</span><span class="sxs-lookup"><span data-stu-id="59be0-158">ieq</span></span>](ieq--sm4---asm-.md)  
[<span data-ttu-id="59be0-159">if</span><span class="sxs-lookup"><span data-stu-id="59be0-159">if</span></span>](if--sm4---asm-.md)  
[<span data-ttu-id="59be0-160">IGE</span><span class="sxs-lookup"><span data-stu-id="59be0-160">ige</span></span>](ige--sm4---asm-.md)  
[<span data-ttu-id="59be0-161">ILT</span><span class="sxs-lookup"><span data-stu-id="59be0-161">ilt</span></span>](ilt--sm4---asm-.md)  
[<span data-ttu-id="59be0-162">imad</span><span class="sxs-lookup"><span data-stu-id="59be0-162">imad</span></span>](imad--sm4---asm-.md)  
[<span data-ttu-id="59be0-163">imin</span><span class="sxs-lookup"><span data-stu-id="59be0-163">imin</span></span>](imin--sm4---asm-.md)  
[<span data-ttu-id="59be0-164">imul</span><span class="sxs-lookup"><span data-stu-id="59be0-164">imul</span></span>](imul--sm4---asm-.md)  
[<span data-ttu-id="59be0-165">igne</span><span class="sxs-lookup"><span data-stu-id="59be0-165">ine</span></span>](ine--sm4---asm-.md)  
[<span data-ttu-id="59be0-166">ineg</span><span class="sxs-lookup"><span data-stu-id="59be0-166">ineg</span></span>](ineg--sm4---asm-.md)  
[<span data-ttu-id="59be0-167">ishl</span><span class="sxs-lookup"><span data-stu-id="59be0-167">ishl</span></span>](ishl--sm4---asm-.md)  
[<span data-ttu-id="59be0-168">ishr</span><span class="sxs-lookup"><span data-stu-id="59be0-168">ishr</span></span>](ishr--sm4---asm-.md)  
[<span data-ttu-id="59be0-169">itof</span><span class="sxs-lookup"><span data-stu-id="59be0-169">itof</span></span>](itof--sm4---asm-.md)  
[<span data-ttu-id="59be0-170">label</span><span class="sxs-lookup"><span data-stu-id="59be0-170">label</span></span>](label--sm4---asm-.md)  
[<span data-ttu-id="59be0-171">ld</span><span class="sxs-lookup"><span data-stu-id="59be0-171">ld</span></span>](ld--sm4---asm-.md)  
[<span data-ttu-id="59be0-172">Sign</span><span class="sxs-lookup"><span data-stu-id="59be0-172">log</span></span>](log--sm4---asm-.md)  
[<span data-ttu-id="59be0-173">loop</span><span class="sxs-lookup"><span data-stu-id="59be0-173">loop</span></span>](loop--sm4---asm-.md)  
[<span data-ttu-id="59be0-174">lt</span><span class="sxs-lookup"><span data-stu-id="59be0-174">lt</span></span>](lt--sm4---asm-.md)  
[<span data-ttu-id="59be0-175">Mad</span><span class="sxs-lookup"><span data-stu-id="59be0-175">mad</span></span>](mad--sm4---asm-.md)  
[<span data-ttu-id="59be0-176">max</span><span class="sxs-lookup"><span data-stu-id="59be0-176">max</span></span>](max--sm4---asm-.md)  
[<span data-ttu-id="59be0-177">min</span><span class="sxs-lookup"><span data-stu-id="59be0-177">min</span></span>](min--sm4---asm-.md)  
[<span data-ttu-id="59be0-178">Moy</span><span class="sxs-lookup"><span data-stu-id="59be0-178">mov</span></span>](mov--sm4---asm-.md)  
[<span data-ttu-id="59be0-179">movc</span><span class="sxs-lookup"><span data-stu-id="59be0-179">movc</span></span>](movc--sm4---asm-.md)  
[<span data-ttu-id="59be0-180">mul</span><span class="sxs-lookup"><span data-stu-id="59be0-180">mul</span></span>](mul--sm4---asm-.md)  
[<span data-ttu-id="59be0-181">ne</span><span class="sxs-lookup"><span data-stu-id="59be0-181">ne</span></span>](ne--sm4---asm-.md)  
[<span data-ttu-id="59be0-182">NOP</span><span class="sxs-lookup"><span data-stu-id="59be0-182">nop</span></span>](nop--sm4---asm-.md)  
[<span data-ttu-id="59be0-183">not</span><span class="sxs-lookup"><span data-stu-id="59be0-183">not</span></span>](not--sm4---asm-.md)  
[<span data-ttu-id="59be0-184">or</span><span class="sxs-lookup"><span data-stu-id="59be0-184">or</span></span>](or--sm4---asm-.md)  
[<span data-ttu-id="59be0-185">ResInfo</span><span class="sxs-lookup"><span data-stu-id="59be0-185">resinfo</span></span>](resinfo--sm4---asm-.md)  
[<span data-ttu-id="59be0-186">Av</span><span class="sxs-lookup"><span data-stu-id="59be0-186">ret</span></span>](ret--sm4---asm-.md)  
[<span data-ttu-id="59be0-187">retc</span><span class="sxs-lookup"><span data-stu-id="59be0-187">retc</span></span>](retc--sm4---asm-.md)  
[<span data-ttu-id="59be0-188">\_arrondir ne</span><span class="sxs-lookup"><span data-stu-id="59be0-188">round\_ne</span></span>](round-ne--sm4---asm-.md)  
[<span data-ttu-id="59be0-189">\_arrondir</span><span class="sxs-lookup"><span data-stu-id="59be0-189">round\_ni</span></span>](round-ni--sm4---asm-.md)  
[<span data-ttu-id="59be0-190">arrondi \_ pi</span><span class="sxs-lookup"><span data-stu-id="59be0-190">round\_pi</span></span>](round-pi--sm4---asm-.md)  
[<span data-ttu-id="59be0-191">rond \_ z</span><span class="sxs-lookup"><span data-stu-id="59be0-191">round\_z</span></span>](round-z--sm4---asm-.md)  
[<span data-ttu-id="59be0-192">rsq</span><span class="sxs-lookup"><span data-stu-id="59be0-192">rsq</span></span>](rsq--sm4---asm-.md)  
[<span data-ttu-id="59be0-193">exemple</span><span class="sxs-lookup"><span data-stu-id="59be0-193">sample</span></span>](sample--sm4---asm-.md)  
[<span data-ttu-id="59be0-194">exemple \_ b</span><span class="sxs-lookup"><span data-stu-id="59be0-194">sample\_b</span></span>](sample-b--sm4---asm-.md)  
[<span data-ttu-id="59be0-195">exemple \_ c</span><span class="sxs-lookup"><span data-stu-id="59be0-195">sample\_c</span></span>](sample-c--sm4---asm-.md)  
[<span data-ttu-id="59be0-196">exemple \_ c \_ LZ</span><span class="sxs-lookup"><span data-stu-id="59be0-196">sample\_c\_lz</span></span>](sample-c-lz--sm4---asm-.md)  
[<span data-ttu-id="59be0-197">exemple \_ d</span><span class="sxs-lookup"><span data-stu-id="59be0-197">sample\_d</span></span>](sample-d--sm4---asm-.md)  
[<span data-ttu-id="59be0-198">exemple \_ l</span><span class="sxs-lookup"><span data-stu-id="59be0-198">sample\_l</span></span>](sample-l--sm4---asm-.md)  
[<span data-ttu-id="59be0-199">SinCos,</span><span class="sxs-lookup"><span data-stu-id="59be0-199">sincos</span></span>](sincos--sm4---asm-.md)  
[<span data-ttu-id="59be0-200">racine</span><span class="sxs-lookup"><span data-stu-id="59be0-200">sqrt</span></span>](sqrt--sm4---asm-.md)  
[<span data-ttu-id="59be0-201">switch</span><span class="sxs-lookup"><span data-stu-id="59be0-201">switch</span></span>](switch--sm4---asm-.md)  
[<span data-ttu-id="59be0-202">UDIV</span><span class="sxs-lookup"><span data-stu-id="59be0-202">udiv</span></span>](udiv--sm4---asm-.md)  
[<span data-ttu-id="59be0-203">uge</span><span class="sxs-lookup"><span data-stu-id="59be0-203">uge</span></span>](uge--sm4---asm-.md)  
[<span data-ttu-id="59be0-204">ULT</span><span class="sxs-lookup"><span data-stu-id="59be0-204">ult</span></span>](ult--sm4---asm-.md)  
[<span data-ttu-id="59be0-205">umad</span><span class="sxs-lookup"><span data-stu-id="59be0-205">umad</span></span>](umad--sm4---asm-.md)  
[<span data-ttu-id="59be0-206">UMAX</span><span class="sxs-lookup"><span data-stu-id="59be0-206">umax</span></span>](umax--sm4---asm-.md)  
[<span data-ttu-id="59be0-207">umin</span><span class="sxs-lookup"><span data-stu-id="59be0-207">umin</span></span>](umin--sm4---asm-.md)  
[<span data-ttu-id="59be0-208">umul</span><span class="sxs-lookup"><span data-stu-id="59be0-208">umul</span></span>](umul--sm4---asm-.md)  
[<span data-ttu-id="59be0-209">ushr</span><span class="sxs-lookup"><span data-stu-id="59be0-209">ushr</span></span>](ushr--sm4---asm-.md)  
[<span data-ttu-id="59be0-210">utof</span><span class="sxs-lookup"><span data-stu-id="59be0-210">utof</span></span>](utof--sm4---asm-.md)  
[<span data-ttu-id="59be0-211">XOR</span><span class="sxs-lookup"><span data-stu-id="59be0-211">xor</span></span>](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a><span data-ttu-id="59be0-212">Assembly modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="59be0-212">Shader Model 4.1 Assembly</span></span>

<span data-ttu-id="59be0-213">Le modèle de nuanceur 4,1 prend en charge toutes les instructions du Shader Model 4,0 et les instructions supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="59be0-213">Shader Model 4.1 supports all of the Shader Model 4.0 instructions and the following additional instructions:</span></span>

<dl>

[<span data-ttu-id="59be0-214">gather4</span><span class="sxs-lookup"><span data-stu-id="59be0-214">gather4</span></span>](gather4--sm4-1---asm-.md)  
[<span data-ttu-id="59be0-215">ld2dms</span><span class="sxs-lookup"><span data-stu-id="59be0-215">ld2dms</span></span>](ld2dms--sm4-1---asm-.md)  
[<span data-ttu-id="59be0-216">écart</span><span class="sxs-lookup"><span data-stu-id="59be0-216">lod</span></span>](lod--sm4-1---asm-.md)  
[<span data-ttu-id="59be0-217">sampleinfo</span><span class="sxs-lookup"><span data-stu-id="59be0-217">sampleinfo</span></span>](sampleinfo--sm4-1---asm-.md)  
[<span data-ttu-id="59be0-218">samplepos</span><span class="sxs-lookup"><span data-stu-id="59be0-218">samplepos</span></span>](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="59be0-219">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59be0-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59be0-220">Référence du nuanceur asm</span><span class="sxs-lookup"><span data-stu-id="59be0-220">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> <dt>

[<span data-ttu-id="59be0-221">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="59be0-221">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




