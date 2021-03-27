---
title: 'Fonction SampleCmpLevelZero :: SampleCmpLevelZero (S, float, float, uint) pour TextureCube'
description: Échantillonne une texture sur le niveau de mipmap 0 uniquement et compare le résultat à une valeur de comparaison. Retourne l’état de l’opération. Pour TextureCube.
ms.assetid: FE40307D-B9BE-434F-A6EF-7CA3C5BC7D70
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
ms.openlocfilehash: ff58c51919e575260c71f7b58d8f3d0fda6c1dd1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982703"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="cee4e-106">Fonction SampleCmpLevelZero :: SampleCmpLevelZero (S, float, float, uint) pour TextureCube</span><span class="sxs-lookup"><span data-stu-id="cee4e-106">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="cee4e-107">Échantillonne une texture sur le niveau de mipmap 0 uniquement et compare le résultat à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="cee4e-107">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="cee4e-108">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="cee4e-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cee4e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cee4e-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="cee4e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cee4e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cee4e-111"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="cee4e-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cee4e-112">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="cee4e-112">Type: **SamplerState**</span></span>

<span data-ttu-id="cee4e-113">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="cee4e-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="cee4e-114">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="cee4e-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="cee4e-115">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cee4e-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cee4e-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="cee4e-116">Type: **float**</span></span>

<span data-ttu-id="cee4e-117">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="cee4e-117">The texture coordinates.</span></span> <span data-ttu-id="cee4e-118">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="cee4e-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="cee4e-119">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="cee4e-119">Texture-Object Type</span></span>                    | <span data-ttu-id="cee4e-120">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="cee4e-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="cee4e-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="cee4e-121">Texture1D</span></span>                              | <span data-ttu-id="cee4e-122">float</span><span class="sxs-lookup"><span data-stu-id="cee4e-122">float</span></span>          |
| <span data-ttu-id="cee4e-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="cee4e-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="cee4e-124">float2</span><span class="sxs-lookup"><span data-stu-id="cee4e-124">float2</span></span>         |
| <span data-ttu-id="cee4e-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="cee4e-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="cee4e-126">float3</span><span class="sxs-lookup"><span data-stu-id="cee4e-126">float3</span></span>         |
| <span data-ttu-id="cee4e-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="cee4e-127">TextureCubeArray</span></span>                       | <span data-ttu-id="cee4e-128">float4</span><span class="sxs-lookup"><span data-stu-id="cee4e-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="cee4e-129">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cee4e-129">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cee4e-130">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="cee4e-130">Type: **float**</span></span>

<span data-ttu-id="cee4e-131">Valeur à virgule flottante à utiliser comme valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="cee4e-131">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="cee4e-132">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cee4e-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cee4e-133">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="cee4e-133">Type: **uint**</span></span>

<span data-ttu-id="cee4e-134">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="cee4e-134">The status of the operation.</span></span> <span data-ttu-id="cee4e-135">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="cee4e-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="cee4e-136">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="cee4e-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="cee4e-137">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="cee4e-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cee4e-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cee4e-138">Return value</span></span>

<span data-ttu-id="cee4e-139">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="cee4e-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="cee4e-140">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="cee4e-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="cee4e-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cee4e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee4e-142">Méthodes SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="cee4e-142">SampleCmpLevelZero methods</span></span>](texturecube-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="cee4e-143">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="cee4e-143">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
