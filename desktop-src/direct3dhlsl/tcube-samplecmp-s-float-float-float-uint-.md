---
title: 'Fonction SampleCmp :: SampleCmp (S, float, float, float, uint) pour TextureCube'
description: 'Cette fonction échantillonne une texture à l’aide d’une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. | Fonction SampleCmp :: SampleCmp (S, float, float, float, uint) pour TextureCube'
ms.assetid: 050E2856-1E93-4C69-8213-EEC082E82D40
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
ms.openlocfilehash: b73bf86b0c24feae87ea0bb4150d313fff604002
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982658"
---
# <a name="samplecmpsamplecmpsfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="e810f-105">Fonction SampleCmp :: SampleCmp (S, float, float, float, uint) pour TextureCube</span><span class="sxs-lookup"><span data-stu-id="e810f-105">SampleCmp::SampleCmp(S,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="e810f-106">Échantillonne une texture, en utilisant une valeur de comparaison pour rejeter les exemples, avec une valeur facultative pour fixer des exemples de valeurs de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="e810f-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="e810f-107">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e810f-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e810f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e810f-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="e810f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e810f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e810f-110"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="e810f-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e810f-111">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="e810f-111">Type: **SamplerState**</span></span>

<span data-ttu-id="e810f-112">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="e810f-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e810f-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="e810f-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e810f-114">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e810f-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e810f-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="e810f-115">Type: **float**</span></span>

<span data-ttu-id="e810f-116">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="e810f-116">The texture coordinates.</span></span> <span data-ttu-id="e810f-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="e810f-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e810f-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e810f-118">Texture-Object Type</span></span>                    | <span data-ttu-id="e810f-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="e810f-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e810f-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e810f-120">Texture1D</span></span>                              | <span data-ttu-id="e810f-121">float</span><span class="sxs-lookup"><span data-stu-id="e810f-121">float</span></span>          |
| <span data-ttu-id="e810f-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e810f-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e810f-123">float2</span><span class="sxs-lookup"><span data-stu-id="e810f-123">float2</span></span>         |
| <span data-ttu-id="e810f-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e810f-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e810f-125">float3</span><span class="sxs-lookup"><span data-stu-id="e810f-125">float3</span></span>         |
| <span data-ttu-id="e810f-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e810f-126">TextureCubeArray</span></span>                       | <span data-ttu-id="e810f-127">float4</span><span class="sxs-lookup"><span data-stu-id="e810f-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e810f-128">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e810f-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e810f-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="e810f-129">Type: **float**</span></span>

<span data-ttu-id="e810f-130">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="e810f-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="e810f-131">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e810f-131">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e810f-132">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="e810f-132">Type: **float**</span></span>

<span data-ttu-id="e810f-133">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="e810f-133">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e810f-134">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="e810f-134">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="e810f-135">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e810f-135">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e810f-136">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="e810f-136">Type: **uint**</span></span>

<span data-ttu-id="e810f-137">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e810f-137">The status of the operation.</span></span> <span data-ttu-id="e810f-138">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e810f-138">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e810f-139">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e810f-139">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e810f-140">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="e810f-140">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e810f-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e810f-141">Return value</span></span>

<span data-ttu-id="e810f-142">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e810f-142">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e810f-143">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e810f-143">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e810f-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e810f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e810f-145">Méthodes SampleCmp</span><span class="sxs-lookup"><span data-stu-id="e810f-145">SampleCmp methods</span></span>](texturecube-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="e810f-146">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="e810f-146">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
