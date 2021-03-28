---
title: sample_c (SM4-ASM)
description: Effectue un filtre de comparaison.
ms.assetid: 59786ED2-48FB-494E-A5A4-F732D63BF01B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23563fe52bbc943e8756d04085b66d156ab259d7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990736"
---
# <a name="sample_c-sm4---asm"></a><span data-ttu-id="3d5f0-103">exemple \_ c (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3d5f0-103">sample\_c (sm4 - asm)</span></span>

<span data-ttu-id="3d5f0-104">Effectue un filtre de comparaison.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-104">Performs a comparison filter.</span></span>



| <span data-ttu-id="3d5f0-105">exemple \_ c \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource. r,//doit être. r Swizzle srcSampler, srcReferenceValue//composant unique sélectionné</span><span class="sxs-lookup"><span data-stu-id="3d5f0-105">sample\_c\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="3d5f0-106">Élément</span><span class="sxs-lookup"><span data-stu-id="3d5f0-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="3d5f0-107">Description</span><span class="sxs-lookup"><span data-stu-id="3d5f0-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5f0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3d5f0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="3d5f0-109">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-109">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="3d5f0-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="3d5f0-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="3d5f0-111">\[dans \] un ensemble de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-111">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="3d5f0-112">Pour plus d’informations, consultez l' [exemple](sample--sm4---asm-.md) d’instruction.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-112">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="3d5f0-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="3d5f0-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="3d5f0-114">\[dans \] un registre de texture.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-114">\[in\] A texture register.</span></span> <span data-ttu-id="3d5f0-115">Pour plus d’informations, consultez l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-115">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="3d5f0-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="3d5f0-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="3d5f0-117">\[dans \] un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-117">\[in\] A sampler register.</span></span> <span data-ttu-id="3d5f0-118">Pour plus d’informations, consultez l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-118">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="3d5f0-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="3d5f0-119"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="3d5f0-120">\[dans \] un registre avec un seul composant sélectionné, qui est utilisé dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-120">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="3d5f0-121">Notes</span><span class="sxs-lookup"><span data-stu-id="3d5f0-121">Remarks</span></span>

<span data-ttu-id="3d5f0-122">L’objectif principal de cette instruction est de fournir un bloc de construction pour Percentage-Closer le filtrage de profondeur.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-122">The primary purpose for this instruction is to provide a building-block for Percentage-Closer Depth filtering.</span></span> <span data-ttu-id="3d5f0-123">Le « c » dans l' **exemple \_ c** représente la comparaison.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-123">The "c" in **sample\_c** stands for Comparison.</span></span>

<span data-ttu-id="3d5f0-124">Les opérandes de l' **exemple \_ c** sont identiques à ceux de l' [exemple](sample--sm4---asm-.md) d’instruction, à ceci près qu’il existe un opérande source float32 supplémentaire, *srcReferenceValue*, qui doit être un registre avec un composant unique sélectionné ou un littéral scalaire.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-124">The operands to **sample\_c** are identical to the [sample](sample--sm4---asm-.md) instruction, except that there is an additional float32 source operand, *srcReferenceValue*, which must be a register with single-component selected, or a scalar literal.</span></span>

<span data-ttu-id="3d5f0-125">Le paramètre *srcResource* doit avoir un. r (rouge) Swizzle.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-125">The *srcResource* parameter must have a .r (red) swizzle.</span></span> <span data-ttu-id="3d5f0-126">l' **exemple \_ c** fonctionne exclusivement sur le composant rouge et retourne une valeur unique.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-126">**sample\_c** operates exclusively on the red component, and returns a single value.</span></span> <span data-ttu-id="3d5f0-127">Le. r Swizzle sur *srcResource* indique que le résultat scalaire est répliqué sur tous les composants.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-127">The .r swizzle on *srcResource* indicates that the scalar result is replicated to all components.</span></span>

<span data-ttu-id="3d5f0-128">Quand une mémoire tampon de profondeur est définie en tant que texture d’entrée, la valeur de profondeur s’affiche dans le composant rouge.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-128">When a Depth Buffer is set as an input texture, the depth value shows up in the red component.</span></span>

<span data-ttu-id="3d5f0-129">Si cette instruction est utilisée avec une ressource qui n’est pas un Texture1D/2D/2DArray/cube/CubeArray, elle produit des résultats non définis.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-129">If this instruction is used with a Resource that is not a Texture1D/2D/2DArray/Cube/CubeArray, it produces undefined results.</span></span>

<span data-ttu-id="3d5f0-130">Lorsque cette instruction est exécutée, le matériel d’échantillonnage utilise le ComparisonFunction de l’échantillonneur actuel pour comparer *srcReferenceValue* par rapport à la valeur du composant rouge pour la ressource source à chaque « TAP » de filtre (Texel) que le filtre de texture actuellement configuré couvre, en fonction des coordonnées fournies dans *srcAddress*.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-130">When this instruction is executed, the sampling hardware uses the current Sampler's ComparisonFunction to compare *srcReferenceValue* against the Red component value for the source Resource at each filter "tap" location (texel) that the currently configured texture filter covers, based on the provided coordinates in *srcAddress*.</span></span>

