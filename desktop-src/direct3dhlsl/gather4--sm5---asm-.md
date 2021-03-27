---
title: gather4 (SM5-ASM)
description: Rassemble les quatre texels qui seraient utilisés dans une opération de filtrage bilinéaire et les regroupe dans un seul registre. | gather4 (SM5-ASM)
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5657265738f12331afc7596286f02170de2a635
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211454"
---
# <a name="gather4-sm5---asm"></a><span data-ttu-id="cdfa6-104">gather4 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="cdfa6-104">gather4 (sm5 - asm)</span></span>

<span data-ttu-id="cdfa6-105">Rassemble les quatre texels qui seraient utilisés dans une opération de filtrage bilinéaire et les regroupe dans un seul registre.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span> <span data-ttu-id="cdfa6-106">Cette instruction fonctionne uniquement avec les textures 2D ou carte cubique, y compris les tableaux.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-106">This instruction only works with 2D or CubeMap textures, including arrays.</span></span> <span data-ttu-id="cdfa6-107">Seuls les modes d’adressage de l’échantillonneur sont utilisés et le niveau supérieur d’une pyramide MIP est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-107">Only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>



| <span data-ttu-id="cdfa6-108">gather4 \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . Select \_ composant\]</span><span class="sxs-lookup"><span data-stu-id="cdfa6-108">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="cdfa6-109">Élément</span><span class="sxs-lookup"><span data-stu-id="cdfa6-109">Item</span></span>                                                                                                               | <span data-ttu-id="cdfa6-110">Description</span><span class="sxs-lookup"><span data-stu-id="cdfa6-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="cdfa6-111"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="cdfa6-111"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="cdfa6-112">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-112">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="cdfa6-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="cdfa6-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="cdfa6-114">\[dans \] un ensemble de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-114">\[in\] A set of texture coordinates.</span></span><br/>                |
| <span data-ttu-id="cdfa6-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="cdfa6-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="cdfa6-116">\[dans \] un registre de texture.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-116">\[in\] A texture register.</span></span><br/>                          |
| <span data-ttu-id="cdfa6-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="cdfa6-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="cdfa6-118">\[dans \] un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-118">\[in\] A sampler register.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="cdfa6-119">Notes</span><span class="sxs-lookup"><span data-stu-id="cdfa6-119">Remarks</span></span>

<span data-ttu-id="cdfa6-120">Cette instruction se comporte comme l' [**exemple**](sample--sm4---asm-.md) d’instruction, mais un échantillon filtré n’est pas généré.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-120">This instruction behaves like the [**sample**](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="cdfa6-121">Les quatre exemples qui contribuent au filtrage sont placés dans XYZW dans le sens inverse des aiguilles d’une montre, en commençant par l’échantillon dans le coin inférieur gauche de l’emplacement interrogé.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-121">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="cdfa6-122">Cela est identique à l’échantillonnage de point avec les deltas de coordonnée de texture (u, v) aux emplacements suivants : (-, +), (+, +), (+,-), (-,-), où l’amplitude des deltas est toujours la moitié d’un Texel.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-122">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="cdfa6-123">Pour les textures carte cubique, quand un encombrement bi-linéaire s’étend sur une arête, les texels de la facette voisine sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-123">For CubeMap textures, when a bi-linear footprint spans an edge, texels from the neighboring face are used.</span></span> <span data-ttu-id="cdfa6-124">Les angles utilisent les mêmes règles que l' [**exemple**](sample--sm4---asm-.md) d’instruction. autrement dit, l’angle inconnu est considéré comme la moyenne des trois angles de face du test.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-124">Corners use the same rules as the [**sample**](sample--sm4---asm-.md) instruction; that is, the unknown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="cdfa6-125">Des restrictions de format de texture s’appliquent aux **gather4** qui sont exprimées dans la liste de formats.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-125">There are texture format restrictions that apply to **gather4** which are expressed in the format list.</span></span>

<span data-ttu-id="cdfa6-126">Swizzle sur *srcResource* permet aux valeurs retournées d’être swizzled arbitrairement avant d’être écrites dans la destination.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="cdfa6-127">Le composant. Select \_ sur *srcSampler* choisit le composant de la texture source (r/g/b/a) à partir duquel lire 4 texels.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-127">The .select\_component on *srcSampler* chooses which component of the source texture (r/g/b/a) to read 4 texels from.</span></span>

