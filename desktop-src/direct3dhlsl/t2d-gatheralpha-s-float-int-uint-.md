---
title: 'Texture2D :: GatherAlpha (S, float, int, uint), fonction'
description: 'Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïque. | Texture2D :: GatherAlpha (S, float, int, uint), fonction'
ms.assetid: A05E9286-2DCA-4A85-A337-0E010EF98D7F
keywords:
- GatherAlpha fonction HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63bdefe7a491499a46e3a9f15d82eaedd922a0b8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973955"
---
# <a name="texture2dgatheralphasfloatintuint-function"></a><span data-ttu-id="df6c1-105">Texture2D :: GatherAlpha (S, float, int, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="df6c1-105">Texture2D::GatherAlpha(S,float,int,uint) function</span></span>

<span data-ttu-id="df6c1-106">Retourne les composants alpha des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïque.</span><span class="sxs-lookup"><span data-stu-id="df6c1-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="df6c1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df6c1-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="df6c1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df6c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df6c1-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="df6c1-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6c1-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="df6c1-110">Type: **SamplerState**</span></span>

<span data-ttu-id="df6c1-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="df6c1-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="df6c1-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df6c1-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6c1-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="df6c1-113">Type: **float**</span></span>

<span data-ttu-id="df6c1-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="df6c1-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="df6c1-115">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df6c1-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6c1-116">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="df6c1-116">Type: **int**</span></span>

<span data-ttu-id="df6c1-117">Décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="df6c1-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="df6c1-118">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="df6c1-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df6c1-119">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="df6c1-119">Type: **uint**</span></span>

<span data-ttu-id="df6c1-120">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="df6c1-120">The status of the operation.</span></span> <span data-ttu-id="df6c1-121">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="df6c1-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="df6c1-122">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="df6c1-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="df6c1-123">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="df6c1-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df6c1-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df6c1-124">Return value</span></span>

<span data-ttu-id="df6c1-125">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="df6c1-125">Type: **TemplateType**</span></span>

<span data-ttu-id="df6c1-126">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="df6c1-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="df6c1-127">Notes</span><span class="sxs-lookup"><span data-stu-id="df6c1-127">Remarks</span></span>

<span data-ttu-id="df6c1-128">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="df6c1-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="df6c1-129">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="df6c1-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="df6c1-130">Sommet</span><span class="sxs-lookup"><span data-stu-id="df6c1-130">Vertex</span></span> | <span data-ttu-id="df6c1-131">Forme</span><span class="sxs-lookup"><span data-stu-id="df6c1-131">Hull</span></span> | <span data-ttu-id="df6c1-132">Domain</span><span class="sxs-lookup"><span data-stu-id="df6c1-132">Domain</span></span> | <span data-ttu-id="df6c1-133">Géométrie</span><span class="sxs-lookup"><span data-stu-id="df6c1-133">Geometry</span></span> | <span data-ttu-id="df6c1-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="df6c1-134">Pixel</span></span> | <span data-ttu-id="df6c1-135">Compute</span><span class="sxs-lookup"><span data-stu-id="df6c1-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="df6c1-136">x</span><span class="sxs-lookup"><span data-stu-id="df6c1-136">x</span></span>      | <span data-ttu-id="df6c1-137">x</span><span class="sxs-lookup"><span data-stu-id="df6c1-137">x</span></span>    | <span data-ttu-id="df6c1-138">x</span><span class="sxs-lookup"><span data-stu-id="df6c1-138">x</span></span>      | <span data-ttu-id="df6c1-139">x</span><span class="sxs-lookup"><span data-stu-id="df6c1-139">x</span></span>        | <span data-ttu-id="df6c1-140">x</span><span class="sxs-lookup"><span data-stu-id="df6c1-140">x</span></span>     | <span data-ttu-id="df6c1-141">x</span><span class="sxs-lookup"><span data-stu-id="df6c1-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="df6c1-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df6c1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6c1-143">Méthodes GatherAlpha</span><span class="sxs-lookup"><span data-stu-id="df6c1-143">GatherAlpha methods</span></span>](texture2d-gatheralpha.md)
</dt> </dl>

 

 
