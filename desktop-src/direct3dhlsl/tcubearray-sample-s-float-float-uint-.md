---
title: 'TextureCubeArray :: Sample (S, float, float, uint), fonction'
description: 'Échantillonne une texture avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération. | TextureCubeArray :: Sample (S, float, float, uint), fonction'
ms.assetid: 5645841D-A32E-452E-873C-E070CF6A4C00
keywords:
- Exemple de fonction HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 24e6d77698507f0d1673b66954db8e78466ac728
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761702"
---
# <a name="texturecubearraysamplesfloatfloatuint-function"></a><span data-ttu-id="14fc5-105">TextureCubeArray :: Sample (S, float, float, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="14fc5-105">TextureCubeArray::Sample(S,float,float,uint) function</span></span>

<span data-ttu-id="14fc5-106">Échantillonne une texture avec une valeur facultative pour fixer des valeurs d’exemple de niveau de détail (LOD) à et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="14fc5-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to, and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="14fc5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14fc5-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="14fc5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14fc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14fc5-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="14fc5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14fc5-110">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="14fc5-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="14fc5-111">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="14fc5-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="14fc5-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14fc5-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14fc5-113">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="14fc5-113">The texture coordinates.</span></span> <span data-ttu-id="14fc5-114">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="14fc5-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="14fc5-115">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="14fc5-115">Texture-Object Type</span></span>                    | <span data-ttu-id="14fc5-116">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="14fc5-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="14fc5-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="14fc5-117">Texture1D</span></span>                              | <span data-ttu-id="14fc5-118">float</span><span class="sxs-lookup"><span data-stu-id="14fc5-118">float</span></span>          |
| <span data-ttu-id="14fc5-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="14fc5-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="14fc5-120">float2</span><span class="sxs-lookup"><span data-stu-id="14fc5-120">float2</span></span>         |
| <span data-ttu-id="14fc5-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="14fc5-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="14fc5-122">float3</span><span class="sxs-lookup"><span data-stu-id="14fc5-122">float3</span></span>         |
| <span data-ttu-id="14fc5-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="14fc5-123">TextureCubeArray</span></span>                       | <span data-ttu-id="14fc5-124">float4</span><span class="sxs-lookup"><span data-stu-id="14fc5-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="14fc5-125">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14fc5-125">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14fc5-126">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="14fc5-126">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="14fc5-127">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="14fc5-127">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="14fc5-128">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="14fc5-128">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14fc5-129">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="14fc5-129">The status of the operation.</span></span> <span data-ttu-id="14fc5-130">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="14fc5-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="14fc5-131">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="14fc5-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="14fc5-132">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="14fc5-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14fc5-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14fc5-133">Return value</span></span>

<span data-ttu-id="14fc5-134">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="14fc5-134">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="14fc5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14fc5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14fc5-136">Exemples de méthodes</span><span class="sxs-lookup"><span data-stu-id="14fc5-136">Sample methods</span></span>](texturecubearray-sample.md)
</dt> <dt>

[<span data-ttu-id="14fc5-137">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="14fc5-137">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
