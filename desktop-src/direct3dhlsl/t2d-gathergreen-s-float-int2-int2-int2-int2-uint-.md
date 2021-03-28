---
title: 'Texture2D :: GatherGreen (S, float, Int2, Int2, Int2, Int2, uint), fonction'
description: 'Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques. | Texture2D :: GatherGreen (S, float, Int2, Int2, Int2, Int2, uint), fonction'
ms.assetid: 61AAC31F-28BC-4DF8-A416-CBAD150829D8
keywords:
- GatherGreen fonction HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e98bc8b34514cf2ac54e7fd96916c66c9f2a53d1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974243"
---
# <a name="texture2dgathergreensfloatint2int2int2int2uint-function"></a><span data-ttu-id="a0f2b-105">Texture2D :: GatherGreen (S, float, Int2, Int2, Int2, Int2, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="a0f2b-105">Texture2D::GatherGreen(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="a0f2b-106">Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f2b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0f2b-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="a0f2b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0f2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f2b-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="a0f2b-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="a0f2b-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-113">Type: **float**</span></span>

<span data-ttu-id="a0f2b-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="a0f2b-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="a0f2b-115">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-116">Type: **int2**</span></span>

<span data-ttu-id="a0f2b-117">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="a0f2b-118">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-119">Type: **int2**</span></span>

<span data-ttu-id="a0f2b-120">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="a0f2b-121">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-122">Type: **int2**</span></span>

<span data-ttu-id="a0f2b-123">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="a0f2b-124">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-125">Type: **int2**</span></span>

<span data-ttu-id="a0f2b-126">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="a0f2b-127">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a0f2b-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f2b-128">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-128">Type: **uint**</span></span>

<span data-ttu-id="a0f2b-129">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-129">The status of the operation.</span></span> <span data-ttu-id="a0f2b-130">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f2b-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a0f2b-131">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a0f2b-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a0f2b-132">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f2b-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0f2b-133">Return value</span></span>

<span data-ttu-id="a0f2b-134">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="a0f2b-134">Type: **TemplateType**</span></span>

<span data-ttu-id="a0f2b-135">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0f2b-136">Notes</span><span class="sxs-lookup"><span data-stu-id="a0f2b-136">Remarks</span></span>

<span data-ttu-id="a0f2b-137">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="a0f2b-138">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="a0f2b-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a0f2b-139">Sommet</span><span class="sxs-lookup"><span data-stu-id="a0f2b-139">Vertex</span></span> | <span data-ttu-id="a0f2b-140">Forme</span><span class="sxs-lookup"><span data-stu-id="a0f2b-140">Hull</span></span> | <span data-ttu-id="a0f2b-141">Domain</span><span class="sxs-lookup"><span data-stu-id="a0f2b-141">Domain</span></span> | <span data-ttu-id="a0f2b-142">Géométrie</span><span class="sxs-lookup"><span data-stu-id="a0f2b-142">Geometry</span></span> | <span data-ttu-id="a0f2b-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="a0f2b-143">Pixel</span></span> | <span data-ttu-id="a0f2b-144">Compute</span><span class="sxs-lookup"><span data-stu-id="a0f2b-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a0f2b-145">x</span><span class="sxs-lookup"><span data-stu-id="a0f2b-145">x</span></span>      | <span data-ttu-id="a0f2b-146">x</span><span class="sxs-lookup"><span data-stu-id="a0f2b-146">x</span></span>    | <span data-ttu-id="a0f2b-147">x</span><span class="sxs-lookup"><span data-stu-id="a0f2b-147">x</span></span>      | <span data-ttu-id="a0f2b-148">x</span><span class="sxs-lookup"><span data-stu-id="a0f2b-148">x</span></span>        | <span data-ttu-id="a0f2b-149">x</span><span class="sxs-lookup"><span data-stu-id="a0f2b-149">x</span></span>     | <span data-ttu-id="a0f2b-150">x</span><span class="sxs-lookup"><span data-stu-id="a0f2b-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a0f2b-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0f2b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f2b-152">Méthodes GatherGreen</span><span class="sxs-lookup"><span data-stu-id="a0f2b-152">GatherGreen methods</span></span>](texture2d-gathergreen.md)
</dt> </dl>

 

 
