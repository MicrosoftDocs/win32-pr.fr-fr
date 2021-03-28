---
title: 'Texture2D :: GatherGreen (S, float, int) (fonction)'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant vert par rapport à une valeur de comparaison. | Texture2D :: GatherGreen (S, float, int) (fonction)'
ms.assetid: 97e1fb52-75f4-4e73-93f1-98b7a5925efc
keywords:
- GatherGreen fonction HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 722d7a3ac90fa3083b8f42f7704f5c9e0aeb1829
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992001"
---
# <a name="texture2dgathergreensfloatint-function"></a><span data-ttu-id="da59c-105">Texture2D :: GatherGreen (S, float, int) (fonction)</span><span class="sxs-lookup"><span data-stu-id="da59c-105">Texture2D::GatherGreen(S,float,int) function</span></span>

<span data-ttu-id="da59c-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant vert par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="da59c-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="da59c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da59c-107">Syntax</span></span>

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="da59c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da59c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da59c-109"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da59c-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da59c-110">Type : **échantillonneur**</span><span class="sxs-lookup"><span data-stu-id="da59c-110">Type: **sampler**</span></span>

<span data-ttu-id="da59c-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="da59c-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="da59c-112">*emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da59c-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da59c-113">Type : **float2**</span><span class="sxs-lookup"><span data-stu-id="da59c-113">Type: **float2**</span></span>

<span data-ttu-id="da59c-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="da59c-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="da59c-115">*décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da59c-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da59c-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="da59c-116">Type: **int2**</span></span>

<span data-ttu-id="da59c-117">Offset appliqué à la coordonnée de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="da59c-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da59c-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da59c-118">Return value</span></span>

<span data-ttu-id="da59c-119">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="da59c-119">Type: **TemplateType**</span></span>

<span data-ttu-id="da59c-120">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="da59c-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="da59c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="da59c-121">Remarks</span></span>

<span data-ttu-id="da59c-122">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="da59c-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="da59c-123">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="da59c-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="da59c-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="da59c-124">Vertex</span></span> | <span data-ttu-id="da59c-125">Forme</span><span class="sxs-lookup"><span data-stu-id="da59c-125">Hull</span></span> | <span data-ttu-id="da59c-126">Domain</span><span class="sxs-lookup"><span data-stu-id="da59c-126">Domain</span></span> | <span data-ttu-id="da59c-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="da59c-127">Geometry</span></span> | <span data-ttu-id="da59c-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="da59c-128">Pixel</span></span> | <span data-ttu-id="da59c-129">Compute</span><span class="sxs-lookup"><span data-stu-id="da59c-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="da59c-130">x</span><span class="sxs-lookup"><span data-stu-id="da59c-130">x</span></span>      | <span data-ttu-id="da59c-131">x</span><span class="sxs-lookup"><span data-stu-id="da59c-131">x</span></span>    | <span data-ttu-id="da59c-132">x</span><span class="sxs-lookup"><span data-stu-id="da59c-132">x</span></span>      | <span data-ttu-id="da59c-133">x</span><span class="sxs-lookup"><span data-stu-id="da59c-133">x</span></span>        | <span data-ttu-id="da59c-134">x</span><span class="sxs-lookup"><span data-stu-id="da59c-134">x</span></span>     | <span data-ttu-id="da59c-135">x</span><span class="sxs-lookup"><span data-stu-id="da59c-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="da59c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da59c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da59c-137">Méthodes GatherGreen</span><span class="sxs-lookup"><span data-stu-id="da59c-137">GatherGreen methods</span></span>](texture2d-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="da59c-138">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="da59c-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




