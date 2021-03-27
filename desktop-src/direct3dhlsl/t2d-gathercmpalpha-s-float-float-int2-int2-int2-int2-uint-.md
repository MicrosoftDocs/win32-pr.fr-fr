---
title: 'Texture2D :: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2, uint), fonction'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison, ainsi que l’état du mappage de mosaïque. | Texture2D :: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2, uint), fonction'
ms.assetid: 4DB56BE2-503A-4D51-89FB-E4DD91EBF028
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
ms.openlocfilehash: 5e1962dc10b5ef45ba3ad7d7196872fd4d27708c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211590"
---
# <a name="texture2dgathercmpalphasfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="12b1b-105">Texture2D :: GatherCmpAlpha (S, float, float, Int2, Int2, Int2, Int2, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="12b1b-105">Texture2D::GatherCmpAlpha(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="12b1b-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison, ainsi que l’état du mappage de mosaïque.</span><span class="sxs-lookup"><span data-stu-id="12b1b-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="12b1b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12b1b-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
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



## <a name="parameters"></a><span data-ttu-id="12b1b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12b1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12b1b-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="12b1b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1b-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="12b1b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="12b1b-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="12b1b-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="12b1b-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12b1b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1b-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="12b1b-113">Type: **float**</span></span>

<span data-ttu-id="12b1b-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="12b1b-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="12b1b-115">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12b1b-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1b-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="12b1b-116">Type: **float**</span></span>

<span data-ttu-id="12b1b-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="12b1b-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="12b1b-118">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12b1b-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1b-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="12b1b-119">Type: **int2**</span></span>

<span data-ttu-id="12b1b-120">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="12b1b-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="12b1b-121">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12b1b-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1b-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="12b1b-122">Type: **int2**</span></span>

<span data-ttu-id="12b1b-123">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="12b1b-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="12b1b-124">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12b1b-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1b-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="12b1b-125">Type: **int2**</span></span>

<span data-ttu-id="12b1b-126">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="12b1b-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="12b1b-127">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12b1b-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1b-128">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="12b1b-128">Type: **int2**</span></span>

<span data-ttu-id="12b1b-129">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="12b1b-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="12b1b-130">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="12b1b-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12b1b-131">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="12b1b-131">Type: **uint**</span></span>

<span data-ttu-id="12b1b-132">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="12b1b-132">The status of the operation.</span></span> <span data-ttu-id="12b1b-133">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="12b1b-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="12b1b-134">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="12b1b-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="12b1b-135">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="12b1b-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12b1b-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12b1b-136">Return value</span></span>

<span data-ttu-id="12b1b-137">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="12b1b-137">Type: **TemplateType**</span></span>

<span data-ttu-id="12b1b-138">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="12b1b-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="12b1b-139">Notes</span><span class="sxs-lookup"><span data-stu-id="12b1b-139">Remarks</span></span>

<span data-ttu-id="12b1b-140">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="12b1b-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="12b1b-141">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="12b1b-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="12b1b-142">Sommet</span><span class="sxs-lookup"><span data-stu-id="12b1b-142">Vertex</span></span> | <span data-ttu-id="12b1b-143">Forme</span><span class="sxs-lookup"><span data-stu-id="12b1b-143">Hull</span></span> | <span data-ttu-id="12b1b-144">Domain</span><span class="sxs-lookup"><span data-stu-id="12b1b-144">Domain</span></span> | <span data-ttu-id="12b1b-145">Géométrie</span><span class="sxs-lookup"><span data-stu-id="12b1b-145">Geometry</span></span> | <span data-ttu-id="12b1b-146">Pixel</span><span class="sxs-lookup"><span data-stu-id="12b1b-146">Pixel</span></span> | <span data-ttu-id="12b1b-147">Compute</span><span class="sxs-lookup"><span data-stu-id="12b1b-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="12b1b-148">x</span><span class="sxs-lookup"><span data-stu-id="12b1b-148">x</span></span>      | <span data-ttu-id="12b1b-149">x</span><span class="sxs-lookup"><span data-stu-id="12b1b-149">x</span></span>    | <span data-ttu-id="12b1b-150">x</span><span class="sxs-lookup"><span data-stu-id="12b1b-150">x</span></span>      | <span data-ttu-id="12b1b-151">x</span><span class="sxs-lookup"><span data-stu-id="12b1b-151">x</span></span>        | <span data-ttu-id="12b1b-152">x</span><span class="sxs-lookup"><span data-stu-id="12b1b-152">x</span></span>     | <span data-ttu-id="12b1b-153">x</span><span class="sxs-lookup"><span data-stu-id="12b1b-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="12b1b-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12b1b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12b1b-155">Méthodes GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="12b1b-155">GatherCmpAlpha methods</span></span>](texture2d-gathercmpalpha.md)
</dt> </dl>

 

 
