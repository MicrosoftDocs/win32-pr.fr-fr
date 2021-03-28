---
title: 'Texture2D :: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2), fonction'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison. | Texture2D :: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2), fonction'
ms.assetid: B20A766E-0B4F-4FBA-A691-70ACE7BECF33
keywords:
- GatherCmpRed fonction HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f84467c798337ac2cc81283637636900933c9e41
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953617"
---
# <a name="texture2dgathercmpredsfloatfloatint2int2int2int2-function"></a><span data-ttu-id="56405-105">Texture2D :: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2), fonction</span><span class="sxs-lookup"><span data-stu-id="56405-105">Texture2D::GatherCmpRed(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="56405-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="56405-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="56405-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56405-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="56405-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56405-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56405-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="56405-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56405-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="56405-110">Type: **SamplerState**</span></span>

<span data-ttu-id="56405-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="56405-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="56405-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56405-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56405-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="56405-113">Type: **float**</span></span>

<span data-ttu-id="56405-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="56405-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="56405-115">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56405-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56405-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="56405-116">Type: **float**</span></span>

<span data-ttu-id="56405-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="56405-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="56405-118">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56405-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56405-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="56405-119">Type: **int2**</span></span>

<span data-ttu-id="56405-120">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="56405-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="56405-121">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56405-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56405-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="56405-122">Type: **int2**</span></span>

<span data-ttu-id="56405-123">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="56405-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="56405-124">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56405-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56405-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="56405-125">Type: **int2**</span></span>

<span data-ttu-id="56405-126">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="56405-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="56405-127">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56405-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56405-128">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="56405-128">Type: **int2**</span></span>

<span data-ttu-id="56405-129">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="56405-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56405-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56405-130">Return value</span></span>

<span data-ttu-id="56405-131">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="56405-131">Type: **TemplateType**</span></span>

<span data-ttu-id="56405-132">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="56405-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="56405-133">Notes</span><span class="sxs-lookup"><span data-stu-id="56405-133">Remarks</span></span>

<span data-ttu-id="56405-134">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="56405-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="56405-135">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="56405-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="56405-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="56405-136">Vertex</span></span> | <span data-ttu-id="56405-137">Forme</span><span class="sxs-lookup"><span data-stu-id="56405-137">Hull</span></span> | <span data-ttu-id="56405-138">Domain</span><span class="sxs-lookup"><span data-stu-id="56405-138">Domain</span></span> | <span data-ttu-id="56405-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="56405-139">Geometry</span></span> | <span data-ttu-id="56405-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="56405-140">Pixel</span></span> | <span data-ttu-id="56405-141">Compute</span><span class="sxs-lookup"><span data-stu-id="56405-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="56405-142">x</span><span class="sxs-lookup"><span data-stu-id="56405-142">x</span></span>      | <span data-ttu-id="56405-143">x</span><span class="sxs-lookup"><span data-stu-id="56405-143">x</span></span>    | <span data-ttu-id="56405-144">x</span><span class="sxs-lookup"><span data-stu-id="56405-144">x</span></span>      | <span data-ttu-id="56405-145">x</span><span class="sxs-lookup"><span data-stu-id="56405-145">x</span></span>        | <span data-ttu-id="56405-146">x</span><span class="sxs-lookup"><span data-stu-id="56405-146">x</span></span>     | <span data-ttu-id="56405-147">x</span><span class="sxs-lookup"><span data-stu-id="56405-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="56405-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56405-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56405-149">Méthodes GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="56405-149">GatherCmpRed methods</span></span>](texture2d-gathercmpred.md)
</dt> </dl>

 

 




