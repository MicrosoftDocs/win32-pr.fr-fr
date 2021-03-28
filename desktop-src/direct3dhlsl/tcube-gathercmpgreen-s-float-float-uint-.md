---
title: 'TextureCube :: GatherCmpGreen (S, float, float, uint), fonction'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison entre leur composant vert et une valeur de comparaison, ainsi que l’état du mappage de mosaïque. | TextureCube :: GatherCmpGreen (S, float, float, uint), fonction'
ms.assetid: 3EFCEFE1-BFE2-4448-962E-108C3C0861E5
keywords:
- GatherCmpGreen fonction HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 910aef93a824b2725b13a177b5bbcfc8fa99aff9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322154"
---
# <a name="texturecubegathercmpgreensfloatfloatuint-function"></a><span data-ttu-id="9023d-105">TextureCube :: GatherCmpGreen (S, float, float, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="9023d-105">TextureCube::GatherCmpGreen(S,float,float,uint) function</span></span>

<span data-ttu-id="9023d-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison entre leur composant vert et une valeur de comparaison, ainsi que l’état du mappage de mosaïque.</span><span class="sxs-lookup"><span data-stu-id="9023d-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="9023d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9023d-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="9023d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9023d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9023d-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="9023d-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9023d-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="9023d-110">Type: **SamplerState**</span></span>

<span data-ttu-id="9023d-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="9023d-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="9023d-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9023d-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9023d-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="9023d-113">Type: **float**</span></span>

<span data-ttu-id="9023d-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="9023d-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="9023d-115">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9023d-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9023d-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="9023d-116">Type: **float**</span></span>

<span data-ttu-id="9023d-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="9023d-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="9023d-118">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9023d-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9023d-119">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="9023d-119">Type: **uint**</span></span>

<span data-ttu-id="9023d-120">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9023d-120">The status of the operation.</span></span> <span data-ttu-id="9023d-121">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="9023d-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="9023d-122">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="9023d-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="9023d-123">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="9023d-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9023d-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9023d-124">Return value</span></span>

<span data-ttu-id="9023d-125">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="9023d-125">Type: **TemplateType**</span></span>

<span data-ttu-id="9023d-126">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="9023d-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="9023d-127">Notes</span><span class="sxs-lookup"><span data-stu-id="9023d-127">Remarks</span></span>

<span data-ttu-id="9023d-128">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="9023d-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="9023d-129">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="9023d-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9023d-130">Sommet</span><span class="sxs-lookup"><span data-stu-id="9023d-130">Vertex</span></span> | <span data-ttu-id="9023d-131">Forme</span><span class="sxs-lookup"><span data-stu-id="9023d-131">Hull</span></span> | <span data-ttu-id="9023d-132">Domain</span><span class="sxs-lookup"><span data-stu-id="9023d-132">Domain</span></span> | <span data-ttu-id="9023d-133">Géométrie</span><span class="sxs-lookup"><span data-stu-id="9023d-133">Geometry</span></span> | <span data-ttu-id="9023d-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="9023d-134">Pixel</span></span> | <span data-ttu-id="9023d-135">Compute</span><span class="sxs-lookup"><span data-stu-id="9023d-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9023d-136">x</span><span class="sxs-lookup"><span data-stu-id="9023d-136">x</span></span>      | <span data-ttu-id="9023d-137">x</span><span class="sxs-lookup"><span data-stu-id="9023d-137">x</span></span>    | <span data-ttu-id="9023d-138">x</span><span class="sxs-lookup"><span data-stu-id="9023d-138">x</span></span>      | <span data-ttu-id="9023d-139">x</span><span class="sxs-lookup"><span data-stu-id="9023d-139">x</span></span>        | <span data-ttu-id="9023d-140">x</span><span class="sxs-lookup"><span data-stu-id="9023d-140">x</span></span>     | <span data-ttu-id="9023d-141">x</span><span class="sxs-lookup"><span data-stu-id="9023d-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9023d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9023d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9023d-143">Méthodes GatherCmpGreen</span><span class="sxs-lookup"><span data-stu-id="9023d-143">GatherCmpGreen methods</span></span>](texturecube-gathercmpgreen.md)
</dt> <dt>

[<span data-ttu-id="9023d-144">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="9023d-144">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
