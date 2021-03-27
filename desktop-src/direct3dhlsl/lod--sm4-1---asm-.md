---
title: LOD (SM 4.1-ASM)
description: Retourne le niveau de détail (LOD) qui serait utilisé pour le filtrage de texture.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679141"
---
# <a name="lod-sm41---asm"></a><span data-ttu-id="5e7af-103">LOD (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="5e7af-103">lod (sm4.1 - asm)</span></span>

<span data-ttu-id="5e7af-104">Retourne le niveau de détail (LOD) qui serait utilisé pour le filtrage de texture.</span><span class="sxs-lookup"><span data-stu-id="5e7af-104">Returns the level of detail (LOD) that would be used for texture filtering.</span></span>



| <span data-ttu-id="5e7af-105">LOD dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler</span><span class="sxs-lookup"><span data-stu-id="5e7af-105">lod dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="5e7af-106">Élément</span><span class="sxs-lookup"><span data-stu-id="5e7af-106">Item</span></span>                                                                                                               | <span data-ttu-id="5e7af-107">Description</span><span class="sxs-lookup"><span data-stu-id="5e7af-107">Description</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="5e7af-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5e7af-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="5e7af-109">\[dans \] l’adresse des résultats.</span><span class="sxs-lookup"><span data-stu-id="5e7af-109">\[in\] The address of the results.</span></span><br/>   |
| <span data-ttu-id="5e7af-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="5e7af-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="5e7af-111">\[dans \] un ensemble de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="5e7af-111">\[in\] A set of texture coordinates.</span></span><br/> |
| <span data-ttu-id="5e7af-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="5e7af-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="5e7af-113">\[dans \] un registre de texture.</span><span class="sxs-lookup"><span data-stu-id="5e7af-113">\[in\] A texture register.</span></span><br/>           |
| <span data-ttu-id="5e7af-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="5e7af-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="5e7af-115">\[dans \] un registre d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="5e7af-115">\[in\] A sampler register.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="5e7af-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5e7af-116">Remarks</span></span>

<span data-ttu-id="5e7af-117">Cela se comporte comme l' [exemple](sample--sm4---asm-.md) d’instruction, mais un échantillon filtré n’est pas généré.</span><span class="sxs-lookup"><span data-stu-id="5e7af-117">This behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="5e7af-118">L’instruction calcule le vecteur suivant (ClampedLOD, NonClampedLOD, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="5e7af-118">The instruction computes the following vector (ClampedLOD, NonClampedLOD, 0, 0).</span></span> <span data-ttu-id="5e7af-119">NonClampedLOD est une valeur LOD calculée qui ignore les conversions de l’échantillonneur ou de la texture (IE : elle peut retourner des valeurs négatives.) ClampedLOD est une valeur de LOD calculée qui serait utilisée par l' **exemple** d’instruction réel.</span><span class="sxs-lookup"><span data-stu-id="5e7af-119">NonClampedLOD is a computed LOD value that ignores any clamping from either the sampler or the texture (ie: it can return negative values.) ClampedLOD is a computed LOD value that would be used by the actual **sample** instruction.</span></span> <span data-ttu-id="5e7af-120">Swizzle sur *srcResource* permet aux valeurs retournées d’être swizzled arbitrairement avant d’être écrites dans la destination.</span><span class="sxs-lookup"><span data-stu-id="5e7af-120">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="5e7af-121">Si aucune ressource n’est liée à l’emplacement spécifié, la valeur 0 est retournée.</span><span class="sxs-lookup"><span data-stu-id="5e7af-121">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="5e7af-122">Si l’échantillonneur utilise le filtrage anisotrope, le LOD doit correspondre au niveau MIP fractionnaire en fonction de l’axe le plus petit de l’empreinte elliptique.</span><span class="sxs-lookup"><span data-stu-id="5e7af-122">If the sampler is using anisotropic filtering the LOD should correspond to the fractional mip level based on the smaller axis of the elliptical footprint.</span></span>

<span data-ttu-id="5e7af-123">Cela est valide pour les types de texture suivants : Texture1D, Texture2D, Texture3D et TextureCube.</span><span class="sxs-lookup"><span data-stu-id="5e7af-123">This is valid for the following texture types: Texture1D, Texture2D, Texture3D and TextureCube.</span></span>

<span data-ttu-id="5e7af-124">L’instruction **LOD** n’est pas définie quand elle est utilisée avec un échantillonneur qui spécifie le filtrage MIP point, en particulier, tout \_ enum de filtre D3D10 qui se termine par le point MIP \_ .</span><span class="sxs-lookup"><span data-stu-id="5e7af-124">The **lod** instruction is not defined when used with a sampler that specifies point mip filtering, specifically, any D3D10\_FILTER enum that ends in MIP\_POINT.</span></span> <span data-ttu-id="5e7af-125">(Voici un exemple de D3D10 \_ FILTRE \_ du \_ point MIP minimum du mag \_ \_ .)</span><span class="sxs-lookup"><span data-stu-id="5e7af-125">(An example of this would be D3D10\_FILTER\_MIN\_MAG\_MIP\_POINT.)</span></span>

<span data-ttu-id="5e7af-126">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="5e7af-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5e7af-127">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="5e7af-127">Vertex Shader</span></span> | <span data-ttu-id="5e7af-128">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="5e7af-128">Geometry Shader</span></span> | <span data-ttu-id="5e7af-129">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="5e7af-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="5e7af-130">x</span><span class="sxs-lookup"><span data-stu-id="5e7af-130">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5e7af-131">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5e7af-131">Minimum Shader Model</span></span>

<span data-ttu-id="5e7af-132">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5e7af-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5e7af-133">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5e7af-133">Shader Model</span></span>                                              | <span data-ttu-id="5e7af-134">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5e7af-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5e7af-135">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="5e7af-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5e7af-136">Oui</span><span class="sxs-lookup"><span data-stu-id="5e7af-136">yes</span></span>       |
| [<span data-ttu-id="5e7af-137">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="5e7af-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5e7af-138">Oui</span><span class="sxs-lookup"><span data-stu-id="5e7af-138">yes</span></span>       |
| [<span data-ttu-id="5e7af-139">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="5e7af-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5e7af-140">non</span><span class="sxs-lookup"><span data-stu-id="5e7af-140">no</span></span>        |
| [<span data-ttu-id="5e7af-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e7af-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5e7af-142">non</span><span class="sxs-lookup"><span data-stu-id="5e7af-142">no</span></span>        |
| [<span data-ttu-id="5e7af-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e7af-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5e7af-144">non</span><span class="sxs-lookup"><span data-stu-id="5e7af-144">no</span></span>        |
| [<span data-ttu-id="5e7af-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e7af-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5e7af-146">non</span><span class="sxs-lookup"><span data-stu-id="5e7af-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5e7af-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5e7af-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e7af-148">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e7af-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





