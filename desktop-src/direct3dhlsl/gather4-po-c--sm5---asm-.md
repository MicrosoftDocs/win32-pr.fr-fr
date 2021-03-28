---
title: gather4_po_c (SM5-ASM)
description: Se comporte comme gather4 \_ po, sauf que effectue une comparaison sur les texels, comme dans l’exemple \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381206"
---
# <a name="gather4_po_c-sm5---asm"></a><span data-ttu-id="a757c-103">gather4 \_ po \_ c (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a757c-103">gather4\_po\_c (sm5 - asm)</span></span>

<span data-ttu-id="a757c-104">Se comporte comme [**gather4 \_ po**](gather4-po--sm5---asm-.md), sauf que effectue une comparaison sur les texels, comme dans l' [**exemple \_ c**](sample-c--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="a757c-104">Behaves the same as [**gather4\_po**](gather4-po--sm5---asm-.md), except performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="a757c-105">gather4 \_ po \_ c dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcOffset \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . R \] , srcReferenceValue</span><span class="sxs-lookup"><span data-stu-id="a757c-105">gather4\_po\_c dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a757c-106">Élément</span><span class="sxs-lookup"><span data-stu-id="a757c-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="a757c-107">Description</span><span class="sxs-lookup"><span data-stu-id="a757c-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a757c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a757c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="a757c-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a757c-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="a757c-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="a757c-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="a757c-111">\[dans \] un ensemble de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="a757c-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="a757c-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span><span class="sxs-lookup"><span data-stu-id="a757c-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>                                 | <span data-ttu-id="a757c-113">\[dans \] le décalage.</span><span class="sxs-lookup"><span data-stu-id="a757c-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="a757c-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="a757c-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="a757c-115">\[dans \] un registre de texture.</span><span class="sxs-lookup"><span data-stu-id="a757c-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="a757c-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="a757c-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="a757c-117">\[dans \] un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="a757c-117">\[in\] A sampler register.</span></span><br/>                         |
| <span data-ttu-id="a757c-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="a757c-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="a757c-119">\[dans \] un seul composant sélectionné.</span><span class="sxs-lookup"><span data-stu-id="a757c-119">\[in\] Single component selected.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a757c-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a757c-120">Remarks</span></span>

<span data-ttu-id="a757c-121">Consultez l' [**exemple \_ c**](sample-c--sm4---asm-.md) pour plus d’informations sur la façon dont *srcReferenceValue* est comparé à chaque Texel extrait.</span><span class="sxs-lookup"><span data-stu-id="a757c-121">See [**sample\_c**](sample-c--sm4---asm-.md) for information about how *srcReferenceValue* is compared against each fetched texel.</span></span> <span data-ttu-id="a757c-122">Contrairement à l' **exemple \_ c**, *gather4 \_ po \_ c* retourne chaque résultat de comparaison, plutôt que de les filtrer.</span><span class="sxs-lookup"><span data-stu-id="a757c-122">Unlike **sample\_c**, *gather4\_po\_c* returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="a757c-123">Cette instruction, par exemple **gather4 \_ po**, fonctionne uniquement avec les textures 2D.</span><span class="sxs-lookup"><span data-stu-id="a757c-123">This instruction, like **gather4\_po**, only works with 2D textures.</span></span> <span data-ttu-id="a757c-124">Contrairement à [**gather4 \_ c**](gather4-c--sm5---asm-.md), qui fonctionne également avec TextureCubes.</span><span class="sxs-lookup"><span data-stu-id="a757c-124">This is unlike [**gather4\_c**](gather4-c--sm5---asm-.md), which also works with TextureCubes.</span></span>

