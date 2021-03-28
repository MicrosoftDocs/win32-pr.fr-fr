---
title: 'Texture2D :: GatherCmp (S, float, float, int) (fonction)'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison. | Texture2D :: GatherCmp (S, float, float, int) (fonction)'
ms.assetid: 1084bcb3-2834-400a-98ff-4e3182f63f20
keywords:
- GatherCmp fonction HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6005d8a95d3ec5ed5cddd9c4fbe6a42f36b7f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974066"
---
# <a name="texture2dgathercmpsfloatfloatint-function"></a><span data-ttu-id="7cf0f-105">Texture2D :: GatherCmp (S, float, float, int) (fonction)</span><span class="sxs-lookup"><span data-stu-id="7cf0f-105">Texture2D::GatherCmp(S,float,float,int) function</span></span>

<span data-ttu-id="7cf0f-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="7cf0f-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf0f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cf0f-107">Syntax</span></span>

``` syntax
float4 GatherCmp(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="7cf0f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cf0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cf0f-109"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cf0f-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf0f-110">Type : **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="7cf0f-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="7cf0f-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="7cf0f-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="7cf0f-112">*emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cf0f-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf0f-113">Type : **float2**</span><span class="sxs-lookup"><span data-stu-id="7cf0f-113">Type: **float2**</span></span>

<span data-ttu-id="7cf0f-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="7cf0f-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="7cf0f-115">*comparer la \_ valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cf0f-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf0f-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="7cf0f-116">Type: **float**</span></span>

<span data-ttu-id="7cf0f-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="7cf0f-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="7cf0f-118">*décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cf0f-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf0f-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="7cf0f-119">Type: **int2**</span></span>

<span data-ttu-id="7cf0f-120">Offset appliqué à la coordonnée de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="7cf0f-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cf0f-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7cf0f-121">Return value</span></span>

<span data-ttu-id="7cf0f-122">Type : **float4**</span><span class="sxs-lookup"><span data-stu-id="7cf0f-122">Type: **float4**</span></span>

<span data-ttu-id="7cf0f-123">Une valeur à quatre composants, chaque composant est le résultat d’une comparaison par composant.</span><span class="sxs-lookup"><span data-stu-id="7cf0f-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cf0f-124">Notes</span><span class="sxs-lookup"><span data-stu-id="7cf0f-124">Remarks</span></span>

<span data-ttu-id="7cf0f-125">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="7cf0f-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="7cf0f-126">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="7cf0f-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7cf0f-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="7cf0f-127">Vertex</span></span> | <span data-ttu-id="7cf0f-128">Forme</span><span class="sxs-lookup"><span data-stu-id="7cf0f-128">Hull</span></span> | <span data-ttu-id="7cf0f-129">Domain</span><span class="sxs-lookup"><span data-stu-id="7cf0f-129">Domain</span></span> | <span data-ttu-id="7cf0f-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="7cf0f-130">Geometry</span></span> | <span data-ttu-id="7cf0f-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="7cf0f-131">Pixel</span></span> | <span data-ttu-id="7cf0f-132">Compute</span><span class="sxs-lookup"><span data-stu-id="7cf0f-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7cf0f-133">x</span><span class="sxs-lookup"><span data-stu-id="7cf0f-133">x</span></span>      | <span data-ttu-id="7cf0f-134">x</span><span class="sxs-lookup"><span data-stu-id="7cf0f-134">x</span></span>    | <span data-ttu-id="7cf0f-135">x</span><span class="sxs-lookup"><span data-stu-id="7cf0f-135">x</span></span>      | <span data-ttu-id="7cf0f-136">x</span><span class="sxs-lookup"><span data-stu-id="7cf0f-136">x</span></span>        | <span data-ttu-id="7cf0f-137">x</span><span class="sxs-lookup"><span data-stu-id="7cf0f-137">x</span></span>     | <span data-ttu-id="7cf0f-138">x</span><span class="sxs-lookup"><span data-stu-id="7cf0f-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7cf0f-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cf0f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf0f-140">Méthodes GatherCmp</span><span class="sxs-lookup"><span data-stu-id="7cf0f-140">GatherCmp methods</span></span>](texture2d-gathercmp.md)
</dt> <dt>

[<span data-ttu-id="7cf0f-141">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="7cf0f-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




