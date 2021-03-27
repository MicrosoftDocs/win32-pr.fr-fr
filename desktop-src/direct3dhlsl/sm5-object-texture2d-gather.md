---
title: 'Texture2D :: Gather (S, float, int) (fonction)'
description: 'Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | Texture2D :: Gather (S, float, int) (fonction)'
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
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
ms.openlocfilehash: 4d0a58be0580572441f91a3b3f637601d70cd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761761"
---
# <a name="texture2dgathersfloatint-function"></a><span data-ttu-id="70d17-105">Texture2D :: Gather (S, float, int) (fonction)</span><span class="sxs-lookup"><span data-stu-id="70d17-105">Texture2D::Gather(S,float,int) function</span></span>

<span data-ttu-id="70d17-106">Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="70d17-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="70d17-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70d17-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="70d17-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70d17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70d17-109"> \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70d17-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70d17-110">Type : **échantillonneur**</span><span class="sxs-lookup"><span data-stu-id="70d17-110">Type: **sampler**</span></span>

<span data-ttu-id="70d17-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="70d17-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="70d17-112">*emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70d17-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70d17-113">Type : **float2**</span><span class="sxs-lookup"><span data-stu-id="70d17-113">Type: **float2**</span></span>

<span data-ttu-id="70d17-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="70d17-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="70d17-115">*décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70d17-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70d17-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="70d17-116">Type: **int2**</span></span>

<span data-ttu-id="70d17-117">Décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="70d17-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70d17-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70d17-118">Return value</span></span>

<span data-ttu-id="70d17-119">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="70d17-119">Type: **TemplateType**</span></span>

<span data-ttu-id="70d17-120">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="70d17-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="70d17-121">Notes</span><span class="sxs-lookup"><span data-stu-id="70d17-121">Remarks</span></span>

<span data-ttu-id="70d17-122">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="70d17-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="70d17-123">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="70d17-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="70d17-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="70d17-124">Vertex</span></span> | <span data-ttu-id="70d17-125">Forme</span><span class="sxs-lookup"><span data-stu-id="70d17-125">Hull</span></span> | <span data-ttu-id="70d17-126">Domain</span><span class="sxs-lookup"><span data-stu-id="70d17-126">Domain</span></span> | <span data-ttu-id="70d17-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="70d17-127">Geometry</span></span> | <span data-ttu-id="70d17-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="70d17-128">Pixel</span></span> | <span data-ttu-id="70d17-129">Compute</span><span class="sxs-lookup"><span data-stu-id="70d17-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="70d17-130">x</span><span class="sxs-lookup"><span data-stu-id="70d17-130">x</span></span>      | <span data-ttu-id="70d17-131">x</span><span class="sxs-lookup"><span data-stu-id="70d17-131">x</span></span>    | <span data-ttu-id="70d17-132">x</span><span class="sxs-lookup"><span data-stu-id="70d17-132">x</span></span>      | <span data-ttu-id="70d17-133">x</span><span class="sxs-lookup"><span data-stu-id="70d17-133">x</span></span>        | <span data-ttu-id="70d17-134">x</span><span class="sxs-lookup"><span data-stu-id="70d17-134">x</span></span>     | <span data-ttu-id="70d17-135">x</span><span class="sxs-lookup"><span data-stu-id="70d17-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="70d17-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70d17-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70d17-137">Méthodes de collecte</span><span class="sxs-lookup"><span data-stu-id="70d17-137">Gather methods</span></span>](texture2d-gather.md)
</dt> <dt>

[<span data-ttu-id="70d17-138">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="70d17-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




