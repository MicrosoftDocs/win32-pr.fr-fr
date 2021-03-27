---
title: 'Fonction SampleGrad :: SampleGrad (S, float, float, float, int, float, uint) pour Texture2D'
description: Échantillonne un Texture2D à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.
ms.assetid: 896497E1-A795-4674-AB41-2440A7D0CC76
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
ms.openlocfilehash: 9f1909c792863a3b480b6bdec553db58f7ff8492
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996413"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture2d"></a><span data-ttu-id="84080-104">Fonction SampleGrad :: SampleGrad (S, float, float, float, int, float, uint) pour Texture2D</span><span class="sxs-lookup"><span data-stu-id="84080-104">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture2D</span></span>

<span data-ttu-id="84080-105">Échantillonne un [**Texture2D**](sm5-object-texture2d.md)à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="84080-105">Samples a [**Texture2D**](sm5-object-texture2d.md), using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="84080-106">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="84080-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="84080-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84080-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="84080-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84080-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84080-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="84080-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84080-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="84080-110">Type: **SamplerState**</span></span>

<span data-ttu-id="84080-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="84080-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="84080-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="84080-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="84080-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84080-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84080-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="84080-114">Type: **float**</span></span>

<span data-ttu-id="84080-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="84080-115">The texture coordinates.</span></span> <span data-ttu-id="84080-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="84080-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="84080-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="84080-117">Texture-Object Type</span></span>                    | <span data-ttu-id="84080-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="84080-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="84080-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="84080-119">Texture1D</span></span>                              | <span data-ttu-id="84080-120">float</span><span class="sxs-lookup"><span data-stu-id="84080-120">float</span></span>          |
| <span data-ttu-id="84080-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="84080-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="84080-122">float2</span><span class="sxs-lookup"><span data-stu-id="84080-122">float2</span></span>         |
| <span data-ttu-id="84080-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="84080-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="84080-124">float3</span><span class="sxs-lookup"><span data-stu-id="84080-124">float3</span></span>         |
| <span data-ttu-id="84080-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="84080-125">TextureCubeArray</span></span>                       | <span data-ttu-id="84080-126">float4</span><span class="sxs-lookup"><span data-stu-id="84080-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="84080-127">*Ddx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84080-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84080-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="84080-128">Type: **float**</span></span>

<span data-ttu-id="84080-129">Taux de modification de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="84080-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="84080-130">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="84080-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="84080-131">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="84080-131">Texture-Object Type</span></span>                      | <span data-ttu-id="84080-132">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="84080-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="84080-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="84080-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="84080-134">float</span><span class="sxs-lookup"><span data-stu-id="84080-134">float</span></span>          |
| <span data-ttu-id="84080-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="84080-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="84080-136">float2</span><span class="sxs-lookup"><span data-stu-id="84080-136">float2</span></span>         |
| <span data-ttu-id="84080-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="84080-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="84080-138">float3</span><span class="sxs-lookup"><span data-stu-id="84080-138">float3</span></span>         |
| <span data-ttu-id="84080-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="84080-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="84080-140">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="84080-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="84080-141">*Ddy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84080-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84080-142">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="84080-142">Type: **float**</span></span>

<span data-ttu-id="84080-143">Taux de modification de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="84080-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="84080-144">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="84080-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="84080-145">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="84080-145">Texture-Object Type</span></span>                      | <span data-ttu-id="84080-146">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="84080-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="84080-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="84080-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="84080-148">float</span><span class="sxs-lookup"><span data-stu-id="84080-148">float</span></span>          |
| <span data-ttu-id="84080-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="84080-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="84080-150">float2</span><span class="sxs-lookup"><span data-stu-id="84080-150">float2</span></span>         |
| <span data-ttu-id="84080-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="84080-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="84080-152">float3</span><span class="sxs-lookup"><span data-stu-id="84080-152">float3</span></span>         |
| <span data-ttu-id="84080-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="84080-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="84080-154">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="84080-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="84080-155">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84080-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84080-156">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="84080-156">Type: **int**</span></span>

<span data-ttu-id="84080-157">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="84080-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="84080-158">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="84080-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="84080-159">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="84080-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="84080-160">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="84080-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="84080-161">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="84080-161">Texture-Object Type</span></span>           | <span data-ttu-id="84080-162">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="84080-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="84080-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="84080-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="84080-164">int</span><span class="sxs-lookup"><span data-stu-id="84080-164">int</span></span>            |
| <span data-ttu-id="84080-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="84080-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="84080-166">int2</span><span class="sxs-lookup"><span data-stu-id="84080-166">int2</span></span>           |
| <span data-ttu-id="84080-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="84080-167">Texture3D</span></span>                     | <span data-ttu-id="84080-168">int3</span><span class="sxs-lookup"><span data-stu-id="84080-168">int3</span></span>           |
| <span data-ttu-id="84080-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="84080-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="84080-170">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="84080-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="84080-171">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84080-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84080-172">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="84080-172">Type: **float**</span></span>

<span data-ttu-id="84080-173">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="84080-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="84080-174">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="84080-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="84080-175">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="84080-175">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84080-176">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="84080-176">Type: **uint**</span></span>

<span data-ttu-id="84080-177">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="84080-177">The status of the operation.</span></span> <span data-ttu-id="84080-178">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="84080-178">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="84080-179">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="84080-179">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="84080-180">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="84080-180">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84080-181">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84080-181">Return value</span></span>

<span data-ttu-id="84080-182">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="84080-182">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="84080-183">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="84080-183">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="84080-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84080-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84080-185">Méthodes SampleGrad</span><span class="sxs-lookup"><span data-stu-id="84080-185">SampleGrad methods</span></span>](texture2d-samplegrad.md)
</dt> </dl>

 

 
