---
title: 'Texture2DArray :: Gather (S, float, int) (fonction)'
description: 'Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | Texture2DArray :: Gather (S, float, int) (fonction)'
ms.assetid: b0355158-01c8-45a1-bb5d-29a8c43b1685
keywords:
- Fonction de collecte HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46866df18a0836b311443a3dd411d74dfa7fb126
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991888"
---
# <a name="texture2darraygathersfloatint-function"></a><span data-ttu-id="45a48-105">Texture2DArray :: Gather (S, float, int) (fonction)</span><span class="sxs-lookup"><span data-stu-id="45a48-105">Texture2DArray::Gather(S,float,int) function</span></span>

<span data-ttu-id="45a48-106">Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="45a48-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="45a48-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45a48-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="45a48-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45a48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45a48-109"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45a48-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45a48-110">Type : **échantillonneur**</span><span class="sxs-lookup"><span data-stu-id="45a48-110">Type: **sampler**</span></span>

<span data-ttu-id="45a48-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="45a48-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="45a48-112">*emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45a48-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45a48-113">Type : **float3**</span><span class="sxs-lookup"><span data-stu-id="45a48-113">Type: **float3**</span></span>

<span data-ttu-id="45a48-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="45a48-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="45a48-115">*décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45a48-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45a48-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="45a48-116">Type: **int2**</span></span>

<span data-ttu-id="45a48-117">Décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="45a48-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45a48-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="45a48-118">Return value</span></span>

<span data-ttu-id="45a48-119">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="45a48-119">Type: **TemplateType**</span></span>

<span data-ttu-id="45a48-120">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="45a48-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="45a48-121">Notes</span><span class="sxs-lookup"><span data-stu-id="45a48-121">Remarks</span></span>

<span data-ttu-id="45a48-122">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="45a48-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="45a48-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="45a48-123">Vertex</span></span> | <span data-ttu-id="45a48-124">Forme</span><span class="sxs-lookup"><span data-stu-id="45a48-124">Hull</span></span> | <span data-ttu-id="45a48-125">Domain</span><span class="sxs-lookup"><span data-stu-id="45a48-125">Domain</span></span> | <span data-ttu-id="45a48-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="45a48-126">Geometry</span></span> | <span data-ttu-id="45a48-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="45a48-127">Pixel</span></span> | <span data-ttu-id="45a48-128">Compute</span><span class="sxs-lookup"><span data-stu-id="45a48-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="45a48-129">x</span><span class="sxs-lookup"><span data-stu-id="45a48-129">x</span></span>      | <span data-ttu-id="45a48-130">x</span><span class="sxs-lookup"><span data-stu-id="45a48-130">x</span></span>    | <span data-ttu-id="45a48-131">x</span><span class="sxs-lookup"><span data-stu-id="45a48-131">x</span></span>      | <span data-ttu-id="45a48-132">x</span><span class="sxs-lookup"><span data-stu-id="45a48-132">x</span></span>        | <span data-ttu-id="45a48-133">x</span><span class="sxs-lookup"><span data-stu-id="45a48-133">x</span></span>     | <span data-ttu-id="45a48-134">x</span><span class="sxs-lookup"><span data-stu-id="45a48-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="45a48-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45a48-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45a48-136">Méthodes de collecte</span><span class="sxs-lookup"><span data-stu-id="45a48-136">Gather methods</span></span>](texture2darray-gather.md)
</dt> <dt>

[<span data-ttu-id="45a48-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="45a48-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