<span data-ttu-id="3d5f0-131">La comparaison se produit après que *srcReferenceValue* a été quantifiée à la précision du format de texture, exactement de la même façon que z est quantifiée à la précision de la mémoire tampon de profondeur avant la comparaison de profondeur au test de visibilité de la fusion de sortie.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-131">The comparison occurs after *srcReferenceValue* has been quantized to the precision of the texture format, in exactly the same way that z is quantized to depth buffer precision before Depth Comparison at the Output Merger visibility test.</span></span> <span data-ttu-id="3d5f0-132">Cela comprend une bride à la plage de format (par exemple, \[ 0.. 1 \] pour un format UNORM).</span><span class="sxs-lookup"><span data-stu-id="3d5f0-132">This includes a clamp to the format range (e.g. \[0..1\] for a UNORM format).</span></span>

<span data-ttu-id="3d5f0-133">Le composant rouge du Texel source est comparé au *srcReferenceValue* quantifié.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-133">The source texel's Red component is compared against the quantized *srcReferenceValue*.</span></span> <span data-ttu-id="3d5f0-134">Pour les texels qui sont en dehors de la ressource, la valeur du composant rouge est déterminée en appliquant les modes d’adresse (et BorderColorR en mode de bordure) à partir de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-134">For texels that fall off the Resource, the Red component value is determined by applying the Address Modes (and BorderColorR if in Border mode) from the Sampler.</span></span> <span data-ttu-id="3d5f0-135">La comparaison honore toutes les règles de comparaison de virgule flottante D3D11, dans le cas où le format de texture est virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-135">The comparison honors all D3D11 floating point comparison rules, in the case the texture format is floating point.</span></span>

<span data-ttu-id="3d5f0-136">Chaque comparaison qui passe retourne 1,0 f comme valeur de composant rouge pour le Texel, et chaque comparaison qui échoue retourne 0,0 f comme valeur rouge pour la texture.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-136">Each comparison that passes returns 1.0f as the Red component value for the texel, and each comparison that fails returns 0.0f as the Red value for the texture.</span></span> <span data-ttu-id="3d5f0-137">Le filtrage se produit exactement comme spécifié par les États de l’échantillonneur, en opérant uniquement dans le composant rouge et en renvoyant un résultat de filtre scalaire unique au nuanceur, répliqué sur tous les composants de *dest* masqués.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-137">Filtering then occurs exactly as specified by the Sampler states, operating only in the Red component, and returning a single scalar filter result back to the Shader, replicated to all masked *dest* components.</span></span>

<span data-ttu-id="3d5f0-138">L’utilisation de l' **exemple \_ c** est orthogonale à tous les autres contrôles de filtrage à usage général.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-138">The use of **sample\_c** is orthogonal to all other general purpose filtering controls.</span></span> <span data-ttu-id="3d5f0-139">l' **exemple \_ c** fonctionne de façon transparente avec les autres modes de filtre à usage général.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-139">**sample\_c** works seamlessly with the other general purpose filter modes.</span></span> <span data-ttu-id="3d5f0-140">l' **exemple \_ c** modifie le comportement des filtres à usage général de telle sorte que les valeurs qui sont filtrées deviennent 1,0 f ou 0.0 f en raison des résultats de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-140">**sample\_c** changes the behavior of the general purpose filters such that the values being filtered all become 1.0f or 0.0f due to comparison results.</span></span>

<span data-ttu-id="3d5f0-141">L’extraction à partir d’un emplacement d’entrée auquel rien n’est lié retourne 0 pour tous les composants.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-141">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="3d5f0-142">Pour plus d’informations, consultez l' [exemple](sample--sm4---asm-.md) d’instruction.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-142">For more information, see the [sample](sample--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="3d5f0-143">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="3d5f0-143">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3d5f0-144">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="3d5f0-144">Vertex Shader</span></span> | <span data-ttu-id="3d5f0-145">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="3d5f0-145">Geometry Shader</span></span> | <span data-ttu-id="3d5f0-146">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="3d5f0-146">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="3d5f0-147">x</span><span class="sxs-lookup"><span data-stu-id="3d5f0-147">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3d5f0-148">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3d5f0-148">Minimum Shader Model</span></span>

<span data-ttu-id="3d5f0-149">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="3d5f0-149">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3d5f0-150">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3d5f0-150">Shader Model</span></span>                                              | <span data-ttu-id="3d5f0-151">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3d5f0-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3d5f0-152">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3d5f0-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3d5f0-153">Oui</span><span class="sxs-lookup"><span data-stu-id="3d5f0-153">yes</span></span>       |
| [<span data-ttu-id="3d5f0-154">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="3d5f0-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3d5f0-155">Oui</span><span class="sxs-lookup"><span data-stu-id="3d5f0-155">yes</span></span>       |
| [<span data-ttu-id="3d5f0-156">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="3d5f0-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3d5f0-157">Oui</span><span class="sxs-lookup"><span data-stu-id="3d5f0-157">yes</span></span>       |
| [<span data-ttu-id="3d5f0-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d5f0-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3d5f0-159">non</span><span class="sxs-lookup"><span data-stu-id="3d5f0-159">no</span></span>        |
| [<span data-ttu-id="3d5f0-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d5f0-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3d5f0-161">non</span><span class="sxs-lookup"><span data-stu-id="3d5f0-161">no</span></span>        |
| [<span data-ttu-id="3d5f0-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d5f0-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3d5f0-163">non</span><span class="sxs-lookup"><span data-stu-id="3d5f0-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3d5f0-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d5f0-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d5f0-165">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d5f0-165">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





