---
title: 'Texture2D :: GatherCmp (S, float, float, int, uint) (fonction)'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison avec l’état du mappage de mosaïques. | Texture2D :: GatherCmp (S, float, float, int, uint) (fonction)'
ms.assetid: A6610587-97C3-4CE5-86A7-3411D422BC8F
keywords:
- GatherCmp fonction HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be8246053e0f7ba6357bdd68dc59059fd225bbc8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974307"
---
# <a name="texture2dgathercmpsfloatfloatintuint-function"></a><span data-ttu-id="74909-105">Texture2D :: GatherCmp (S, float, float, int, uint) (fonction)</span><span class="sxs-lookup"><span data-stu-id="74909-105">Texture2D::GatherCmp(S,float,float,int,uint) function</span></span>

<span data-ttu-id="74909-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison avec l’état du mappage de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="74909-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="74909-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74909-107">Syntax</span></span>


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="74909-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74909-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74909-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="74909-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74909-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="74909-110">Type: **SamplerState**</span></span>

<span data-ttu-id="74909-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="74909-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="74909-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74909-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74909-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="74909-113">Type: **float**</span></span>

<span data-ttu-id="74909-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="74909-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="74909-115">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74909-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74909-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="74909-116">Type: **float**</span></span>

<span data-ttu-id="74909-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="74909-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="74909-118">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74909-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74909-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="74909-119">Type: **int2**</span></span>

<span data-ttu-id="74909-120">Décalage dans les texels appliqués aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="74909-120">The offset in texels applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="74909-121">Doit être une valeur littérale.</span><span class="sxs-lookup"><span data-stu-id="74909-121">Must be a literal value.</span></span>

</dd> <dt>

<span data-ttu-id="74909-122">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="74909-122">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74909-123">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="74909-123">Type: **uint**</span></span>

<span data-ttu-id="74909-124">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="74909-124">The status of the operation.</span></span> <span data-ttu-id="74909-125">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="74909-125">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="74909-126">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="74909-126">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="74909-127">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="74909-127">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74909-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74909-128">Return value</span></span>

<span data-ttu-id="74909-129">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="74909-129">Type: **TemplateType**</span></span>

<span data-ttu-id="74909-130">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="74909-130">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="74909-131">Notes</span><span class="sxs-lookup"><span data-stu-id="74909-131">Remarks</span></span>

<span data-ttu-id="74909-132">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="74909-132">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="74909-133">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="74909-133">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="74909-134">Sommet</span><span class="sxs-lookup"><span data-stu-id="74909-134">Vertex</span></span> | <span data-ttu-id="74909-135">Forme</span><span class="sxs-lookup"><span data-stu-id="74909-135">Hull</span></span> | <span data-ttu-id="74909-136">Domain</span><span class="sxs-lookup"><span data-stu-id="74909-136">Domain</span></span> | <span data-ttu-id="74909-137">Géométrie</span><span class="sxs-lookup"><span data-stu-id="74909-137">Geometry</span></span> | <span data-ttu-id="74909-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="74909-138">Pixel</span></span> | <span data-ttu-id="74909-139">Compute</span><span class="sxs-lookup"><span data-stu-id="74909-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="74909-140">x</span><span class="sxs-lookup"><span data-stu-id="74909-140">x</span></span>      | <span data-ttu-id="74909-141">x</span><span class="sxs-lookup"><span data-stu-id="74909-141">x</span></span>    | <span data-ttu-id="74909-142">x</span><span class="sxs-lookup"><span data-stu-id="74909-142">x</span></span>      | <span data-ttu-id="74909-143">x</span><span class="sxs-lookup"><span data-stu-id="74909-143">x</span></span>        | <span data-ttu-id="74909-144">x</span><span class="sxs-lookup"><span data-stu-id="74909-144">x</span></span>     | <span data-ttu-id="74909-145">x</span><span class="sxs-lookup"><span data-stu-id="74909-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="74909-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74909-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74909-147">Méthodes GatherCmp</span><span class="sxs-lookup"><span data-stu-id="74909-147">GatherCmp methods</span></span>](texture2d-gathercmp.md)
</dt> </dl>

 

 
