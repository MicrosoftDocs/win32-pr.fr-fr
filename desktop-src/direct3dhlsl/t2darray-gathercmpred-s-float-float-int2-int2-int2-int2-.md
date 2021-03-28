---
title: 'Texture2DArray :: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2), fonction'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison. | Texture2DArray :: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2), fonction'
ms.assetid: B436FB9A-C55C-477F-B8BE-933B1EB04AE1
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
ms.openlocfilehash: 2d621bf26d097eeac17962fd14557f73f295a2e3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043040"
---
# <a name="texture2darraygathercmpredsfloatfloatint2int2int2int2-function"></a><span data-ttu-id="c3a91-105">Texture2DArray :: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2), fonction</span><span class="sxs-lookup"><span data-stu-id="c3a91-105">Texture2DArray::GatherCmpRed(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="c3a91-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant rouge par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="c3a91-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a91-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3a91-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c3a91-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3a91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3a91-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="c3a91-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a91-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="c3a91-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c3a91-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="c3a91-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="c3a91-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3a91-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a91-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="c3a91-113">Type: **float**</span></span>

<span data-ttu-id="c3a91-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="c3a91-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="c3a91-115">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3a91-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a91-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="c3a91-116">Type: **float**</span></span>

<span data-ttu-id="c3a91-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="c3a91-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="c3a91-118">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3a91-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a91-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="c3a91-119">Type: **int2**</span></span>

<span data-ttu-id="c3a91-120">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="c3a91-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c3a91-121">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3a91-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a91-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="c3a91-122">Type: **int2**</span></span>

<span data-ttu-id="c3a91-123">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="c3a91-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c3a91-124">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3a91-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a91-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="c3a91-125">Type: **int2**</span></span>

<span data-ttu-id="c3a91-126">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="c3a91-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c3a91-127">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3a91-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a91-128">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="c3a91-128">Type: **int2**</span></span>

<span data-ttu-id="c3a91-129">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="c3a91-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3a91-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3a91-130">Return value</span></span>

<span data-ttu-id="c3a91-131">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="c3a91-131">Type: **TemplateType**</span></span>

<span data-ttu-id="c3a91-132">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="c3a91-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3a91-133">Notes</span><span class="sxs-lookup"><span data-stu-id="c3a91-133">Remarks</span></span>

<span data-ttu-id="c3a91-134">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="c3a91-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="c3a91-135">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="c3a91-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c3a91-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="c3a91-136">Vertex</span></span> | <span data-ttu-id="c3a91-137">Forme</span><span class="sxs-lookup"><span data-stu-id="c3a91-137">Hull</span></span> | <span data-ttu-id="c3a91-138">Domain</span><span class="sxs-lookup"><span data-stu-id="c3a91-138">Domain</span></span> | <span data-ttu-id="c3a91-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="c3a91-139">Geometry</span></span> | <span data-ttu-id="c3a91-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="c3a91-140">Pixel</span></span> | <span data-ttu-id="c3a91-141">Compute</span><span class="sxs-lookup"><span data-stu-id="c3a91-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c3a91-142">x</span><span class="sxs-lookup"><span data-stu-id="c3a91-142">x</span></span>      | <span data-ttu-id="c3a91-143">x</span><span class="sxs-lookup"><span data-stu-id="c3a91-143">x</span></span>    | <span data-ttu-id="c3a91-144">x</span><span class="sxs-lookup"><span data-stu-id="c3a91-144">x</span></span>      | <span data-ttu-id="c3a91-145">x</span><span class="sxs-lookup"><span data-stu-id="c3a91-145">x</span></span>        | <span data-ttu-id="c3a91-146">x</span><span class="sxs-lookup"><span data-stu-id="c3a91-146">x</span></span>     | <span data-ttu-id="c3a91-147">x</span><span class="sxs-lookup"><span data-stu-id="c3a91-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c3a91-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3a91-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a91-149">Méthodes GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="c3a91-149">GatherCmpRed methods</span></span>](texture2darray-gathercmpred.md)
</dt> </dl>

 

 




