---
title: 'Fonction SampleBias :: SampleBias (S, float, float, int, float, uint) pour Texture3D'
description: 'Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. | Fonction SampleBias :: SampleBias (S, float, float, int, float, uint) pour Texture3D'
ms.assetid: 87B06414-F1A3-4BC8-B7DE-137B2156CFA7
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
ms.openlocfilehash: e6155bbd4a3b21b86add57d13bc14a1185c76b73
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982671"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture3d"></a><span data-ttu-id="af0a4-105">Fonction SampleBias :: SampleBias (S, float, float, int, float, uint) pour Texture3D</span><span class="sxs-lookup"><span data-stu-id="af0a4-105">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture3D</span></span>

<span data-ttu-id="af0a4-106">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="af0a4-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="af0a4-107">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="af0a4-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="af0a4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af0a4-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="af0a4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af0a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af0a4-110"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="af0a4-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af0a4-111">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="af0a4-111">Type: **SamplerState**</span></span>

<span data-ttu-id="af0a4-112">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="af0a4-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="af0a4-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="af0a4-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="af0a4-114">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af0a4-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af0a4-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="af0a4-115">Type: **float**</span></span>

<span data-ttu-id="af0a4-116">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="af0a4-116">The texture coordinates.</span></span> <span data-ttu-id="af0a4-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="af0a4-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="af0a4-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="af0a4-118">Texture-Object Type</span></span>                    | <span data-ttu-id="af0a4-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="af0a4-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="af0a4-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="af0a4-120">Texture1D</span></span>                              | <span data-ttu-id="af0a4-121">float</span><span class="sxs-lookup"><span data-stu-id="af0a4-121">float</span></span>          |
| <span data-ttu-id="af0a4-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="af0a4-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="af0a4-123">float2</span><span class="sxs-lookup"><span data-stu-id="af0a4-123">float2</span></span>         |
| <span data-ttu-id="af0a4-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="af0a4-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="af0a4-125">float3</span><span class="sxs-lookup"><span data-stu-id="af0a4-125">float3</span></span>         |
| <span data-ttu-id="af0a4-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="af0a4-126">TextureCubeArray</span></span>                       | <span data-ttu-id="af0a4-127">float4</span><span class="sxs-lookup"><span data-stu-id="af0a4-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="af0a4-128">*Biais* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af0a4-128">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af0a4-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="af0a4-129">Type: **float**</span></span>

<span data-ttu-id="af0a4-130">La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="af0a4-130">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="af0a4-131">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af0a4-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af0a4-132">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="af0a4-132">Type: **int**</span></span>

<span data-ttu-id="af0a4-133">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="af0a4-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="af0a4-134">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="af0a4-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="af0a4-135">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="af0a4-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="af0a4-136">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="af0a4-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="af0a4-137">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="af0a4-137">Texture-Object Type</span></span>           | <span data-ttu-id="af0a4-138">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="af0a4-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="af0a4-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="af0a4-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="af0a4-140">int</span><span class="sxs-lookup"><span data-stu-id="af0a4-140">int</span></span>            |
| <span data-ttu-id="af0a4-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="af0a4-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="af0a4-142">int2</span><span class="sxs-lookup"><span data-stu-id="af0a4-142">int2</span></span>           |
| <span data-ttu-id="af0a4-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="af0a4-143">Texture3D</span></span>                     | <span data-ttu-id="af0a4-144">int3</span><span class="sxs-lookup"><span data-stu-id="af0a4-144">int3</span></span>           |
| <span data-ttu-id="af0a4-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="af0a4-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="af0a4-146">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="af0a4-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="af0a4-147">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af0a4-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af0a4-148">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="af0a4-148">Type: **float**</span></span>

<span data-ttu-id="af0a4-149">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="af0a4-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="af0a4-150">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="af0a4-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="af0a4-151">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="af0a4-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af0a4-152">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="af0a4-152">Type: **uint**</span></span>

<span data-ttu-id="af0a4-153">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="af0a4-153">The status of the operation.</span></span> <span data-ttu-id="af0a4-154">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="af0a4-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="af0a4-155">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="af0a4-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="af0a4-156">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="af0a4-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af0a4-157">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af0a4-157">Return value</span></span>

<span data-ttu-id="af0a4-158">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="af0a4-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="af0a4-159">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="af0a4-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="af0a4-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af0a4-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af0a4-161">Méthodes SampleBias</span><span class="sxs-lookup"><span data-stu-id="af0a4-161">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="af0a4-162">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="af0a4-162">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
