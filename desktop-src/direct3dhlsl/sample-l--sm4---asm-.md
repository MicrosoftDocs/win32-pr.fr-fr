---
title: sample_l (SM4-ASM)
description: Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné. | sample_l (SM4-ASM)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322321"
---
# <a name="sample_l-sm4---asm"></a><span data-ttu-id="b4564-104">exemple \_ l (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b4564-104">sample\_l (sm4 - asm)</span></span>

<span data-ttu-id="b4564-105">Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné.</span><span class="sxs-lookup"><span data-stu-id="b4564-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="b4564-106">exemple \_ l \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler, srcLOD. Sélectionner un \_ composant</span><span class="sxs-lookup"><span data-stu-id="b4564-106">sample\_l\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLOD.select\_component</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b4564-107">Élément</span><span class="sxs-lookup"><span data-stu-id="b4564-107">Item</span></span>                                                                                                               | <span data-ttu-id="b4564-108">Description</span><span class="sxs-lookup"><span data-stu-id="b4564-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4564-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b4564-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="b4564-110">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b4564-110">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="b4564-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="b4564-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="b4564-112">\[dans \] un ensemble de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="b4564-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="b4564-113">Pour plus d’informations, consultez l' [exemple](sample--sm4---asm-.md) d’instruction.</span><span class="sxs-lookup"><span data-stu-id="b4564-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="b4564-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="b4564-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="b4564-115">\[dans \] un registre de texture.</span><span class="sxs-lookup"><span data-stu-id="b4564-115">\[in\] A texture register.</span></span> <span data-ttu-id="b4564-116">Pour plus d’informations, consultez l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="b4564-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="b4564-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="b4564-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="b4564-118">\[dans \] un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="b4564-118">\[in\] A sampler register.</span></span> <span data-ttu-id="b4564-119">Pour plus d’informations, consultez l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="b4564-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="b4564-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*</span><span class="sxs-lookup"><span data-stu-id="b4564-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*</span></span><br/>                     | <span data-ttu-id="b4564-121">\[dans \] le LOD.</span><span class="sxs-lookup"><span data-stu-id="b4564-121">\[in\] The LOD.</span></span><br/>                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="b4564-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b4564-122">Remarks</span></span>

<span data-ttu-id="b4564-123">Cette instruction est identique à [Sample](sample--sm4---asm-.md), sauf que LOD est fourni directement par l’application en tant que valeur scalaire, ce qui ne représente pas de anisotrope.</span><span class="sxs-lookup"><span data-stu-id="b4564-123">This instruction is identical to [sample](sample--sm4---asm-.md), except that LOD is provided directly by the application as a scalar value, representing no anisotropy.</span></span> <span data-ttu-id="b4564-124">Cette instruction est disponible dans toutes les étapes de nuanceur prodisponibles.</span><span class="sxs-lookup"><span data-stu-id="b4564-124">This instruction is available in all progammable Shader stages.</span></span>

<span data-ttu-id="b4564-125">**Sample \_ l** échantillonne la texture à l’aide de *SRCLOD* pour être le LOD.</span><span class="sxs-lookup"><span data-stu-id="b4564-125">**sample\_l** samples the texture using *srcLOD* to be the LOD.</span></span> <span data-ttu-id="b4564-126">Si la valeur LOD est <= 0, zero’th (mappage le plus grand) est choisi, avec le filtre loupe appliqué (le cas échéant, en fonction du mode de filtre).</span><span class="sxs-lookup"><span data-stu-id="b4564-126">If the LOD value is <= 0, the zero'th (biggest map) is chosen, with the magnify filter applied (if applicable based on the filter mode).</span></span> <span data-ttu-id="b4564-127">Étant donné que *srcLOD* est une valeur à virgule flottante, la valeur fractionnaire est utilisée pour interpoler entre deux niveaux MIP, si le filtre réduire est linéaire ou avec un filtrage anisotrope.</span><span class="sxs-lookup"><span data-stu-id="b4564-127">Because *srcLOD* is a floating point value, the fractional value is used to interpolate between two mip levels, if the minify filter is LINEAR or with anisotropic filtering.</span></span>

<span data-ttu-id="b4564-128">l' **exemple \_ l** ignore les dérivés d’adresse, de sorte que le comportement de filtrage est purement isotrope.</span><span class="sxs-lookup"><span data-stu-id="b4564-128">**sample\_l** ignores address derivatives, so filtering behavior is purely isotropic.</span></span> <span data-ttu-id="b4564-129">Étant donné que les dérivés sont ignorés, le filtrage anisotrope se comporte comme un filtrage isotrope.</span><span class="sxs-lookup"><span data-stu-id="b4564-129">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="b4564-130">Les États de l’échantillonneur MIPLODBIAS et MAX/MINMIPLEVEL sont honorés.</span><span class="sxs-lookup"><span data-stu-id="b4564-130">Sampler states MIPLODBIAS and MAX/MINMIPLEVEL are honored.</span></span>

<span data-ttu-id="b4564-131">Lorsqu’il est utilisé dans le nuanceur de pixels, l' **exemple \_ l** signifie que le choix de LOD est par pixel, sans effet des pixels voisins, par exemple dans le même horodatage 2x2.</span><span class="sxs-lookup"><span data-stu-id="b4564-131">When used in the Pixel Shader, **sample\_l** implies that the choice of LOD is per-pixel, with no effect from neighboring pixels, for example in the same 2x2 stamp.</span></span>

<span data-ttu-id="b4564-132">L’extraction à partir d’un emplacement d’entrée auquel rien n’est lié retourne 0 pour tous les composants.</span><span class="sxs-lookup"><span data-stu-id="b4564-132">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="b4564-133">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="b4564-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b4564-134">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="b4564-134">Vertex Shader</span></span> | <span data-ttu-id="b4564-135">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="b4564-135">Geometry Shader</span></span> | <span data-ttu-id="b4564-136">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="b4564-136">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b4564-137">X</span><span class="sxs-lookup"><span data-stu-id="b4564-137">X</span></span>             | <span data-ttu-id="b4564-138">X</span><span class="sxs-lookup"><span data-stu-id="b4564-138">X</span></span>               | <span data-ttu-id="b4564-139">x</span><span class="sxs-lookup"><span data-stu-id="b4564-139">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b4564-140">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b4564-140">Minimum Shader Model</span></span>

<span data-ttu-id="b4564-141">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b4564-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b4564-142">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b4564-142">Shader Model</span></span>                                              | <span data-ttu-id="b4564-143">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b4564-143">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b4564-144">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="b4564-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b4564-145">Oui</span><span class="sxs-lookup"><span data-stu-id="b4564-145">yes</span></span>       |
| [<span data-ttu-id="b4564-146">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="b4564-146">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b4564-147">Oui</span><span class="sxs-lookup"><span data-stu-id="b4564-147">yes</span></span>       |
| [<span data-ttu-id="b4564-148">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="b4564-148">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b4564-149">Oui</span><span class="sxs-lookup"><span data-stu-id="b4564-149">yes</span></span>       |
| [<span data-ttu-id="b4564-150">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4564-150">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b4564-151">non</span><span class="sxs-lookup"><span data-stu-id="b4564-151">no</span></span>        |
| [<span data-ttu-id="b4564-152">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4564-152">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b4564-153">non</span><span class="sxs-lookup"><span data-stu-id="b4564-153">no</span></span>        |
| [<span data-ttu-id="b4564-154">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4564-154">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b4564-155">non</span><span class="sxs-lookup"><span data-stu-id="b4564-155">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b4564-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4564-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4564-157">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4564-157">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





