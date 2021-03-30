---
title: 'SampleBias :: SampleBias (S, float, float, float, uint) (fonction)'
description: 'Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à. Retourne l’état de l’opération. | SampleBias :: SampleBias (S, float, float, float, uint) (fonction)'
ms.assetid: 376F11E6-4FFF-4685-9285-9D6143C77F2D
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
ms.openlocfilehash: b91491b6ff43862a8dbbdb55120f5af8f80bec85
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974110"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function"></a><span data-ttu-id="69a73-106">SampleBias :: SampleBias (S, float, float, float, uint) (fonction)</span><span class="sxs-lookup"><span data-stu-id="69a73-106">SampleBias::SampleBias(S,float,float,float,uint) function</span></span>

<span data-ttu-id="69a73-107">Échantillonne une texture après avoir appliqué la valeur de biais au niveau de mipmap, avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="69a73-107">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="69a73-108">Retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="69a73-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="69a73-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69a73-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="69a73-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69a73-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69a73-111"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="69a73-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69a73-112">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="69a73-112">Type: **SamplerState**</span></span>

<span data-ttu-id="69a73-113">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="69a73-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="69a73-114">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="69a73-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="69a73-115">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69a73-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69a73-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="69a73-116">Type: **float**</span></span>

<span data-ttu-id="69a73-117">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="69a73-117">The texture coordinates.</span></span> <span data-ttu-id="69a73-118">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="69a73-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="69a73-119">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="69a73-119">Texture-Object Type</span></span>                    | <span data-ttu-id="69a73-120">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="69a73-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="69a73-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="69a73-121">Texture1D</span></span>                              | <span data-ttu-id="69a73-122">float</span><span class="sxs-lookup"><span data-stu-id="69a73-122">float</span></span>          |
| <span data-ttu-id="69a73-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="69a73-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="69a73-124">float2</span><span class="sxs-lookup"><span data-stu-id="69a73-124">float2</span></span>         |
| <span data-ttu-id="69a73-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="69a73-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="69a73-126">float3</span><span class="sxs-lookup"><span data-stu-id="69a73-126">float3</span></span>         |
| <span data-ttu-id="69a73-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="69a73-127">TextureCubeArray</span></span>                       | <span data-ttu-id="69a73-128">float4</span><span class="sxs-lookup"><span data-stu-id="69a73-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="69a73-129">*Biais* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69a73-129">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69a73-130">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="69a73-130">Type: **float**</span></span>

<span data-ttu-id="69a73-131">La valeur de biais, qui est un nombre à virgule flottante compris entre 0,0 et 1,0 inclus, est appliquée à un niveau MIP avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="69a73-131">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="69a73-132">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69a73-132">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69a73-133">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="69a73-133">Type: **float**</span></span>

<span data-ttu-id="69a73-134">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="69a73-134">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="69a73-135">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="69a73-135">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="69a73-136">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="69a73-136">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69a73-137">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="69a73-137">Type: **uint**</span></span>

<span data-ttu-id="69a73-138">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="69a73-138">The status of the operation.</span></span> <span data-ttu-id="69a73-139">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="69a73-139">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="69a73-140">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="69a73-140">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="69a73-141">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="69a73-141">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69a73-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69a73-142">Return value</span></span>

<span data-ttu-id="69a73-143">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="69a73-143">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="69a73-144">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="69a73-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="69a73-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69a73-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69a73-146">Méthodes SampleBias</span><span class="sxs-lookup"><span data-stu-id="69a73-146">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="69a73-147">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="69a73-147">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
