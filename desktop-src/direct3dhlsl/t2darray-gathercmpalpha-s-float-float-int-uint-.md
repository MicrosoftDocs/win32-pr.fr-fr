---
title: 'Texture2DArray :: GatherCmpAlpha (S, float, float, int, uint) (fonction)'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison, ainsi que l’état du mappage de mosaïque. | Texture2DArray :: GatherCmpAlpha (S, float, float, int, uint) (fonction)'
ms.assetid: DCCF7F40-8A0D-47B8-910A-508382D3AE3F
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
ms.openlocfilehash: afd427c5af46f333deb0b05de551f8081d9bd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322037"
---
# <a name="texture2darraygathercmpalphasfloatfloatintuint-function"></a><span data-ttu-id="af9a3-105">Texture2DArray :: GatherCmpAlpha (S, float, float, int, uint) (fonction)</span><span class="sxs-lookup"><span data-stu-id="af9a3-105">Texture2DArray::GatherCmpAlpha(S,float,float,int,uint) function</span></span>

<span data-ttu-id="af9a3-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison de leur composant alpha par rapport à une valeur de comparaison, ainsi que l’état du mappage de mosaïque.</span><span class="sxs-lookup"><span data-stu-id="af9a3-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9a3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af9a3-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="af9a3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af9a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af9a3-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="af9a3-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9a3-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="af9a3-110">Type: **SamplerState**</span></span>

<span data-ttu-id="af9a3-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="af9a3-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="af9a3-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af9a3-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9a3-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="af9a3-113">Type: **float**</span></span>

<span data-ttu-id="af9a3-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="af9a3-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="af9a3-115">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af9a3-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9a3-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="af9a3-116">Type: **float**</span></span>

<span data-ttu-id="af9a3-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="af9a3-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="af9a3-118">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af9a3-118">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9a3-119">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="af9a3-119">Type: **int**</span></span>

<span data-ttu-id="af9a3-120">Décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="af9a3-120">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="af9a3-121">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="af9a3-121">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af9a3-122">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="af9a3-122">Type: **uint**</span></span>

<span data-ttu-id="af9a3-123">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="af9a3-123">The status of the operation.</span></span> <span data-ttu-id="af9a3-124">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="af9a3-124">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="af9a3-125">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="af9a3-125">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="af9a3-126">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="af9a3-126">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af9a3-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af9a3-127">Return value</span></span>

<span data-ttu-id="af9a3-128">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="af9a3-128">Type: **TemplateType**</span></span>

<span data-ttu-id="af9a3-129">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="af9a3-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="af9a3-130">Notes</span><span class="sxs-lookup"><span data-stu-id="af9a3-130">Remarks</span></span>

<span data-ttu-id="af9a3-131">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="af9a3-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="af9a3-132">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="af9a3-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="af9a3-133">Sommet</span><span class="sxs-lookup"><span data-stu-id="af9a3-133">Vertex</span></span> | <span data-ttu-id="af9a3-134">Forme</span><span class="sxs-lookup"><span data-stu-id="af9a3-134">Hull</span></span> | <span data-ttu-id="af9a3-135">Domain</span><span class="sxs-lookup"><span data-stu-id="af9a3-135">Domain</span></span> | <span data-ttu-id="af9a3-136">Géométrie</span><span class="sxs-lookup"><span data-stu-id="af9a3-136">Geometry</span></span> | <span data-ttu-id="af9a3-137">Pixel</span><span class="sxs-lookup"><span data-stu-id="af9a3-137">Pixel</span></span> | <span data-ttu-id="af9a3-138">Compute</span><span class="sxs-lookup"><span data-stu-id="af9a3-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="af9a3-139">x</span><span class="sxs-lookup"><span data-stu-id="af9a3-139">x</span></span>      | <span data-ttu-id="af9a3-140">x</span><span class="sxs-lookup"><span data-stu-id="af9a3-140">x</span></span>    | <span data-ttu-id="af9a3-141">x</span><span class="sxs-lookup"><span data-stu-id="af9a3-141">x</span></span>      | <span data-ttu-id="af9a3-142">x</span><span class="sxs-lookup"><span data-stu-id="af9a3-142">x</span></span>        | <span data-ttu-id="af9a3-143">x</span><span class="sxs-lookup"><span data-stu-id="af9a3-143">x</span></span>     | <span data-ttu-id="af9a3-144">x</span><span class="sxs-lookup"><span data-stu-id="af9a3-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="af9a3-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af9a3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af9a3-146">Méthodes GatherCmpAlpha</span><span class="sxs-lookup"><span data-stu-id="af9a3-146">GatherCmpAlpha methods</span></span>](texture2darray-gathercmpalpha.md)
</dt> </dl>

 

 
