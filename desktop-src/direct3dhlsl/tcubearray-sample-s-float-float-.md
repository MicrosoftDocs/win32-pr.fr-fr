---
title: 'TextureCubeArray :: Sample (S, float, float), fonction'
description: 'Échantillonne une texture avec une valeur facultative pour fixer l’exemple de valeurs de niveau de détail (LOD) à. | TextureCubeArray :: Sample (S, float, float), fonction'
ms.assetid: E3BACA5E-18FC-4BD7-A8D8-C2808BDF1517
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
ms.openlocfilehash: 0f3f822ee334262dc50950064c6b4257aca3dd1f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974114"
---
# <a name="texturecubearraysamplesfloatfloat-function"></a><span data-ttu-id="657c5-105">TextureCubeArray :: Sample (S, float, float), fonction</span><span class="sxs-lookup"><span data-stu-id="657c5-105">TextureCubeArray::Sample(S,float,float) function</span></span>

<span data-ttu-id="657c5-106">Échantillonne une texture avec une valeur facultative pour fixer l’exemple de valeurs de niveau de détail (LOD) à.</span><span class="sxs-lookup"><span data-stu-id="657c5-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="657c5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="657c5-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="657c5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="657c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="657c5-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="657c5-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="657c5-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="657c5-110">Type: **SamplerState**</span></span>

<span data-ttu-id="657c5-111">État de l' [échantillonneur](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="657c5-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="657c5-112">Il s’agit d’un objet déclaré dans un fichier d’effet qui contient des assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="657c5-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="657c5-113">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="657c5-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="657c5-114">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="657c5-114">Type: **float**</span></span>

<span data-ttu-id="657c5-115">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="657c5-115">The texture coordinates.</span></span> <span data-ttu-id="657c5-116">Le type d’argument est dépendant du type de texture-objet.</span><span class="sxs-lookup"><span data-stu-id="657c5-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="657c5-117">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="657c5-117">Texture-Object Type</span></span>                    | <span data-ttu-id="657c5-118">Type de paramètre</span><span class="sxs-lookup"><span data-stu-id="657c5-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="657c5-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="657c5-119">Texture1D</span></span>                              | <span data-ttu-id="657c5-120">float</span><span class="sxs-lookup"><span data-stu-id="657c5-120">float</span></span>          |
| <span data-ttu-id="657c5-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="657c5-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="657c5-122">float2</span><span class="sxs-lookup"><span data-stu-id="657c5-122">float2</span></span>         |
| <span data-ttu-id="657c5-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="657c5-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="657c5-124">float3</span><span class="sxs-lookup"><span data-stu-id="657c5-124">float3</span></span>         |
| <span data-ttu-id="657c5-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="657c5-125">TextureCubeArray</span></span>                       | <span data-ttu-id="657c5-126">float4</span><span class="sxs-lookup"><span data-stu-id="657c5-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="657c5-127">*Clamp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="657c5-127">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="657c5-128">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="657c5-128">Type: **float**</span></span>

<span data-ttu-id="657c5-129">Valeur facultative pour fixer l’exemple de valeurs LOD à.</span><span class="sxs-lookup"><span data-stu-id="657c5-129">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="657c5-130">Par exemple, si vous transmettez 2.0 f pour la valeur clamp, vous vous assurez qu’aucun exemple individuel n’accède à un niveau MIP inférieur à 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="657c5-130">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="657c5-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="657c5-131">Return value</span></span>

<span data-ttu-id="657c5-132">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="657c5-132">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="657c5-133">Le format de texture, qui est l’une des valeurs typées énumérées dans le [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="657c5-133">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="657c5-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="657c5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="657c5-135">Exemples de méthodes</span><span class="sxs-lookup"><span data-stu-id="657c5-135">Sample methods</span></span>](texturecubearray-sample.md)
</dt> <dt>

[<span data-ttu-id="657c5-136">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="657c5-136">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
