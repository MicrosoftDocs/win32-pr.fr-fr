---
title: 'Texture2D :: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2, uint), fonction'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison entre le composant rouge et une valeur de comparaison, ainsi que l’état du mappage de mosaïque. | Texture2D :: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2, uint), fonction'
ms.assetid: 69B1F8FF-CE29-49DD-B756-3308E11D866D
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
ms.openlocfilehash: 2d872623d7dcc8ea599e3c790493f2e1a8596b91
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991913"
---
# <a name="texture2dgathercmpredsfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="db45b-105">Texture2D :: GatherCmpRed (S, float, float, Int2, Int2, Int2, Int2, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="db45b-105">Texture2D::GatherCmpRed(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="db45b-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison entre le composant rouge et une valeur de comparaison, ainsi que l’état du mappage de mosaïque.</span><span class="sxs-lookup"><span data-stu-id="db45b-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="db45b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db45b-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
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



## <a name="parameters"></a><span data-ttu-id="db45b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db45b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db45b-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="db45b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db45b-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="db45b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="db45b-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="db45b-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="db45b-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db45b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db45b-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="db45b-113">Type: **float**</span></span>

<span data-ttu-id="db45b-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="db45b-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="db45b-115">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db45b-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db45b-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="db45b-116">Type: **float**</span></span>

<span data-ttu-id="db45b-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="db45b-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="db45b-118">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db45b-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db45b-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="db45b-119">Type: **int2**</span></span>

<span data-ttu-id="db45b-120">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="db45b-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="db45b-121">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db45b-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db45b-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="db45b-122">Type: **int2**</span></span>

<span data-ttu-id="db45b-123">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="db45b-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="db45b-124">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db45b-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db45b-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="db45b-125">Type: **int2**</span></span>

<span data-ttu-id="db45b-126">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="db45b-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="db45b-127">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db45b-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db45b-128">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="db45b-128">Type: **int2**</span></span>

<span data-ttu-id="db45b-129">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="db45b-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="db45b-130">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="db45b-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db45b-131">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="db45b-131">Type: **uint**</span></span>

<span data-ttu-id="db45b-132">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="db45b-132">The status of the operation.</span></span> <span data-ttu-id="db45b-133">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="db45b-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="db45b-134">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="db45b-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="db45b-135">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="db45b-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db45b-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db45b-136">Return value</span></span>

<span data-ttu-id="db45b-137">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="db45b-137">Type: **TemplateType**</span></span>

<span data-ttu-id="db45b-138">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="db45b-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="db45b-139">Notes</span><span class="sxs-lookup"><span data-stu-id="db45b-139">Remarks</span></span>

<span data-ttu-id="db45b-140">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="db45b-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="db45b-141">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="db45b-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="db45b-142">Sommet</span><span class="sxs-lookup"><span data-stu-id="db45b-142">Vertex</span></span> | <span data-ttu-id="db45b-143">Forme</span><span class="sxs-lookup"><span data-stu-id="db45b-143">Hull</span></span> | <span data-ttu-id="db45b-144">Domain</span><span class="sxs-lookup"><span data-stu-id="db45b-144">Domain</span></span> | <span data-ttu-id="db45b-145">Géométrie</span><span class="sxs-lookup"><span data-stu-id="db45b-145">Geometry</span></span> | <span data-ttu-id="db45b-146">Pixel</span><span class="sxs-lookup"><span data-stu-id="db45b-146">Pixel</span></span> | <span data-ttu-id="db45b-147">Compute</span><span class="sxs-lookup"><span data-stu-id="db45b-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="db45b-148">x</span><span class="sxs-lookup"><span data-stu-id="db45b-148">x</span></span>      | <span data-ttu-id="db45b-149">x</span><span class="sxs-lookup"><span data-stu-id="db45b-149">x</span></span>    | <span data-ttu-id="db45b-150">x</span><span class="sxs-lookup"><span data-stu-id="db45b-150">x</span></span>      | <span data-ttu-id="db45b-151">x</span><span class="sxs-lookup"><span data-stu-id="db45b-151">x</span></span>        | <span data-ttu-id="db45b-152">x</span><span class="sxs-lookup"><span data-stu-id="db45b-152">x</span></span>     | <span data-ttu-id="db45b-153">x</span><span class="sxs-lookup"><span data-stu-id="db45b-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="db45b-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db45b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db45b-155">Méthodes GatherCmpRed</span><span class="sxs-lookup"><span data-stu-id="db45b-155">GatherCmpRed methods</span></span>](texture2d-gathercmpred.md)
</dt> </dl>

 

 
