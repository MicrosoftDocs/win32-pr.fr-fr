---
title: 'Fonction SampleGrad :: SampleGrad (S, float, float, float, float, uint) pour TextureCubeArray'
description: Découvrez comment cette fonction échantillonne une texture, en utilisant un dégradé pour influencer la manière dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. Pour TextureCubeArray.
ms.assetid: 849FAF04-A133-4E5B-967E-0679AE335CCC
keywords:
- SampleGrad fonction HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 00adfb5c7a1a95e5462b1bc524a6c7d86f71c2e8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982647"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="39722-105">Fonction SampleGrad :: SampleGrad (S, float, float, float, float, uint) pour TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="39722-105">SampleGrad::SampleGrad(S,float,float,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="39722-106">Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="39722-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="39722-107">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="39722-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="39722-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39722-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="39722-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39722-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39722-110"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="39722-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39722-111">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="39722-111">Type: **SamplerState**</span></span>

<span data-ttu-id="39722-112">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="39722-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="39722-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="39722-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="39722-114">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39722-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39722-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="39722-115">Type: **float**</span></span>

<span data-ttu-id="39722-116">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="39722-116">The texture coordinates.</span></span> <span data-ttu-id="39722-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="39722-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="39722-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="39722-118">Texture-Object Type</span></span>                    | <span data-ttu-id="39722-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="39722-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="39722-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="39722-120">Texture1D</span></span>                              | <span data-ttu-id="39722-121">float</span><span class="sxs-lookup"><span data-stu-id="39722-121">float</span></span>          |
| <span data-ttu-id="39722-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="39722-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="39722-123">float2</span><span class="sxs-lookup"><span data-stu-id="39722-123">float2</span></span>         |
| <span data-ttu-id="39722-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="39722-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="39722-125">float3</span><span class="sxs-lookup"><span data-stu-id="39722-125">float3</span></span>         |
| <span data-ttu-id="39722-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="39722-126">TextureCubeArray</span></span>                       | <span data-ttu-id="39722-127">float4</span><span class="sxs-lookup"><span data-stu-id="39722-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="39722-128">*Ddx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39722-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39722-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="39722-129">Type: **float**</span></span>

<span data-ttu-id="39722-130">Taux de modification de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="39722-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="39722-131">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="39722-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="39722-132">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="39722-132">Texture-Object Type</span></span>                      | <span data-ttu-id="39722-133">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="39722-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="39722-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="39722-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="39722-135">float</span><span class="sxs-lookup"><span data-stu-id="39722-135">float</span></span>          |
| <span data-ttu-id="39722-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="39722-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="39722-137">float2</span><span class="sxs-lookup"><span data-stu-id="39722-137">float2</span></span>         |
| <span data-ttu-id="39722-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="39722-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="39722-139">float3</span><span class="sxs-lookup"><span data-stu-id="39722-139">float3</span></span>         |
| <span data-ttu-id="39722-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="39722-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="39722-141">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="39722-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="39722-142">*Ddy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39722-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39722-143">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="39722-143">Type: **float**</span></span>

<span data-ttu-id="39722-144">Taux de modification de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="39722-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="39722-145">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="39722-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="39722-146">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="39722-146">Texture-Object Type</span></span>                      | <span data-ttu-id="39722-147">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="39722-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="39722-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="39722-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="39722-149">float</span><span class="sxs-lookup"><span data-stu-id="39722-149">float</span></span>          |
| <span data-ttu-id="39722-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="39722-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="39722-151">float2</span><span class="sxs-lookup"><span data-stu-id="39722-151">float2</span></span>         |
| <span data-ttu-id="39722-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="39722-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="39722-153">float3</span><span class="sxs-lookup"><span data-stu-id="39722-153">float3</span></span>         |
| <span data-ttu-id="39722-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="39722-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="39722-155">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="39722-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="39722-156">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39722-156">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39722-157">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="39722-157">Type: **float**</span></span>

<span data-ttu-id="39722-158">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="39722-158">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="39722-159">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="39722-159">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="39722-160">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="39722-160">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39722-161">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="39722-161">Type: **uint**</span></span>

<span data-ttu-id="39722-162">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="39722-162">The status of the operation.</span></span> <span data-ttu-id="39722-163">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="39722-163">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="39722-164">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="39722-164">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="39722-165">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="39722-165">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39722-166">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39722-166">Return value</span></span>

<span data-ttu-id="39722-167">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="39722-167">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="39722-168">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="39722-168">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="39722-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39722-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39722-170">Méthodes SampleGrad</span><span class="sxs-lookup"><span data-stu-id="39722-170">SampleGrad methods</span></span>](texturecubearray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="39722-171">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="39722-171">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
