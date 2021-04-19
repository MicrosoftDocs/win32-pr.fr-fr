---
title: 'Fonction SampleBias :: SampleBias (S, float, float, float, uint) pour TextureCube'
description: 'La fonction SampleBias :: SampleBias (S, float, float, float, uint) de TextureCube échantillonne une texture après avoir appliqué la valeur de biais au niveau du mipmap.'
ms.assetid: A2F10B9B-5DF2-4389-83A9-F6A29781BF0A
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
ms.openlocfilehash: 116749acdc23bb8ac2fd057139bf8ef7c8f5ddcc
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106525692"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="f0431-104">Fonction SampleBias :: SampleBias (S, float, float, float, uint) pour TextureCube</span><span class="sxs-lookup"><span data-stu-id="f0431-104">SampleBias::SampleBias(S,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="f0431-105">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="f0431-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="f0431-106">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f0431-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0431-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0431-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="f0431-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0431-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0431-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="f0431-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0431-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="f0431-110">Type: **SamplerState**</span></span>

<span data-ttu-id="f0431-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f0431-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f0431-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="f0431-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f0431-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0431-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0431-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f0431-114">Type: **float**</span></span>

<span data-ttu-id="f0431-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="f0431-115">The texture coordinates.</span></span> <span data-ttu-id="f0431-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="f0431-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f0431-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f0431-117">Texture-Object Type</span></span>                    | <span data-ttu-id="f0431-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="f0431-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f0431-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f0431-119">Texture1D</span></span>                              | <span data-ttu-id="f0431-120">float</span><span class="sxs-lookup"><span data-stu-id="f0431-120">float</span></span>          |
| <span data-ttu-id="f0431-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f0431-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f0431-122">float2</span><span class="sxs-lookup"><span data-stu-id="f0431-122">float2</span></span>         |
| <span data-ttu-id="f0431-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="f0431-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f0431-124">float3</span><span class="sxs-lookup"><span data-stu-id="f0431-124">float3</span></span>         |
| <span data-ttu-id="f0431-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f0431-125">TextureCubeArray</span></span>                       | <span data-ttu-id="f0431-126">float4</span><span class="sxs-lookup"><span data-stu-id="f0431-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f0431-127">*Biais* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0431-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0431-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f0431-128">Type: **float**</span></span>

<span data-ttu-id="f0431-129">La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="f0431-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="f0431-130">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0431-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0431-131">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f0431-131">Type: **float**</span></span>

<span data-ttu-id="f0431-132">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="f0431-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f0431-133">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="f0431-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="f0431-134">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f0431-134">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0431-135">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="f0431-135">Type: **uint**</span></span>

<span data-ttu-id="f0431-136">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f0431-136">The status of the operation.</span></span> <span data-ttu-id="f0431-137">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="f0431-137">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="f0431-138">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="f0431-138">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="f0431-139">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="f0431-139">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0431-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0431-140">Return value</span></span>

<span data-ttu-id="f0431-141">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f0431-141">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f0431-142">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f0431-142">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f0431-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0431-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0431-144">Méthodes SampleBias</span><span class="sxs-lookup"><span data-stu-id="f0431-144">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="f0431-145">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="f0431-145">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
