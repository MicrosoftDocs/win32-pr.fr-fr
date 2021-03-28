---
title: sample_d (SM4-ASM)
description: Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné. | sample_d (SM4-ASM)
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe2d3ad310c18ff2bb10e101c95e0267d534fed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992041"
---
# <a name="sample_d-sm4---asm"></a><span data-ttu-id="6a9f9-104">exemple \_ d (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6a9f9-104">sample\_d (sm4 - asm)</span></span>

<span data-ttu-id="6a9f9-105">Échantillonne des données à partir de l’élément/texture spécifié à l’aide de l’adresse spécifiée et du mode de filtrage identifié par l’échantillonneur donné.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="6a9f9-106">ssample \_ d \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler, srcXDerivatives \[ . Swizzle \] , srcYDerivatives \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6a9f9-106">ssample\_d\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcXDerivatives\[.swizzle\], srcYDerivatives\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="6a9f9-107">Élément</span><span class="sxs-lookup"><span data-stu-id="6a9f9-107">Item</span></span>                                                                                                                               | <span data-ttu-id="6a9f9-108">Description</span><span class="sxs-lookup"><span data-stu-id="6a9f9-108">Description</span></span>                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a9f9-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6a9f9-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                    | <span data-ttu-id="6a9f9-110">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-110">\[in\] The address of the results of the operation.</span></span><br/>                                                                  |
| <span data-ttu-id="6a9f9-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="6a9f9-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                     | <span data-ttu-id="6a9f9-112">\[dans \] un ensemble de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="6a9f9-113">Pour plus d’informations, consultez l' [exemple](sample--sm4---asm-.md) d’instruction.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/>      |
| <span data-ttu-id="6a9f9-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="6a9f9-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                 | <span data-ttu-id="6a9f9-115">\[dans \] un registre de texture.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-115">\[in\] A texture register.</span></span> <span data-ttu-id="6a9f9-116">Pour plus d’informations, consultez l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-116">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="6a9f9-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="6a9f9-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                     | <span data-ttu-id="6a9f9-118">\[dans \] un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-118">\[in\] A sampler register.</span></span> <span data-ttu-id="6a9f9-119">Pour plus d’informations, consultez l' **exemple** d’instruction.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-119">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="6a9f9-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*</span><span class="sxs-lookup"><span data-stu-id="6a9f9-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*</span></span><br/> | <span data-ttu-id="6a9f9-121">\[dans \] les dérivés de l’adresse source sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-121">\[in\] The derivatives for the source address in the x direction.</span></span> <span data-ttu-id="6a9f9-122">Pour plus d’informations, consultez la section **Notes** .</span><span class="sxs-lookup"><span data-stu-id="6a9f9-122">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="6a9f9-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*</span><span class="sxs-lookup"><span data-stu-id="6a9f9-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*</span></span><br/> | <span data-ttu-id="6a9f9-124">\[dans \] les dérivés de l’adresse source de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-124">\[in\] The derivatives for the source address in the y direction.</span></span> <span data-ttu-id="6a9f9-125">Pour plus d’informations, consultez la section **Notes** .</span><span class="sxs-lookup"><span data-stu-id="6a9f9-125">For more information, see the **Remarks** section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a9f9-126">Notes</span><span class="sxs-lookup"><span data-stu-id="6a9f9-126">Remarks</span></span>

<span data-ttu-id="6a9f9-127">Cette instruction se comporte comme l' [exemple](sample--sm4---asm-.md) d’instruction, sauf que les dérivés de l’adresse source sur la direction x et de l’axe y sont fournis par des paramètres supplémentaires, *srcXDerivatives* et *srcYDerivatives*, respectivement.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-127">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, except that derivatives for the source address in the x direction and the y direction are provided by extra parameters, *srcXDerivatives* and *srcYDerivatives*, respectively.</span></span> <span data-ttu-id="6a9f9-128">Ces dérivés se trouvent dans l’espace de coordonnées de texture normalisé.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-128">These derivatives are in normalized texture coordinate space.</span></span>

<span data-ttu-id="6a9f9-129">Les composants r, g et b de *srcXDerivatives* (pos-Swizzle) fournissent du/DX, DV/DX et DW/DX.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-129">The r, g and b components of *srcXDerivatives* (POS-swizzle) provide du/dx, dv/dx and dw/dx.</span></span> <span data-ttu-id="6a9f9-130">Le composant « a » (POS-Swizzle) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-130">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="6a9f9-131">Les composants r, g et b de *srcYDerivatives* (pos-Swizzle) fournissent du/dy, DV/dy et DW/dy.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-131">The r, g and b components of *srcYDerivatives* (POS-swizzle) provide du/dy, dv/dy and dw/dy.</span></span> <span data-ttu-id="6a9f9-132">Le composant « a » (POS-Swizzle) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-132">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="6a9f9-133">Contrairement à l' **exemple** d’instruction, qui est autorisé à partager un calcul de LOD unique sur un tampon 2x2, l' **échantillon \_ d** doit calculer la valeur de LOD entièrement indépendamment, par pixel lorsqu’il est utilisé dans le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-133">Unlike the **sample** instruction, which is permitted to share a single LOD calculation across a 2x2 stamp, **sample\_d** must calculate LOD completely independently, per-pixel when used in the Pixel Shader.</span></span>

