---
title: 'Texture2D :: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2), fonction'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison. | Texture2D :: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2), fonction'
ms.assetid: C8325626-F281-4D10-9299-0E5DA01BB1BD
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
ms.openlocfilehash: f5095fdb83814ab8c7d52add0fba05cbbf876678
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974298"
---
# <a name="texture2dgathercmpalphasfloatfloatint2int2int2int2-function"></a><span data-ttu-id="62dc0-105">Texture2D :: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2), fonction</span><span class="sxs-lookup"><span data-stu-id="62dc0-105">Texture2D::GatherCmpAlpha(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="62dc0-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="62dc0-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="62dc0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62dc0-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="62dc0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62dc0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62dc0-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="62dc0-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dc0-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="62dc0-110">Type: **SamplerState**</span></span>

<span data-ttu-id="62dc0-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="62dc0-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="62dc0-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62dc0-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dc0-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="62dc0-113">Type: **float**</span></span>

<span data-ttu-id="62dc0-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="62dc0-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="62dc0-115">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62dc0-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dc0-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="62dc0-116">Type: **float**</span></span>

<span data-ttu-id="62dc0-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="62dc0-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="62dc0-118">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62dc0-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dc0-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="62dc0-119">Type: **int2**</span></span>

<span data-ttu-id="62dc0-120">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="62dc0-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="62dc0-121">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62dc0-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dc0-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="62dc0-122">Type: **int2**</span></span>

<span data-ttu-id="62dc0-123">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="62dc0-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="62dc0-124">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62dc0-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dc0-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="62dc0-125">Type: **int2**</span></span>

<span data-ttu-id="62dc0-126">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="62dc0-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="62dc0-127">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62dc0-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62dc0-128">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="62dc0-128">Type: **int2**</span></span>

<span data-ttu-id="62dc0-129">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="62dc0-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62dc0-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62dc0-130">Return value</span></span>

<span data-ttu-id="62dc0-131">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="62dc0-131">Type: **TemplateType**</span></span>

<span data-ttu-id="62dc0-132">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="62dc0-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="62dc0-133">Notes</span><span class="sxs-lookup"><span data-stu-id="62dc0-133">Remarks</span></span>

<span data-ttu-id="62dc0-134">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="62dc0-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="62dc0-135">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="62dc0-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="62dc0-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="62dc0-136">Vertex</span></span> | <span data-ttu-id="62dc0-137">Forme</span><span class="sxs-lookup"><span data-stu-id="62dc0-137">Hull</span></span> | <span data-ttu-id="62dc0-138">Domain</span><span class="sxs-lookup"><span data-stu-id="62dc0-138">Domain</span></span> | <span data-ttu-id="62dc0-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="62dc0-139">Geometry</span></span> | <span data-ttu-id="62dc0-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="62dc0-140">Pixel</span></span> | <span data-ttu-id="62dc0-141">Compute</span><span class="sxs-lookup"><span data-stu-id="62dc0-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="62dc0-142">x</span><span class="sxs-lookup"><span data-stu-id="62dc0-142">x</span></span>      | <span data-ttu-id="62dc0-143">x</span><span class="sxs-lookup"><span data-stu-id="62dc0-143">x</span></span>    | <span data-ttu-id="62dc0-144">x</span><span class="sxs-lookup"><span data-stu-id="62dc0-144">x</span></span>      | <span data-ttu-id="62dc0-145">x</span><span class="sxs-lookup"><span data-stu-id="62dc0-145">x</span></span>        | <span data-ttu-id="62dc0-146">x</span><span class="sxs-lookup"><span data-stu-id="62dc0-146">x</span></span>     | <span data-ttu-id="62dc0-147">x</span><span class="sxs-lookup"><span data-stu-id="62dc0-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="62dc0-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62dc0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62dc0-149">Méthodes GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="62dc0-149">GatherCmpAlpha methods</span></span>](texture2d-gathercmpalpha.md)
</dt> </dl>

 

 




