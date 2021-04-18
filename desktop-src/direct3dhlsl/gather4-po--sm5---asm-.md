---
title: gather4_po (SM5-ASM)
description: Une variante de gather4, mais au lieu de prendre en charge un décalage immédiat \-8.. 7 \, le décalage est fourni en tant que paramètre à l’instruction, et la plus grande plage de \-32.. 31 \.
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971586"
---
# <a name="gather4_po-sm5---asm"></a><span data-ttu-id="1b842-103">gather4 \_ po (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1b842-103">gather4\_po (sm5 - asm)</span></span>

<span data-ttu-id="1b842-104">Une variante de [gather4](gather4--sm5---asm-.md), mais au lieu de prendre en charge un offset immédiat \[ -8.. 7 \] , le décalage est fourni en tant que paramètre à l’instruction, et la plus grande plage de \[ -32.. 31 \] .</span><span class="sxs-lookup"><span data-stu-id="1b842-104">A variant of [gather4](gather4--sm5---asm-.md), but instead of supporting an immediate offset \[-8..7\], the offset comes as a parameter to the instruction, and also has larger range of \[-32..31\].</span></span>



| <span data-ttu-id="1b842-105">gather4 \_ po dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcOffset \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . Select \_ composant\]</span><span class="sxs-lookup"><span data-stu-id="1b842-105">gather4\_po dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1b842-106">Élément</span><span class="sxs-lookup"><span data-stu-id="1b842-106">Item</span></span>                                                                                                               | <span data-ttu-id="1b842-107">Description</span><span class="sxs-lookup"><span data-stu-id="1b842-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1b842-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1b842-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="1b842-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1b842-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="1b842-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="1b842-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="1b842-111">\[dans \] un ensemble de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="1b842-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="1b842-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span><span class="sxs-lookup"><span data-stu-id="1b842-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>         | <span data-ttu-id="1b842-113">\[dans \] le décalage.</span><span class="sxs-lookup"><span data-stu-id="1b842-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="1b842-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="1b842-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="1b842-115">\[dans \] un registre de texture.</span><span class="sxs-lookup"><span data-stu-id="1b842-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="1b842-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="1b842-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="1b842-117">\[dans \] un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="1b842-117">\[in\] A sampler register.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="1b842-118">Notes</span><span class="sxs-lookup"><span data-stu-id="1b842-118">Remarks</span></span>

<span data-ttu-id="1b842-119">Les deux premiers composants du paramètre décalage à 4 vecteurs fournissent des décalages d’entiers 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1b842-119">The first two components of the 4-vector offset parameter supply 32-bit integer offsets.</span></span> <span data-ttu-id="1b842-120">Les autres composants de ce paramètre sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="1b842-120">The other components of this parameter are ignored.</span></span>

<span data-ttu-id="1b842-121">Les 6 bits les moins significatifs de chaque valeur de décalage sont honorés en tant que valeur signée, ce qui donne \[ -32.. 31 \] .</span><span class="sxs-lookup"><span data-stu-id="1b842-121">The 6 least significant bits of each offset value is honored as a signed value, yielding \[-32..31\] range.</span></span>

<span data-ttu-id="1b842-122">Cette instruction fonctionne uniquement avec les textures 2D, contrairement à **gather4**, qui fonctionne également avec TextureCubes.</span><span class="sxs-lookup"><span data-stu-id="1b842-122">This instruction only works with 2D textures, unlike **gather4**, which also works with TextureCubes.</span></span>

<span data-ttu-id="1b842-123">Les seuls modes honorés dans l’échantillonneur sont les modes d’adressage.</span><span class="sxs-lookup"><span data-stu-id="1b842-123">The only modes honored in the sampler are the addressing modes.</span></span> <span data-ttu-id="1b842-124">Seul le MIP le plus détaillé dans l’affichage des ressources est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1b842-124">Only the most detailed mip in the resource view is used.</span></span>

<span data-ttu-id="1b842-125">Si l’adresse se trouve sur un centre de Texel, cela ne signifie pas que les autres texels peuvent être mis à zéro.</span><span class="sxs-lookup"><span data-stu-id="1b842-125">If the address falls on a texel center, this does not mean the other texels can be zeroed out.</span></span>

