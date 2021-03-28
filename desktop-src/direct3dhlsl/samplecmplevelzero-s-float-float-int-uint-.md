---
title: 'Fonction SampleCmpLevelZero :: SampleCmpLevelZero (S, float, float, int, uint) pour Texture2D'
description: Échantillonne un Texture2D sur le niveau de mipmap 0 uniquement et compare le résultat à une valeur de comparaison, puis retourne l’état de l’opération. Pour Texture2D.
ms.assetid: AEFE424F-2C77-434C-B9C0-8173778CB108
keywords:
- SampleCmpLevelZero fonction HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a28dddeb687093a76f4f8bc60c96777468abc9f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996421"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatintuint-function-for-texture2d"></a><span data-ttu-id="7c291-105">Fonction SampleCmpLevelZero :: SampleCmpLevelZero (S, float, float, int, uint) pour Texture2D</span><span class="sxs-lookup"><span data-stu-id="7c291-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) function for Texture2D</span></span>

<span data-ttu-id="7c291-106">Échantillonne un [**Texture2D**](sm5-object-texture2d.md) sur le niveau de mipmap 0 uniquement et compare le résultat à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="7c291-106">Samples a [**Texture2D**](sm5-object-texture2d.md) on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="7c291-107">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7c291-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c291-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c291-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="7c291-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c291-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c291-110"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="7c291-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c291-111">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="7c291-111">Type: **SamplerState**</span></span>

<span data-ttu-id="7c291-112">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="7c291-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="7c291-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="7c291-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="7c291-114">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7c291-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c291-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="7c291-115">Type: **float**</span></span>

<span data-ttu-id="7c291-116">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="7c291-116">The texture coordinates.</span></span> <span data-ttu-id="7c291-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="7c291-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="7c291-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="7c291-118">Texture-Object Type</span></span>                    | <span data-ttu-id="7c291-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="7c291-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="7c291-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7c291-120">Texture1D</span></span>                              | <span data-ttu-id="7c291-121">float</span><span class="sxs-lookup"><span data-stu-id="7c291-121">float</span></span>          |
| <span data-ttu-id="7c291-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="7c291-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="7c291-123">float2</span><span class="sxs-lookup"><span data-stu-id="7c291-123">float2</span></span>         |
| <span data-ttu-id="7c291-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="7c291-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="7c291-125">float3</span><span class="sxs-lookup"><span data-stu-id="7c291-125">float3</span></span>         |
| <span data-ttu-id="7c291-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="7c291-126">TextureCubeArray</span></span>                       | <span data-ttu-id="7c291-127">float4</span><span class="sxs-lookup"><span data-stu-id="7c291-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="7c291-128">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7c291-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c291-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="7c291-129">Type: **float**</span></span>

<span data-ttu-id="7c291-130">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="7c291-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="7c291-131">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7c291-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c291-132">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="7c291-132">Type: **int**</span></span>

<span data-ttu-id="7c291-133">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="7c291-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="7c291-134">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="7c291-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="7c291-135">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="7c291-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="7c291-136">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="7c291-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="7c291-137">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="7c291-137">Texture-Object Type</span></span>           | <span data-ttu-id="7c291-138">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="7c291-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="7c291-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="7c291-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="7c291-140">int</span><span class="sxs-lookup"><span data-stu-id="7c291-140">int</span></span>            |
| <span data-ttu-id="7c291-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="7c291-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="7c291-142">int2</span><span class="sxs-lookup"><span data-stu-id="7c291-142">int2</span></span>           |
| <span data-ttu-id="7c291-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="7c291-143">Texture3D</span></span>                     | <span data-ttu-id="7c291-144">int3</span><span class="sxs-lookup"><span data-stu-id="7c291-144">int3</span></span>           |
| <span data-ttu-id="7c291-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="7c291-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="7c291-146">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c291-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="7c291-147">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7c291-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c291-148">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="7c291-148">Type: **uint**</span></span>

<span data-ttu-id="7c291-149">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7c291-149">The status of the operation.</span></span> <span data-ttu-id="7c291-150">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="7c291-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="7c291-151">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="7c291-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="7c291-152">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="7c291-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c291-153">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c291-153">Return value</span></span>

<span data-ttu-id="7c291-154">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="7c291-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="7c291-155">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="7c291-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="7c291-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c291-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c291-157">Méthodes SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="7c291-157">SampleCmpLevelZero methods</span></span>](texture2d-samplecmplevelzero.md)
</dt> </dl>

 

 
