---
title: 'Texture1DArray :: Sample (S, float, int, float, uint), fonction'
description: 'Échantillonne une texture avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération. | Texture1DArray :: Sample (S, float, int, float, uint), fonction'
ms.assetid: 584901B7-4F58-4491-9543-F27433386292
keywords:
- Exemple de fonction HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a2f608d7dbbd4eec51139b6f285529849f708af
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992105"
---
# <a name="texture1darraysamplesfloatintfloatuint-function"></a><span data-ttu-id="07d77-105">Texture1DArray :: Sample (S, float, int, float, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="07d77-105">Texture1DArray::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="07d77-106">Échantillonne une texture avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="07d77-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d77-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07d77-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="07d77-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07d77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d77-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="07d77-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d77-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="07d77-110">Type: **SamplerState**</span></span>

<span data-ttu-id="07d77-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="07d77-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="07d77-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="07d77-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="07d77-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="07d77-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d77-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="07d77-114">Type: **float**</span></span>

<span data-ttu-id="07d77-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="07d77-115">The texture coordinates.</span></span> <span data-ttu-id="07d77-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="07d77-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="07d77-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="07d77-117">Texture-Object Type</span></span>                    | <span data-ttu-id="07d77-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="07d77-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="07d77-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="07d77-119">Texture1D</span></span>                              | <span data-ttu-id="07d77-120">float</span><span class="sxs-lookup"><span data-stu-id="07d77-120">float</span></span>          |
| <span data-ttu-id="07d77-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="07d77-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="07d77-122">float2</span><span class="sxs-lookup"><span data-stu-id="07d77-122">float2</span></span>         |
| <span data-ttu-id="07d77-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="07d77-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="07d77-124">float3</span><span class="sxs-lookup"><span data-stu-id="07d77-124">float3</span></span>         |
| <span data-ttu-id="07d77-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="07d77-125">TextureCubeArray</span></span>                       | <span data-ttu-id="07d77-126">float4</span><span class="sxs-lookup"><span data-stu-id="07d77-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="07d77-127">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="07d77-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d77-128">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="07d77-128">Type: **int**</span></span>

<span data-ttu-id="07d77-129">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="07d77-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="07d77-130">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="07d77-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="07d77-131">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="07d77-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="07d77-132">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="07d77-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="07d77-133">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="07d77-133">Texture-Object Type</span></span>           | <span data-ttu-id="07d77-134">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="07d77-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="07d77-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="07d77-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="07d77-136">int</span><span class="sxs-lookup"><span data-stu-id="07d77-136">int</span></span>            |
| <span data-ttu-id="07d77-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="07d77-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="07d77-138">int2</span><span class="sxs-lookup"><span data-stu-id="07d77-138">int2</span></span>           |
| <span data-ttu-id="07d77-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="07d77-139">Texture3D</span></span>                     | <span data-ttu-id="07d77-140">int3</span><span class="sxs-lookup"><span data-stu-id="07d77-140">int3</span></span>           |
| <span data-ttu-id="07d77-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="07d77-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="07d77-142">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="07d77-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="07d77-143">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="07d77-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d77-144">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="07d77-144">Type: **float**</span></span>

<span data-ttu-id="07d77-145">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="07d77-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="07d77-146">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="07d77-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="07d77-147">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="07d77-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07d77-148">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="07d77-148">Type: **uint**</span></span>

<span data-ttu-id="07d77-149">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="07d77-149">The status of the operation.</span></span> <span data-ttu-id="07d77-150">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="07d77-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="07d77-151">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="07d77-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="07d77-152">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="07d77-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d77-153">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07d77-153">Return value</span></span>

<span data-ttu-id="07d77-154">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="07d77-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="07d77-155">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="07d77-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="07d77-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07d77-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d77-157">Exemples de méthodes</span><span class="sxs-lookup"><span data-stu-id="07d77-157">Sample methods</span></span>](texture1darray-sample.md)
</dt> </dl>

 

 