<span data-ttu-id="1b842-126">Le paramètre *srcSampler* inclut le \[ composant. Select \_ \] , qui permet de récupérer n’importe quel composant d’une texture, y compris les valeurs par défaut pour les composants manquants.</span><span class="sxs-lookup"><span data-stu-id="1b842-126">The *srcSampler* parameter includes \[.select\_component\], allowing any single component of a texture to be retrieved, including returning defaults for missing components.</span></span>

<span data-ttu-id="1b842-127">Pour les formats avec des composants float32, si la valeur extraite est normalisée, dénormalisée, +-0 ou +-INF, elle est retournée au nuanceur non modifié.</span><span class="sxs-lookup"><span data-stu-id="1b842-127">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="1b842-128">NaN est retourné en tant que NaN, mais la représentation exacte du bit de NaN peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="1b842-128">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="1b842-129">Pour TextureCubes, une certaine synthèse du 4e Texel manquant doit se produire au niveau des angles, de sorte que la notion de retour de bits inchangé pour le Texel synthétisé ne s’applique pas et les dénormes peuvent être vidées.</span><span class="sxs-lookup"><span data-stu-id="1b842-129">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="1b842-130">Utilisez cette instruction pour étendre la plage de décalage de **gather4** à plus grande taille et programmable.</span><span class="sxs-lookup"><span data-stu-id="1b842-130">Use this instruction to extend offset range of **gather4** to be larger and programmable.</span></span> <span data-ttu-id="1b842-131">Le suffixe « po » sur le nom signifie « décalage programmable ».</span><span class="sxs-lookup"><span data-stu-id="1b842-131">The "po" suffix on the name means "programmable offset".</span></span>

<span data-ttu-id="1b842-132">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="1b842-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1b842-133">Sommet</span><span class="sxs-lookup"><span data-stu-id="1b842-133">Vertex</span></span> | <span data-ttu-id="1b842-134">Forme</span><span class="sxs-lookup"><span data-stu-id="1b842-134">Hull</span></span> | <span data-ttu-id="1b842-135">Domain</span><span class="sxs-lookup"><span data-stu-id="1b842-135">Domain</span></span> | <span data-ttu-id="1b842-136">Géométrie</span><span class="sxs-lookup"><span data-stu-id="1b842-136">Geometry</span></span> | <span data-ttu-id="1b842-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="1b842-137">Pixel</span></span> | <span data-ttu-id="1b842-138">Compute</span><span class="sxs-lookup"><span data-stu-id="1b842-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1b842-139">X</span><span class="sxs-lookup"><span data-stu-id="1b842-139">X</span></span>      | <span data-ttu-id="1b842-140">X</span><span class="sxs-lookup"><span data-stu-id="1b842-140">X</span></span>    | <span data-ttu-id="1b842-141">X</span><span class="sxs-lookup"><span data-stu-id="1b842-141">X</span></span>      | <span data-ttu-id="1b842-142">X</span><span class="sxs-lookup"><span data-stu-id="1b842-142">X</span></span>        | <span data-ttu-id="1b842-143">X</span><span class="sxs-lookup"><span data-stu-id="1b842-143">X</span></span>     | <span data-ttu-id="1b842-144">X</span><span class="sxs-lookup"><span data-stu-id="1b842-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1b842-145">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="1b842-145">Minimum Shader Model</span></span>

<span data-ttu-id="1b842-146">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="1b842-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1b842-147">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1b842-147">Shader Model</span></span>                                              | <span data-ttu-id="1b842-148">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="1b842-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1b842-149">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1b842-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1b842-150">Oui</span><span class="sxs-lookup"><span data-stu-id="1b842-150">yes</span></span>       |
| [<span data-ttu-id="1b842-151">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="1b842-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1b842-152">non</span><span class="sxs-lookup"><span data-stu-id="1b842-152">no</span></span>        |
| [<span data-ttu-id="1b842-153">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="1b842-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1b842-154">non</span><span class="sxs-lookup"><span data-stu-id="1b842-154">no</span></span>        |
| [<span data-ttu-id="1b842-155">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b842-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1b842-156">non</span><span class="sxs-lookup"><span data-stu-id="1b842-156">no</span></span>        |
| [<span data-ttu-id="1b842-157">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b842-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1b842-158">non</span><span class="sxs-lookup"><span data-stu-id="1b842-158">no</span></span>        |
| [<span data-ttu-id="1b842-159">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b842-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1b842-160">non</span><span class="sxs-lookup"><span data-stu-id="1b842-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1b842-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b842-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b842-162">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b842-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