<span data-ttu-id="a757c-125">Pour les formats avec des composants float32, si la valeur extraite est normalisée, ou +-INF, elle est utilisée dans l’opération de comparaison non touchée.</span><span class="sxs-lookup"><span data-stu-id="a757c-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="a757c-126">NaN est utilisé dans l’opération de comparaison comme NaN, mais la représentation exacte du bit de NaN peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="a757c-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="a757c-127">Les dénormes sont vidées jusqu’à zéro dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="a757c-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="a757c-128">Pour TextureCubes, une certaine synthèse du 4ème Texel manquant doit se produire au niveau des angles, de sorte que la notion de retour de bits inchangé pour le Texel synthétisé ne s’applique pas.</span><span class="sxs-lookup"><span data-stu-id="a757c-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="a757c-129">Les formats pris en charge pour **gather4 \_ po \_ c** sont les mêmes que ceux pris en charge pour l' **exemple \_ c**.</span><span class="sxs-lookup"><span data-stu-id="a757c-129">Formats supported for **gather4\_po\_c** are same as those supported for **sample\_c**.</span></span> <span data-ttu-id="a757c-130">Il s’agit de formats à un seul composant, donc. R sur srcSampler, plutôt qu’un Swizzle arbitraire.</span><span class="sxs-lookup"><span data-stu-id="a757c-130">These are single-component formats, thus the .R on srcSampler, rather than an arbitrary swizzle.</span></span>

<span data-ttu-id="a757c-131">**gather4 \_ po \_ c** sur une ressource indépendante retourne 0.</span><span class="sxs-lookup"><span data-stu-id="a757c-131">**gather4\_po\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="a757c-132">Utilisez cette méthode pour le filtrage de table fictive.</span><span class="sxs-lookup"><span data-stu-id="a757c-132">Use this method for shadow map filtering.</span></span>

<span data-ttu-id="a757c-133">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="a757c-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a757c-134">Sommet</span><span class="sxs-lookup"><span data-stu-id="a757c-134">Vertex</span></span> | <span data-ttu-id="a757c-135">Forme</span><span class="sxs-lookup"><span data-stu-id="a757c-135">Hull</span></span> | <span data-ttu-id="a757c-136">Domain</span><span class="sxs-lookup"><span data-stu-id="a757c-136">Domain</span></span> | <span data-ttu-id="a757c-137">Géométrie</span><span class="sxs-lookup"><span data-stu-id="a757c-137">Geometry</span></span> | <span data-ttu-id="a757c-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="a757c-138">Pixel</span></span> | <span data-ttu-id="a757c-139">Compute</span><span class="sxs-lookup"><span data-stu-id="a757c-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a757c-140">X</span><span class="sxs-lookup"><span data-stu-id="a757c-140">X</span></span>      | <span data-ttu-id="a757c-141">X</span><span class="sxs-lookup"><span data-stu-id="a757c-141">X</span></span>    | <span data-ttu-id="a757c-142">X</span><span class="sxs-lookup"><span data-stu-id="a757c-142">X</span></span>      | <span data-ttu-id="a757c-143">X</span><span class="sxs-lookup"><span data-stu-id="a757c-143">X</span></span>        | <span data-ttu-id="a757c-144">X</span><span class="sxs-lookup"><span data-stu-id="a757c-144">X</span></span>     | <span data-ttu-id="a757c-145">X</span><span class="sxs-lookup"><span data-stu-id="a757c-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a757c-146">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="a757c-146">Minimum Shader Model</span></span>

<span data-ttu-id="a757c-147">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="a757c-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a757c-148">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a757c-148">Shader Model</span></span>                                              | <span data-ttu-id="a757c-149">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="a757c-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a757c-150">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="a757c-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a757c-151">Oui</span><span class="sxs-lookup"><span data-stu-id="a757c-151">yes</span></span>       |
| [<span data-ttu-id="a757c-152">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="a757c-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a757c-153">non</span><span class="sxs-lookup"><span data-stu-id="a757c-153">no</span></span>        |
| [<span data-ttu-id="a757c-154">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="a757c-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a757c-155">non</span><span class="sxs-lookup"><span data-stu-id="a757c-155">no</span></span>        |
| [<span data-ttu-id="a757c-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a757c-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a757c-157">non</span><span class="sxs-lookup"><span data-stu-id="a757c-157">no</span></span>        |
| [<span data-ttu-id="a757c-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a757c-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a757c-159">non</span><span class="sxs-lookup"><span data-stu-id="a757c-159">no</span></span>        |
| [<span data-ttu-id="a757c-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a757c-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a757c-161">non</span><span class="sxs-lookup"><span data-stu-id="a757c-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a757c-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a757c-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a757c-163">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a757c-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





