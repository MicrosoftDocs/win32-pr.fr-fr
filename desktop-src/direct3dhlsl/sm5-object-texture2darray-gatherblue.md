---
title: 'Texture2DArray :: GatherBlue (S, float, int) (fonction)'
description: 'Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | Texture2DArray :: GatherBlue (S, float, int) (fonction)'
ms.assetid: f81596b5-afd1-4baf-b6c0-ca4661a3ef22
keywords:
- GatherBlue fonction HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1844b898deca767b04aba438f4784a54a5afa112
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991928"
---
# <a name="texture2darraygatherbluesfloatint-function"></a><span data-ttu-id="0a4f8-105">Texture2DArray :: GatherBlue (S, float, int) (fonction)</span><span class="sxs-lookup"><span data-stu-id="0a4f8-105">Texture2DArray::GatherBlue(S,float,int) function</span></span>

<span data-ttu-id="0a4f8-106">Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="0a4f8-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4f8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a4f8-107">Syntax</span></span>

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="0a4f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a4f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a4f8-109"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a4f8-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4f8-110">Type : **échantillonneur**</span><span class="sxs-lookup"><span data-stu-id="0a4f8-110">Type: **sampler**</span></span>

<span data-ttu-id="0a4f8-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="0a4f8-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f8-112">*emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a4f8-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4f8-113">Type : **float3**</span><span class="sxs-lookup"><span data-stu-id="0a4f8-113">Type: **float3**</span></span>

<span data-ttu-id="0a4f8-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="0a4f8-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="0a4f8-115">*décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a4f8-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4f8-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="0a4f8-116">Type: **int2**</span></span>

<span data-ttu-id="0a4f8-117">Offset appliqué à la coordonnée de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="0a4f8-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a4f8-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a4f8-118">Return value</span></span>

<span data-ttu-id="0a4f8-119">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="0a4f8-119">Type: **TemplateType**</span></span>

<span data-ttu-id="0a4f8-120">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="0a4f8-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a4f8-121">Notes</span><span class="sxs-lookup"><span data-stu-id="0a4f8-121">Remarks</span></span>

<span data-ttu-id="0a4f8-122">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="0a4f8-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="0a4f8-123">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="0a4f8-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0a4f8-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="0a4f8-124">Vertex</span></span> | <span data-ttu-id="0a4f8-125">Forme</span><span class="sxs-lookup"><span data-stu-id="0a4f8-125">Hull</span></span> | <span data-ttu-id="0a4f8-126">Domain</span><span class="sxs-lookup"><span data-stu-id="0a4f8-126">Domain</span></span> | <span data-ttu-id="0a4f8-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="0a4f8-127">Geometry</span></span> | <span data-ttu-id="0a4f8-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="0a4f8-128">Pixel</span></span> | <span data-ttu-id="0a4f8-129">Compute</span><span class="sxs-lookup"><span data-stu-id="0a4f8-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0a4f8-130">x</span><span class="sxs-lookup"><span data-stu-id="0a4f8-130">x</span></span>      | <span data-ttu-id="0a4f8-131">x</span><span class="sxs-lookup"><span data-stu-id="0a4f8-131">x</span></span>    | <span data-ttu-id="0a4f8-132">x</span><span class="sxs-lookup"><span data-stu-id="0a4f8-132">x</span></span>      | <span data-ttu-id="0a4f8-133">x</span><span class="sxs-lookup"><span data-stu-id="0a4f8-133">x</span></span>        | <span data-ttu-id="0a4f8-134">x</span><span class="sxs-lookup"><span data-stu-id="0a4f8-134">x</span></span>     | <span data-ttu-id="0a4f8-135">x</span><span class="sxs-lookup"><span data-stu-id="0a4f8-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0a4f8-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a4f8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4f8-137">Méthodes GatherBlue</span><span class="sxs-lookup"><span data-stu-id="0a4f8-137">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="0a4f8-138">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="0a4f8-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




