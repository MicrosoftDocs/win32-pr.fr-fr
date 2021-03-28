---
title: gather4_c (SM5-ASM)
description: Identique à gather4, sauf que cette Inserte effectue une comparaison des texels, similaire à l’exemple \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35414aa2cd4d9f0686ab7a5cc17b94caa960cec1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990792"
---
# <a name="gather4_c-sm5---asm"></a><span data-ttu-id="7a6d5-103">gather4 \_ c (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7a6d5-103">gather4\_c (sm5 - asm)</span></span>

<span data-ttu-id="7a6d5-104">Identique à [**gather4**](gather4--sm5---asm-.md), sauf que cette Inserte effectue une comparaison des texels, similaire à l' [**exemple \_ c**](sample-c--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="7a6d5-104">Same as [**gather4**](gather4--sm5---asm-.md), except this instrution performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="7a6d5-105">gather4 \_ c \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . R \] , srcReferenceValue</span><span class="sxs-lookup"><span data-stu-id="7a6d5-105">gather4\_c\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="7a6d5-106">Élément</span><span class="sxs-lookup"><span data-stu-id="7a6d5-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="7a6d5-107">Description</span><span class="sxs-lookup"><span data-stu-id="7a6d5-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a6d5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="7a6d5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="7a6d5-109">\[dans \] l’adresse du résultat de l’opération</span><span class="sxs-lookup"><span data-stu-id="7a6d5-109">\[in\] The address of the result of the operation</span></span><br/>                                    |
| <span data-ttu-id="7a6d5-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="7a6d5-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="7a6d5-111">\[dans \] un ensemble de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-111">\[in\] A set of texture coordinates.</span></span><br/>                                                 |
| <span data-ttu-id="7a6d5-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="7a6d5-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="7a6d5-113">\[dans \] un registre de texture.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-113">\[in\] A texture register.</span></span><br/>                                                           |
| <span data-ttu-id="7a6d5-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="7a6d5-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="7a6d5-115">\[dans \] un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-115">\[in\] A sampler register.</span></span><br/>                                                           |
| <span data-ttu-id="7a6d5-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="7a6d5-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="7a6d5-117">\[dans \] un registre avec un seul composant sélectionné, qui est utilisé dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-117">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a6d5-118">Notes</span><span class="sxs-lookup"><span data-stu-id="7a6d5-118">Remarks</span></span>

<span data-ttu-id="7a6d5-119">Consultez l' [**exemple \_ c**](sample-c--sm4---asm-.md) pour obtenir une description de la façon dont *srcReferenceValue* est comparé à chaque Texel extrait.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-119">See [**sample\_c**](sample-c--sm4---asm-.md) for a description of how *srcReferenceValue* gets compared against each fetched texel.</span></span> <span data-ttu-id="7a6d5-120">Contrairement à l' **exemple \_ c**, **gather4 \_ c** retourne chaque résultat de comparaison, plutôt que de les filtrer.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-120">Unlike **sample\_c**, **gather4\_c** returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="7a6d5-121">Pour les TextureCube Corners, où trois texels réels et un quatrième doivent être synthétisés, la synthèse doit se produire après l’étape de comparaison.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-121">For TextureCube corners, where there are three real texels and a fourth must be synthesized, the synthesis must occur after the comparison step.</span></span> <span data-ttu-id="7a6d5-122">Cela signifie que le résultat de la comparaison renvoyée pour la Texel syntesized peut être 0, 0,33, 0,66 ou 1.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-122">This means the returned comparison result for the syntesized texel can be 0, 0.33 , 0.66 , or 1.</span></span> <span data-ttu-id="7a6d5-123">Certaines implémentations ne peuvent retourner que 0 ou 1 pour le Texel synthétisé.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-123">Some implementations may only return either 0 or 1 for the synthesized texel.</span></span> <span data-ttu-id="7a6d5-124">Hormis cette liste de résultats possibles, la méthode permettant de synthétiser le Texel n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-124">Aside from this listing of possible results, the method for synthesizing the texel is unspecified.</span></span>

