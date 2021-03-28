---
title: 'Fonction de fonction SampleGrad :: SampleGrad (S, float, float, float, int, float) pour Texture3D'
description: Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. Pour Texture3D.
ms.assetid: F59D54F8-CC9E-47F8-97DD-735C70939C07
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
ms.openlocfilehash: 6d0bd1c47a82784b2b96a93a7f43ecd158e4782a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982722"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture3d"></a><span data-ttu-id="5654a-105">Fonction SampleGrad :: SampleGrad (S, float, float, float, int, float) pour Texture3D</span><span class="sxs-lookup"><span data-stu-id="5654a-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture3D</span></span>

<span data-ttu-id="5654a-106">Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="5654a-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="5654a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5654a-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="5654a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5654a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5654a-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="5654a-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5654a-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="5654a-110">Type: **SamplerState**</span></span>

<span data-ttu-id="5654a-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="5654a-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="5654a-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="5654a-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="5654a-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5654a-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5654a-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="5654a-114">Type: **float**</span></span>

<span data-ttu-id="5654a-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="5654a-115">The texture coordinates.</span></span> <span data-ttu-id="5654a-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="5654a-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5654a-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5654a-117">Texture-Object Type</span></span>                    | <span data-ttu-id="5654a-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="5654a-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="5654a-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5654a-119">Texture1D</span></span>                              | <span data-ttu-id="5654a-120">float</span><span class="sxs-lookup"><span data-stu-id="5654a-120">float</span></span>          |
| <span data-ttu-id="5654a-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="5654a-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="5654a-122">float2</span><span class="sxs-lookup"><span data-stu-id="5654a-122">float2</span></span>         |
| <span data-ttu-id="5654a-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="5654a-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="5654a-124">float3</span><span class="sxs-lookup"><span data-stu-id="5654a-124">float3</span></span>         |
| <span data-ttu-id="5654a-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5654a-125">TextureCubeArray</span></span>                       | <span data-ttu-id="5654a-126">float4</span><span class="sxs-lookup"><span data-stu-id="5654a-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="5654a-127">*Ddx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5654a-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5654a-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="5654a-128">Type: **float**</span></span>

<span data-ttu-id="5654a-129">Taux de modification de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="5654a-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="5654a-130">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="5654a-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5654a-131">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5654a-131">Texture-Object Type</span></span>                      | <span data-ttu-id="5654a-132">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="5654a-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="5654a-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5654a-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="5654a-134">float</span><span class="sxs-lookup"><span data-stu-id="5654a-134">float</span></span>          |
| <span data-ttu-id="5654a-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5654a-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="5654a-136">float2</span><span class="sxs-lookup"><span data-stu-id="5654a-136">float2</span></span>         |
| <span data-ttu-id="5654a-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5654a-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="5654a-138">float3</span><span class="sxs-lookup"><span data-stu-id="5654a-138">float3</span></span>         |
| <span data-ttu-id="5654a-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="5654a-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="5654a-140">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="5654a-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="5654a-141">*Ddy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5654a-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5654a-142">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="5654a-142">Type: **float**</span></span>

<span data-ttu-id="5654a-143">Taux de modification de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="5654a-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="5654a-144">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="5654a-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5654a-145">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5654a-145">Texture-Object Type</span></span>                      | <span data-ttu-id="5654a-146">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="5654a-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="5654a-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5654a-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="5654a-148">float</span><span class="sxs-lookup"><span data-stu-id="5654a-148">float</span></span>          |
| <span data-ttu-id="5654a-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5654a-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="5654a-150">float2</span><span class="sxs-lookup"><span data-stu-id="5654a-150">float2</span></span>         |
| <span data-ttu-id="5654a-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5654a-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="5654a-152">float3</span><span class="sxs-lookup"><span data-stu-id="5654a-152">float3</span></span>         |
| <span data-ttu-id="5654a-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="5654a-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="5654a-154">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="5654a-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="5654a-155">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5654a-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5654a-156">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="5654a-156">Type: **int**</span></span>

<span data-ttu-id="5654a-157">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="5654a-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="5654a-158">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="5654a-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="5654a-159">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="5654a-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="5654a-160">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="5654a-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="5654a-161">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5654a-161">Texture-Object Type</span></span>           | <span data-ttu-id="5654a-162">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="5654a-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="5654a-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5654a-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="5654a-164">int</span><span class="sxs-lookup"><span data-stu-id="5654a-164">int</span></span>            |
| <span data-ttu-id="5654a-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5654a-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="5654a-166">int2</span><span class="sxs-lookup"><span data-stu-id="5654a-166">int2</span></span>           |
| <span data-ttu-id="5654a-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5654a-167">Texture3D</span></span>                     | <span data-ttu-id="5654a-168">int3</span><span class="sxs-lookup"><span data-stu-id="5654a-168">int3</span></span>           |
| <span data-ttu-id="5654a-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5654a-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="5654a-170">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="5654a-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="5654a-171">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5654a-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5654a-172">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="5654a-172">Type: **float**</span></span>

<span data-ttu-id="5654a-173">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="5654a-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="5654a-174">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="5654a-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5654a-175">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5654a-175">Return value</span></span>

<span data-ttu-id="5654a-176">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="5654a-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="5654a-177">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="5654a-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="5654a-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5654a-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5654a-179">Méthodes SampleGrad</span><span class="sxs-lookup"><span data-stu-id="5654a-179">SampleGrad methods</span></span>](texture3d-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="5654a-180">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="5654a-180">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
