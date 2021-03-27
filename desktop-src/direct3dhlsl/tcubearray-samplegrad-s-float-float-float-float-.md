---
title: 'Fonction SampleGrad :: SampleGrad (S, float, float, float, float) pour TextureCubeArray'
description: Découvrez comment cette fonction échantillonne une texture à l’aide d’un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé. Pour TextureCubeArray.
ms.assetid: 0C7DC9AA-3F0A-47E4-852F-7AE25CF67EA3
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
ms.openlocfilehash: 5320f47a5ae4db5bd96232dfa0a1d55b54f29c25
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762403"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="49a43-105">Fonction SampleGrad :: SampleGrad (S, float, float, float, float) pour TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="49a43-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="49a43-106">Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="49a43-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a43-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49a43-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="49a43-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49a43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49a43-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="49a43-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a43-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="49a43-110">Type: **SamplerState**</span></span>

<span data-ttu-id="49a43-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="49a43-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="49a43-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="49a43-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="49a43-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49a43-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a43-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="49a43-114">Type: **float**</span></span>

<span data-ttu-id="49a43-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="49a43-115">The texture coordinates.</span></span> <span data-ttu-id="49a43-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="49a43-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="49a43-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="49a43-117">Texture-Object Type</span></span>                    | <span data-ttu-id="49a43-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="49a43-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="49a43-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="49a43-119">Texture1D</span></span>                              | <span data-ttu-id="49a43-120">float</span><span class="sxs-lookup"><span data-stu-id="49a43-120">float</span></span>          |
| <span data-ttu-id="49a43-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="49a43-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="49a43-122">float2</span><span class="sxs-lookup"><span data-stu-id="49a43-122">float2</span></span>         |
| <span data-ttu-id="49a43-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="49a43-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="49a43-124">float3</span><span class="sxs-lookup"><span data-stu-id="49a43-124">float3</span></span>         |
| <span data-ttu-id="49a43-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="49a43-125">TextureCubeArray</span></span>                       | <span data-ttu-id="49a43-126">float4</span><span class="sxs-lookup"><span data-stu-id="49a43-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="49a43-127">*Ddx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49a43-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a43-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="49a43-128">Type: **float**</span></span>

<span data-ttu-id="49a43-129">Taux de modification de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="49a43-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="49a43-130">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="49a43-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="49a43-131">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="49a43-131">Texture-Object Type</span></span>                      | <span data-ttu-id="49a43-132">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="49a43-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="49a43-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="49a43-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="49a43-134">float</span><span class="sxs-lookup"><span data-stu-id="49a43-134">float</span></span>          |
| <span data-ttu-id="49a43-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="49a43-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="49a43-136">float2</span><span class="sxs-lookup"><span data-stu-id="49a43-136">float2</span></span>         |
| <span data-ttu-id="49a43-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="49a43-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="49a43-138">float3</span><span class="sxs-lookup"><span data-stu-id="49a43-138">float3</span></span>         |
| <span data-ttu-id="49a43-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="49a43-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="49a43-140">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="49a43-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="49a43-141">*Ddy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49a43-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a43-142">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="49a43-142">Type: **float**</span></span>

<span data-ttu-id="49a43-143">Taux de modification de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="49a43-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="49a43-144">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="49a43-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="49a43-145">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="49a43-145">Texture-Object Type</span></span>                      | <span data-ttu-id="49a43-146">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="49a43-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="49a43-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="49a43-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="49a43-148">float</span><span class="sxs-lookup"><span data-stu-id="49a43-148">float</span></span>          |
| <span data-ttu-id="49a43-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="49a43-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="49a43-150">float2</span><span class="sxs-lookup"><span data-stu-id="49a43-150">float2</span></span>         |
| <span data-ttu-id="49a43-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="49a43-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="49a43-152">float3</span><span class="sxs-lookup"><span data-stu-id="49a43-152">float3</span></span>         |
| <span data-ttu-id="49a43-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="49a43-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="49a43-154">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="49a43-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="49a43-155">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49a43-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a43-156">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="49a43-156">Type: **float**</span></span>

<span data-ttu-id="49a43-157">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="49a43-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="49a43-158">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="49a43-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49a43-159">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49a43-159">Return value</span></span>

<span data-ttu-id="49a43-160">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="49a43-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="49a43-161">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="49a43-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="49a43-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49a43-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49a43-163">Méthodes SampleGrad</span><span class="sxs-lookup"><span data-stu-id="49a43-163">SampleGrad methods</span></span>](texturecubearray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="49a43-164">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="49a43-164">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
