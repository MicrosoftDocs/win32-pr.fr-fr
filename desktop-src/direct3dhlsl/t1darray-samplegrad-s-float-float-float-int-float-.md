---
title: 'Fonction SampleGrad :: SampleGrad (S, float, float, float, int, float) pour Texture1DArray'
description: Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. Pour Texture1DArray.
ms.assetid: 328EEC75-1E0A-4196-AD82-A48F3C66D65B
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
ms.openlocfilehash: e4af761ab82492fd49a4f6f048c74016a19aa872
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982738"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture1darray"></a><span data-ttu-id="29042-105">Fonction SampleGrad :: SampleGrad (S, float, float, float, int, float) pour Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="29042-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture1DArray</span></span>

<span data-ttu-id="29042-106">Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="29042-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="29042-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29042-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="29042-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29042-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29042-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="29042-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29042-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="29042-110">Type: **SamplerState**</span></span>

<span data-ttu-id="29042-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="29042-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="29042-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="29042-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="29042-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29042-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29042-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="29042-114">Type: **float**</span></span>

<span data-ttu-id="29042-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="29042-115">The texture coordinates.</span></span> <span data-ttu-id="29042-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="29042-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="29042-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="29042-117">Texture-Object Type</span></span>                    | <span data-ttu-id="29042-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="29042-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="29042-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="29042-119">Texture1D</span></span>                              | <span data-ttu-id="29042-120">float</span><span class="sxs-lookup"><span data-stu-id="29042-120">float</span></span>          |
| <span data-ttu-id="29042-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="29042-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="29042-122">float2</span><span class="sxs-lookup"><span data-stu-id="29042-122">float2</span></span>         |
| <span data-ttu-id="29042-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="29042-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="29042-124">float3</span><span class="sxs-lookup"><span data-stu-id="29042-124">float3</span></span>         |
| <span data-ttu-id="29042-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="29042-125">TextureCubeArray</span></span>                       | <span data-ttu-id="29042-126">float4</span><span class="sxs-lookup"><span data-stu-id="29042-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="29042-127">*Ddx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29042-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29042-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="29042-128">Type: **float**</span></span>

<span data-ttu-id="29042-129">Taux de modification de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="29042-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="29042-130">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="29042-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="29042-131">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="29042-131">Texture-Object Type</span></span>                      | <span data-ttu-id="29042-132">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="29042-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="29042-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="29042-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="29042-134">float</span><span class="sxs-lookup"><span data-stu-id="29042-134">float</span></span>          |
| <span data-ttu-id="29042-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="29042-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="29042-136">float2</span><span class="sxs-lookup"><span data-stu-id="29042-136">float2</span></span>         |
| <span data-ttu-id="29042-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="29042-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="29042-138">float3</span><span class="sxs-lookup"><span data-stu-id="29042-138">float3</span></span>         |
| <span data-ttu-id="29042-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="29042-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="29042-140">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="29042-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="29042-141">*Ddy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29042-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29042-142">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="29042-142">Type: **float**</span></span>

<span data-ttu-id="29042-143">Taux de modification de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="29042-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="29042-144">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="29042-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="29042-145">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="29042-145">Texture-Object Type</span></span>                      | <span data-ttu-id="29042-146">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="29042-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="29042-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="29042-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="29042-148">float</span><span class="sxs-lookup"><span data-stu-id="29042-148">float</span></span>          |
| <span data-ttu-id="29042-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="29042-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="29042-150">float2</span><span class="sxs-lookup"><span data-stu-id="29042-150">float2</span></span>         |
| <span data-ttu-id="29042-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="29042-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="29042-152">float3</span><span class="sxs-lookup"><span data-stu-id="29042-152">float3</span></span>         |
| <span data-ttu-id="29042-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="29042-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="29042-154">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="29042-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="29042-155">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29042-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29042-156">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="29042-156">Type: **int**</span></span>

<span data-ttu-id="29042-157">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="29042-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="29042-158">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="29042-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="29042-159">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="29042-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="29042-160">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="29042-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="29042-161">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="29042-161">Texture-Object Type</span></span>           | <span data-ttu-id="29042-162">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="29042-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="29042-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="29042-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="29042-164">int</span><span class="sxs-lookup"><span data-stu-id="29042-164">int</span></span>            |
| <span data-ttu-id="29042-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="29042-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="29042-166">int2</span><span class="sxs-lookup"><span data-stu-id="29042-166">int2</span></span>           |
| <span data-ttu-id="29042-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="29042-167">Texture3D</span></span>                     | <span data-ttu-id="29042-168">int3</span><span class="sxs-lookup"><span data-stu-id="29042-168">int3</span></span>           |
| <span data-ttu-id="29042-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="29042-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="29042-170">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="29042-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="29042-171">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29042-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29042-172">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="29042-172">Type: **float**</span></span>

<span data-ttu-id="29042-173">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="29042-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="29042-174">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="29042-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29042-175">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29042-175">Return value</span></span>

<span data-ttu-id="29042-176">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="29042-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="29042-177">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="29042-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="29042-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29042-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29042-179">Méthodes SampleGrad</span><span class="sxs-lookup"><span data-stu-id="29042-179">SampleGrad methods</span></span>](texture1darray-samplegrad.md)
</dt> </dl>

 

 
