---
title: 'Fonction SampleCmp :: SampleCmp (S, float, float, int, float) pour Texture2DArray'
description: Découvrez comment cette fonction échantillonne une texture à l’aide d’une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à. Pour Texture2DArray.
ms.assetid: 6455BF80-2A22-43BB-80A2-61FBEC66C348
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
ms.openlocfilehash: 0692166766b9f52a1b6b13719c2427438b59835f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762428"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2darray"></a><span data-ttu-id="4c748-105">Fonction SampleCmp :: SampleCmp (S, float, float, int, float) pour Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4c748-105">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture2DArray</span></span>

<span data-ttu-id="4c748-106">Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="4c748-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c748-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c748-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="4c748-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c748-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c748-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="4c748-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c748-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="4c748-110">Type: **SamplerState**</span></span>

<span data-ttu-id="4c748-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="4c748-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="4c748-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="4c748-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="4c748-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c748-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c748-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="4c748-114">Type: **float**</span></span>

<span data-ttu-id="4c748-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="4c748-115">The texture coordinates.</span></span> <span data-ttu-id="4c748-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="4c748-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4c748-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4c748-117">Texture-Object Type</span></span>                    | <span data-ttu-id="4c748-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="4c748-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="4c748-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4c748-119">Texture1D</span></span>                              | <span data-ttu-id="4c748-120">float</span><span class="sxs-lookup"><span data-stu-id="4c748-120">float</span></span>          |
| <span data-ttu-id="4c748-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="4c748-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="4c748-122">float2</span><span class="sxs-lookup"><span data-stu-id="4c748-122">float2</span></span>         |
| <span data-ttu-id="4c748-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="4c748-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="4c748-124">float3</span><span class="sxs-lookup"><span data-stu-id="4c748-124">float3</span></span>         |
| <span data-ttu-id="4c748-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4c748-125">TextureCubeArray</span></span>                       | <span data-ttu-id="4c748-126">float4</span><span class="sxs-lookup"><span data-stu-id="4c748-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="4c748-127">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c748-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c748-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="4c748-128">Type: **float**</span></span>

<span data-ttu-id="4c748-129">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="4c748-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="4c748-130">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c748-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c748-131">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="4c748-131">Type: **int**</span></span>

<span data-ttu-id="4c748-132">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="4c748-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="4c748-133">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="4c748-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="4c748-134">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="4c748-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="4c748-135">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4c748-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="4c748-136">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4c748-136">Texture-Object Type</span></span>           | <span data-ttu-id="4c748-137">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="4c748-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="4c748-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4c748-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="4c748-139">int</span><span class="sxs-lookup"><span data-stu-id="4c748-139">int</span></span>            |
| <span data-ttu-id="4c748-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4c748-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="4c748-141">int2</span><span class="sxs-lookup"><span data-stu-id="4c748-141">int2</span></span>           |
| <span data-ttu-id="4c748-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4c748-142">Texture3D</span></span>                     | <span data-ttu-id="4c748-143">int3</span><span class="sxs-lookup"><span data-stu-id="4c748-143">int3</span></span>           |
| <span data-ttu-id="4c748-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4c748-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="4c748-145">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c748-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4c748-146">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c748-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c748-147">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="4c748-147">Type: **float**</span></span>

<span data-ttu-id="4c748-148">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="4c748-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="4c748-149">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="4c748-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c748-150">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c748-150">Return value</span></span>

<span data-ttu-id="4c748-151">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="4c748-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="4c748-152">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="4c748-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="4c748-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c748-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c748-154">Méthodes SampleCmp</span><span class="sxs-lookup"><span data-stu-id="4c748-154">SampleCmp methods</span></span>](texture2darray-samplecmp.md)
</dt> </dl>

 

 
