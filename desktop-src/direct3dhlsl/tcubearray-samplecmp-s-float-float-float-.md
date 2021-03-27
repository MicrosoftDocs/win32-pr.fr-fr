---
title: 'Fonction SampleCmp :: SampleCmp (S, float, float, float) pour TextureCubeArray'
description: 'Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à. | Fonction SampleCmp :: SampleCmp (S, float, float, float) pour TextureCubeArray'
ms.assetid: A8824A82-A3FD-4FEE-BC10-56843997BBCE
keywords:
- SampleCmp fonction HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e65b1747d03b3a0555267f7b57e95a4d5aba54da
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982642"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="41e15-105">Fonction SampleCmp :: SampleCmp (S, float, float, float) pour TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="41e15-105">SampleCmp::SampleCmp(S,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="41e15-106">Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="41e15-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e15-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41e15-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="41e15-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41e15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e15-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="41e15-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e15-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="41e15-110">Type: **SamplerState**</span></span>

<span data-ttu-id="41e15-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="41e15-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="41e15-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="41e15-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="41e15-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41e15-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e15-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="41e15-114">Type: **float**</span></span>

<span data-ttu-id="41e15-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="41e15-115">The texture coordinates.</span></span> <span data-ttu-id="41e15-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="41e15-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="41e15-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="41e15-117">Texture-Object Type</span></span>                    | <span data-ttu-id="41e15-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="41e15-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="41e15-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="41e15-119">Texture1D</span></span>                              | <span data-ttu-id="41e15-120">float</span><span class="sxs-lookup"><span data-stu-id="41e15-120">float</span></span>          |
| <span data-ttu-id="41e15-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="41e15-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="41e15-122">float2</span><span class="sxs-lookup"><span data-stu-id="41e15-122">float2</span></span>         |
| <span data-ttu-id="41e15-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="41e15-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="41e15-124">float3</span><span class="sxs-lookup"><span data-stu-id="41e15-124">float3</span></span>         |
| <span data-ttu-id="41e15-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="41e15-125">TextureCubeArray</span></span>                       | <span data-ttu-id="41e15-126">float4</span><span class="sxs-lookup"><span data-stu-id="41e15-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="41e15-127">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41e15-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e15-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="41e15-128">Type: **float**</span></span>

<span data-ttu-id="41e15-129">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="41e15-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="41e15-130">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41e15-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e15-131">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="41e15-131">Type: **float**</span></span>

<span data-ttu-id="41e15-132">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="41e15-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="41e15-133">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="41e15-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41e15-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41e15-134">Return value</span></span>

<span data-ttu-id="41e15-135">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="41e15-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="41e15-136">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="41e15-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="41e15-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41e15-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e15-138">Méthodes SampleCmp</span><span class="sxs-lookup"><span data-stu-id="41e15-138">SampleCmp methods</span></span>](texturecubearray-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="41e15-139">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="41e15-139">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