<span data-ttu-id="6a9f9-134">Si les entrées dérivées de l' **exemple \_ d** proviennent d’instructions de calcul dérivées dans le nuanceur de pixels et que les valeurs incluent INF/Nan, le comportement de l' **exemple \_ d** peut ne pas correspondre à l' **exemple** d’instruction, qui calcule implicitement la dérivée.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-134">If the derivative inputs to **sample\_d** came from derivative calculation instructions in the Pixel Shader and the values include INF/NaN, the behavior of **sample\_d** may not match the **sample** instruction, which implicitly computes the derivative.</span></span> <span data-ttu-id="6a9f9-135">Les valeurs INF/NaN peuvent affecter différemment le calcul de LOD.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-135">The INF/NaN values may affect the LOD calculation differently.</span></span>

<span data-ttu-id="6a9f9-136">L’extraction à partir d’un emplacement d’entrée auquel rien n’est lié retourne 0 pour tous les composants.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-136">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="6a9f9-137">Restrictions</span><span class="sxs-lookup"><span data-stu-id="6a9f9-137">Restrictions</span></span>

-   <span data-ttu-id="6a9f9-138">l' **exemple \_ d** hérite des mêmes restrictions que l' **exemple** d’instruction, ainsi qu’une restriction supplémentaire ci-dessous pour ses paramètres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-138">**sample\_d** inherits the same restrictions as the **sample** instruction, plus additional an restriction below for its additional parameters.</span></span>
-   <span data-ttu-id="6a9f9-139">*srcXDerivatives* et *srcYDerivatives* doivent être des registres Temp (r \# /x \# ), constantBuffer (CB \# ), Input (v \# ) ou une ou plusieurs valeurs immédiates.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-139">*srcXDerivatives* and *srcYDerivatives* must be temp (r\#/x\#), constantBuffer (cb\#), input (v\#) registers or immediate value(s).</span></span>

<span data-ttu-id="6a9f9-140">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="6a9f9-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6a9f9-141">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="6a9f9-141">Vertex Shader</span></span> | <span data-ttu-id="6a9f9-142">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="6a9f9-142">Geometry Shader</span></span> | <span data-ttu-id="6a9f9-143">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="6a9f9-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6a9f9-144">X</span><span class="sxs-lookup"><span data-stu-id="6a9f9-144">X</span></span>             | <span data-ttu-id="6a9f9-145">X</span><span class="sxs-lookup"><span data-stu-id="6a9f9-145">X</span></span>               | <span data-ttu-id="6a9f9-146">x</span><span class="sxs-lookup"><span data-stu-id="6a9f9-146">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6a9f9-147">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="6a9f9-147">Minimum Shader Model</span></span>

<span data-ttu-id="6a9f9-148">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="6a9f9-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6a9f9-149">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6a9f9-149">Shader Model</span></span>                                              | <span data-ttu-id="6a9f9-150">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="6a9f9-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6a9f9-151">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="6a9f9-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6a9f9-152">Oui</span><span class="sxs-lookup"><span data-stu-id="6a9f9-152">yes</span></span>       |
| [<span data-ttu-id="6a9f9-153">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="6a9f9-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6a9f9-154">Oui</span><span class="sxs-lookup"><span data-stu-id="6a9f9-154">yes</span></span>       |
| [<span data-ttu-id="6a9f9-155">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="6a9f9-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6a9f9-156">Oui</span><span class="sxs-lookup"><span data-stu-id="6a9f9-156">yes</span></span>       |
| [<span data-ttu-id="6a9f9-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a9f9-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6a9f9-158">non</span><span class="sxs-lookup"><span data-stu-id="6a9f9-158">no</span></span>        |
| [<span data-ttu-id="6a9f9-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a9f9-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6a9f9-160">non</span><span class="sxs-lookup"><span data-stu-id="6a9f9-160">no</span></span>        |
| [<span data-ttu-id="6a9f9-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a9f9-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6a9f9-162">non</span><span class="sxs-lookup"><span data-stu-id="6a9f9-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6a9f9-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a9f9-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a9f9-164">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a9f9-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





