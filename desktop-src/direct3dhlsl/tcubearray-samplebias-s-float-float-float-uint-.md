---
title: 'Fonction SampleBias :: SampleBias (S, float, float, float, uint) pour TextureCubeArray'
description: 'La fonction SampleBias :: SampleBias (S, float, float, float, uint) de TextureCubeArray échantillonne une texture après avoir appliqué la valeur de biais au niveau du mipmap.'
ms.assetid: 376F11E6-4FFF-4685-9285-9D6143C77F2D
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
ms.openlocfilehash: 4bcd5b2239a8b2d219fde28b1c9a00a693906b5c
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106541571"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="b6503-104">Fonction SampleBias :: SampleBias (S, float, float, float, uint) pour TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b6503-104">SampleBias::SampleBias(S,float,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="b6503-105">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="b6503-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="b6503-106">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b6503-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6503-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6503-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="b6503-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6503-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6503-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="b6503-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6503-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="b6503-110">Type: **SamplerState**</span></span>

<span data-ttu-id="b6503-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="b6503-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="b6503-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="b6503-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="b6503-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6503-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6503-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="b6503-114">Type: **float**</span></span>

<span data-ttu-id="b6503-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="b6503-115">The texture coordinates.</span></span> <span data-ttu-id="b6503-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="b6503-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b6503-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b6503-117">Texture-Object Type</span></span>                    | <span data-ttu-id="b6503-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="b6503-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="b6503-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b6503-119">Texture1D</span></span>                              | <span data-ttu-id="b6503-120">float</span><span class="sxs-lookup"><span data-stu-id="b6503-120">float</span></span>          |
| <span data-ttu-id="b6503-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="b6503-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="b6503-122">float2</span><span class="sxs-lookup"><span data-stu-id="b6503-122">float2</span></span>         |
| <span data-ttu-id="b6503-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="b6503-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="b6503-124">float3</span><span class="sxs-lookup"><span data-stu-id="b6503-124">float3</span></span>         |
| <span data-ttu-id="b6503-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b6503-125">TextureCubeArray</span></span>                       | <span data-ttu-id="b6503-126">float4</span><span class="sxs-lookup"><span data-stu-id="b6503-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="b6503-127">*Biais* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6503-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6503-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="b6503-128">Type: **float**</span></span>

<span data-ttu-id="b6503-129">La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="b6503-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="b6503-130">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6503-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6503-131">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="b6503-131">Type: **float**</span></span>

<span data-ttu-id="b6503-132">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="b6503-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="b6503-133">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="b6503-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="b6503-134">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b6503-134">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6503-135">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="b6503-135">Type: **uint**</span></span>

<span data-ttu-id="b6503-136">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b6503-136">The status of the operation.</span></span> <span data-ttu-id="b6503-137">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="b6503-137">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b6503-138">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="b6503-138">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b6503-139">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="b6503-139">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6503-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6503-140">Return value</span></span>

<span data-ttu-id="b6503-141">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="b6503-141">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="b6503-142">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="b6503-142">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="b6503-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6503-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6503-144">Méthodes SampleBias</span><span class="sxs-lookup"><span data-stu-id="b6503-144">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="b6503-145">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="b6503-145">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
