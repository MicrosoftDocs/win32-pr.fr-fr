---
title: 'Fonction SampleGrad :: SampleGrad (S, float, float, float, int, float, uint) pour Texture1D'
description: Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. Pour Texture1D.
ms.assetid: E2B131AC-99E6-493A-91EE-EB0D3EE7FA8B
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
ms.openlocfilehash: 3a5f95a87f46e94c971dd19989ffa670e6993e8f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103954032"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture1d"></a><span data-ttu-id="1a621-105">Fonction SampleGrad :: SampleGrad (S, float, float, float, int, float, uint) pour Texture1D</span><span class="sxs-lookup"><span data-stu-id="1a621-105">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture1D</span></span>

<span data-ttu-id="1a621-106">Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="1a621-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="1a621-107">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1a621-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a621-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a621-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1a621-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a621-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a621-110"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="1a621-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a621-111">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="1a621-111">Type: **SamplerState**</span></span>

<span data-ttu-id="1a621-112">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="1a621-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="1a621-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="1a621-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="1a621-114">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a621-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a621-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="1a621-115">Type: **float**</span></span>

<span data-ttu-id="1a621-116">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="1a621-116">The texture coordinates.</span></span> <span data-ttu-id="1a621-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="1a621-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1a621-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1a621-118">Texture-Object Type</span></span>                    | <span data-ttu-id="1a621-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="1a621-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="1a621-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1a621-120">Texture1D</span></span>                              | <span data-ttu-id="1a621-121">float</span><span class="sxs-lookup"><span data-stu-id="1a621-121">float</span></span>          |
| <span data-ttu-id="1a621-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="1a621-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="1a621-123">float2</span><span class="sxs-lookup"><span data-stu-id="1a621-123">float2</span></span>         |
| <span data-ttu-id="1a621-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="1a621-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="1a621-125">float3</span><span class="sxs-lookup"><span data-stu-id="1a621-125">float3</span></span>         |
| <span data-ttu-id="1a621-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1a621-126">TextureCubeArray</span></span>                       | <span data-ttu-id="1a621-127">float4</span><span class="sxs-lookup"><span data-stu-id="1a621-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="1a621-128">*Ddx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a621-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a621-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="1a621-129">Type: **float**</span></span>

<span data-ttu-id="1a621-130">Taux de modification de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="1a621-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="1a621-131">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="1a621-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1a621-132">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1a621-132">Texture-Object Type</span></span>                      | <span data-ttu-id="1a621-133">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="1a621-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="1a621-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1a621-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="1a621-135">float</span><span class="sxs-lookup"><span data-stu-id="1a621-135">float</span></span>          |
| <span data-ttu-id="1a621-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1a621-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="1a621-137">float2</span><span class="sxs-lookup"><span data-stu-id="1a621-137">float2</span></span>         |
| <span data-ttu-id="1a621-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1a621-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="1a621-139">float3</span><span class="sxs-lookup"><span data-stu-id="1a621-139">float3</span></span>         |
| <span data-ttu-id="1a621-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="1a621-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="1a621-141">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a621-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="1a621-142">*Ddy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a621-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a621-143">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="1a621-143">Type: **float**</span></span>

<span data-ttu-id="1a621-144">Taux de modification de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="1a621-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="1a621-145">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="1a621-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1a621-146">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1a621-146">Texture-Object Type</span></span>                      | <span data-ttu-id="1a621-147">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="1a621-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="1a621-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1a621-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="1a621-149">float</span><span class="sxs-lookup"><span data-stu-id="1a621-149">float</span></span>          |
| <span data-ttu-id="1a621-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1a621-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="1a621-151">float2</span><span class="sxs-lookup"><span data-stu-id="1a621-151">float2</span></span>         |
| <span data-ttu-id="1a621-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1a621-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="1a621-153">float3</span><span class="sxs-lookup"><span data-stu-id="1a621-153">float3</span></span>         |
| <span data-ttu-id="1a621-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="1a621-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="1a621-155">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a621-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="1a621-156">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a621-156">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a621-157">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="1a621-157">Type: **int**</span></span>

<span data-ttu-id="1a621-158">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="1a621-158">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="1a621-159">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="1a621-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="1a621-160">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="1a621-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="1a621-161">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1a621-161">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="1a621-162">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1a621-162">Texture-Object Type</span></span>           | <span data-ttu-id="1a621-163">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="1a621-163">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="1a621-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1a621-164">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="1a621-165">int</span><span class="sxs-lookup"><span data-stu-id="1a621-165">int</span></span>            |
| <span data-ttu-id="1a621-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1a621-166">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="1a621-167">int2</span><span class="sxs-lookup"><span data-stu-id="1a621-167">int2</span></span>           |
| <span data-ttu-id="1a621-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="1a621-168">Texture3D</span></span>                     | <span data-ttu-id="1a621-169">int3</span><span class="sxs-lookup"><span data-stu-id="1a621-169">int3</span></span>           |
| <span data-ttu-id="1a621-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1a621-170">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="1a621-171">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a621-171">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="1a621-172">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a621-172">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a621-173">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="1a621-173">Type: **float**</span></span>

<span data-ttu-id="1a621-174">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="1a621-174">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="1a621-175">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="1a621-175">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="1a621-176">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1a621-176">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a621-177">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1a621-177">Type: **uint**</span></span>

<span data-ttu-id="1a621-178">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1a621-178">The status of the operation.</span></span> <span data-ttu-id="1a621-179">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="1a621-179">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1a621-180">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="1a621-180">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1a621-181">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="1a621-181">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a621-182">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a621-182">Return value</span></span>

<span data-ttu-id="1a621-183">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="1a621-183">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="1a621-184">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="1a621-184">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="1a621-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a621-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a621-186">Méthodes SampleGrad</span><span class="sxs-lookup"><span data-stu-id="1a621-186">SampleGrad methods</span></span>](texture1d-samplegrad.md)
</dt> </dl>

 

 
