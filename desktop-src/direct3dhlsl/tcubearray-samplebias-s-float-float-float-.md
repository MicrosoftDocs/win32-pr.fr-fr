---
title: 'SampleBias :: SampleBias (S, float, float, float), fonction'
description: 'Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. | SampleBias :: SampleBias (S, float, float, float), fonction'
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
ms.openlocfilehash: 8d95a1b0341e61853a20d313a04d1cde64dde66d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104116114"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function"></a><span data-ttu-id="00dd1-105">SampleBias :: SampleBias (S, float, float, float), fonction</span><span class="sxs-lookup"><span data-stu-id="00dd1-105">SampleBias::SampleBias(S,float,float,float) function</span></span>

<span data-ttu-id="00dd1-106">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="00dd1-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="00dd1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00dd1-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="00dd1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00dd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00dd1-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="00dd1-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dd1-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="00dd1-110">Type: **SamplerState**</span></span>

<span data-ttu-id="00dd1-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="00dd1-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="00dd1-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="00dd1-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="00dd1-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00dd1-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dd1-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="00dd1-114">Type: **float**</span></span>

<span data-ttu-id="00dd1-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="00dd1-115">The texture coordinates.</span></span> <span data-ttu-id="00dd1-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="00dd1-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="00dd1-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="00dd1-117">Texture-Object Type</span></span>                    | <span data-ttu-id="00dd1-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="00dd1-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="00dd1-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="00dd1-119">Texture1D</span></span>                              | <span data-ttu-id="00dd1-120">float</span><span class="sxs-lookup"><span data-stu-id="00dd1-120">float</span></span>          |
| <span data-ttu-id="00dd1-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="00dd1-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="00dd1-122">float2</span><span class="sxs-lookup"><span data-stu-id="00dd1-122">float2</span></span>         |
| <span data-ttu-id="00dd1-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="00dd1-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="00dd1-124">float3</span><span class="sxs-lookup"><span data-stu-id="00dd1-124">float3</span></span>         |
| <span data-ttu-id="00dd1-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="00dd1-125">TextureCubeArray</span></span>                       | <span data-ttu-id="00dd1-126">float4</span><span class="sxs-lookup"><span data-stu-id="00dd1-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="00dd1-127">*Biais* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00dd1-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dd1-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="00dd1-128">Type: **float**</span></span>

<span data-ttu-id="00dd1-129">La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="00dd1-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="00dd1-130">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00dd1-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00dd1-131">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="00dd1-131">Type: **float**</span></span>

<span data-ttu-id="00dd1-132">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="00dd1-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="00dd1-133">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="00dd1-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00dd1-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00dd1-134">Return value</span></span>

<span data-ttu-id="00dd1-135">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="00dd1-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="00dd1-136">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="00dd1-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="00dd1-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00dd1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00dd1-138">Méthodes SampleBias</span><span class="sxs-lookup"><span data-stu-id="00dd1-138">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="00dd1-139">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="00dd1-139">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
