---
title: 'Fonction SampleGrad :: SampleGrad (S, float, float, float, float, uint) pour TextureCube'
description: Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. Pour TextureCube.
ms.assetid: 36DF7846-416A-4F2F-A7F8-44EE768CDEE1
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
ms.openlocfilehash: 3e75bccaeac28aefc50620a5dea31fa62b880332
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531095"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="a0f2b-105">Fonction SampleGrad :: SampleGrad (S, float, float, float, float, uint) pour TextureCube</span><span class="sxs-lookup"><span data-stu-id="a0f2b-105">SampleGrad::SampleGrad(S,float,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="a0f2b-106">Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="a0f2b-107">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f2b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0f2b-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a0f2b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0f2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f2b-110"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-111">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-111">Type: **SamplerState**</span></span>

<span data-ttu-id="a0f2b-112">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a0f2b-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a0f2b-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a0f2b-114">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-115">Type: **float**</span></span>

<span data-ttu-id="a0f2b-116">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-116">The texture coordinates.</span></span> <span data-ttu-id="a0f2b-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a0f2b-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a0f2b-118">Texture-Object Type</span></span>                    | <span data-ttu-id="a0f2b-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="a0f2b-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a0f2b-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a0f2b-120">Texture1D</span></span>                              | <span data-ttu-id="a0f2b-121">float</span><span class="sxs-lookup"><span data-stu-id="a0f2b-121">float</span></span>          |
| <span data-ttu-id="a0f2b-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a0f2b-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a0f2b-123">float2</span><span class="sxs-lookup"><span data-stu-id="a0f2b-123">float2</span></span>         |
| <span data-ttu-id="a0f2b-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="a0f2b-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a0f2b-125">float3</span><span class="sxs-lookup"><span data-stu-id="a0f2b-125">float3</span></span>         |
| <span data-ttu-id="a0f2b-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a0f2b-126">TextureCubeArray</span></span>                       | <span data-ttu-id="a0f2b-127">float4</span><span class="sxs-lookup"><span data-stu-id="a0f2b-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a0f2b-128">*Ddx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-129">Type: **float**</span></span>

<span data-ttu-id="a0f2b-130">Taux de modification de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="a0f2b-131">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a0f2b-132">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a0f2b-132">Texture-Object Type</span></span>                      | <span data-ttu-id="a0f2b-133">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="a0f2b-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="a0f2b-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a0f2b-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="a0f2b-135">float</span><span class="sxs-lookup"><span data-stu-id="a0f2b-135">float</span></span>          |
| <span data-ttu-id="a0f2b-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a0f2b-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="a0f2b-137">float2</span><span class="sxs-lookup"><span data-stu-id="a0f2b-137">float2</span></span>         |
| <span data-ttu-id="a0f2b-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a0f2b-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a0f2b-139">float3</span><span class="sxs-lookup"><span data-stu-id="a0f2b-139">float3</span></span>         |
| <span data-ttu-id="a0f2b-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="a0f2b-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="a0f2b-141">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0f2b-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a0f2b-142">*Ddy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-143">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-143">Type: **float**</span></span>

<span data-ttu-id="a0f2b-144">Taux de modification de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="a0f2b-145">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a0f2b-146">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a0f2b-146">Texture-Object Type</span></span>                      | <span data-ttu-id="a0f2b-147">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="a0f2b-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="a0f2b-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a0f2b-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="a0f2b-149">float</span><span class="sxs-lookup"><span data-stu-id="a0f2b-149">float</span></span>          |
| <span data-ttu-id="a0f2b-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a0f2b-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="a0f2b-151">float2</span><span class="sxs-lookup"><span data-stu-id="a0f2b-151">float2</span></span>         |
| <span data-ttu-id="a0f2b-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a0f2b-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a0f2b-153">float3</span><span class="sxs-lookup"><span data-stu-id="a0f2b-153">float3</span></span>         |
| <span data-ttu-id="a0f2b-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="a0f2b-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="a0f2b-155">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0f2b-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a0f2b-156">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-156">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-157">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-157">Type: **float**</span></span>

<span data-ttu-id="a0f2b-158">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-158">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a0f2b-159">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-159">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="a0f2b-160">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-160">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-161">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-161">Type: **uint**</span></span>

<span data-ttu-id="a0f2b-162">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-162">The status of the operation.</span></span> <span data-ttu-id="a0f2b-163">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f2b-163">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a0f2b-164">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a0f2b-164">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a0f2b-165">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-165">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f2b-166">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0f2b-166">Return value</span></span>

<span data-ttu-id="a0f2b-167">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-167">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="a0f2b-168">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="a0f2b-168">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a0f2b-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0f2b-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f2b-170">Méthodes SampleGrad</span><span class="sxs-lookup"><span data-stu-id="a0f2b-170">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="a0f2b-171">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-171">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
