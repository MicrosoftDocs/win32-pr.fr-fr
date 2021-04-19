---
title: 'Fonction SampleBias :: SampleBias (S, float, float, float) pour TextureCubeArray'
description: 'La fonction SampleBias :: SampleBias (S, float, float, float) de TextureCubeArray échantillonne une texture après avoir appliqué la valeur de biais au niveau du mipmap.'
ms.assetid: 6683F115-4F81-4C24-B735-67DB4B52455B
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
ms.openlocfilehash: 0c57eec224ca92b2584ba7262488530ea7080939
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106542825"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="5f8e7-104">Fonction SampleBias :: SampleBias (S, float, float, float) pour TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5f8e7-104">SampleBias::SampleBias(S,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="5f8e7-105">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8e7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f8e7-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="5f8e7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f8e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f8e7-108"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="5f8e7-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8e7-109">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="5f8e7-109">Type: **SamplerState**</span></span>

<span data-ttu-id="5f8e7-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="5f8e7-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="5f8e7-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e7-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f8e7-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8e7-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="5f8e7-113">Type: **float**</span></span>

<span data-ttu-id="5f8e7-114">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-114">The texture coordinates.</span></span> <span data-ttu-id="5f8e7-115">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5f8e7-116">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5f8e7-116">Texture-Object Type</span></span>                    | <span data-ttu-id="5f8e7-117">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="5f8e7-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="5f8e7-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5f8e7-118">Texture1D</span></span>                              | <span data-ttu-id="5f8e7-119">float</span><span class="sxs-lookup"><span data-stu-id="5f8e7-119">float</span></span>          |
| <span data-ttu-id="5f8e7-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="5f8e7-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="5f8e7-121">float2</span><span class="sxs-lookup"><span data-stu-id="5f8e7-121">float2</span></span>         |
| <span data-ttu-id="5f8e7-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="5f8e7-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="5f8e7-123">float3</span><span class="sxs-lookup"><span data-stu-id="5f8e7-123">float3</span></span>         |
| <span data-ttu-id="5f8e7-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5f8e7-124">TextureCubeArray</span></span>                       | <span data-ttu-id="5f8e7-125">float4</span><span class="sxs-lookup"><span data-stu-id="5f8e7-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="5f8e7-126">*Biais* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f8e7-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8e7-127">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="5f8e7-127">Type: **float**</span></span>

<span data-ttu-id="5f8e7-128">La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e7-129">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f8e7-129">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8e7-130">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="5f8e7-130">Type: **float**</span></span>

<span data-ttu-id="5f8e7-131">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-131">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="5f8e7-132">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="5f8e7-132">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f8e7-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f8e7-133">Return value</span></span>

<span data-ttu-id="5f8e7-134">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="5f8e7-134">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="5f8e7-135">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="5f8e7-135">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="5f8e7-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f8e7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f8e7-137">Méthodes SampleBias</span><span class="sxs-lookup"><span data-stu-id="5f8e7-137">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="5f8e7-138">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="5f8e7-138">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
