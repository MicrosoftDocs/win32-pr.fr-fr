---
title: 'Fonction SampleCmpLevelZero :: SampleCmpLevelZero (S, float, float, int, uint) pour Texture1D'
description: Échantillonne une texture sur le niveau de mipmap 0 uniquement et compare le résultat à une valeur de comparaison, puis retourne l’état de l’opération. Pour Texture1D.
ms.assetid: A2F7FD4A-49D8-41B3-A5AF-7B54A8B5266C
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
ms.openlocfilehash: a63644cff0bcc5a437ff4ae3e1dffba8f5a0676c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104211985"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatintuint-function-for-texture1d"></a><span data-ttu-id="acaa9-105">Fonction SampleCmpLevelZero :: SampleCmpLevelZero (S, float, float, int, uint) pour Texture1D</span><span class="sxs-lookup"><span data-stu-id="acaa9-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) function for Texture1D</span></span>

<span data-ttu-id="acaa9-106">Échantillonne une texture sur le niveau de mipmap 0 uniquement et compare le résultat à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="acaa9-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="acaa9-107">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="acaa9-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="acaa9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acaa9-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="acaa9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acaa9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acaa9-110"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="acaa9-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acaa9-111">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="acaa9-111">Type: **SamplerState**</span></span>

<span data-ttu-id="acaa9-112">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="acaa9-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="acaa9-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="acaa9-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="acaa9-114">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acaa9-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acaa9-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="acaa9-115">Type: **float**</span></span>

<span data-ttu-id="acaa9-116">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="acaa9-116">The texture coordinates.</span></span> <span data-ttu-id="acaa9-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="acaa9-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="acaa9-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="acaa9-118">Texture-Object Type</span></span>                    | <span data-ttu-id="acaa9-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="acaa9-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="acaa9-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="acaa9-120">Texture1D</span></span>                              | <span data-ttu-id="acaa9-121">float</span><span class="sxs-lookup"><span data-stu-id="acaa9-121">float</span></span>          |
| <span data-ttu-id="acaa9-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="acaa9-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="acaa9-123">float2</span><span class="sxs-lookup"><span data-stu-id="acaa9-123">float2</span></span>         |
| <span data-ttu-id="acaa9-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="acaa9-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="acaa9-125">float3</span><span class="sxs-lookup"><span data-stu-id="acaa9-125">float3</span></span>         |
| <span data-ttu-id="acaa9-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="acaa9-126">TextureCubeArray</span></span>                       | <span data-ttu-id="acaa9-127">float4</span><span class="sxs-lookup"><span data-stu-id="acaa9-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="acaa9-128">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acaa9-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acaa9-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="acaa9-129">Type: **float**</span></span>

<span data-ttu-id="acaa9-130">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="acaa9-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="acaa9-131">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acaa9-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acaa9-132">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="acaa9-132">Type: **int**</span></span>

<span data-ttu-id="acaa9-133">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="acaa9-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="acaa9-134">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="acaa9-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="acaa9-135">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="acaa9-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="acaa9-136">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="acaa9-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="acaa9-137">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="acaa9-137">Texture-Object Type</span></span>           | <span data-ttu-id="acaa9-138">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="acaa9-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="acaa9-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="acaa9-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="acaa9-140">int</span><span class="sxs-lookup"><span data-stu-id="acaa9-140">int</span></span>            |
| <span data-ttu-id="acaa9-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="acaa9-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="acaa9-142">int2</span><span class="sxs-lookup"><span data-stu-id="acaa9-142">int2</span></span>           |
| <span data-ttu-id="acaa9-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="acaa9-143">Texture3D</span></span>                     | <span data-ttu-id="acaa9-144">int3</span><span class="sxs-lookup"><span data-stu-id="acaa9-144">int3</span></span>           |
| <span data-ttu-id="acaa9-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="acaa9-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="acaa9-146">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="acaa9-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="acaa9-147">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="acaa9-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acaa9-148">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="acaa9-148">Type: **uint**</span></span>

<span data-ttu-id="acaa9-149">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="acaa9-149">The status of the operation.</span></span> <span data-ttu-id="acaa9-150">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="acaa9-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="acaa9-151">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="acaa9-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="acaa9-152">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="acaa9-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acaa9-153">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acaa9-153">Return value</span></span>

<span data-ttu-id="acaa9-154">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="acaa9-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="acaa9-155">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="acaa9-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="acaa9-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acaa9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acaa9-157">Méthodes SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="acaa9-157">SampleCmpLevelZero methods</span></span>](texture1d-samplecmplevelzero.md)
</dt> </dl>

 

 
