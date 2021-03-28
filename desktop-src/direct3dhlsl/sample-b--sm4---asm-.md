---
title: sample_b (SM4-ASM)
description: Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné. | sample_b (SM4-ASM)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211571"
---
# <a name="sample_b-sm4---asm"></a><span data-ttu-id="21bcc-104">exemple \_ b (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="21bcc-104">sample\_b (sm4 - asm)</span></span>

<span data-ttu-id="21bcc-105">Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné.</span><span class="sxs-lookup"><span data-stu-id="21bcc-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="21bcc-106">exemple \_ b \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler, srcLODBias. Select ( \_ composant)</span><span class="sxs-lookup"><span data-stu-id="21bcc-106">sample\_b\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLODBias.select\_component</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="21bcc-107">Élément</span><span class="sxs-lookup"><span data-stu-id="21bcc-107">Item</span></span>                                                                                                               | <span data-ttu-id="21bcc-108">Description</span><span class="sxs-lookup"><span data-stu-id="21bcc-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21bcc-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="21bcc-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="21bcc-110">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="21bcc-110">\[in\] The address of the result of the operation.</span></span><br/>                                                              |
| <span data-ttu-id="21bcc-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="21bcc-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="21bcc-112">\[dans \] un ensemble de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="21bcc-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="21bcc-113">Pour plus d’informations, consultez l' [exemple](sample--sm4---asm-.md) d’instruction.</span><span class="sxs-lookup"><span data-stu-id="21bcc-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="21bcc-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="21bcc-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="21bcc-115">\[dans \] un registre de texture.</span><span class="sxs-lookup"><span data-stu-id="21bcc-115">\[in\] A texture register.</span></span> <span data-ttu-id="21bcc-116">Pour plus d’informations, consultez l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="21bcc-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="21bcc-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="21bcc-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="21bcc-118">\[dans \] un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="21bcc-118">\[in\] A sampler register.</span></span> <span data-ttu-id="21bcc-119">Pour plus d’informations, consultez l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="21bcc-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="21bcc-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*</span><span class="sxs-lookup"><span data-stu-id="21bcc-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*</span></span><br/>     | <span data-ttu-id="21bcc-121">\[\]pour plus d’informations sur ce paramètre, consultez la section **Notes** .</span><span class="sxs-lookup"><span data-stu-id="21bcc-121">\[in\] See the **Remarks** section for information about this parameter.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="21bcc-122">Notes</span><span class="sxs-lookup"><span data-stu-id="21bcc-122">Remarks</span></span>

<span data-ttu-id="21bcc-123">Les données sources peuvent provenir de n’importe quel type de ressource, autre que des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="21bcc-123">The source data may come from any Resource Type, other than Buffers.</span></span> <span data-ttu-id="21bcc-124">Un décalage supplémentaire est appliqué au niveau de détail calculé dans le cadre de l’exécution de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="21bcc-124">An additional bias is applied to the level of detail computed as part of the instruction execution.</span></span>

<span data-ttu-id="21bcc-125">Cette instruction se comporte comme l' [exemple](sample--sm4---asm-.md) d’instruction, avec l’ajout de la valeur *srcLODBias* spécifiée au niveau de détail calculé dans le cadre de l’exécution de l’instruction avant de sélectionner le ou les mappages MIP.</span><span class="sxs-lookup"><span data-stu-id="21bcc-125">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction with the addition of applying the specified *srcLODBias* value to the level of detail value computed as part of the instruction execution prior to selecting the mip map(s).</span></span> <span data-ttu-id="21bcc-126">La valeur *srcLODBias* est ajoutée au LOD calculé sur une base par pixel, avec la valeur de l’échantillonneur MipLODBias, avant la bride à MinLOD et MaxLOD.</span><span class="sxs-lookup"><span data-stu-id="21bcc-126">The *srcLODBias* value is added to the computed LOD on a per-pixel basis, along with the sampler MipLODBias value, prior to the clamp to MinLOD and MaxLOD.</span></span>

### <a name="restrictions"></a><span data-ttu-id="21bcc-127">Restrictions</span><span class="sxs-lookup"><span data-stu-id="21bcc-127">Restrictions</span></span>

-   <span data-ttu-id="21bcc-128">l' **exemple \_ b** hérite des mêmes restrictions que l' [exemple](sample--sm4---asm-.md) d’instruction, ainsi que des restrictions supplémentaires pour son paramètre supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="21bcc-128">**sample\_b** inherits the same restrictions as the [sample](sample--sm4---asm-.md) instruction, plus additional restrictions for its additional parameter.</span></span>
-   <span data-ttu-id="21bcc-129">La plage de *srcLODBias* est (-16 f à 15.99 f); les valeurs qui ne sont pas comprises dans cette plage produisent des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="21bcc-129">The range of *srcLODBias* is (-16.0f to 15.99f); values outside of this range will produce undefined results.</span></span>
-   <span data-ttu-id="21bcc-130">*srcLODBias* doit utiliser un sélecteur de composant unique s’il n’est pas un scalaire immédiat.</span><span class="sxs-lookup"><span data-stu-id="21bcc-130">*srcLODBias* must use a single component selector if it is not a scalar immediate.</span></span>

<span data-ttu-id="21bcc-131">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="21bcc-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="21bcc-132">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="21bcc-132">Vertex Shader</span></span> | <span data-ttu-id="21bcc-133">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="21bcc-133">Geometry Shader</span></span> | <span data-ttu-id="21bcc-134">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="21bcc-134">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="21bcc-135">x</span><span class="sxs-lookup"><span data-stu-id="21bcc-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="21bcc-136">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="21bcc-136">Minimum Shader Model</span></span>

<span data-ttu-id="21bcc-137">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="21bcc-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="21bcc-138">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="21bcc-138">Shader Model</span></span>                                              | <span data-ttu-id="21bcc-139">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="21bcc-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="21bcc-140">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="21bcc-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="21bcc-141">Oui</span><span class="sxs-lookup"><span data-stu-id="21bcc-141">yes</span></span>       |
| [<span data-ttu-id="21bcc-142">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="21bcc-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="21bcc-143">Oui</span><span class="sxs-lookup"><span data-stu-id="21bcc-143">yes</span></span>       |
| [<span data-ttu-id="21bcc-144">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="21bcc-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="21bcc-145">Oui</span><span class="sxs-lookup"><span data-stu-id="21bcc-145">yes</span></span>       |
| [<span data-ttu-id="21bcc-146">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="21bcc-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="21bcc-147">non</span><span class="sxs-lookup"><span data-stu-id="21bcc-147">no</span></span>        |
| [<span data-ttu-id="21bcc-148">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="21bcc-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="21bcc-149">non</span><span class="sxs-lookup"><span data-stu-id="21bcc-149">no</span></span>        |
| [<span data-ttu-id="21bcc-150">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="21bcc-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="21bcc-151">non</span><span class="sxs-lookup"><span data-stu-id="21bcc-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="21bcc-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="21bcc-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21bcc-153">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="21bcc-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





