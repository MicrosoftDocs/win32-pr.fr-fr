---
title: 'Texture2D :: GatherAlpha (S, float, int) (fonction)'
description: 'Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | Texture2D :: GatherAlpha (S, float, int) (fonction)'
ms.assetid: 4c980e06-d768-479e-bee3-1b2541c23038
keywords:
- GatherAlpha fonction HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36561e6bc16a84e0a377292ededf58df3c15f800
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974279"
---
# <a name="texture2dgatheralphasfloatint-function"></a><span data-ttu-id="d5849-105">Texture2D :: GatherAlpha (S, float, int) (fonction)</span><span class="sxs-lookup"><span data-stu-id="d5849-105">Texture2D::GatherAlpha(S,float,int) function</span></span>

<span data-ttu-id="d5849-106">Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="d5849-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5849-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5849-107">Syntax</span></span>

``` syntax
TemplateType GatherAlpha(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="d5849-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5849-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5849-109"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5849-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5849-110">Type : **échantillonneur**</span><span class="sxs-lookup"><span data-stu-id="d5849-110">Type: **sampler**</span></span>

<span data-ttu-id="d5849-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="d5849-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="d5849-112">*emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5849-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5849-113">Type : **float2**</span><span class="sxs-lookup"><span data-stu-id="d5849-113">Type: **float2**</span></span>

<span data-ttu-id="d5849-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="d5849-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="d5849-115">*décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5849-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5849-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="d5849-116">Type: **int2**</span></span>

<span data-ttu-id="d5849-117">Offset appliqué à la coordonnée de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="d5849-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5849-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5849-118">Return value</span></span>

<span data-ttu-id="d5849-119">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="d5849-119">Type: **TemplateType**</span></span>

<span data-ttu-id="d5849-120">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="d5849-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5849-121">Notes</span><span class="sxs-lookup"><span data-stu-id="d5849-121">Remarks</span></span>

<span data-ttu-id="d5849-122">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="d5849-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="d5849-123">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="d5849-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d5849-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="d5849-124">Vertex</span></span> | <span data-ttu-id="d5849-125">Forme</span><span class="sxs-lookup"><span data-stu-id="d5849-125">Hull</span></span> | <span data-ttu-id="d5849-126">Domain</span><span class="sxs-lookup"><span data-stu-id="d5849-126">Domain</span></span> | <span data-ttu-id="d5849-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="d5849-127">Geometry</span></span> | <span data-ttu-id="d5849-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="d5849-128">Pixel</span></span> | <span data-ttu-id="d5849-129">Compute</span><span class="sxs-lookup"><span data-stu-id="d5849-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d5849-130">x</span><span class="sxs-lookup"><span data-stu-id="d5849-130">x</span></span>      | <span data-ttu-id="d5849-131">x</span><span class="sxs-lookup"><span data-stu-id="d5849-131">x</span></span>    | <span data-ttu-id="d5849-132">x</span><span class="sxs-lookup"><span data-stu-id="d5849-132">x</span></span>      | <span data-ttu-id="d5849-133">x</span><span class="sxs-lookup"><span data-stu-id="d5849-133">x</span></span>        | <span data-ttu-id="d5849-134">x</span><span class="sxs-lookup"><span data-stu-id="d5849-134">x</span></span>     | <span data-ttu-id="d5849-135">x</span><span class="sxs-lookup"><span data-stu-id="d5849-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d5849-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5849-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5849-137">Méthodes GatherAlpha</span><span class="sxs-lookup"><span data-stu-id="d5849-137">GatherAlpha methods</span></span>](texture2d-gatheralpha.md)
</dt> <dt>

[<span data-ttu-id="d5849-138">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="d5849-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




