---
title: 'Fonction SampleCmp :: SampleCmp (S, float, float, int, float, uint) pour Texture2D'
description: Découvrez comment cette fonction échantillonne un Texture2D, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer l’exemple de valeurs de niveau de détail (LOD) à. Retourne l’état de l’opération.
ms.assetid: 039EA69B-DFE0-4351-963A-C0326FDEF844
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
ms.openlocfilehash: 4b4667594a4b4eeaf9e533338411b79810fee5eb
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982778"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture2d"></a><span data-ttu-id="e9413-105">Fonction SampleCmp :: SampleCmp (S, float, float, int, float, uint) pour Texture2D</span><span class="sxs-lookup"><span data-stu-id="e9413-105">SampleCmp::SampleCmp(S,float,float,int,float,uint) function for Texture2D</span></span>

<span data-ttu-id="e9413-106">Échantillonne un [**Texture2D**](sm5-object-texture2d.md), en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="e9413-106">Samples a [**Texture2D**](sm5-object-texture2d.md), using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="e9413-107">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e9413-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9413-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9413-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="e9413-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9413-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9413-110"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="e9413-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9413-111">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="e9413-111">Type: **SamplerState**</span></span>

<span data-ttu-id="e9413-112">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="e9413-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e9413-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="e9413-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e9413-114">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9413-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9413-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="e9413-115">Type: **float**</span></span>

<span data-ttu-id="e9413-116">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="e9413-116">The texture coordinates.</span></span> <span data-ttu-id="e9413-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="e9413-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e9413-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e9413-118">Texture-Object Type</span></span>                    | <span data-ttu-id="e9413-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="e9413-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e9413-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e9413-120">Texture1D</span></span>                              | <span data-ttu-id="e9413-121">float</span><span class="sxs-lookup"><span data-stu-id="e9413-121">float</span></span>          |
| <span data-ttu-id="e9413-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e9413-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e9413-123">float2</span><span class="sxs-lookup"><span data-stu-id="e9413-123">float2</span></span>         |
| <span data-ttu-id="e9413-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e9413-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e9413-125">float3</span><span class="sxs-lookup"><span data-stu-id="e9413-125">float3</span></span>         |
| <span data-ttu-id="e9413-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e9413-126">TextureCubeArray</span></span>                       | <span data-ttu-id="e9413-127">float4</span><span class="sxs-lookup"><span data-stu-id="e9413-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e9413-128">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9413-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9413-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="e9413-129">Type: **float**</span></span>

<span data-ttu-id="e9413-130">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="e9413-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="e9413-131">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9413-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9413-132">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="e9413-132">Type: **int**</span></span>

<span data-ttu-id="e9413-133">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="e9413-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="e9413-134">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="e9413-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="e9413-135">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="e9413-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="e9413-136">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e9413-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="e9413-137">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e9413-137">Texture-Object Type</span></span>           | <span data-ttu-id="e9413-138">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="e9413-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="e9413-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e9413-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="e9413-140">int</span><span class="sxs-lookup"><span data-stu-id="e9413-140">int</span></span>            |
| <span data-ttu-id="e9413-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e9413-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="e9413-142">int2</span><span class="sxs-lookup"><span data-stu-id="e9413-142">int2</span></span>           |
| <span data-ttu-id="e9413-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e9413-143">Texture3D</span></span>                     | <span data-ttu-id="e9413-144">int3</span><span class="sxs-lookup"><span data-stu-id="e9413-144">int3</span></span>           |
| <span data-ttu-id="e9413-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e9413-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e9413-146">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9413-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e9413-147">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9413-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9413-148">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="e9413-148">Type: **float**</span></span>

<span data-ttu-id="e9413-149">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="e9413-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e9413-150">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="e9413-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="e9413-151">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e9413-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9413-152">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="e9413-152">Type: **uint**</span></span>

<span data-ttu-id="e9413-153">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e9413-153">The status of the operation.</span></span> <span data-ttu-id="e9413-154">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e9413-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e9413-155">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e9413-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e9413-156">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="e9413-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9413-157">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9413-157">Return value</span></span>

<span data-ttu-id="e9413-158">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e9413-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e9413-159">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e9413-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e9413-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9413-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9413-161">Méthodes SampleCmp</span><span class="sxs-lookup"><span data-stu-id="e9413-161">SampleCmp methods</span></span>](texture2d-samplecmp.md)
</dt> </dl>

 

 
