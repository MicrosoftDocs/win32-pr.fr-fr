---
title: 'Fonction SampleCmp :: SampleCmp (S, float, float, int, float, uint) pour Texture2DArray'
description: Cette fonction échantillonne une texture à l’aide d’une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. Pour Texture2DArray.
ms.assetid: 847A6B79-3A66-4209-AB01-7C1FDA8A433A
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
ms.openlocfilehash: cc8957ca2f6c1eb3e4a665b5d6df134c854ccc3c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104211983"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture2darray"></a><span data-ttu-id="a8a15-105">Fonction SampleCmp :: SampleCmp (S, float, float, int, float, uint) pour Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a8a15-105">SampleCmp::SampleCmp(S,float,float,int,float,uint) function for Texture2DArray</span></span>

<span data-ttu-id="a8a15-106">Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="a8a15-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="a8a15-107">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a8a15-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8a15-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8a15-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="a8a15-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8a15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8a15-110"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="a8a15-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8a15-111">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="a8a15-111">Type: **SamplerState**</span></span>

<span data-ttu-id="a8a15-112">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a8a15-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a8a15-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="a8a15-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a8a15-114">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a8a15-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8a15-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a8a15-115">Type: **float**</span></span>

<span data-ttu-id="a8a15-116">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="a8a15-116">The texture coordinates.</span></span> <span data-ttu-id="a8a15-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="a8a15-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a8a15-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a8a15-118">Texture-Object Type</span></span>                    | <span data-ttu-id="a8a15-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="a8a15-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a8a15-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a8a15-120">Texture1D</span></span>                              | <span data-ttu-id="a8a15-121">float</span><span class="sxs-lookup"><span data-stu-id="a8a15-121">float</span></span>          |
| <span data-ttu-id="a8a15-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a8a15-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a8a15-123">float2</span><span class="sxs-lookup"><span data-stu-id="a8a15-123">float2</span></span>         |
| <span data-ttu-id="a8a15-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="a8a15-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a8a15-125">float3</span><span class="sxs-lookup"><span data-stu-id="a8a15-125">float3</span></span>         |
| <span data-ttu-id="a8a15-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a8a15-126">TextureCubeArray</span></span>                       | <span data-ttu-id="a8a15-127">float4</span><span class="sxs-lookup"><span data-stu-id="a8a15-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a8a15-128">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a8a15-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8a15-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a8a15-129">Type: **float**</span></span>

<span data-ttu-id="a8a15-130">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="a8a15-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="a8a15-131">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a8a15-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8a15-132">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="a8a15-132">Type: **int**</span></span>

<span data-ttu-id="a8a15-133">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="a8a15-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="a8a15-134">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="a8a15-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="a8a15-135">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="a8a15-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="a8a15-136">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a8a15-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="a8a15-137">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a8a15-137">Texture-Object Type</span></span>           | <span data-ttu-id="a8a15-138">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="a8a15-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="a8a15-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a8a15-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="a8a15-140">int</span><span class="sxs-lookup"><span data-stu-id="a8a15-140">int</span></span>            |
| <span data-ttu-id="a8a15-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a8a15-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="a8a15-142">int2</span><span class="sxs-lookup"><span data-stu-id="a8a15-142">int2</span></span>           |
| <span data-ttu-id="a8a15-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a8a15-143">Texture3D</span></span>                     | <span data-ttu-id="a8a15-144">int3</span><span class="sxs-lookup"><span data-stu-id="a8a15-144">int3</span></span>           |
| <span data-ttu-id="a8a15-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="a8a15-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a8a15-146">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8a15-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a8a15-147">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a8a15-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8a15-148">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a8a15-148">Type: **float**</span></span>

<span data-ttu-id="a8a15-149">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="a8a15-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a8a15-150">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="a8a15-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="a8a15-151">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a8a15-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8a15-152">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="a8a15-152">Type: **uint**</span></span>

<span data-ttu-id="a8a15-153">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a8a15-153">The status of the operation.</span></span> <span data-ttu-id="a8a15-154">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a8a15-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a8a15-155">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a8a15-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a8a15-156">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="a8a15-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8a15-157">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8a15-157">Return value</span></span>

<span data-ttu-id="a8a15-158">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a8a15-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="a8a15-159">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="a8a15-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a8a15-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8a15-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a15-161">Méthodes SampleCmp</span><span class="sxs-lookup"><span data-stu-id="a8a15-161">SampleCmp methods</span></span>](texture2darray-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="a8a15-162">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="a8a15-162">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
