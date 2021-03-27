---
title: 'Fonction SampleLevel :: SampleLevel (S, float, float, int, uint) pour Texture1D'
description: 'Échantillonne une texture sur le niveau de mipmap spécifié et retourne l’état de l’opération. Pour Texture1D. | SampleLevel :: SampleLevel (S, float, float, int, uint) (fonction)'
ms.assetid: B797C7F9-7436-4DD5-9CAB-EFF81D410174
keywords:
- SampleLevel fonction HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6d0c74bd59c8e693b009e9d53a766f339a20a2d6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996440"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture1d"></a><span data-ttu-id="18dc2-106">Fonction SampleLevel :: SampleLevel (S, float, float, int, uint) pour Texture1D</span><span class="sxs-lookup"><span data-stu-id="18dc2-106">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture1D</span></span>

<span data-ttu-id="18dc2-107">Échantillonne une texture sur le niveau de mipmap spécifié et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="18dc2-107">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="18dc2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18dc2-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="18dc2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18dc2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18dc2-110"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="18dc2-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18dc2-111">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="18dc2-111">Type: **SamplerState**</span></span>

<span data-ttu-id="18dc2-112">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="18dc2-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="18dc2-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="18dc2-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="18dc2-114">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18dc2-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18dc2-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="18dc2-115">Type: **float**</span></span>

<span data-ttu-id="18dc2-116">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="18dc2-116">The texture coordinates.</span></span> <span data-ttu-id="18dc2-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="18dc2-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="18dc2-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="18dc2-118">Texture-Object Type</span></span>                    | <span data-ttu-id="18dc2-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="18dc2-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="18dc2-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="18dc2-120">Texture1D</span></span>                              | <span data-ttu-id="18dc2-121">float</span><span class="sxs-lookup"><span data-stu-id="18dc2-121">float</span></span>          |
| <span data-ttu-id="18dc2-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="18dc2-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="18dc2-123">float2</span><span class="sxs-lookup"><span data-stu-id="18dc2-123">float2</span></span>         |
| <span data-ttu-id="18dc2-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="18dc2-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="18dc2-125">float3</span><span class="sxs-lookup"><span data-stu-id="18dc2-125">float3</span></span>         |
| <span data-ttu-id="18dc2-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="18dc2-126">TextureCubeArray</span></span>                       | <span data-ttu-id="18dc2-127">float4</span><span class="sxs-lookup"><span data-stu-id="18dc2-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="18dc2-128">*LOD* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18dc2-128">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18dc2-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="18dc2-129">Type: **float**</span></span>

<span data-ttu-id="18dc2-130">\[dans \] un nombre qui spécifie le niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="18dc2-130">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="18dc2-131">Si la valeur est ≤ 0, le mipmap niveau 0 (mappage le plus grand) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="18dc2-131">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="18dc2-132">La valeur fractionnaire (si fournie) est utilisée pour interpoler entre deux niveaux de mipmap.</span><span class="sxs-lookup"><span data-stu-id="18dc2-132">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="18dc2-133">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18dc2-133">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18dc2-134">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="18dc2-134">Type: **int**</span></span>

<span data-ttu-id="18dc2-135">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="18dc2-135">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="18dc2-136">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="18dc2-136">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="18dc2-137">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="18dc2-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="18dc2-138">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="18dc2-138">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="18dc2-139">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="18dc2-139">Texture-Object Type</span></span>           | <span data-ttu-id="18dc2-140">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="18dc2-140">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="18dc2-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="18dc2-141">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="18dc2-142">int</span><span class="sxs-lookup"><span data-stu-id="18dc2-142">int</span></span>            |
| <span data-ttu-id="18dc2-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="18dc2-143">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="18dc2-144">int2</span><span class="sxs-lookup"><span data-stu-id="18dc2-144">int2</span></span>           |
| <span data-ttu-id="18dc2-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="18dc2-145">Texture3D</span></span>                     | <span data-ttu-id="18dc2-146">int3</span><span class="sxs-lookup"><span data-stu-id="18dc2-146">int3</span></span>           |
| <span data-ttu-id="18dc2-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="18dc2-147">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="18dc2-148">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="18dc2-148">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="18dc2-149">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="18dc2-149">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18dc2-150">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="18dc2-150">Type: **uint**</span></span>

<span data-ttu-id="18dc2-151">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="18dc2-151">The status of the operation.</span></span> <span data-ttu-id="18dc2-152">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="18dc2-152">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="18dc2-153">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="18dc2-153">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="18dc2-154">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="18dc2-154">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18dc2-155">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18dc2-155">Return value</span></span>

<span data-ttu-id="18dc2-156">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="18dc2-156">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="18dc2-157">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="18dc2-157">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="18dc2-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18dc2-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18dc2-159">Méthodes SampleLevel</span><span class="sxs-lookup"><span data-stu-id="18dc2-159">SampleLevel methods</span></span>](texture1d-samplelevel.md)
</dt> </dl>

 

 
