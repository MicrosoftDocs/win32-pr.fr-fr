---
title: 'Fonction SampleCmp :: SampleCmp (S, float, float, int, float) Function) pour Texture2D'
description: Cette fonction échantillonne un Texture2D à l’aide d’une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer l’exemple de valeurs de niveau de détail (LOD) à.
ms.assetid: 1B5E6559-2524-4557-8F43-7AF258C39FB2
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
ms.openlocfilehash: 9df6a84fff7c6988ed9333584a7196fa06ad30ec
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982783"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2d"></a><span data-ttu-id="2708f-104">Fonction SampleCmp :: SampleCmp (S, float, float, int, float) pour Texture2D</span><span class="sxs-lookup"><span data-stu-id="2708f-104">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture2D</span></span>

<span data-ttu-id="2708f-105">Échantillonne un [**Texture2D**](sm5-object-texture2d.md), en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="2708f-105">Samples a [**Texture2D**](sm5-object-texture2d.md), using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="2708f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2708f-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="2708f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2708f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2708f-108"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="2708f-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2708f-109">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="2708f-109">Type: **SamplerState**</span></span>

<span data-ttu-id="2708f-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2708f-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="2708f-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="2708f-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="2708f-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2708f-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2708f-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="2708f-113">Type: **float**</span></span>

<span data-ttu-id="2708f-114">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="2708f-114">The texture coordinates.</span></span> <span data-ttu-id="2708f-115">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="2708f-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2708f-116">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2708f-116">Texture-Object Type</span></span>                    | <span data-ttu-id="2708f-117">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="2708f-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="2708f-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2708f-118">Texture1D</span></span>                              | <span data-ttu-id="2708f-119">float</span><span class="sxs-lookup"><span data-stu-id="2708f-119">float</span></span>          |
| <span data-ttu-id="2708f-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2708f-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="2708f-121">float2</span><span class="sxs-lookup"><span data-stu-id="2708f-121">float2</span></span>         |
| <span data-ttu-id="2708f-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="2708f-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="2708f-123">float3</span><span class="sxs-lookup"><span data-stu-id="2708f-123">float3</span></span>         |
| <span data-ttu-id="2708f-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2708f-124">TextureCubeArray</span></span>                       | <span data-ttu-id="2708f-125">float4</span><span class="sxs-lookup"><span data-stu-id="2708f-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="2708f-126">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2708f-126">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2708f-127">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="2708f-127">Type: **float**</span></span>

<span data-ttu-id="2708f-128">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="2708f-128">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="2708f-129">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2708f-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2708f-130">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="2708f-130">Type: **int**</span></span>

<span data-ttu-id="2708f-131">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="2708f-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="2708f-132">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="2708f-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="2708f-133">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="2708f-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="2708f-134">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2708f-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="2708f-135">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2708f-135">Texture-Object Type</span></span>           | <span data-ttu-id="2708f-136">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="2708f-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="2708f-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2708f-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="2708f-138">int</span><span class="sxs-lookup"><span data-stu-id="2708f-138">int</span></span>            |
| <span data-ttu-id="2708f-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2708f-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="2708f-140">int2</span><span class="sxs-lookup"><span data-stu-id="2708f-140">int2</span></span>           |
| <span data-ttu-id="2708f-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2708f-141">Texture3D</span></span>                     | <span data-ttu-id="2708f-142">int3</span><span class="sxs-lookup"><span data-stu-id="2708f-142">int3</span></span>           |
| <span data-ttu-id="2708f-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2708f-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2708f-144">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="2708f-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2708f-145">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2708f-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2708f-146">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="2708f-146">Type: **float**</span></span>

<span data-ttu-id="2708f-147">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="2708f-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="2708f-148">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="2708f-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2708f-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2708f-149">Return value</span></span>

<span data-ttu-id="2708f-150">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="2708f-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="2708f-151">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2708f-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="2708f-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2708f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2708f-153">Méthodes SampleCmp</span><span class="sxs-lookup"><span data-stu-id="2708f-153">SampleCmp methods</span></span>](texture2d-samplecmp.md)
</dt> </dl>

 

 