<span data-ttu-id="cdfa6-128">Pour les formats avec des composants float32, si la valeur extraite est normalisée, dénormalisée, +-0 ou +-INF, elle est retournée au nuanceur non modifié.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-128">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="cdfa6-129">NaN est retourné en tant que NaN, mais la représentation exacte du bit de NaN peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-129">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="cdfa6-130">Pour TextureCubes, une certaine synthèse du 4ème Texel manquant doit se produire au niveau des angles, de sorte que les bits inchangés pour le Texel synthétisé ne s’appliquent pas et les dénormes peuvent être vidées.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-130">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="cdfa6-131">Pour les implémentations matérielles, les optimisations dans le filtrage bilinéaire traditionnel qui détectent des échantillons directement sur les texels et ignorent la lecture des texels qui auraient un poids égal à 0 ne peuvent pas être exploitées avec cette instruction.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-131">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with this instruction.</span></span> <span data-ttu-id="cdfa6-132">*gather4* retourne toujours tous les texels demandés.</span><span class="sxs-lookup"><span data-stu-id="cdfa6-132">*gather4* always returns all requested texels.</span></span>

<span data-ttu-id="cdfa6-133">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="cdfa6-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cdfa6-134">Sommet</span><span class="sxs-lookup"><span data-stu-id="cdfa6-134">Vertex</span></span> | <span data-ttu-id="cdfa6-135">Forme</span><span class="sxs-lookup"><span data-stu-id="cdfa6-135">Hull</span></span> | <span data-ttu-id="cdfa6-136">Domain</span><span class="sxs-lookup"><span data-stu-id="cdfa6-136">Domain</span></span> | <span data-ttu-id="cdfa6-137">Géométrie</span><span class="sxs-lookup"><span data-stu-id="cdfa6-137">Geometry</span></span> | <span data-ttu-id="cdfa6-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="cdfa6-138">Pixel</span></span> | <span data-ttu-id="cdfa6-139">Compute</span><span class="sxs-lookup"><span data-stu-id="cdfa6-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cdfa6-140">X</span><span class="sxs-lookup"><span data-stu-id="cdfa6-140">X</span></span>      | <span data-ttu-id="cdfa6-141">X</span><span class="sxs-lookup"><span data-stu-id="cdfa6-141">X</span></span>    | <span data-ttu-id="cdfa6-142">X</span><span class="sxs-lookup"><span data-stu-id="cdfa6-142">X</span></span>      | <span data-ttu-id="cdfa6-143">X</span><span class="sxs-lookup"><span data-stu-id="cdfa6-143">X</span></span>        | <span data-ttu-id="cdfa6-144">X</span><span class="sxs-lookup"><span data-stu-id="cdfa6-144">X</span></span>     | <span data-ttu-id="cdfa6-145">X</span><span class="sxs-lookup"><span data-stu-id="cdfa6-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cdfa6-146">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="cdfa6-146">Minimum Shader Model</span></span>

<span data-ttu-id="cdfa6-147">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="cdfa6-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="cdfa6-148">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="cdfa6-148">Shader Model</span></span>                                              | <span data-ttu-id="cdfa6-149">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="cdfa6-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cdfa6-150">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="cdfa6-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cdfa6-151">Oui</span><span class="sxs-lookup"><span data-stu-id="cdfa6-151">yes</span></span>       |
| [<span data-ttu-id="cdfa6-152">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="cdfa6-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cdfa6-153">non</span><span class="sxs-lookup"><span data-stu-id="cdfa6-153">no</span></span>        |
| [<span data-ttu-id="cdfa6-154">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="cdfa6-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cdfa6-155">non</span><span class="sxs-lookup"><span data-stu-id="cdfa6-155">no</span></span>        |
| [<span data-ttu-id="cdfa6-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cdfa6-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cdfa6-157">non</span><span class="sxs-lookup"><span data-stu-id="cdfa6-157">no</span></span>        |
| [<span data-ttu-id="cdfa6-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cdfa6-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cdfa6-159">non</span><span class="sxs-lookup"><span data-stu-id="cdfa6-159">no</span></span>        |
| [<span data-ttu-id="cdfa6-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cdfa6-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cdfa6-161">non</span><span class="sxs-lookup"><span data-stu-id="cdfa6-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cdfa6-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cdfa6-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdfa6-163">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cdfa6-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





