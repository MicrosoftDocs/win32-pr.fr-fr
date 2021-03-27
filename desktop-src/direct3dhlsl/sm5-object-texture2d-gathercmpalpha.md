---
title: 'Texture2D :: GatherCmpAlpha (S, float, float, int) (fonction)'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison. | Texture2D :: GatherCmpAlpha (S, float, float, int) (fonction)'
ms.assetid: 6fa60604-1eac-405d-bffa-3055569b7a09
keywords:
- GatherCmpAlpha fonction HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a7f7fcdc6e24cac5c04068fda7f781d0bdd376a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393911"
---
# <a name="texture2dgathercmpalphasfloatfloatint-function"></a><span data-ttu-id="6d406-105">Texture2D :: GatherCmpAlpha (S, float, float, int) (fonction)</span><span class="sxs-lookup"><span data-stu-id="6d406-105">Texture2D::GatherCmpAlpha(S,float,float,int) function</span></span>

<span data-ttu-id="6d406-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="6d406-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d406-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d406-107">Syntax</span></span>

``` syntax
float4 GatherCmpAlpha(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="6d406-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d406-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d406-109"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d406-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d406-110">Type : **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="6d406-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="6d406-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="6d406-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="6d406-112">*emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d406-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d406-113">Type : **float2**</span><span class="sxs-lookup"><span data-stu-id="6d406-113">Type: **float2**</span></span>

<span data-ttu-id="6d406-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="6d406-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="6d406-115">*comparer la \_ valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d406-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d406-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="6d406-116">Type: **float**</span></span>

<span data-ttu-id="6d406-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="6d406-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="6d406-118">*décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d406-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d406-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="6d406-119">Type: **int2**</span></span>

<span data-ttu-id="6d406-120">Offset appliqué à la coordonnée de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="6d406-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d406-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d406-121">Return value</span></span>

<span data-ttu-id="6d406-122">Type : **float4**</span><span class="sxs-lookup"><span data-stu-id="6d406-122">Type: **float4**</span></span>

<span data-ttu-id="6d406-123">Une valeur à quatre composants, chaque composant est le résultat d’une comparaison par composant.</span><span class="sxs-lookup"><span data-stu-id="6d406-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d406-124">Notes</span><span class="sxs-lookup"><span data-stu-id="6d406-124">Remarks</span></span>

<span data-ttu-id="6d406-125">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="6d406-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="6d406-126">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="6d406-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6d406-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="6d406-127">Vertex</span></span> | <span data-ttu-id="6d406-128">Forme</span><span class="sxs-lookup"><span data-stu-id="6d406-128">Hull</span></span> | <span data-ttu-id="6d406-129">Domain</span><span class="sxs-lookup"><span data-stu-id="6d406-129">Domain</span></span> | <span data-ttu-id="6d406-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="6d406-130">Geometry</span></span> | <span data-ttu-id="6d406-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="6d406-131">Pixel</span></span> | <span data-ttu-id="6d406-132">Compute</span><span class="sxs-lookup"><span data-stu-id="6d406-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6d406-133">x</span><span class="sxs-lookup"><span data-stu-id="6d406-133">x</span></span>      | <span data-ttu-id="6d406-134">x</span><span class="sxs-lookup"><span data-stu-id="6d406-134">x</span></span>    | <span data-ttu-id="6d406-135">x</span><span class="sxs-lookup"><span data-stu-id="6d406-135">x</span></span>      | <span data-ttu-id="6d406-136">x</span><span class="sxs-lookup"><span data-stu-id="6d406-136">x</span></span>        | <span data-ttu-id="6d406-137">x</span><span class="sxs-lookup"><span data-stu-id="6d406-137">x</span></span>     | <span data-ttu-id="6d406-138">x</span><span class="sxs-lookup"><span data-stu-id="6d406-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6d406-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d406-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d406-140">Méthodes GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="6d406-140">GatherCmpAlpha methods</span></span>](texture2d-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="6d406-141">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="6d406-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




