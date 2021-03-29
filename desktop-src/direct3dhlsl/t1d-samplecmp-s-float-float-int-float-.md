---
title: 'Fonction SampleCmp :: SampleCmp (S, float, float, int, float) pour Texture1D'
description: 'Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à. | Fonction SampleCmp :: SampleCmp (S, float, float, int, float) pour Texture1D'
ms.assetid: 91AD0B59-D3F0-4A0D-8825-17282815D64B
keywords:
- SampleCmp fonction HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 811636e7e7002afedf026d4e3955f08f647c2c5d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996384"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="76526-105">Fonction SampleCmp :: SampleCmp (S, float, float, int, float) pour Texture1D</span><span class="sxs-lookup"><span data-stu-id="76526-105">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="76526-106">Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="76526-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="76526-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76526-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="76526-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76526-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76526-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="76526-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76526-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="76526-110">Type: **SamplerState**</span></span>

<span data-ttu-id="76526-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="76526-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="76526-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="76526-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="76526-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76526-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76526-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="76526-114">Type: **float**</span></span>

<span data-ttu-id="76526-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="76526-115">The texture coordinates.</span></span> <span data-ttu-id="76526-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="76526-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="76526-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="76526-117">Texture-Object Type</span></span>                    | <span data-ttu-id="76526-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="76526-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="76526-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="76526-119">Texture1D</span></span>                              | <span data-ttu-id="76526-120">float</span><span class="sxs-lookup"><span data-stu-id="76526-120">float</span></span>          |
| <span data-ttu-id="76526-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="76526-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="76526-122">float2</span><span class="sxs-lookup"><span data-stu-id="76526-122">float2</span></span>         |
| <span data-ttu-id="76526-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="76526-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="76526-124">float3</span><span class="sxs-lookup"><span data-stu-id="76526-124">float3</span></span>         |
| <span data-ttu-id="76526-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="76526-125">TextureCubeArray</span></span>                       | <span data-ttu-id="76526-126">float4</span><span class="sxs-lookup"><span data-stu-id="76526-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="76526-127">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76526-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76526-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="76526-128">Type: **float**</span></span>

<span data-ttu-id="76526-129">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="76526-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="76526-130">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76526-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76526-131">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="76526-131">Type: **int**</span></span>

<span data-ttu-id="76526-132">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="76526-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="76526-133">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="76526-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="76526-134">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="76526-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="76526-135">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="76526-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="76526-136">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="76526-136">Texture-Object Type</span></span>           | <span data-ttu-id="76526-137">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="76526-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="76526-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="76526-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="76526-139">int</span><span class="sxs-lookup"><span data-stu-id="76526-139">int</span></span>            |
| <span data-ttu-id="76526-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="76526-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="76526-141">int2</span><span class="sxs-lookup"><span data-stu-id="76526-141">int2</span></span>           |
| <span data-ttu-id="76526-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="76526-142">Texture3D</span></span>                     | <span data-ttu-id="76526-143">int3</span><span class="sxs-lookup"><span data-stu-id="76526-143">int3</span></span>           |
| <span data-ttu-id="76526-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="76526-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="76526-145">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="76526-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="76526-146">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76526-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76526-147">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="76526-147">Type: **float**</span></span>

<span data-ttu-id="76526-148">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="76526-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="76526-149">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="76526-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76526-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76526-150">Return value</span></span>

<span data-ttu-id="76526-151">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="76526-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="76526-152">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="76526-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="76526-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76526-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76526-154">Méthodes SampleCmp</span><span class="sxs-lookup"><span data-stu-id="76526-154">SampleCmp methods</span></span>](texture1d-samplecmp.md)
</dt> </dl>

 

 
