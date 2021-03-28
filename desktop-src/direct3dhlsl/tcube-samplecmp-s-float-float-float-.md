---
title: 'Fonction SampleCmp :: SampleCmp (S, float, float, float) pour TextureCube'
description: 'Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à. | Fonction SampleCmp :: SampleCmp (S, float, float, float) pour TextureCube'
ms.assetid: FCCF12CF-3F0A-4468-9FC4-27CAAF0BEEE3
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
ms.openlocfilehash: e8a326101df26ab7f4925c9c6cce3673385309fd
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982727"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="eed7c-105">Fonction SampleCmp :: SampleCmp (S, float, float, float) pour TextureCube</span><span class="sxs-lookup"><span data-stu-id="eed7c-105">SampleCmp::SampleCmp(S,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="eed7c-106">Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="eed7c-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed7c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eed7c-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="eed7c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eed7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eed7c-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="eed7c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eed7c-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="eed7c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="eed7c-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="eed7c-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="eed7c-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="eed7c-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="eed7c-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eed7c-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eed7c-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="eed7c-114">Type: **float**</span></span>

<span data-ttu-id="eed7c-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="eed7c-115">The texture coordinates.</span></span> <span data-ttu-id="eed7c-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="eed7c-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="eed7c-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="eed7c-117">Texture-Object Type</span></span>                    | <span data-ttu-id="eed7c-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="eed7c-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="eed7c-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="eed7c-119">Texture1D</span></span>                              | <span data-ttu-id="eed7c-120">float</span><span class="sxs-lookup"><span data-stu-id="eed7c-120">float</span></span>          |
| <span data-ttu-id="eed7c-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="eed7c-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="eed7c-122">float2</span><span class="sxs-lookup"><span data-stu-id="eed7c-122">float2</span></span>         |
| <span data-ttu-id="eed7c-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="eed7c-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="eed7c-124">float3</span><span class="sxs-lookup"><span data-stu-id="eed7c-124">float3</span></span>         |
| <span data-ttu-id="eed7c-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="eed7c-125">TextureCubeArray</span></span>                       | <span data-ttu-id="eed7c-126">float4</span><span class="sxs-lookup"><span data-stu-id="eed7c-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="eed7c-127">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eed7c-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eed7c-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="eed7c-128">Type: **float**</span></span>

<span data-ttu-id="eed7c-129">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="eed7c-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="eed7c-130">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eed7c-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eed7c-131">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="eed7c-131">Type: **float**</span></span>

<span data-ttu-id="eed7c-132">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="eed7c-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="eed7c-133">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="eed7c-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eed7c-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eed7c-134">Return value</span></span>

<span data-ttu-id="eed7c-135">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="eed7c-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="eed7c-136">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="eed7c-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="eed7c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eed7c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed7c-138">Méthodes SampleCmp</span><span class="sxs-lookup"><span data-stu-id="eed7c-138">SampleCmp methods</span></span>](texturecube-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="eed7c-139">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="eed7c-139">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
