---
title: 'Texture2DArray :: GatherCmpBlue (S, float, float, Int2, Int2, Int2, Int2, uint), fonction'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison entre leur composant bleu et une valeur de comparaison, ainsi que l’état du mappage de mosaïque. | Texture2DArray :: GatherCmpBlue (S, float, float, Int2, Int2, Int2, Int2, uint), fonction'
ms.assetid: C47FD97F-2848-44F7-91E0-2120D08D89C7
keywords:
- GatherCmpBlue fonction HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 059c81d64520df98846b4b9397a5eb3ab0488991
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974406"
---
# <a name="texture2darraygathercmpbluesfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="e1eb8-105">Texture2DArray :: GatherCmpBlue (S, float, float, Int2, Int2, Int2, Int2, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="e1eb8-105">Texture2DArray::GatherCmpBlue(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="e1eb8-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison entre leur composant bleu et une valeur de comparaison, ainsi que l’état du mappage de mosaïque.</span><span class="sxs-lookup"><span data-stu-id="e1eb8-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1eb8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1eb8-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpBlue(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="e1eb8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1eb8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1eb8-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="e1eb8-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1eb8-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="e1eb8-110">Type: **SamplerState**</span></span>

<span data-ttu-id="e1eb8-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="e1eb8-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="e1eb8-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1eb8-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1eb8-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="e1eb8-113">Type: **float**</span></span>

<span data-ttu-id="e1eb8-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="e1eb8-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="e1eb8-115">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1eb8-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1eb8-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="e1eb8-116">Type: **float**</span></span>

<span data-ttu-id="e1eb8-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="e1eb8-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="e1eb8-118">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1eb8-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1eb8-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="e1eb8-119">Type: **int2**</span></span>

<span data-ttu-id="e1eb8-120">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="e1eb8-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e1eb8-121">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1eb8-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1eb8-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="e1eb8-122">Type: **int2**</span></span>

<span data-ttu-id="e1eb8-123">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="e1eb8-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e1eb8-124">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1eb8-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1eb8-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="e1eb8-125">Type: **int2**</span></span>

<span data-ttu-id="e1eb8-126">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="e1eb8-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e1eb8-127">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1eb8-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1eb8-128">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="e1eb8-128">Type: **int2**</span></span>

<span data-ttu-id="e1eb8-129">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="e1eb8-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e1eb8-130">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e1eb8-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1eb8-131">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="e1eb8-131">Type: **uint**</span></span>

<span data-ttu-id="e1eb8-132">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e1eb8-132">The status of the operation.</span></span> <span data-ttu-id="e1eb8-133">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="e1eb8-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e1eb8-134">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="e1eb8-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e1eb8-135">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="e1eb8-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1eb8-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1eb8-136">Return value</span></span>

<span data-ttu-id="e1eb8-137">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="e1eb8-137">Type: **TemplateType**</span></span>

<span data-ttu-id="e1eb8-138">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="e1eb8-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1eb8-139">Notes</span><span class="sxs-lookup"><span data-stu-id="e1eb8-139">Remarks</span></span>

<span data-ttu-id="e1eb8-140">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="e1eb8-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="e1eb8-141">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="e1eb8-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e1eb8-142">Sommet</span><span class="sxs-lookup"><span data-stu-id="e1eb8-142">Vertex</span></span> | <span data-ttu-id="e1eb8-143">Forme</span><span class="sxs-lookup"><span data-stu-id="e1eb8-143">Hull</span></span> | <span data-ttu-id="e1eb8-144">Domain</span><span class="sxs-lookup"><span data-stu-id="e1eb8-144">Domain</span></span> | <span data-ttu-id="e1eb8-145">Géométrie</span><span class="sxs-lookup"><span data-stu-id="e1eb8-145">Geometry</span></span> | <span data-ttu-id="e1eb8-146">Pixel</span><span class="sxs-lookup"><span data-stu-id="e1eb8-146">Pixel</span></span> | <span data-ttu-id="e1eb8-147">Compute</span><span class="sxs-lookup"><span data-stu-id="e1eb8-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e1eb8-148">x</span><span class="sxs-lookup"><span data-stu-id="e1eb8-148">x</span></span>      | <span data-ttu-id="e1eb8-149">x</span><span class="sxs-lookup"><span data-stu-id="e1eb8-149">x</span></span>    | <span data-ttu-id="e1eb8-150">x</span><span class="sxs-lookup"><span data-stu-id="e1eb8-150">x</span></span>      | <span data-ttu-id="e1eb8-151">x</span><span class="sxs-lookup"><span data-stu-id="e1eb8-151">x</span></span>        | <span data-ttu-id="e1eb8-152">x</span><span class="sxs-lookup"><span data-stu-id="e1eb8-152">x</span></span>     | <span data-ttu-id="e1eb8-153">x</span><span class="sxs-lookup"><span data-stu-id="e1eb8-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e1eb8-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1eb8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1eb8-155">Méthodes GatherCmpBlue</span><span class="sxs-lookup"><span data-stu-id="e1eb8-155">GatherCmpBlue methods</span></span>](texture2darray-gathercmpblue.md)
</dt> </dl>

 

 
