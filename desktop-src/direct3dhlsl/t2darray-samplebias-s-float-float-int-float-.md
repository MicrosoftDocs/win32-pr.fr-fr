---
title: 'Fonction SampleBias :: SampleBias (S, float, float, int, float) pour Texture2DArray'
description: 'La fonction SampleBias :: SampleBias (S, float, float, int, float) de Texture2DArray échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap.'
ms.assetid: CC399CB8-1BD8-4CDE-9BFF-66A8917FDAFC
keywords:
- SampleBias fonction HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ae1f5ca8816763ef43f0687312bdf61bbeca9725
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982775"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function-for-texture2darray"></a><span data-ttu-id="32698-104">Fonction SampleBias :: SampleBias (S, float, float, int, float) pour Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="32698-104">SampleBias::SampleBias(S,float,float,int,float) function for Texture2DArray</span></span>

<span data-ttu-id="32698-105">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="32698-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="32698-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32698-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="32698-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32698-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32698-108"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="32698-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32698-109">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="32698-109">Type: **SamplerState**</span></span>

<span data-ttu-id="32698-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="32698-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="32698-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="32698-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="32698-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32698-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32698-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="32698-113">Type: **float**</span></span>

<span data-ttu-id="32698-114">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="32698-114">The texture coordinates.</span></span> <span data-ttu-id="32698-115">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="32698-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="32698-116">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="32698-116">Texture-Object Type</span></span>                    | <span data-ttu-id="32698-117">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="32698-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="32698-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="32698-118">Texture1D</span></span>                              | <span data-ttu-id="32698-119">float</span><span class="sxs-lookup"><span data-stu-id="32698-119">float</span></span>          |
| <span data-ttu-id="32698-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="32698-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="32698-121">float2</span><span class="sxs-lookup"><span data-stu-id="32698-121">float2</span></span>         |
| <span data-ttu-id="32698-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="32698-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="32698-123">float3</span><span class="sxs-lookup"><span data-stu-id="32698-123">float3</span></span>         |
| <span data-ttu-id="32698-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="32698-124">TextureCubeArray</span></span>                       | <span data-ttu-id="32698-125">float4</span><span class="sxs-lookup"><span data-stu-id="32698-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="32698-126">*Biais* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32698-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32698-127">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="32698-127">Type: **float**</span></span>

<span data-ttu-id="32698-128">La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="32698-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="32698-129">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32698-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32698-130">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="32698-130">Type: **int**</span></span>

<span data-ttu-id="32698-131">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="32698-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="32698-132">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="32698-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="32698-133">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="32698-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="32698-134">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="32698-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="32698-135">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="32698-135">Texture-Object Type</span></span>           | <span data-ttu-id="32698-136">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="32698-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="32698-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="32698-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="32698-138">int</span><span class="sxs-lookup"><span data-stu-id="32698-138">int</span></span>            |
| <span data-ttu-id="32698-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="32698-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="32698-140">int2</span><span class="sxs-lookup"><span data-stu-id="32698-140">int2</span></span>           |
| <span data-ttu-id="32698-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="32698-141">Texture3D</span></span>                     | <span data-ttu-id="32698-142">int3</span><span class="sxs-lookup"><span data-stu-id="32698-142">int3</span></span>           |
| <span data-ttu-id="32698-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="32698-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="32698-144">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="32698-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="32698-145">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32698-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32698-146">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="32698-146">Type: **float**</span></span>

<span data-ttu-id="32698-147">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="32698-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="32698-148">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="32698-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32698-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32698-149">Return value</span></span>

<span data-ttu-id="32698-150">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="32698-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="32698-151">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="32698-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="32698-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32698-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32698-153">Méthodes SampleBias</span><span class="sxs-lookup"><span data-stu-id="32698-153">SampleBias methods</span></span>](texture2darray-samplebias.md)
</dt> </dl>

 

 
