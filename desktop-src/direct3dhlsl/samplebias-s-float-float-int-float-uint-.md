---
title: 'Fonction SampleBias :: SampleBias (S, float, float, int, float, uint) pour Texture2D'
description: 'La fonction SampleBias :: SampleBias (S, float, float, int, float, uint) échantillonne un Texture2D, après avoir appliqué la valeur de biais au niveau du mipmap.'
ms.assetid: ACABF551-1DBF-4979-B0B1-D025E04EC08C
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
ms.openlocfilehash: 86840748d12a92eca24b8d0d2bfba26eee69cff5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982786"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture2d"></a><span data-ttu-id="f132f-104">Fonction SampleBias :: SampleBias (S, float, float, int, float, uint) pour Texture2D</span><span class="sxs-lookup"><span data-stu-id="f132f-104">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture2D</span></span>

<span data-ttu-id="f132f-105">Échantillonne un [**Texture2D**](sm5-object-texture2d.md), après avoir appliqué la valeur de biais au niveau du mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="f132f-105">Samples a [**Texture2D**](sm5-object-texture2d.md), after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="f132f-106">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f132f-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f132f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f132f-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f132f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f132f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f132f-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="f132f-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f132f-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="f132f-110">Type: **SamplerState**</span></span>

<span data-ttu-id="f132f-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f132f-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f132f-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="f132f-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f132f-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f132f-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f132f-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f132f-114">Type: **float**</span></span>

<span data-ttu-id="f132f-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="f132f-115">The texture coordinates.</span></span> <span data-ttu-id="f132f-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="f132f-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f132f-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f132f-117">Texture-Object Type</span></span>                    | <span data-ttu-id="f132f-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="f132f-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f132f-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f132f-119">Texture1D</span></span>                              | <span data-ttu-id="f132f-120">float</span><span class="sxs-lookup"><span data-stu-id="f132f-120">float</span></span>          |
| <span data-ttu-id="f132f-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f132f-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f132f-122">float2</span><span class="sxs-lookup"><span data-stu-id="f132f-122">float2</span></span>         |
| <span data-ttu-id="f132f-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="f132f-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f132f-124">float3</span><span class="sxs-lookup"><span data-stu-id="f132f-124">float3</span></span>         |
| <span data-ttu-id="f132f-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f132f-125">TextureCubeArray</span></span>                       | <span data-ttu-id="f132f-126">float4</span><span class="sxs-lookup"><span data-stu-id="f132f-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f132f-127">*Biais* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f132f-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f132f-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f132f-128">Type: **float**</span></span>

<span data-ttu-id="f132f-129">La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="f132f-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="f132f-130">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f132f-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f132f-131">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="f132f-131">Type: **int**</span></span>

<span data-ttu-id="f132f-132">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="f132f-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="f132f-133">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="f132f-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="f132f-134">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="f132f-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="f132f-135">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f132f-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="f132f-136">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f132f-136">Texture-Object Type</span></span>           | <span data-ttu-id="f132f-137">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="f132f-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="f132f-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f132f-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="f132f-139">int</span><span class="sxs-lookup"><span data-stu-id="f132f-139">int</span></span>            |
| <span data-ttu-id="f132f-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f132f-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="f132f-141">int2</span><span class="sxs-lookup"><span data-stu-id="f132f-141">int2</span></span>           |
| <span data-ttu-id="f132f-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f132f-142">Texture3D</span></span>                     | <span data-ttu-id="f132f-143">int3</span><span class="sxs-lookup"><span data-stu-id="f132f-143">int3</span></span>           |
| <span data-ttu-id="f132f-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f132f-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f132f-145">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="f132f-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f132f-146">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f132f-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f132f-147">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f132f-147">Type: **float**</span></span>

<span data-ttu-id="f132f-148">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="f132f-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f132f-149">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="f132f-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="f132f-150">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f132f-150">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f132f-151">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="f132f-151">Type: **uint**</span></span>

<span data-ttu-id="f132f-152">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f132f-152">The status of the operation.</span></span> <span data-ttu-id="f132f-153">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="f132f-153">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f132f-154">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="f132f-154">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f132f-155">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="f132f-155">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f132f-156">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f132f-156">Return value</span></span>

<span data-ttu-id="f132f-157">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f132f-157">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f132f-158">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f132f-158">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f132f-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f132f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f132f-160">Méthodes SampleBias</span><span class="sxs-lookup"><span data-stu-id="f132f-160">SampleBias methods</span></span>](texture2d-samplebias.md)
</dt> </dl>

 

 
