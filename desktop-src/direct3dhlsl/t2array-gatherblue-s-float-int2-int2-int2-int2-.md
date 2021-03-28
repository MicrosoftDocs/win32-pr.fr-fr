---
title: GatherBlue (S, float, Int2, Int2, Int2, Int2), fonction (référence HLSL)
description: Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | GatherBlue (S, float, Int2, Int2, Int2, Int2), fonction (référence HLSL)
ms.assetid: 0DDD3235-4F12-4D74-975A-F70A271C1FC0
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
ms.openlocfilehash: a5676d9d6b25c6e67123c59dac14efa234386d4e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322393"
---
# <a name="gatherbluesfloatint2int2int2int2-function-hlsl-reference"></a><span data-ttu-id="ec20f-105">GatherBlue (S, float, Int2, Int2, Int2, Int2), fonction (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="ec20f-105">GatherBlue(S,float,int2,int2,int2,int2) function (HLSL reference)</span></span>

<span data-ttu-id="ec20f-106">Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="ec20f-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec20f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec20f-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="ec20f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec20f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec20f-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="ec20f-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec20f-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="ec20f-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ec20f-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="ec20f-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ec20f-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec20f-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec20f-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="ec20f-113">Type: **float**</span></span>

<span data-ttu-id="ec20f-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="ec20f-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ec20f-115">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec20f-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec20f-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="ec20f-116">Type: **int2**</span></span>

<span data-ttu-id="ec20f-117">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ec20f-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ec20f-118">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec20f-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec20f-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="ec20f-119">Type: **int2**</span></span>

<span data-ttu-id="ec20f-120">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ec20f-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ec20f-121">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec20f-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec20f-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="ec20f-122">Type: **int2**</span></span>

<span data-ttu-id="ec20f-123">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ec20f-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ec20f-124">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec20f-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec20f-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="ec20f-125">Type: **int2**</span></span>

<span data-ttu-id="ec20f-126">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ec20f-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec20f-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec20f-127">Return value</span></span>

<span data-ttu-id="ec20f-128">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ec20f-128">Type: **TemplateType**</span></span>

<span data-ttu-id="ec20f-129">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="ec20f-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec20f-130">Notes</span><span class="sxs-lookup"><span data-stu-id="ec20f-130">Remarks</span></span>

<span data-ttu-id="ec20f-131">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="ec20f-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ec20f-132">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="ec20f-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ec20f-133">Sommet</span><span class="sxs-lookup"><span data-stu-id="ec20f-133">Vertex</span></span> | <span data-ttu-id="ec20f-134">Forme</span><span class="sxs-lookup"><span data-stu-id="ec20f-134">Hull</span></span> | <span data-ttu-id="ec20f-135">Domain</span><span class="sxs-lookup"><span data-stu-id="ec20f-135">Domain</span></span> | <span data-ttu-id="ec20f-136">Géométrie</span><span class="sxs-lookup"><span data-stu-id="ec20f-136">Geometry</span></span> | <span data-ttu-id="ec20f-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="ec20f-137">Pixel</span></span> | <span data-ttu-id="ec20f-138">Compute</span><span class="sxs-lookup"><span data-stu-id="ec20f-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ec20f-139">x</span><span class="sxs-lookup"><span data-stu-id="ec20f-139">x</span></span>      | <span data-ttu-id="ec20f-140">x</span><span class="sxs-lookup"><span data-stu-id="ec20f-140">x</span></span>    | <span data-ttu-id="ec20f-141">x</span><span class="sxs-lookup"><span data-stu-id="ec20f-141">x</span></span>      | <span data-ttu-id="ec20f-142">x</span><span class="sxs-lookup"><span data-stu-id="ec20f-142">x</span></span>        | <span data-ttu-id="ec20f-143">x</span><span class="sxs-lookup"><span data-stu-id="ec20f-143">x</span></span>     | <span data-ttu-id="ec20f-144">x</span><span class="sxs-lookup"><span data-stu-id="ec20f-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ec20f-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec20f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec20f-146">Méthodes GatherBlue</span><span class="sxs-lookup"><span data-stu-id="ec20f-146">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> </dl>

 

 




