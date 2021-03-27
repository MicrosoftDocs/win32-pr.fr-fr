---
title: 'Fonction SampleCmpLevelZero :: SampleCmpLevelZero (S, float, float, uint) pour TextureCubeArray'
description: Échantillonne une texture sur le niveau de mipmap 0 uniquement et compare le résultat à une valeur de comparaison, puis retourne l’état de l’opération. Pour TextureCubeArray.
ms.assetid: D73447C6-E77C-4027-B265-24F96C679357
keywords:
- SampleCmpLevelZero fonction HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac042bd2856aa69bbba1293fb91ff74d95c0de53
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762398"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="140c7-105">Fonction SampleCmpLevelZero :: SampleCmpLevelZero (S, float, float, uint) pour TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="140c7-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="140c7-106">Échantillonne une texture sur le niveau de mipmap 0 uniquement et compare le résultat à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="140c7-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="140c7-107">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="140c7-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="140c7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="140c7-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="140c7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="140c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="140c7-110"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="140c7-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="140c7-111">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="140c7-111">Type: **SamplerState**</span></span>

<span data-ttu-id="140c7-112">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="140c7-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="140c7-113">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="140c7-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="140c7-114">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="140c7-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="140c7-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="140c7-115">Type: **float**</span></span>

<span data-ttu-id="140c7-116">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="140c7-116">The texture coordinates.</span></span> <span data-ttu-id="140c7-117">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="140c7-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="140c7-118">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="140c7-118">Texture-Object Type</span></span>                    | <span data-ttu-id="140c7-119">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="140c7-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="140c7-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="140c7-120">Texture1D</span></span>                              | <span data-ttu-id="140c7-121">float</span><span class="sxs-lookup"><span data-stu-id="140c7-121">float</span></span>          |
| <span data-ttu-id="140c7-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="140c7-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="140c7-123">float2</span><span class="sxs-lookup"><span data-stu-id="140c7-123">float2</span></span>         |
| <span data-ttu-id="140c7-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="140c7-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="140c7-125">float3</span><span class="sxs-lookup"><span data-stu-id="140c7-125">float3</span></span>         |
| <span data-ttu-id="140c7-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="140c7-126">TextureCubeArray</span></span>                       | <span data-ttu-id="140c7-127">float4</span><span class="sxs-lookup"><span data-stu-id="140c7-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="140c7-128">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="140c7-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="140c7-129">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="140c7-129">Type: **float**</span></span>

<span data-ttu-id="140c7-130">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="140c7-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="140c7-131">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="140c7-131">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="140c7-132">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="140c7-132">Type: **uint**</span></span>

<span data-ttu-id="140c7-133">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="140c7-133">The status of the operation.</span></span> <span data-ttu-id="140c7-134">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="140c7-134">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="140c7-135">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="140c7-135">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="140c7-136">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="140c7-136">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="140c7-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="140c7-137">Return value</span></span>

<span data-ttu-id="140c7-138">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="140c7-138">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="140c7-139">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="140c7-139">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="140c7-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="140c7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140c7-141">Méthodes SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="140c7-141">SampleCmpLevelZero methods</span></span>](texturecubearray-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="140c7-142">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="140c7-142">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
