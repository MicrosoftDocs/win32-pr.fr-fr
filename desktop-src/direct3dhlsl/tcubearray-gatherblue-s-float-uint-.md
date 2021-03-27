---
title: 'TextureCubeArray :: GatherBlue (S, float, uint), fonction'
description: 'Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques. | TextureCubeArray :: GatherBlue (S, float, uint), fonction'
ms.assetid: 85606EE7-9B05-439F-B525-A1CD42FE32F6
keywords:
- GatherBlue fonction HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b96282bd57b6cbef248a7090ad4a297cd5a81740
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393995"
---
# <a name="texturecubearraygatherbluesfloatuint-function"></a><span data-ttu-id="8d48b-105">TextureCubeArray :: GatherBlue (S, float, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="8d48b-105">TextureCubeArray::GatherBlue(S,float,uint) function</span></span>

<span data-ttu-id="8d48b-106">Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="8d48b-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d48b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d48b-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="8d48b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d48b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d48b-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="8d48b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d48b-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="8d48b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="8d48b-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="8d48b-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="8d48b-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d48b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d48b-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="8d48b-113">Type: **float**</span></span>

<span data-ttu-id="8d48b-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="8d48b-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="8d48b-115">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8d48b-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d48b-116">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="8d48b-116">Type: **uint**</span></span>

<span data-ttu-id="8d48b-117">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="8d48b-117">The status of the operation.</span></span> <span data-ttu-id="8d48b-118">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="8d48b-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8d48b-119">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="8d48b-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8d48b-120">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="8d48b-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d48b-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d48b-121">Return value</span></span>

<span data-ttu-id="8d48b-122">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="8d48b-122">Type: **TemplateType**</span></span>

<span data-ttu-id="8d48b-123">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="8d48b-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d48b-124">Notes</span><span class="sxs-lookup"><span data-stu-id="8d48b-124">Remarks</span></span>

<span data-ttu-id="8d48b-125">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="8d48b-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="8d48b-126">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="8d48b-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8d48b-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="8d48b-127">Vertex</span></span> | <span data-ttu-id="8d48b-128">Forme</span><span class="sxs-lookup"><span data-stu-id="8d48b-128">Hull</span></span> | <span data-ttu-id="8d48b-129">Domain</span><span class="sxs-lookup"><span data-stu-id="8d48b-129">Domain</span></span> | <span data-ttu-id="8d48b-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="8d48b-130">Geometry</span></span> | <span data-ttu-id="8d48b-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="8d48b-131">Pixel</span></span> | <span data-ttu-id="8d48b-132">Compute</span><span class="sxs-lookup"><span data-stu-id="8d48b-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8d48b-133">x</span><span class="sxs-lookup"><span data-stu-id="8d48b-133">x</span></span>      | <span data-ttu-id="8d48b-134">x</span><span class="sxs-lookup"><span data-stu-id="8d48b-134">x</span></span>    | <span data-ttu-id="8d48b-135">x</span><span class="sxs-lookup"><span data-stu-id="8d48b-135">x</span></span>      | <span data-ttu-id="8d48b-136">x</span><span class="sxs-lookup"><span data-stu-id="8d48b-136">x</span></span>        | <span data-ttu-id="8d48b-137">x</span><span class="sxs-lookup"><span data-stu-id="8d48b-137">x</span></span>     | <span data-ttu-id="8d48b-138">x</span><span class="sxs-lookup"><span data-stu-id="8d48b-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8d48b-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d48b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d48b-140">Méthodes GatherBlue</span><span class="sxs-lookup"><span data-stu-id="8d48b-140">GatherBlue methods</span></span>](texturecubearray-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="8d48b-141">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="8d48b-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
