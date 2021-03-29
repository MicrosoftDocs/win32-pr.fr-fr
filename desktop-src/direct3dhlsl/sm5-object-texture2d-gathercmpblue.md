---
title: 'Texture2D :: GatherCmpBlue (S, float, float, int) (fonction)'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison. | Texture2D :: GatherCmpBlue (S, float, float, int) (fonction)'
ms.assetid: d8e03c55-18f1-4598-a700-9ba3a680d78a
keywords:
- GatherCmpBlue fonction HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eedeb21141c1e694effe4eb8c7be70c828aa0a3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991929"
---
# <a name="texture2dgathercmpbluesfloatfloatint-function"></a><span data-ttu-id="dfd31-105">Texture2D :: GatherCmpBlue (S, float, float, int) (fonction)</span><span class="sxs-lookup"><span data-stu-id="dfd31-105">Texture2D::GatherCmpBlue(S,float,float,int) function</span></span>

<span data-ttu-id="dfd31-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant bleu par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="dfd31-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd31-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfd31-107">Syntax</span></span>

``` syntax
float4 GatherCmpBlue(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="dfd31-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfd31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfd31-109"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfd31-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd31-110">Type : **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="dfd31-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="dfd31-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="dfd31-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="dfd31-112">*emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfd31-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd31-113">Type : **float2**</span><span class="sxs-lookup"><span data-stu-id="dfd31-113">Type: **float2**</span></span>

<span data-ttu-id="dfd31-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="dfd31-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="dfd31-115">*comparer la \_ valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfd31-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd31-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="dfd31-116">Type: **float**</span></span>

<span data-ttu-id="dfd31-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="dfd31-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="dfd31-118">*décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfd31-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd31-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="dfd31-119">Type: **int2**</span></span>

<span data-ttu-id="dfd31-120">Offset appliqué à la coordonnée de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="dfd31-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfd31-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dfd31-121">Return value</span></span>

<span data-ttu-id="dfd31-122">Type : **float4**</span><span class="sxs-lookup"><span data-stu-id="dfd31-122">Type: **float4**</span></span>

<span data-ttu-id="dfd31-123">Une valeur à quatre composants, chaque composant est le résultat d’une comparaison par composant.</span><span class="sxs-lookup"><span data-stu-id="dfd31-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfd31-124">Notes</span><span class="sxs-lookup"><span data-stu-id="dfd31-124">Remarks</span></span>

<span data-ttu-id="dfd31-125">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="dfd31-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="dfd31-126">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="dfd31-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="dfd31-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="dfd31-127">Vertex</span></span> | <span data-ttu-id="dfd31-128">Forme</span><span class="sxs-lookup"><span data-stu-id="dfd31-128">Hull</span></span> | <span data-ttu-id="dfd31-129">Domain</span><span class="sxs-lookup"><span data-stu-id="dfd31-129">Domain</span></span> | <span data-ttu-id="dfd31-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="dfd31-130">Geometry</span></span> | <span data-ttu-id="dfd31-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="dfd31-131">Pixel</span></span> | <span data-ttu-id="dfd31-132">Compute</span><span class="sxs-lookup"><span data-stu-id="dfd31-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="dfd31-133">x</span><span class="sxs-lookup"><span data-stu-id="dfd31-133">x</span></span>      | <span data-ttu-id="dfd31-134">x</span><span class="sxs-lookup"><span data-stu-id="dfd31-134">x</span></span>    | <span data-ttu-id="dfd31-135">x</span><span class="sxs-lookup"><span data-stu-id="dfd31-135">x</span></span>      | <span data-ttu-id="dfd31-136">x</span><span class="sxs-lookup"><span data-stu-id="dfd31-136">x</span></span>        | <span data-ttu-id="dfd31-137">x</span><span class="sxs-lookup"><span data-stu-id="dfd31-137">x</span></span>     | <span data-ttu-id="dfd31-138">x</span><span class="sxs-lookup"><span data-stu-id="dfd31-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dfd31-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfd31-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd31-140">Méthodes GatherCmpBlue</span><span class="sxs-lookup"><span data-stu-id="dfd31-140">GatherCmpBlue methods</span></span>](texture2d-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="dfd31-141">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="dfd31-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




