---
title: 'Texture1DArray :: Sample (S, float, int, float), fonction'
description: 'Échantillonne une texture avec une valeur facultative pour fixer l’exemple de valeurs de niveau de détail (LOD) à. | Texture1DArray :: Sample (S, float, int, float), fonction'
ms.assetid: 3A965EEE-FCA3-4DD8-87D2-56679DFF5D3A
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
ms.openlocfilehash: 16d0a651d70aa618b9791fb760c51dfa05945752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992053"
---
# <a name="texture1darraysamplesfloatintfloat-function"></a><span data-ttu-id="e7f94-105">Texture1DArray :: Sample (S, float, int, float), fonction</span><span class="sxs-lookup"><span data-stu-id="e7f94-105">Texture1DArray::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="e7f94-106">Échantillonne une texture avec une valeur facultative pour fixer l’exemple de valeurs de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="e7f94-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f94-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7f94-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="e7f94-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7f94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7f94-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f94-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f94-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="e7f94-110">Type: **SamplerState**</span></span>

<span data-ttu-id="e7f94-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="e7f94-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e7f94-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="e7f94-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e7f94-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f94-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f94-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="e7f94-114">Type: **float**</span></span>

<span data-ttu-id="e7f94-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="e7f94-115">The texture coordinates.</span></span> <span data-ttu-id="e7f94-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="e7f94-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e7f94-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e7f94-117">Texture-Object Type</span></span>                    | <span data-ttu-id="e7f94-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="e7f94-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e7f94-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e7f94-119">Texture1D</span></span>                              | <span data-ttu-id="e7f94-120">float</span><span class="sxs-lookup"><span data-stu-id="e7f94-120">float</span></span>          |
| <span data-ttu-id="e7f94-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e7f94-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e7f94-122">float2</span><span class="sxs-lookup"><span data-stu-id="e7f94-122">float2</span></span>         |
| <span data-ttu-id="e7f94-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e7f94-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e7f94-124">float3</span><span class="sxs-lookup"><span data-stu-id="e7f94-124">float3</span></span>         |
| <span data-ttu-id="e7f94-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e7f94-125">TextureCubeArray</span></span>                       | <span data-ttu-id="e7f94-126">float4</span><span class="sxs-lookup"><span data-stu-id="e7f94-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e7f94-127">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f94-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f94-128">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="e7f94-128">Type: **int**</span></span>

<span data-ttu-id="e7f94-129">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="e7f94-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="e7f94-130">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="e7f94-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="e7f94-131">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="e7f94-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="e7f94-132">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e7f94-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="e7f94-133">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e7f94-133">Texture-Object Type</span></span>           | <span data-ttu-id="e7f94-134">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="e7f94-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="e7f94-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e7f94-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="e7f94-136">int</span><span class="sxs-lookup"><span data-stu-id="e7f94-136">int</span></span>            |
| <span data-ttu-id="e7f94-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e7f94-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="e7f94-138">int2</span><span class="sxs-lookup"><span data-stu-id="e7f94-138">int2</span></span>           |
| <span data-ttu-id="e7f94-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e7f94-139">Texture3D</span></span>                     | <span data-ttu-id="e7f94-140">int3</span><span class="sxs-lookup"><span data-stu-id="e7f94-140">int3</span></span>           |
| <span data-ttu-id="e7f94-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e7f94-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e7f94-142">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f94-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e7f94-143">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f94-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f94-144">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="e7f94-144">Type: **float**</span></span>

<span data-ttu-id="e7f94-145">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="e7f94-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e7f94-146">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="e7f94-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7f94-147">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7f94-147">Return value</span></span>

<span data-ttu-id="e7f94-148">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e7f94-148">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e7f94-149">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e7f94-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e7f94-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7f94-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7f94-151">Exemples de méthodes</span><span class="sxs-lookup"><span data-stu-id="e7f94-151">Sample methods</span></span>](texture1darray-sample.md)
</dt> </dl>

 

 
