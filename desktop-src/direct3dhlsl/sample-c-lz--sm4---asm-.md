---
title: sample_c_lz (SM4-ASM)
description: Effectue un filtre de comparaison. Cette instruction se comporte comme l’exemple \_ c, sauf que LOD est égal à 0 et que les dérivés sont ignorés.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ec2889dd3ea4c86af51c8e36bf2e302c6ad4dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381165"
---
# <a name="sample_c_lz-sm4---asm"></a><span data-ttu-id="d5510-104">exemple \_ c \_ LZ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d5510-104">sample\_c\_lz (sm4 - asm)</span></span>

<span data-ttu-id="d5510-105">Effectue un filtre de comparaison.</span><span class="sxs-lookup"><span data-stu-id="d5510-105">Performs a comparison filter.</span></span> <span data-ttu-id="d5510-106">Cette instruction se comporte comme l' [exemple \_ c](sample-c--sm4---asm-.md), sauf que LOD est égal à 0 et que les dérivés sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="d5510-106">This instruction behaves like [sample\_c](sample-c--sm4---asm-.md), except LOD is 0, and derivatives are ignored.</span></span>



| <span data-ttu-id="d5510-107">exemple \_ c \_ LZ \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource. r,//doit être. r Swizzle srcSampler, srcReferenceValue//composant unique sélectionné</span><span class="sxs-lookup"><span data-stu-id="d5510-107">sample\_c\_lz\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d5510-108">Élément</span><span class="sxs-lookup"><span data-stu-id="d5510-108">Item</span></span>                                                                                                                                       | <span data-ttu-id="d5510-109">Description</span><span class="sxs-lookup"><span data-stu-id="d5510-109">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5510-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d5510-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="d5510-111">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d5510-111">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="d5510-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="d5510-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="d5510-113">\[dans \] un ensemble de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="d5510-113">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="d5510-114">Pour plus d’informations, consultez l' [exemple](sample--sm4---asm-.md) d’instruction.</span><span class="sxs-lookup"><span data-stu-id="d5510-114">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="d5510-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="d5510-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="d5510-116">\[dans \] un registre de texture.</span><span class="sxs-lookup"><span data-stu-id="d5510-116">\[in\] A texture register.</span></span> <span data-ttu-id="d5510-117">Pour plus d’informations, consultez l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="d5510-117">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="d5510-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="d5510-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="d5510-119">\[dans \] un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="d5510-119">\[in\] A sampler register.</span></span> <span data-ttu-id="d5510-120">Pour plus d’informations, consultez l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="d5510-120">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="d5510-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span><span class="sxs-lookup"><span data-stu-id="d5510-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="d5510-122">\[dans \] un registre avec un seul composant sélectionné, qui est utilisé dans la comparaison.</span><span class="sxs-lookup"><span data-stu-id="d5510-122">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="d5510-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d5510-123">Remarks</span></span>

<span data-ttu-id="d5510-124">La valeur « LZ » correspond au niveau zéro.</span><span class="sxs-lookup"><span data-stu-id="d5510-124">The "lz" stands for level-zero.</span></span> <span data-ttu-id="d5510-125">Étant donné que les dérivés sont ignorés, cette instruction est disponible dans les nuanceurs autres que le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="d5510-125">Because derivatives are ignored, this instruction is available in shaders other than the Pixel Shader.</span></span>

<span data-ttu-id="d5510-126">Si cette instruction est utilisée avec une texture mipmapped, LOD 0 est échantillonné, à moins que l’échantillonneur ait une pince LOD qui place le LOD ailleurs, ou s’il existe un décalage de LOD, ce qui ferait un décalage à partir de 0.</span><span class="sxs-lookup"><span data-stu-id="d5510-126">If this instruction is used with a mipmapped texture, LOD 0 gets sampled, unless the sampler has an LOD clamp which places the LOD somewhere else, or if there is an LOD Bias, which would simply bias starting from 0.</span></span> <span data-ttu-id="d5510-127">Étant donné que les dérivés sont ignorés, le filtrage anisotrope se comporte comme un filtrage isotrope.</span><span class="sxs-lookup"><span data-stu-id="d5510-127">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="d5510-128">Dans les nuanceurs de pixels, cette instruction peut être utilisée à l’intérieur d’un contrôle de Flow variable lorsque les coordonnées de texture sont dérivées dans le nuanceur, contrairement à l' **exemple \_ c**.</span><span class="sxs-lookup"><span data-stu-id="d5510-128">In Pixel Shaders, this instruction can be used inside varying flow control when the texture coordinates are derived in the shader, unlike **sample\_c**.</span></span>

<span data-ttu-id="d5510-129">L’extraction à partir d’un emplacement d’entrée auquel rien n’est lié retourne 0 pour tous les composants.</span><span class="sxs-lookup"><span data-stu-id="d5510-129">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="d5510-130">Cette instruction est disponible dans tous les nuanceurs, et pas seulement dans le nuanceur de pixels, à des fins de cohérence.</span><span class="sxs-lookup"><span data-stu-id="d5510-130">This instruction is available in all shaders, not just the Pixel Shader, for consistency.</span></span>



| <span data-ttu-id="d5510-131">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="d5510-131">Vertex Shader</span></span> | <span data-ttu-id="d5510-132">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="d5510-132">Geometry Shader</span></span> | <span data-ttu-id="d5510-133">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d5510-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d5510-134">X</span><span class="sxs-lookup"><span data-stu-id="d5510-134">X</span></span>             | <span data-ttu-id="d5510-135">X</span><span class="sxs-lookup"><span data-stu-id="d5510-135">X</span></span>               | <span data-ttu-id="d5510-136">x</span><span class="sxs-lookup"><span data-stu-id="d5510-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d5510-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d5510-137">Minimum Shader Model</span></span>

<span data-ttu-id="d5510-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d5510-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d5510-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d5510-139">Shader Model</span></span>                                              | <span data-ttu-id="d5510-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d5510-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d5510-141">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="d5510-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d5510-142">Oui</span><span class="sxs-lookup"><span data-stu-id="d5510-142">yes</span></span>       |
| [<span data-ttu-id="d5510-143">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="d5510-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d5510-144">Oui</span><span class="sxs-lookup"><span data-stu-id="d5510-144">yes</span></span>       |
| [<span data-ttu-id="d5510-145">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="d5510-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d5510-146">Oui</span><span class="sxs-lookup"><span data-stu-id="d5510-146">yes</span></span>       |
| [<span data-ttu-id="d5510-147">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5510-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d5510-148">non</span><span class="sxs-lookup"><span data-stu-id="d5510-148">no</span></span>        |
| [<span data-ttu-id="d5510-149">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5510-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d5510-150">non</span><span class="sxs-lookup"><span data-stu-id="d5510-150">no</span></span>        |
| [<span data-ttu-id="d5510-151">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5510-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d5510-152">non</span><span class="sxs-lookup"><span data-stu-id="d5510-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d5510-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5510-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5510-154">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5510-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





