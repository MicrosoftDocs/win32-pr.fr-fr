---
title: 'Texture3D :: Sample (S, float, int, float), fonction'
description: 'Échantillonne une texture avec une valeur facultative pour fixer l’exemple de valeurs de niveau de détail (LOD) à. | Texture3D :: Sample (S, float, int, float), fonction'
ms.assetid: A1114A4A-16B9-4A5D-9A9D-262D6BAA9F2E
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
ms.openlocfilehash: 11577e6151d2353477a70e6ef2873d287eb71a87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991896"
---
# <a name="texture3dsamplesfloatintfloat-function"></a><span data-ttu-id="2e797-105">Texture3D :: Sample (S, float, int, float), fonction</span><span class="sxs-lookup"><span data-stu-id="2e797-105">Texture3D::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="2e797-106">Échantillonne une texture avec une valeur facultative pour fixer l’exemple de valeurs de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="2e797-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e797-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e797-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="2e797-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e797-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e797-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="2e797-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e797-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2e797-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="2e797-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="2e797-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="2e797-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e797-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e797-113">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="2e797-113">The texture coordinates.</span></span> <span data-ttu-id="2e797-114">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="2e797-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2e797-115">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2e797-115">Texture-Object Type</span></span>                    | <span data-ttu-id="2e797-116">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="2e797-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="2e797-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2e797-117">Texture1D</span></span>                              | <span data-ttu-id="2e797-118">float</span><span class="sxs-lookup"><span data-stu-id="2e797-118">float</span></span>          |
| <span data-ttu-id="2e797-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2e797-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="2e797-120">float2</span><span class="sxs-lookup"><span data-stu-id="2e797-120">float2</span></span>         |
| <span data-ttu-id="2e797-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="2e797-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="2e797-122">float3</span><span class="sxs-lookup"><span data-stu-id="2e797-122">float3</span></span>         |
| <span data-ttu-id="2e797-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2e797-123">TextureCubeArray</span></span>                       | <span data-ttu-id="2e797-124">float4</span><span class="sxs-lookup"><span data-stu-id="2e797-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="2e797-125">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e797-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e797-126">Décalage de coordonnée de texture facultatif, qui peut être utilisé pour tout type d’objet de texture ; l’offset est appliqué à l’emplacement avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="2e797-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="2e797-127">Utilisez un décalage uniquement au niveau d’un miplevel entier ; dans le cas contraire, vous risquez d’obtenir des résultats qui ne se traduisent pas bien en matériel.</span><span class="sxs-lookup"><span data-stu-id="2e797-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="2e797-128">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="2e797-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="2e797-129">Pour plus d’informations, consultez [application de décalages d’entiers](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2e797-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="2e797-130">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2e797-130">Texture-Object Type</span></span>           | <span data-ttu-id="2e797-131">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="2e797-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="2e797-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2e797-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="2e797-133">int</span><span class="sxs-lookup"><span data-stu-id="2e797-133">int</span></span>            |
| <span data-ttu-id="2e797-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2e797-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="2e797-135">int2</span><span class="sxs-lookup"><span data-stu-id="2e797-135">int2</span></span>           |
| <span data-ttu-id="2e797-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2e797-136">Texture3D</span></span>                     | <span data-ttu-id="2e797-137">int3</span><span class="sxs-lookup"><span data-stu-id="2e797-137">int3</span></span>           |
| <span data-ttu-id="2e797-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2e797-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2e797-139">non pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e797-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2e797-140">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e797-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e797-141">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="2e797-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="2e797-142">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="2e797-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e797-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e797-143">Return value</span></span>

<span data-ttu-id="2e797-144">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2e797-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="2e797-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e797-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e797-146">Exemples de méthodes</span><span class="sxs-lookup"><span data-stu-id="2e797-146">Sample methods</span></span>](texture3d-sample.md)
</dt> <dt>

[<span data-ttu-id="2e797-147">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="2e797-147">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
