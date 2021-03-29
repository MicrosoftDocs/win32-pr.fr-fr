---
title: 'Texture3D :: Sample (S, float, int, float, uint), fonction'
description: 'Échantillonne une texture avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération. | Texture3D :: Sample (S, float, int, float, uint), fonction'
ms.assetid: DB8401A1-1065-4616-BDDE-9ADB59B09C8B
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
ms.openlocfilehash: 1f1704a30ba689d50bc9c551ac6a43a4a38f90a9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991893"
---
# <a name="texture3dsamplesfloatintfloatuint-function"></a><span data-ttu-id="9cb01-105">Texture3D :: Sample (S, float, int, float, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="9cb01-105">Texture3D::Sample(S,float,int,float,uint) function</span></span>

<span data-ttu-id="9cb01-106">Échantillonne une texture avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9cb01-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cb01-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9cb01-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="9cb01-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9cb01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cb01-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="9cb01-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb01-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="9cb01-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="9cb01-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="9cb01-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="9cb01-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9cb01-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb01-113">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="9cb01-113">The texture coordinates.</span></span> <span data-ttu-id="9cb01-114">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="9cb01-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="9cb01-115">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="9cb01-115">Texture-Object Type</span></span>                    | <span data-ttu-id="9cb01-116">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="9cb01-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="9cb01-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="9cb01-117">Texture1D</span></span>                              | <span data-ttu-id="9cb01-118">float</span><span class="sxs-lookup"><span data-stu-id="9cb01-118">float</span></span>          |
| <span data-ttu-id="9cb01-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="9cb01-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="9cb01-120">float2</span><span class="sxs-lookup"><span data-stu-id="9cb01-120">float2</span></span>         |
| <span data-ttu-id="9cb01-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="9cb01-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="9cb01-122">float3</span><span class="sxs-lookup"><span data-stu-id="9cb01-122">float3</span></span>         |
| <span data-ttu-id="9cb01-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="9cb01-123">TextureCubeArray</span></span>                       | <span data-ttu-id="9cb01-124">float4</span><span class="sxs-lookup"><span data-stu-id="9cb01-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="9cb01-125">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9cb01-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb01-126">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="9cb01-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="9cb01-127">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="9cb01-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="9cb01-128">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="9cb01-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="9cb01-129">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9cb01-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="9cb01-130">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="9cb01-130">Texture-Object Type</span></span>           | <span data-ttu-id="9cb01-131">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="9cb01-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="9cb01-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="9cb01-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="9cb01-133">int</span><span class="sxs-lookup"><span data-stu-id="9cb01-133">int</span></span>            |
| <span data-ttu-id="9cb01-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="9cb01-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="9cb01-135">int2</span><span class="sxs-lookup"><span data-stu-id="9cb01-135">int2</span></span>           |
| <span data-ttu-id="9cb01-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="9cb01-136">Texture3D</span></span>                     | <span data-ttu-id="9cb01-137">int3</span><span class="sxs-lookup"><span data-stu-id="9cb01-137">int3</span></span>           |
| <span data-ttu-id="9cb01-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="9cb01-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="9cb01-139">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="9cb01-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="9cb01-140">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9cb01-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb01-141">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="9cb01-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="9cb01-142">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="9cb01-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="9cb01-143">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9cb01-143">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb01-144">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9cb01-144">The status of the operation.</span></span> <span data-ttu-id="9cb01-145">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="9cb01-145">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="9cb01-146">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="9cb01-146">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="9cb01-147">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="9cb01-147">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cb01-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9cb01-148">Return value</span></span>

<span data-ttu-id="9cb01-149">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="9cb01-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="9cb01-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cb01-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cb01-151">Exemples de méthodes</span><span class="sxs-lookup"><span data-stu-id="9cb01-151">Sample methods</span></span>](texture3d-sample.md)
</dt> <dt>

[<span data-ttu-id="9cb01-152">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="9cb01-152">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
