---
title: 'TextureCube :: Gather (S, float, uint), fonction'
description: 'Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | TextureCube :: Gather (S, float, uint), fonction'
ms.assetid: 23FA8135-ECF0-4CAE-9A1C-B05DA3676453
keywords:
- Fonction de collecte HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9710343ff9b09e4425bc133db6dab4d118d807e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973963"
---
# <a name="texturecubegathersfloatuint-function"></a><span data-ttu-id="a622c-105">TextureCube :: Gather (S, float, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="a622c-105">TextureCube::Gather(S,float,uint) function</span></span>

<span data-ttu-id="a622c-106">Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="a622c-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a622c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a622c-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="a622c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a622c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a622c-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="a622c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a622c-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="a622c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="a622c-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="a622c-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="a622c-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a622c-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a622c-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a622c-113">Type: **float**</span></span>

<span data-ttu-id="a622c-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="a622c-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="a622c-115">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a622c-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a622c-116">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="a622c-116">Type: **uint**</span></span>

<span data-ttu-id="a622c-117">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a622c-117">The status of the operation.</span></span> <span data-ttu-id="a622c-118">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a622c-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a622c-119">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a622c-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a622c-120">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="a622c-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a622c-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a622c-121">Return value</span></span>

<span data-ttu-id="a622c-122">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="a622c-122">Type: **TemplateType**</span></span>

<span data-ttu-id="a622c-123">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="a622c-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="a622c-124">Notes</span><span class="sxs-lookup"><span data-stu-id="a622c-124">Remarks</span></span>

<span data-ttu-id="a622c-125">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="a622c-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="a622c-126">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="a622c-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a622c-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="a622c-127">Vertex</span></span> | <span data-ttu-id="a622c-128">Forme</span><span class="sxs-lookup"><span data-stu-id="a622c-128">Hull</span></span> | <span data-ttu-id="a622c-129">Domain</span><span class="sxs-lookup"><span data-stu-id="a622c-129">Domain</span></span> | <span data-ttu-id="a622c-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="a622c-130">Geometry</span></span> | <span data-ttu-id="a622c-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="a622c-131">Pixel</span></span> | <span data-ttu-id="a622c-132">Compute</span><span class="sxs-lookup"><span data-stu-id="a622c-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a622c-133">x</span><span class="sxs-lookup"><span data-stu-id="a622c-133">x</span></span>      | <span data-ttu-id="a622c-134">x</span><span class="sxs-lookup"><span data-stu-id="a622c-134">x</span></span>    | <span data-ttu-id="a622c-135">x</span><span class="sxs-lookup"><span data-stu-id="a622c-135">x</span></span>      | <span data-ttu-id="a622c-136">x</span><span class="sxs-lookup"><span data-stu-id="a622c-136">x</span></span>        | <span data-ttu-id="a622c-137">x</span><span class="sxs-lookup"><span data-stu-id="a622c-137">x</span></span>     | <span data-ttu-id="a622c-138">x</span><span class="sxs-lookup"><span data-stu-id="a622c-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a622c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a622c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a622c-140">Méthodes de collecte</span><span class="sxs-lookup"><span data-stu-id="a622c-140">Gather methods</span></span>](texturecube-gather.md)
</dt> <dt>

[<span data-ttu-id="a622c-141">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="a622c-141">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
