---
title: 'TextureCubeArray :: GatherCmpBlue (S, float, float, uint), fonction'
description: 'Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison entre leur composant bleu et une valeur de comparaison, ainsi que l’état du mappage de mosaïque. | TextureCubeArray :: GatherCmpBlue (S, float, float, uint), fonction'
ms.assetid: 81F82EB1-D662-4A18-856F-26AE5C1A41C6
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
ms.openlocfilehash: 9de8d578706cd0799bd2132f05b8a31b7daa8afe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211464"
---
# <a name="texturecubearraygathercmpbluesfloatfloatuint-function"></a><span data-ttu-id="bb793-105">TextureCubeArray :: GatherCmpBlue (S, float, float, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="bb793-105">TextureCubeArray::GatherCmpBlue(S,float,float,uint) function</span></span>

<span data-ttu-id="bb793-106">Pour quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, retourne une comparaison entre leur composant bleu et une valeur de comparaison, ainsi que l’état du mappage de mosaïque.</span><span class="sxs-lookup"><span data-stu-id="bb793-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb793-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb793-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpBlue(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="bb793-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb793-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb793-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="bb793-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb793-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="bb793-110">Type: **SamplerState**</span></span>

<span data-ttu-id="bb793-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="bb793-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="bb793-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb793-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb793-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="bb793-113">Type: **float**</span></span>

<span data-ttu-id="bb793-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="bb793-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="bb793-115">*CompareValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb793-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb793-116">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="bb793-116">Type: **float**</span></span>

<span data-ttu-id="bb793-117">Valeur à comparer pour chaque valeur échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="bb793-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="bb793-118">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bb793-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb793-119">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="bb793-119">Type: **uint**</span></span>

<span data-ttu-id="bb793-120">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="bb793-120">The status of the operation.</span></span> <span data-ttu-id="bb793-121">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="bb793-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="bb793-122">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="bb793-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="bb793-123">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="bb793-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb793-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb793-124">Return value</span></span>

<span data-ttu-id="bb793-125">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="bb793-125">Type: **TemplateType**</span></span>

<span data-ttu-id="bb793-126">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="bb793-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb793-127">Notes</span><span class="sxs-lookup"><span data-stu-id="bb793-127">Remarks</span></span>

<span data-ttu-id="bb793-128">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="bb793-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="bb793-129">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="bb793-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="bb793-130">Sommet</span><span class="sxs-lookup"><span data-stu-id="bb793-130">Vertex</span></span> | <span data-ttu-id="bb793-131">Forme</span><span class="sxs-lookup"><span data-stu-id="bb793-131">Hull</span></span> | <span data-ttu-id="bb793-132">Domain</span><span class="sxs-lookup"><span data-stu-id="bb793-132">Domain</span></span> | <span data-ttu-id="bb793-133">Géométrie</span><span class="sxs-lookup"><span data-stu-id="bb793-133">Geometry</span></span> | <span data-ttu-id="bb793-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="bb793-134">Pixel</span></span> | <span data-ttu-id="bb793-135">Compute</span><span class="sxs-lookup"><span data-stu-id="bb793-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bb793-136">x</span><span class="sxs-lookup"><span data-stu-id="bb793-136">x</span></span>      | <span data-ttu-id="bb793-137">x</span><span class="sxs-lookup"><span data-stu-id="bb793-137">x</span></span>    | <span data-ttu-id="bb793-138">x</span><span class="sxs-lookup"><span data-stu-id="bb793-138">x</span></span>      | <span data-ttu-id="bb793-139">x</span><span class="sxs-lookup"><span data-stu-id="bb793-139">x</span></span>        | <span data-ttu-id="bb793-140">x</span><span class="sxs-lookup"><span data-stu-id="bb793-140">x</span></span>     | <span data-ttu-id="bb793-141">x</span><span class="sxs-lookup"><span data-stu-id="bb793-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bb793-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb793-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb793-143">Méthodes GatherCmpBlue</span><span class="sxs-lookup"><span data-stu-id="bb793-143">GatherCmpBlue methods</span></span>](texturecubearray-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="bb793-144">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="bb793-144">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
