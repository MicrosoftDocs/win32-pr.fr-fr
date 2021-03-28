---
title: 'SampleBias :: SampleBias (S, float, float, int, float) (fonction)'
description: 'Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. | SampleBias :: SampleBias (S, float, float, int, float) (fonction)'
ms.assetid: 88BC4E99-B33D-4DAA-9A77-849B2F5FE6A7
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
ms.openlocfilehash: 3af7ddaf3c015c2254761cce1d7cd30a2a68629b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991985"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function"></a><span data-ttu-id="4db8a-105">SampleBias :: SampleBias (S, float, float, int, float) (fonction)</span><span class="sxs-lookup"><span data-stu-id="4db8a-105">SampleBias::SampleBias(S,float,float,int,float) function</span></span>

<span data-ttu-id="4db8a-106">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="4db8a-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="4db8a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4db8a-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="4db8a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4db8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4db8a-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="4db8a-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db8a-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="4db8a-110">Type: **SamplerState**</span></span>

<span data-ttu-id="4db8a-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="4db8a-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="4db8a-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="4db8a-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="4db8a-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4db8a-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db8a-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="4db8a-114">Type: **float**</span></span>

<span data-ttu-id="4db8a-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="4db8a-115">The texture coordinates.</span></span> <span data-ttu-id="4db8a-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="4db8a-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4db8a-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4db8a-117">Texture-Object Type</span></span>                    | <span data-ttu-id="4db8a-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="4db8a-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="4db8a-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4db8a-119">Texture1D</span></span>                              | <span data-ttu-id="4db8a-120">float</span><span class="sxs-lookup"><span data-stu-id="4db8a-120">float</span></span>          |
| <span data-ttu-id="4db8a-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="4db8a-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="4db8a-122">float2</span><span class="sxs-lookup"><span data-stu-id="4db8a-122">float2</span></span>         |
| <span data-ttu-id="4db8a-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="4db8a-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="4db8a-124">float3</span><span class="sxs-lookup"><span data-stu-id="4db8a-124">float3</span></span>         |
| <span data-ttu-id="4db8a-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4db8a-125">TextureCubeArray</span></span>                       | <span data-ttu-id="4db8a-126">float4</span><span class="sxs-lookup"><span data-stu-id="4db8a-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="4db8a-127">*Biais* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4db8a-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db8a-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="4db8a-128">Type: **float**</span></span>

<span data-ttu-id="4db8a-129">La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="4db8a-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4db8a-130">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4db8a-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db8a-131">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="4db8a-131">Type: **int**</span></span>

<span data-ttu-id="4db8a-132">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="4db8a-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="4db8a-133">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="4db8a-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="4db8a-134">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="4db8a-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="4db8a-135">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4db8a-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="4db8a-136">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4db8a-136">Texture-Object Type</span></span>           | <span data-ttu-id="4db8a-137">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="4db8a-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="4db8a-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4db8a-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="4db8a-139">int</span><span class="sxs-lookup"><span data-stu-id="4db8a-139">int</span></span>            |
| <span data-ttu-id="4db8a-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4db8a-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="4db8a-141">int2</span><span class="sxs-lookup"><span data-stu-id="4db8a-141">int2</span></span>           |
| <span data-ttu-id="4db8a-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4db8a-142">Texture3D</span></span>                     | <span data-ttu-id="4db8a-143">int3</span><span class="sxs-lookup"><span data-stu-id="4db8a-143">int3</span></span>           |
| <span data-ttu-id="4db8a-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4db8a-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="4db8a-145">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="4db8a-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4db8a-146">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4db8a-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db8a-147">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="4db8a-147">Type: **float**</span></span>

<span data-ttu-id="4db8a-148">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="4db8a-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="4db8a-149">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="4db8a-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4db8a-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4db8a-150">Return value</span></span>

<span data-ttu-id="4db8a-151">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="4db8a-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="4db8a-152">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="4db8a-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="4db8a-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4db8a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db8a-154">Méthodes SampleBias</span><span class="sxs-lookup"><span data-stu-id="4db8a-154">SampleBias methods</span></span>](texture1d-samplebias.md)
</dt> </dl>

 

 
