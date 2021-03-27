---
title: 'Texture2DArray :: GatherAlpha (S, float, Int2, Int2, Int2, Int2), fonction'
description: 'Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | Texture2DArray :: GatherAlpha (S, float, Int2, Int2, Int2, Int2), fonction'
ms.assetid: A7F96B45-A097-437B-A0D0-18555FF76544
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
ms.openlocfilehash: ff6910152c9ac133c819456b9ec7aaeb2406b791
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953580"
---
# <a name="texture2darraygatheralphasfloatint2int2int2int2-function"></a><span data-ttu-id="68497-105">Texture2DArray :: GatherAlpha (S, float, Int2, Int2, Int2, Int2), fonction</span><span class="sxs-lookup"><span data-stu-id="68497-105">Texture2DArray::GatherAlpha(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="68497-106">Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="68497-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="68497-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68497-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="68497-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68497-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68497-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="68497-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68497-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="68497-110">Type: **SamplerState**</span></span>

<span data-ttu-id="68497-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="68497-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="68497-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68497-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68497-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="68497-113">Type: **float**</span></span>

<span data-ttu-id="68497-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="68497-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="68497-115">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68497-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68497-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="68497-116">Type: **int2**</span></span>

<span data-ttu-id="68497-117">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="68497-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="68497-118">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68497-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68497-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="68497-119">Type: **int2**</span></span>

<span data-ttu-id="68497-120">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="68497-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="68497-121">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68497-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68497-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="68497-122">Type: **int2**</span></span>

<span data-ttu-id="68497-123">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="68497-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="68497-124">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68497-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68497-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="68497-125">Type: **int2**</span></span>

<span data-ttu-id="68497-126">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="68497-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68497-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68497-127">Return value</span></span>

<span data-ttu-id="68497-128">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="68497-128">Type: **TemplateType**</span></span>

<span data-ttu-id="68497-129">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="68497-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="68497-130">Notes</span><span class="sxs-lookup"><span data-stu-id="68497-130">Remarks</span></span>

<span data-ttu-id="68497-131">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="68497-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="68497-132">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="68497-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="68497-133">Sommet</span><span class="sxs-lookup"><span data-stu-id="68497-133">Vertex</span></span> | <span data-ttu-id="68497-134">Forme</span><span class="sxs-lookup"><span data-stu-id="68497-134">Hull</span></span> | <span data-ttu-id="68497-135">Domain</span><span class="sxs-lookup"><span data-stu-id="68497-135">Domain</span></span> | <span data-ttu-id="68497-136">Géométrie</span><span class="sxs-lookup"><span data-stu-id="68497-136">Geometry</span></span> | <span data-ttu-id="68497-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="68497-137">Pixel</span></span> | <span data-ttu-id="68497-138">Compute</span><span class="sxs-lookup"><span data-stu-id="68497-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="68497-139">x</span><span class="sxs-lookup"><span data-stu-id="68497-139">x</span></span>      | <span data-ttu-id="68497-140">x</span><span class="sxs-lookup"><span data-stu-id="68497-140">x</span></span>    | <span data-ttu-id="68497-141">x</span><span class="sxs-lookup"><span data-stu-id="68497-141">x</span></span>      | <span data-ttu-id="68497-142">x</span><span class="sxs-lookup"><span data-stu-id="68497-142">x</span></span>        | <span data-ttu-id="68497-143">x</span><span class="sxs-lookup"><span data-stu-id="68497-143">x</span></span>     | <span data-ttu-id="68497-144">x</span><span class="sxs-lookup"><span data-stu-id="68497-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="68497-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68497-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68497-146">Méthodes GatherAlpha</span><span class="sxs-lookup"><span data-stu-id="68497-146">GatherAlpha methods</span></span>](texture2darray-gatheralpha.md)
</dt> </dl>

 

 




