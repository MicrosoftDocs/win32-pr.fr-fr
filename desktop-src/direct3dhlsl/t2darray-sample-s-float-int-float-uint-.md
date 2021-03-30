---
title: 'Texture2DArray :: Sample (S, float, int, float, uint), fonction'
description: 'Échantillonne une texture avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération. | Texture2DArray :: Sample (S, float, int, float, uint), fonction'
ms.assetid: 0F9DBC0D-F35D-4A7A-B8F5-1EFBF7E14615
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
ms.openlocfilehash: e2027377a1659aa46fcf10e39f39b21e2243c943
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973970"
---
# <a name="texture2darraysamplesfloatintfloatuint-function"></a><span data-ttu-id="06b43-105">Texture2DArray :: Sample (S, float, int, float, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="06b43-105">Texture2DArray::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="06b43-106">Échantillonne une texture avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="06b43-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="06b43-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06b43-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="06b43-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06b43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06b43-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="06b43-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b43-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="06b43-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="06b43-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="06b43-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="06b43-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06b43-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b43-113">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="06b43-113">The texture coordinates.</span></span> <span data-ttu-id="06b43-114">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="06b43-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="06b43-115">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="06b43-115">Texture-Object Type</span></span>                    | <span data-ttu-id="06b43-116">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="06b43-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="06b43-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="06b43-117">Texture1D</span></span>                              | <span data-ttu-id="06b43-118">float</span><span class="sxs-lookup"><span data-stu-id="06b43-118">float</span></span>          |
| <span data-ttu-id="06b43-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="06b43-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="06b43-120">float2</span><span class="sxs-lookup"><span data-stu-id="06b43-120">float2</span></span>         |
| <span data-ttu-id="06b43-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="06b43-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="06b43-122">float3</span><span class="sxs-lookup"><span data-stu-id="06b43-122">float3</span></span>         |
| <span data-ttu-id="06b43-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="06b43-123">TextureCubeArray</span></span>                       | <span data-ttu-id="06b43-124">float4</span><span class="sxs-lookup"><span data-stu-id="06b43-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="06b43-125">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06b43-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b43-126">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="06b43-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="06b43-127">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="06b43-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="06b43-128">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="06b43-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="06b43-129">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="06b43-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="06b43-130">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="06b43-130">Texture-Object Type</span></span>           | <span data-ttu-id="06b43-131">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="06b43-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="06b43-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="06b43-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="06b43-133">int</span><span class="sxs-lookup"><span data-stu-id="06b43-133">int</span></span>            |
| <span data-ttu-id="06b43-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="06b43-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="06b43-135">int2</span><span class="sxs-lookup"><span data-stu-id="06b43-135">int2</span></span>           |
| <span data-ttu-id="06b43-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="06b43-136">Texture3D</span></span>                     | <span data-ttu-id="06b43-137">int3</span><span class="sxs-lookup"><span data-stu-id="06b43-137">int3</span></span>           |
| <span data-ttu-id="06b43-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="06b43-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="06b43-139">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="06b43-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="06b43-140">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06b43-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b43-141">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="06b43-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="06b43-142">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="06b43-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="06b43-143">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="06b43-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06b43-144">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="06b43-144">The status of the operation.</span></span> <span data-ttu-id="06b43-145">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="06b43-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="06b43-146">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="06b43-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="06b43-147">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="06b43-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06b43-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06b43-148">Return value</span></span>

<span data-ttu-id="06b43-149">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="06b43-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="06b43-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06b43-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b43-151">Exemples de méthodes</span><span class="sxs-lookup"><span data-stu-id="06b43-151">Sample methods</span></span>](texture2darray-sample.md)
</dt> </dl>

 

 
