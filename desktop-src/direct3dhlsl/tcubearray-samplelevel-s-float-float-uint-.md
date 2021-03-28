---
title: 'SampleLevel :: SampleLevel (S, float, float, uint), fonction'
description: 'Échantillonne une texture sur le niveau de mipmap spécifié et retourne l’état de l’opération. | SampleLevel :: SampleLevel (S, float, float, uint), fonction'
ms.assetid: 3794D17F-BC70-4D3A-9F2C-ADF900983D2C
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
ms.openlocfilehash: 356e2779d82e886946e93d2071ae693279c07eb8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211514"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function"></a><span data-ttu-id="1508b-105">SampleLevel :: SampleLevel (S, float, float, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="1508b-105">SampleLevel::SampleLevel(S,float,float,uint) function</span></span>

<span data-ttu-id="1508b-106">Échantillonne une texture sur le niveau de mipmap spécifié et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1508b-106">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1508b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1508b-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="1508b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1508b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1508b-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="1508b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1508b-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="1508b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="1508b-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="1508b-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="1508b-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="1508b-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="1508b-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1508b-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1508b-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="1508b-114">Type: **float**</span></span>

<span data-ttu-id="1508b-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="1508b-115">The texture coordinates.</span></span> <span data-ttu-id="1508b-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="1508b-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1508b-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="1508b-117">Texture-Object Type</span></span>                    | <span data-ttu-id="1508b-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="1508b-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="1508b-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1508b-119">Texture1D</span></span>                              | <span data-ttu-id="1508b-120">float</span><span class="sxs-lookup"><span data-stu-id="1508b-120">float</span></span>          |
| <span data-ttu-id="1508b-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="1508b-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="1508b-122">float2</span><span class="sxs-lookup"><span data-stu-id="1508b-122">float2</span></span>         |
| <span data-ttu-id="1508b-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="1508b-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="1508b-124">float3</span><span class="sxs-lookup"><span data-stu-id="1508b-124">float3</span></span>         |
| <span data-ttu-id="1508b-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1508b-125">TextureCubeArray</span></span>                       | <span data-ttu-id="1508b-126">float4</span><span class="sxs-lookup"><span data-stu-id="1508b-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="1508b-127">*LOD* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1508b-127">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1508b-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="1508b-128">Type: **float**</span></span>

<span data-ttu-id="1508b-129">\[dans \] un nombre qui spécifie le niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="1508b-129">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="1508b-130">Si la valeur est ≤ 0, le mipmap niveau 0 (mappage le plus grand) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1508b-130">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="1508b-131">La valeur fractionnaire (si fournie) est utilisée pour interpoler entre deux niveaux de mipmap.</span><span class="sxs-lookup"><span data-stu-id="1508b-131">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="1508b-132">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1508b-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1508b-133">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1508b-133">Type: **uint**</span></span>

<span data-ttu-id="1508b-134">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1508b-134">The status of the operation.</span></span> <span data-ttu-id="1508b-135">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="1508b-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="1508b-136">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="1508b-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="1508b-137">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="1508b-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1508b-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1508b-138">Return value</span></span>

<span data-ttu-id="1508b-139">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="1508b-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="1508b-140">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="1508b-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="1508b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1508b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1508b-142">Méthodes SampleLevel</span><span class="sxs-lookup"><span data-stu-id="1508b-142">SampleLevel methods</span></span>](texturecubearray-samplelevel.md)
</dt> <dt>

[<span data-ttu-id="1508b-143">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="1508b-143">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