<span data-ttu-id="7a6d5-125">Pour les formats avec des composants float32, si la valeur extraite est normalisée, ou +-INF, elle est utilisée dans l’opération de comparaison non touchée.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="7a6d5-126">NaN est utilisé dans l’opération de comparaison comme NaN, mais la représentation exacte du bit de NaN peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="7a6d5-127">Les dénormes sont vidées jusqu’à zéro dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="7a6d5-128">Pour TextureCubes, une certaine synthèse du 4ème Texel manquant doit se produire au niveau des angles, de sorte que la notion de retour de bits inchangé pour le Texel synthétisé ne s’applique pas.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="7a6d5-129">Les formats pris en charge pour *gather4 \_ c* sont les mêmes que ceux pris en charge pour l' *exemple \_ c*.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-129">Formats supported for *gather4\_c* are same as those supported for *sample\_c*.</span></span> <span data-ttu-id="7a6d5-130">Il s’agit de formats à un seul composant, donc. R sur *srcSampler*, plutôt qu’un Swizzle arbitraire.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-130">These are single-component formats, thus the .R on *srcSampler*, rather than an arbitrary swizzle.</span></span> <span data-ttu-id="7a6d5-131">**gather4 \_ c** sur une ressource indépendante retourne 0.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-131">**gather4\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="7a6d5-132">Utilisez cette instruction pour le filtrage personnalisé des mappages d’ombres.</span><span class="sxs-lookup"><span data-stu-id="7a6d5-132">Use this instruction for custom shadow map filtering.</span></span>

<span data-ttu-id="7a6d5-133">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="7a6d5-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7a6d5-134">Sommet</span><span class="sxs-lookup"><span data-stu-id="7a6d5-134">Vertex</span></span> | <span data-ttu-id="7a6d5-135">Forme</span><span class="sxs-lookup"><span data-stu-id="7a6d5-135">Hull</span></span> | <span data-ttu-id="7a6d5-136">Domain</span><span class="sxs-lookup"><span data-stu-id="7a6d5-136">Domain</span></span> | <span data-ttu-id="7a6d5-137">Géométrie</span><span class="sxs-lookup"><span data-stu-id="7a6d5-137">Geometry</span></span> | <span data-ttu-id="7a6d5-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="7a6d5-138">Pixel</span></span> | <span data-ttu-id="7a6d5-139">Compute</span><span class="sxs-lookup"><span data-stu-id="7a6d5-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7a6d5-140">X</span><span class="sxs-lookup"><span data-stu-id="7a6d5-140">X</span></span>      | <span data-ttu-id="7a6d5-141">X</span><span class="sxs-lookup"><span data-stu-id="7a6d5-141">X</span></span>    | <span data-ttu-id="7a6d5-142">X</span><span class="sxs-lookup"><span data-stu-id="7a6d5-142">X</span></span>      | <span data-ttu-id="7a6d5-143">X</span><span class="sxs-lookup"><span data-stu-id="7a6d5-143">X</span></span>        | <span data-ttu-id="7a6d5-144">X</span><span class="sxs-lookup"><span data-stu-id="7a6d5-144">X</span></span>     | <span data-ttu-id="7a6d5-145">X</span><span class="sxs-lookup"><span data-stu-id="7a6d5-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7a6d5-146">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="7a6d5-146">Minimum Shader Model</span></span>

<span data-ttu-id="7a6d5-147">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="7a6d5-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7a6d5-148">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="7a6d5-148">Shader Model</span></span>                                              | <span data-ttu-id="7a6d5-149">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="7a6d5-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7a6d5-150">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="7a6d5-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7a6d5-151">Oui</span><span class="sxs-lookup"><span data-stu-id="7a6d5-151">yes</span></span>       |
| [<span data-ttu-id="7a6d5-152">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="7a6d5-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7a6d5-153">non</span><span class="sxs-lookup"><span data-stu-id="7a6d5-153">no</span></span>        |
| [<span data-ttu-id="7a6d5-154">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="7a6d5-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7a6d5-155">non</span><span class="sxs-lookup"><span data-stu-id="7a6d5-155">no</span></span>        |
| [<span data-ttu-id="7a6d5-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a6d5-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7a6d5-157">non</span><span class="sxs-lookup"><span data-stu-id="7a6d5-157">no</span></span>        |
| [<span data-ttu-id="7a6d5-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a6d5-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7a6d5-159">non</span><span class="sxs-lookup"><span data-stu-id="7a6d5-159">no</span></span>        |
| [<span data-ttu-id="7a6d5-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a6d5-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7a6d5-161">non</span><span class="sxs-lookup"><span data-stu-id="7a6d5-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7a6d5-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a6d5-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a6d5-163">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a6d5-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





