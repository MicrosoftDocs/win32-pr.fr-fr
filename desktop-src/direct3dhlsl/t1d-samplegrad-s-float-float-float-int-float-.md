---
title: 'Fonction SampleGrad :: SampleGrad (S, float, float, float, int, float) pour Texture1D'
description: La fonction échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.
ms.assetid: 34A79CB6-0C45-40ED-845C-77C08F1DEC57
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
ms.openlocfilehash: 8c6222d8fa9548e3154abf7605fc5032dd67235a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982746"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="ca8e1-104">Fonction SampleGrad :: SampleGrad (S, float, float, float, int, float) pour Texture1D</span><span class="sxs-lookup"><span data-stu-id="ca8e1-104">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="ca8e1-105">Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-105">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca8e1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca8e1-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ca8e1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca8e1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca8e1-108"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="ca8e1-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca8e1-109">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="ca8e1-109">Type: **SamplerState**</span></span>

<span data-ttu-id="ca8e1-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="ca8e1-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="ca8e1-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="ca8e1-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca8e1-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca8e1-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="ca8e1-113">Type: **float**</span></span>

<span data-ttu-id="ca8e1-114">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-114">The texture coordinates.</span></span> <span data-ttu-id="ca8e1-115">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ca8e1-116">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ca8e1-116">Texture-Object Type</span></span>                    | <span data-ttu-id="ca8e1-117">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="ca8e1-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="ca8e1-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ca8e1-118">Texture1D</span></span>                              | <span data-ttu-id="ca8e1-119">float</span><span class="sxs-lookup"><span data-stu-id="ca8e1-119">float</span></span>          |
| <span data-ttu-id="ca8e1-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ca8e1-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="ca8e1-121">float2</span><span class="sxs-lookup"><span data-stu-id="ca8e1-121">float2</span></span>         |
| <span data-ttu-id="ca8e1-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ca8e1-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="ca8e1-123">float3</span><span class="sxs-lookup"><span data-stu-id="ca8e1-123">float3</span></span>         |
| <span data-ttu-id="ca8e1-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ca8e1-124">TextureCubeArray</span></span>                       | <span data-ttu-id="ca8e1-125">float4</span><span class="sxs-lookup"><span data-stu-id="ca8e1-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="ca8e1-126">*Ddx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca8e1-126">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca8e1-127">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="ca8e1-127">Type: **float**</span></span>

<span data-ttu-id="ca8e1-128">Taux de modification de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-128">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="ca8e1-129">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-129">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ca8e1-130">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ca8e1-130">Texture-Object Type</span></span>                      | <span data-ttu-id="ca8e1-131">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="ca8e1-131">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="ca8e1-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ca8e1-132">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="ca8e1-133">float</span><span class="sxs-lookup"><span data-stu-id="ca8e1-133">float</span></span>          |
| <span data-ttu-id="ca8e1-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ca8e1-134">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="ca8e1-135">float2</span><span class="sxs-lookup"><span data-stu-id="ca8e1-135">float2</span></span>         |
| <span data-ttu-id="ca8e1-136">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ca8e1-136">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ca8e1-137">float3</span><span class="sxs-lookup"><span data-stu-id="ca8e1-137">float3</span></span>         |
| <span data-ttu-id="ca8e1-138">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ca8e1-138">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="ca8e1-139">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca8e1-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ca8e1-140">*Ddy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca8e1-140">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca8e1-141">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="ca8e1-141">Type: **float**</span></span>

<span data-ttu-id="ca8e1-142">Taux de modification de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-142">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="ca8e1-143">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-143">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ca8e1-144">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ca8e1-144">Texture-Object Type</span></span>                      | <span data-ttu-id="ca8e1-145">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="ca8e1-145">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="ca8e1-146">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ca8e1-146">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="ca8e1-147">float</span><span class="sxs-lookup"><span data-stu-id="ca8e1-147">float</span></span>          |
| <span data-ttu-id="ca8e1-148">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ca8e1-148">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="ca8e1-149">float2</span><span class="sxs-lookup"><span data-stu-id="ca8e1-149">float2</span></span>         |
| <span data-ttu-id="ca8e1-150">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ca8e1-150">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ca8e1-151">float3</span><span class="sxs-lookup"><span data-stu-id="ca8e1-151">float3</span></span>         |
| <span data-ttu-id="ca8e1-152">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="ca8e1-152">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="ca8e1-153">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca8e1-153">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ca8e1-154">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca8e1-154">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca8e1-155">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="ca8e1-155">Type: **int**</span></span>

<span data-ttu-id="ca8e1-156">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-156">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="ca8e1-157">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-157">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="ca8e1-158">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-158">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ca8e1-159">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="ca8e1-159">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="ca8e1-160">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ca8e1-160">Texture-Object Type</span></span>           | <span data-ttu-id="ca8e1-161">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="ca8e1-161">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="ca8e1-162">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ca8e1-162">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="ca8e1-163">int</span><span class="sxs-lookup"><span data-stu-id="ca8e1-163">int</span></span>            |
| <span data-ttu-id="ca8e1-164">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ca8e1-164">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="ca8e1-165">int2</span><span class="sxs-lookup"><span data-stu-id="ca8e1-165">int2</span></span>           |
| <span data-ttu-id="ca8e1-166">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ca8e1-166">Texture3D</span></span>                     | <span data-ttu-id="ca8e1-167">int3</span><span class="sxs-lookup"><span data-stu-id="ca8e1-167">int3</span></span>           |
| <span data-ttu-id="ca8e1-168">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ca8e1-168">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ca8e1-169">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca8e1-169">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ca8e1-170">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ca8e1-170">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca8e1-171">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="ca8e1-171">Type: **float**</span></span>

<span data-ttu-id="ca8e1-172">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-172">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="ca8e1-173">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="ca8e1-173">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca8e1-174">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca8e1-174">Return value</span></span>

<span data-ttu-id="ca8e1-175">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="ca8e1-175">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="ca8e1-176">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="ca8e1-176">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="ca8e1-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca8e1-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca8e1-178">Méthodes SampleGrad</span><span class="sxs-lookup"><span data-stu-id="ca8e1-178">SampleGrad methods</span></span>](texture1d-samplegrad.md)
</dt> </dl>

 

 
