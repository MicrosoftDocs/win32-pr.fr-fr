---
title: 'Texture2D :: GatherRed (S, float, Int2, Int2, Int2, Int2), fonction'
description: 'Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | Texture2D :: GatherRed (S, float, Int2, Int2, Int2, Int2), fonction'
ms.assetid: 85C321CB-B77C-430B-921D-D56E5597B24A
keywords:
- GatherRed fonction HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b17e192388b6fc439d31cfe35eca99168da1c3f5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211365"
---
# <a name="texture2dgatherredsfloatint2int2int2int2-function"></a><span data-ttu-id="89cf9-105">Texture2D :: GatherRed (S, float, Int2, Int2, Int2, Int2), fonction</span><span class="sxs-lookup"><span data-stu-id="89cf9-105">Texture2D::GatherRed(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="89cf9-106">Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="89cf9-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="89cf9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89cf9-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="89cf9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89cf9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89cf9-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="89cf9-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="89cf9-110">Type: **SamplerState**</span></span>

<span data-ttu-id="89cf9-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="89cf9-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89cf9-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="89cf9-113">Type: **float**</span></span>

<span data-ttu-id="89cf9-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="89cf9-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-115">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89cf9-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="89cf9-116">Type: **int2**</span></span>

<span data-ttu-id="89cf9-117">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="89cf9-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-118">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89cf9-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="89cf9-119">Type: **int2**</span></span>

<span data-ttu-id="89cf9-120">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="89cf9-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-121">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89cf9-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="89cf9-122">Type: **int2**</span></span>

<span data-ttu-id="89cf9-123">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="89cf9-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-124">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89cf9-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="89cf9-125">Type: **int2**</span></span>

<span data-ttu-id="89cf9-126">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="89cf9-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89cf9-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89cf9-127">Return value</span></span>

<span data-ttu-id="89cf9-128">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="89cf9-128">Type: **TemplateType**</span></span>

<span data-ttu-id="89cf9-129">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="89cf9-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="89cf9-130">Notes</span><span class="sxs-lookup"><span data-stu-id="89cf9-130">Remarks</span></span>

<span data-ttu-id="89cf9-131">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="89cf9-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="89cf9-132">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="89cf9-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="89cf9-133">Sommet</span><span class="sxs-lookup"><span data-stu-id="89cf9-133">Vertex</span></span> | <span data-ttu-id="89cf9-134">Forme</span><span class="sxs-lookup"><span data-stu-id="89cf9-134">Hull</span></span> | <span data-ttu-id="89cf9-135">Domain</span><span class="sxs-lookup"><span data-stu-id="89cf9-135">Domain</span></span> | <span data-ttu-id="89cf9-136">Géométrie</span><span class="sxs-lookup"><span data-stu-id="89cf9-136">Geometry</span></span> | <span data-ttu-id="89cf9-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="89cf9-137">Pixel</span></span> | <span data-ttu-id="89cf9-138">Compute</span><span class="sxs-lookup"><span data-stu-id="89cf9-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="89cf9-139">x</span><span class="sxs-lookup"><span data-stu-id="89cf9-139">x</span></span>      | <span data-ttu-id="89cf9-140">x</span><span class="sxs-lookup"><span data-stu-id="89cf9-140">x</span></span>    | <span data-ttu-id="89cf9-141">x</span><span class="sxs-lookup"><span data-stu-id="89cf9-141">x</span></span>      | <span data-ttu-id="89cf9-142">x</span><span class="sxs-lookup"><span data-stu-id="89cf9-142">x</span></span>        | <span data-ttu-id="89cf9-143">x</span><span class="sxs-lookup"><span data-stu-id="89cf9-143">x</span></span>     | <span data-ttu-id="89cf9-144">x</span><span class="sxs-lookup"><span data-stu-id="89cf9-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="89cf9-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89cf9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89cf9-146">Méthodes GatherRed</span><span class="sxs-lookup"><span data-stu-id="89cf9-146">GatherRed methods</span></span>](texture2d-gatherred.md)
</dt> </dl>

 

 




