---
title: 'SampleBias :: SampleBias (S, float, float, int, float) (fonction)'
description: Échantillonne un Texture2D, après avoir appliqué la valeur de biais au niveau du mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.
ms.assetid: 4E4A1188-DE45-4A43-B54D-4CA2E66707E3
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
ms.openlocfilehash: d91ce53da6dbf2c1e39f23967d1c1dc36085e764
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032158"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function"></a><span data-ttu-id="054bd-104">SampleBias :: SampleBias (S, float, float, int, float) (fonction)</span><span class="sxs-lookup"><span data-stu-id="054bd-104">SampleBias::SampleBias(S,float,float,int,float) function</span></span>

<span data-ttu-id="054bd-105">Échantillonne un [**Texture2D**](sm5-object-texture2d.md), après avoir appliqué la valeur de biais au niveau du mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="054bd-105">Samples a [**Texture2D**](sm5-object-texture2d.md), after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="054bd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="054bd-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="054bd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="054bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="054bd-108"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="054bd-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="054bd-109">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="054bd-109">Type: **SamplerState**</span></span>

<span data-ttu-id="054bd-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="054bd-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="054bd-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="054bd-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="054bd-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="054bd-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="054bd-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="054bd-113">Type: **float**</span></span>

<span data-ttu-id="054bd-114">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="054bd-114">The texture coordinates.</span></span> <span data-ttu-id="054bd-115">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="054bd-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="054bd-116">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="054bd-116">Texture-Object Type</span></span>                    | <span data-ttu-id="054bd-117">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="054bd-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="054bd-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="054bd-118">Texture1D</span></span>                              | <span data-ttu-id="054bd-119">float</span><span class="sxs-lookup"><span data-stu-id="054bd-119">float</span></span>          |
| <span data-ttu-id="054bd-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="054bd-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="054bd-121">float2</span><span class="sxs-lookup"><span data-stu-id="054bd-121">float2</span></span>         |
| <span data-ttu-id="054bd-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="054bd-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="054bd-123">float3</span><span class="sxs-lookup"><span data-stu-id="054bd-123">float3</span></span>         |
| <span data-ttu-id="054bd-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="054bd-124">TextureCubeArray</span></span>                       | <span data-ttu-id="054bd-125">float4</span><span class="sxs-lookup"><span data-stu-id="054bd-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="054bd-126">*Biais* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="054bd-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="054bd-127">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="054bd-127">Type: **float**</span></span>

<span data-ttu-id="054bd-128">La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="054bd-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="054bd-129">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="054bd-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="054bd-130">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="054bd-130">Type: **int**</span></span>

<span data-ttu-id="054bd-131">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="054bd-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="054bd-132">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="054bd-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="054bd-133">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="054bd-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="054bd-134">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="054bd-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="054bd-135">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="054bd-135">Texture-Object Type</span></span>           | <span data-ttu-id="054bd-136">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="054bd-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="054bd-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="054bd-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="054bd-138">int</span><span class="sxs-lookup"><span data-stu-id="054bd-138">int</span></span>            |
| <span data-ttu-id="054bd-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="054bd-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="054bd-140">int2</span><span class="sxs-lookup"><span data-stu-id="054bd-140">int2</span></span>           |
| <span data-ttu-id="054bd-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="054bd-141">Texture3D</span></span>                     | <span data-ttu-id="054bd-142">int3</span><span class="sxs-lookup"><span data-stu-id="054bd-142">int3</span></span>           |
| <span data-ttu-id="054bd-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="054bd-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="054bd-144">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="054bd-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="054bd-145">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="054bd-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="054bd-146">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="054bd-146">Type: **float**</span></span>

<span data-ttu-id="054bd-147">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="054bd-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="054bd-148">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="054bd-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="054bd-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="054bd-149">Return value</span></span>

<span data-ttu-id="054bd-150">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="054bd-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="054bd-151">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="054bd-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="054bd-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="054bd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="054bd-153">Méthodes SampleBias</span><span class="sxs-lookup"><span data-stu-id="054bd-153">SampleBias methods</span></span>](texture2d-samplebias.md)
</dt> </dl>

 

 
