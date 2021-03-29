---
title: 'Fonction SampleGrad :: SampleGrad (S, float, float, float, float) pour TextureCube'
description: Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. Pour TextureCube
ms.assetid: C5BC71FA-63E3-4DE2-9202-B9C79789AE8E
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
ms.openlocfilehash: e4a51c49d9373dc210cbf216089e4c82835bf2c4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531120"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="0cf82-105">Fonction SampleGrad :: SampleGrad (S, float, float, float, float) pour TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cf82-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="0cf82-106">Échantillonne une texture en utilisant un dégradé pour influencer la façon dont l’emplacement de l’échantillon est calculé, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="0cf82-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf82-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cf82-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="0cf82-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cf82-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cf82-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="0cf82-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf82-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="0cf82-110">Type: **SamplerState**</span></span>

<span data-ttu-id="0cf82-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="0cf82-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="0cf82-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="0cf82-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="0cf82-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0cf82-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf82-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="0cf82-114">Type: **float**</span></span>

<span data-ttu-id="0cf82-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="0cf82-115">The texture coordinates.</span></span> <span data-ttu-id="0cf82-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="0cf82-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="0cf82-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="0cf82-117">Texture-Object Type</span></span>                    | <span data-ttu-id="0cf82-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="0cf82-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="0cf82-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0cf82-119">Texture1D</span></span>                              | <span data-ttu-id="0cf82-120">float</span><span class="sxs-lookup"><span data-stu-id="0cf82-120">float</span></span>          |
| <span data-ttu-id="0cf82-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="0cf82-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="0cf82-122">float2</span><span class="sxs-lookup"><span data-stu-id="0cf82-122">float2</span></span>         |
| <span data-ttu-id="0cf82-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="0cf82-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="0cf82-124">float3</span><span class="sxs-lookup"><span data-stu-id="0cf82-124">float3</span></span>         |
| <span data-ttu-id="0cf82-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0cf82-125">TextureCubeArray</span></span>                       | <span data-ttu-id="0cf82-126">float4</span><span class="sxs-lookup"><span data-stu-id="0cf82-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="0cf82-127">*Ddx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0cf82-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf82-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="0cf82-128">Type: **float**</span></span>

<span data-ttu-id="0cf82-129">Taux de modification de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="0cf82-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="0cf82-130">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="0cf82-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="0cf82-131">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="0cf82-131">Texture-Object Type</span></span>                      | <span data-ttu-id="0cf82-132">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="0cf82-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="0cf82-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="0cf82-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="0cf82-134">float</span><span class="sxs-lookup"><span data-stu-id="0cf82-134">float</span></span>          |
| <span data-ttu-id="0cf82-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0cf82-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="0cf82-136">float2</span><span class="sxs-lookup"><span data-stu-id="0cf82-136">float2</span></span>         |
| <span data-ttu-id="0cf82-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0cf82-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="0cf82-138">float3</span><span class="sxs-lookup"><span data-stu-id="0cf82-138">float3</span></span>         |
| <span data-ttu-id="0cf82-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="0cf82-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="0cf82-140">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cf82-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="0cf82-141">*Ddy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0cf82-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf82-142">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="0cf82-142">Type: **float**</span></span>

<span data-ttu-id="0cf82-143">Taux de modification de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="0cf82-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="0cf82-144">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="0cf82-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="0cf82-145">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="0cf82-145">Texture-Object Type</span></span>                      | <span data-ttu-id="0cf82-146">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="0cf82-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="0cf82-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="0cf82-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="0cf82-148">float</span><span class="sxs-lookup"><span data-stu-id="0cf82-148">float</span></span>          |
| <span data-ttu-id="0cf82-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0cf82-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="0cf82-150">float2</span><span class="sxs-lookup"><span data-stu-id="0cf82-150">float2</span></span>         |
| <span data-ttu-id="0cf82-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0cf82-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="0cf82-152">float3</span><span class="sxs-lookup"><span data-stu-id="0cf82-152">float3</span></span>         |
| <span data-ttu-id="0cf82-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="0cf82-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="0cf82-154">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cf82-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="0cf82-155">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0cf82-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cf82-156">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="0cf82-156">Type: **float**</span></span>

<span data-ttu-id="0cf82-157">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="0cf82-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="0cf82-158">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="0cf82-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cf82-159">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0cf82-159">Return value</span></span>

<span data-ttu-id="0cf82-160">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="0cf82-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="0cf82-161">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="0cf82-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="0cf82-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cf82-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf82-163">Méthodes SampleGrad</span><span class="sxs-lookup"><span data-stu-id="0cf82-163">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="0cf82-164">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="0cf82-164">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
