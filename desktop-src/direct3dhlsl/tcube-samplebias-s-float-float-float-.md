---
title: 'SampleBias :: SampleBias (S, float, float, float), fonction'
description: 'Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. | SampleBias :: SampleBias (S, float, float, float), fonction'
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
ms.openlocfilehash: ae1c14903748f53d9890ff1a4dd9bd806caececf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043047"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function"></a><span data-ttu-id="f3e93-105">SampleBias :: SampleBias (S, float, float, float), fonction</span><span class="sxs-lookup"><span data-stu-id="f3e93-105">SampleBias::SampleBias(S,float,float,float) function</span></span>

<span data-ttu-id="f3e93-106">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="f3e93-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3e93-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3e93-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="f3e93-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3e93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3e93-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="f3e93-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e93-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="f3e93-110">Type: **SamplerState**</span></span>

<span data-ttu-id="f3e93-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f3e93-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f3e93-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="f3e93-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f3e93-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3e93-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e93-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f3e93-114">Type: **float**</span></span>

<span data-ttu-id="f3e93-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="f3e93-115">The texture coordinates.</span></span> <span data-ttu-id="f3e93-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="f3e93-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f3e93-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f3e93-117">Texture-Object Type</span></span>                    | <span data-ttu-id="f3e93-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="f3e93-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f3e93-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f3e93-119">Texture1D</span></span>                              | <span data-ttu-id="f3e93-120">float</span><span class="sxs-lookup"><span data-stu-id="f3e93-120">float</span></span>          |
| <span data-ttu-id="f3e93-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f3e93-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f3e93-122">float2</span><span class="sxs-lookup"><span data-stu-id="f3e93-122">float2</span></span>         |
| <span data-ttu-id="f3e93-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="f3e93-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f3e93-124">float3</span><span class="sxs-lookup"><span data-stu-id="f3e93-124">float3</span></span>         |
| <span data-ttu-id="f3e93-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f3e93-125">TextureCubeArray</span></span>                       | <span data-ttu-id="f3e93-126">float4</span><span class="sxs-lookup"><span data-stu-id="f3e93-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f3e93-127">*Biais* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3e93-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e93-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f3e93-128">Type: **float**</span></span>

<span data-ttu-id="f3e93-129">La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="f3e93-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="f3e93-130">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3e93-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e93-131">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f3e93-131">Type: **float**</span></span>

<span data-ttu-id="f3e93-132">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="f3e93-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f3e93-133">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="f3e93-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3e93-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3e93-134">Return value</span></span>

<span data-ttu-id="f3e93-135">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f3e93-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f3e93-136">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f3e93-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f3e93-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3e93-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e93-138">Méthodes SampleBias</span><span class="sxs-lookup"><span data-stu-id="f3e93-138">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="f3e93-139">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="f3e93-139">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
