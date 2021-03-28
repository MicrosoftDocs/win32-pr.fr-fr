---
title: gather4 (SM 4.1-ASM)
description: Rassemble les quatre texels qui seraient utilisés dans une opération de filtrage bilinéaire et les regroupe dans un seul registre. | gather4 (SM 4.1-ASM)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84387bfe027e30b338b4701ec941a9d4e1b5e242
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974151"
---
# <a name="gather4-sm41---asm"></a><span data-ttu-id="2d8e9-104">gather4 (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="2d8e9-104">gather4 (sm4.1 - asm)</span></span>

<span data-ttu-id="2d8e9-105">Rassemble les quatre texels qui seraient utilisés dans une opération de filtrage bilinéaire et les regroupe dans un seul registre.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span>



| <span data-ttu-id="2d8e9-106">gather4 \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] srcSampler. r</span><span class="sxs-lookup"><span data-stu-id="2d8e9-106">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\] srcSampler.r</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2d8e9-107">Élément</span><span class="sxs-lookup"><span data-stu-id="2d8e9-107">Item</span></span>                                                                                                               | <span data-ttu-id="2d8e9-108">Description</span><span class="sxs-lookup"><span data-stu-id="2d8e9-108">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d8e9-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2d8e9-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="2d8e9-110">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-110">\[in\] The address of the result of the operation.</span></span><br/>                                                                                                       |
| <span data-ttu-id="2d8e9-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="2d8e9-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="2d8e9-112">\[dans \] contient les coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-112">\[in\] Contains the texture coordinates.</span></span> <br/>                                                                                                                |
| <span data-ttu-id="2d8e9-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="2d8e9-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="2d8e9-114">\[dans \] un registre des ressources.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-114">\[in\] A resource register.</span></span> <br/> <span data-ttu-id="2d8e9-115">Le Swizzle permet aux valeurs retournées d’être swizzled arbitrairement avant qu’elles soient écrites dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-115">The swizzle allows the returned values to be swizzled arbitrarily before they are written to *dest*.</span></span> <br/>            |
| <span data-ttu-id="2d8e9-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="2d8e9-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="2d8e9-117">\[dans \] un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-117">\[in\] A sampler register.</span></span><br/> <span data-ttu-id="2d8e9-118">Ce paramètre doit avoir un. r (rouge) Swizzle, ce qui indique que la valeur du canal R est copiée vers *dest*.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-118">This parameter must have a .r (red) swizzle, which indicates that the value of the R channel is copied to *dest*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="2d8e9-119">Notes</span><span class="sxs-lookup"><span data-stu-id="2d8e9-119">Remarks</span></span>

<span data-ttu-id="2d8e9-120">Cette opération fonctionne uniquement avec les textures 2D ou carte cubique à canal unique.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-120">This operation only works with single channel 2D or CubeMap textures.</span></span> <span data-ttu-id="2d8e9-121">Pour les textures 2D, seuls les modes d’adressage de l’échantillonneur sont utilisés et le niveau supérieur d’une pyramide MIP est utilisé.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-121">For 2D textures only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>

<span data-ttu-id="2d8e9-122">Cette instruction se comporte comme l' [exemple](sample--sm4---asm-.md) d’instruction, mais un échantillon filtré n’est pas généré.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-122">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="2d8e9-123">Les quatre exemples qui contribuent au filtrage sont placés dans XYZW dans le sens inverse des aiguilles d’une montre, en commençant par l’échantillon dans le coin inférieur gauche de l’emplacement interrogé.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-123">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="2d8e9-124">Cela est identique à l’échantillonnage de point avec les deltas de coordonnée de texture (u, v) aux emplacements suivants : (-, +), (+, +), (+,-), (-,-), où l’amplitude des deltas est toujours la moitié d’un Texel.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-124">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="2d8e9-125">Pour les textures de carte cubique lorsqu’un encombrement bi-linéaire s’étend sur un contour, les texels de la facette voisine sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-125">For CubeMap textures when a bi-linear footprint spans an edge texels from the neighboring face are used.</span></span> <span data-ttu-id="2d8e9-126">Les angles utilisent les mêmes règles que l' **exemple** d’instruction. autrement dit, l’angle inconnu est considéré comme la moyenne des trois angles de face de l’Intertest.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-126">Corners use the same rules as the **sample** instruction; that is the unkown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="2d8e9-127">Les restrictions de format de texture qui s’appliquent aux instructions d' **exemple** s’appliquent également à l’instruction **gather4** .</span><span class="sxs-lookup"><span data-stu-id="2d8e9-127">The texture format restrictions that apply to the **sample** instructions also apply to the **gather4** instruction.</span></span>

<span data-ttu-id="2d8e9-128">Pour les implémentations matérielles, les optimisations dans le filtrage bilinéaire traditionnel qui détectent les échantillons directement sur les texels et ignorent la lecture des texels qui auraient un poids égal à 0 ne peuvent pas être exploitées avec **gather4**.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-128">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with **gather4**.</span></span> <span data-ttu-id="2d8e9-129">**gather4** retourne toujours tous les texels demandés.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-129">**gather4** always returns all requested texels.</span></span>

<span data-ttu-id="2d8e9-130">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="2d8e9-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2d8e9-131">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="2d8e9-131">Vertex Shader</span></span> | <span data-ttu-id="2d8e9-132">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="2d8e9-132">Geometry Shader</span></span> | <span data-ttu-id="2d8e9-133">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="2d8e9-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2d8e9-134">x</span><span class="sxs-lookup"><span data-stu-id="2d8e9-134">x</span></span>             | <span data-ttu-id="2d8e9-135">x</span><span class="sxs-lookup"><span data-stu-id="2d8e9-135">x</span></span>               | <span data-ttu-id="2d8e9-136">x</span><span class="sxs-lookup"><span data-stu-id="2d8e9-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2d8e9-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="2d8e9-137">Minimum Shader Model</span></span>

<span data-ttu-id="2d8e9-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="2d8e9-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2d8e9-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="2d8e9-139">Shader Model</span></span>                                              | <span data-ttu-id="2d8e9-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="2d8e9-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2d8e9-141">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="2d8e9-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2d8e9-142">Oui</span><span class="sxs-lookup"><span data-stu-id="2d8e9-142">yes</span></span>       |
| [<span data-ttu-id="2d8e9-143">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="2d8e9-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2d8e9-144">Oui</span><span class="sxs-lookup"><span data-stu-id="2d8e9-144">yes</span></span>       |
| [<span data-ttu-id="2d8e9-145">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="2d8e9-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2d8e9-146">non</span><span class="sxs-lookup"><span data-stu-id="2d8e9-146">no</span></span>        |
| [<span data-ttu-id="2d8e9-147">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d8e9-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2d8e9-148">non</span><span class="sxs-lookup"><span data-stu-id="2d8e9-148">no</span></span>        |
| [<span data-ttu-id="2d8e9-149">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d8e9-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2d8e9-150">non</span><span class="sxs-lookup"><span data-stu-id="2d8e9-150">no</span></span>        |
| [<span data-ttu-id="2d8e9-151">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d8e9-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2d8e9-152">non</span><span class="sxs-lookup"><span data-stu-id="2d8e9-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2d8e9-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2d8e9-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d8e9-154">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d8e9-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





