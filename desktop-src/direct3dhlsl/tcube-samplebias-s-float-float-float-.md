---
title: 'Fonction SampleBias :: SampleBias (S, float, float, float) pour TextureCube'
description: 'La fonction SampleBias :: SampleBias (S, float, float, float) de TextureCube échantillonne une texture après avoir appliqué la valeur de biais au niveau du mipmap.'
ms.assetid: BCDDADD9-D8B0-47C9-A312-5E6AF9C3C07B
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
ms.openlocfilehash: 55404f2e32f45e5b19e7b0cd4c109a6d5a8bcc13
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106541804"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="2fc6f-104">Fonction SampleBias :: SampleBias (S, float, float, float) pour TextureCube</span><span class="sxs-lookup"><span data-stu-id="2fc6f-104">SampleBias::SampleBias(S,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="2fc6f-105">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="2fc6f-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc6f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fc6f-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="2fc6f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fc6f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc6f-108"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="2fc6f-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc6f-109">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="2fc6f-109">Type: **SamplerState**</span></span>

<span data-ttu-id="2fc6f-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2fc6f-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="2fc6f-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="2fc6f-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="2fc6f-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fc6f-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc6f-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="2fc6f-113">Type: **float**</span></span>

<span data-ttu-id="2fc6f-114">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="2fc6f-114">The texture coordinates.</span></span> <span data-ttu-id="2fc6f-115">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="2fc6f-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2fc6f-116">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2fc6f-116">Texture-Object Type</span></span>                    | <span data-ttu-id="2fc6f-117">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="2fc6f-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="2fc6f-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2fc6f-118">Texture1D</span></span>                              | <span data-ttu-id="2fc6f-119">float</span><span class="sxs-lookup"><span data-stu-id="2fc6f-119">float</span></span>          |
| <span data-ttu-id="2fc6f-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2fc6f-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="2fc6f-121">float2</span><span class="sxs-lookup"><span data-stu-id="2fc6f-121">float2</span></span>         |
| <span data-ttu-id="2fc6f-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="2fc6f-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="2fc6f-123">float3</span><span class="sxs-lookup"><span data-stu-id="2fc6f-123">float3</span></span>         |
| <span data-ttu-id="2fc6f-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="2fc6f-124">TextureCubeArray</span></span>                       | <span data-ttu-id="2fc6f-125">float4</span><span class="sxs-lookup"><span data-stu-id="2fc6f-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="2fc6f-126">*Biais* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fc6f-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc6f-127">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="2fc6f-127">Type: **float**</span></span>

<span data-ttu-id="2fc6f-128">La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="2fc6f-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2fc6f-129">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fc6f-129">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc6f-130">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="2fc6f-130">Type: **float**</span></span>

<span data-ttu-id="2fc6f-131">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="2fc6f-131">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="2fc6f-132">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="2fc6f-132">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fc6f-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2fc6f-133">Return value</span></span>

<span data-ttu-id="2fc6f-134">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="2fc6f-134">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="2fc6f-135">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2fc6f-135">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="2fc6f-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fc6f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc6f-137">Méthodes SampleBias</span><span class="sxs-lookup"><span data-stu-id="2fc6f-137">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="2fc6f-138">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="2fc6f-138">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
