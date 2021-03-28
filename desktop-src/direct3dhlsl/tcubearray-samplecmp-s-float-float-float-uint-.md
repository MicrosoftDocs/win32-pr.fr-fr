---
title: 'Fonction SampleCmp :: SampleCmp (S, float, float, float, uint) pour TextureCubeArray'
description: 'Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à. | Fonction SampleCmp :: SampleCmp (S, float, float, float, uint) pour TextureCubeArray'
ms.assetid: 5596D341-C057-414D-B1EC-7AA78693D32C
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
ms.openlocfilehash: 20626fe9d209ef4bfb64805f1a12561fd324f5a2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104996352"
---
# <a name="samplecmpsamplecmpsfloatfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="65be7-105">Fonction SampleCmp :: SampleCmp (S, float, float, float, uint) pour TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="65be7-105">SampleCmp::SampleCmp(S,float,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="65be7-106">Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="65be7-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="65be7-107">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="65be7-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="65be7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65be7-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="65be7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65be7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65be7-110"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="65be7-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65be7-111">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="65be7-111">Type: **SamplerState**</span></span>

<span data-ttu-id="65be7-112">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="65be7-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="65be7-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="65be7-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="65be7-114">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65be7-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65be7-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="65be7-115">Type: **float**</span></span>

<span data-ttu-id="65be7-116">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="65be7-116">The texture coordinates.</span></span> <span data-ttu-id="65be7-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="65be7-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="65be7-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="65be7-118">Texture-Object Type</span></span>                    | <span data-ttu-id="65be7-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="65be7-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="65be7-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="65be7-120">Texture1D</span></span>                              | <span data-ttu-id="65be7-121">float</span><span class="sxs-lookup"><span data-stu-id="65be7-121">float</span></span>          |
| <span data-ttu-id="65be7-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="65be7-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="65be7-123">float2</span><span class="sxs-lookup"><span data-stu-id="65be7-123">float2</span></span>         |
| <span data-ttu-id="65be7-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="65be7-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="65be7-125">float3</span><span class="sxs-lookup"><span data-stu-id="65be7-125">float3</span></span>         |
| <span data-ttu-id="65be7-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="65be7-126">TextureCubeArray</span></span>                       | <span data-ttu-id="65be7-127">float4</span><span class="sxs-lookup"><span data-stu-id="65be7-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="65be7-128">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65be7-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65be7-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="65be7-129">Type: **float**</span></span>

<span data-ttu-id="65be7-130">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="65be7-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="65be7-131">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65be7-131">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65be7-132">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="65be7-132">Type: **float**</span></span>

<span data-ttu-id="65be7-133">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="65be7-133">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="65be7-134">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="65be7-134">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="65be7-135">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="65be7-135">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65be7-136">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="65be7-136">Type: **uint**</span></span>

<span data-ttu-id="65be7-137">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="65be7-137">The status of the operation.</span></span> <span data-ttu-id="65be7-138">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="65be7-138">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="65be7-139">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="65be7-139">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="65be7-140">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="65be7-140">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65be7-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65be7-141">Return value</span></span>

<span data-ttu-id="65be7-142">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="65be7-142">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="65be7-143">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="65be7-143">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="65be7-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65be7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65be7-145">Méthodes SampleCmp</span><span class="sxs-lookup"><span data-stu-id="65be7-145">SampleCmp methods</span></span>](texturecubearray-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="65be7-146">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="65be7-146">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
