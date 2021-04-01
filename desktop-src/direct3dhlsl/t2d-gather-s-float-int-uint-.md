---
title: 'Texture2D :: Gather (S, float, int, uint), fonction'
description: 'Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques. | Texture2D :: Gather (S, float, int, uint), fonction'
ms.assetid: 3B8733B0-BB80-4414-8BDD-033116D7EFE0
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
ms.openlocfilehash: d59ad2a29e7721309209b0a5ea9b773f64167c44
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211594"
---
# <a name="texture2dgathersfloatintuint-function"></a><span data-ttu-id="2b6ed-105">Texture2D :: Gather (S, float, int, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="2b6ed-105">Texture2D::Gather(S,float,int,uint) function</span></span>

<span data-ttu-id="2b6ed-106">Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="2b6ed-106">Returns the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b6ed-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b6ed-107">Syntax</span></span>


``` syntax
TemplateType Gather(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="2b6ed-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b6ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b6ed-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="2b6ed-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6ed-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="2b6ed-110">Type: **SamplerState**</span></span>

<span data-ttu-id="2b6ed-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="2b6ed-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="2b6ed-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b6ed-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6ed-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="2b6ed-113">Type: **float**</span></span>

<span data-ttu-id="2b6ed-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="2b6ed-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="2b6ed-115">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b6ed-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6ed-116">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="2b6ed-116">Type: **int**</span></span>

<span data-ttu-id="2b6ed-117">Décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="2b6ed-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2b6ed-118">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2b6ed-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6ed-119">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="2b6ed-119">Type: **uint**</span></span>

<span data-ttu-id="2b6ed-120">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="2b6ed-120">The status of the operation.</span></span> <span data-ttu-id="2b6ed-121">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="2b6ed-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="2b6ed-122">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="2b6ed-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="2b6ed-123">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="2b6ed-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b6ed-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b6ed-124">Return value</span></span>

<span data-ttu-id="2b6ed-125">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="2b6ed-125">Type: **TemplateType**</span></span>

<span data-ttu-id="2b6ed-126">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="2b6ed-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b6ed-127">Notes</span><span class="sxs-lookup"><span data-stu-id="2b6ed-127">Remarks</span></span>

<span data-ttu-id="2b6ed-128">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="2b6ed-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="2b6ed-129">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="2b6ed-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2b6ed-130">Sommet</span><span class="sxs-lookup"><span data-stu-id="2b6ed-130">Vertex</span></span> | <span data-ttu-id="2b6ed-131">Forme</span><span class="sxs-lookup"><span data-stu-id="2b6ed-131">Hull</span></span> | <span data-ttu-id="2b6ed-132">Domain</span><span class="sxs-lookup"><span data-stu-id="2b6ed-132">Domain</span></span> | <span data-ttu-id="2b6ed-133">Géométrie</span><span class="sxs-lookup"><span data-stu-id="2b6ed-133">Geometry</span></span> | <span data-ttu-id="2b6ed-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="2b6ed-134">Pixel</span></span> | <span data-ttu-id="2b6ed-135">Compute</span><span class="sxs-lookup"><span data-stu-id="2b6ed-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2b6ed-136">x</span><span class="sxs-lookup"><span data-stu-id="2b6ed-136">x</span></span>      | <span data-ttu-id="2b6ed-137">x</span><span class="sxs-lookup"><span data-stu-id="2b6ed-137">x</span></span>    | <span data-ttu-id="2b6ed-138">x</span><span class="sxs-lookup"><span data-stu-id="2b6ed-138">x</span></span>      | <span data-ttu-id="2b6ed-139">x</span><span class="sxs-lookup"><span data-stu-id="2b6ed-139">x</span></span>        | <span data-ttu-id="2b6ed-140">x</span><span class="sxs-lookup"><span data-stu-id="2b6ed-140">x</span></span>     | <span data-ttu-id="2b6ed-141">x</span><span class="sxs-lookup"><span data-stu-id="2b6ed-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2b6ed-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b6ed-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b6ed-143">Méthodes de collecte</span><span class="sxs-lookup"><span data-stu-id="2b6ed-143">Gather methods</span></span>](texture2d-gather.md)
</dt> </dl>

 

 
