---
title: 'Fonction SampleLevel :: SampleLevel (S, float, float, int, uint) pour Texture2D'
description: Échantillonne un Texture2D sur le niveau de mipmap spécifié et retourne l’état de l’opération.
ms.assetid: B021D42E-9F63-4CCE-939B-F93D91F7CB80
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
ms.openlocfilehash: 1455454649e24bd984948a81837181a7bcdba11a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996408"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2d"></a><span data-ttu-id="043a0-104">Fonction SampleLevel :: SampleLevel (S, float, float, int, uint) pour Texture2D</span><span class="sxs-lookup"><span data-stu-id="043a0-104">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture2D</span></span>

<span data-ttu-id="043a0-105">Échantillonne un [**Texture2D**](sm5-object-texture2d.md) sur le niveau de mipmap spécifié et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="043a0-105">Samples a [**Texture2D**](sm5-object-texture2d.md) on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="043a0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="043a0-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="043a0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="043a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="043a0-108"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="043a0-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="043a0-109">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="043a0-109">Type: **SamplerState**</span></span>

<span data-ttu-id="043a0-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="043a0-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="043a0-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="043a0-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="043a0-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="043a0-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="043a0-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="043a0-113">Type: **float**</span></span>

<span data-ttu-id="043a0-114">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="043a0-114">The texture coordinates.</span></span> <span data-ttu-id="043a0-115">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="043a0-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="043a0-116">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="043a0-116">Texture-Object Type</span></span>                    | <span data-ttu-id="043a0-117">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="043a0-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="043a0-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="043a0-118">Texture1D</span></span>                              | <span data-ttu-id="043a0-119">float</span><span class="sxs-lookup"><span data-stu-id="043a0-119">float</span></span>          |
| <span data-ttu-id="043a0-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="043a0-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="043a0-121">float2</span><span class="sxs-lookup"><span data-stu-id="043a0-121">float2</span></span>         |
| <span data-ttu-id="043a0-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="043a0-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="043a0-123">float3</span><span class="sxs-lookup"><span data-stu-id="043a0-123">float3</span></span>         |
| <span data-ttu-id="043a0-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="043a0-124">TextureCubeArray</span></span>                       | <span data-ttu-id="043a0-125">float4</span><span class="sxs-lookup"><span data-stu-id="043a0-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="043a0-126">*LOD* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="043a0-126">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="043a0-127">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="043a0-127">Type: **float**</span></span>

<span data-ttu-id="043a0-128">\[dans \] un nombre qui spécifie le niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="043a0-128">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="043a0-129">Si la valeur est ≤ 0, le mipmap niveau 0 (mappage le plus grand) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="043a0-129">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="043a0-130">La valeur fractionnaire (si fournie) est utilisée pour interpoler entre deux niveaux de mipmap.</span><span class="sxs-lookup"><span data-stu-id="043a0-130">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="043a0-131">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="043a0-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="043a0-132">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="043a0-132">Type: **int**</span></span>

<span data-ttu-id="043a0-133">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="043a0-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="043a0-134">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="043a0-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="043a0-135">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="043a0-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="043a0-136">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="043a0-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="043a0-137">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="043a0-137">Texture-Object Type</span></span>           | <span data-ttu-id="043a0-138">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="043a0-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="043a0-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="043a0-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="043a0-140">int</span><span class="sxs-lookup"><span data-stu-id="043a0-140">int</span></span>            |
| <span data-ttu-id="043a0-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="043a0-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="043a0-142">int2</span><span class="sxs-lookup"><span data-stu-id="043a0-142">int2</span></span>           |
| <span data-ttu-id="043a0-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="043a0-143">Texture3D</span></span>                     | <span data-ttu-id="043a0-144">int3</span><span class="sxs-lookup"><span data-stu-id="043a0-144">int3</span></span>           |
| <span data-ttu-id="043a0-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="043a0-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="043a0-146">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="043a0-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="043a0-147">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="043a0-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="043a0-148">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="043a0-148">Type: **uint**</span></span>

<span data-ttu-id="043a0-149">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="043a0-149">The status of the operation.</span></span> <span data-ttu-id="043a0-150">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="043a0-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="043a0-151">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="043a0-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="043a0-152">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="043a0-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="043a0-153">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="043a0-153">Return value</span></span>

<span data-ttu-id="043a0-154">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="043a0-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="043a0-155">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="043a0-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="043a0-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="043a0-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="043a0-157">Méthodes SampleLevel</span><span class="sxs-lookup"><span data-stu-id="043a0-157">SampleLevel methods</span></span>](texture2d-samplelevel.md)
</dt> </dl>

 

 
