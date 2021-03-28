---
title: 'Texture2D :: GatherRed (S, float, Int2, Int2, Int2, Int2, uint), fonction'
description: 'Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques. | Texture2D :: GatherRed (S, float, Int2, Int2, Int2, Int2, uint), fonction'
ms.assetid: 7CDFAA5A-315A-40AE-A662-9AF97D486039
keywords:
- GatherRed fonction HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d26de431f66fd9106ac37ed4f09bf3ce14dbad2d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104042994"
---
# <a name="texture2dgatherredsfloatint2int2int2int2uint-function"></a><span data-ttu-id="97c70-105">Texture2D :: GatherRed (S, float, Int2, Int2, Int2, Int2, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="97c70-105">Texture2D::GatherRed(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="97c70-106">Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="97c70-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c70-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97c70-107">Syntax</span></span>


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="97c70-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97c70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c70-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="97c70-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c70-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="97c70-110">Type: **SamplerState**</span></span>

<span data-ttu-id="97c70-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="97c70-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="97c70-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97c70-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c70-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="97c70-113">Type: **float**</span></span>

<span data-ttu-id="97c70-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="97c70-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="97c70-115">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97c70-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c70-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="97c70-116">Type: **int2**</span></span>

<span data-ttu-id="97c70-117">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="97c70-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="97c70-118">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97c70-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c70-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="97c70-119">Type: **int2**</span></span>

<span data-ttu-id="97c70-120">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="97c70-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="97c70-121">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97c70-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c70-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="97c70-122">Type: **int2**</span></span>

<span data-ttu-id="97c70-123">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="97c70-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="97c70-124">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97c70-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c70-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="97c70-125">Type: **int2**</span></span>

<span data-ttu-id="97c70-126">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="97c70-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="97c70-127">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="97c70-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97c70-128">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="97c70-128">Type: **uint**</span></span>

<span data-ttu-id="97c70-129">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="97c70-129">The status of the operation.</span></span> <span data-ttu-id="97c70-130">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="97c70-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="97c70-131">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="97c70-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="97c70-132">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="97c70-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c70-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97c70-133">Return value</span></span>

<span data-ttu-id="97c70-134">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="97c70-134">Type: **TemplateType**</span></span>

<span data-ttu-id="97c70-135">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="97c70-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="97c70-136">Notes</span><span class="sxs-lookup"><span data-stu-id="97c70-136">Remarks</span></span>

<span data-ttu-id="97c70-137">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="97c70-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="97c70-138">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="97c70-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="97c70-139">Sommet</span><span class="sxs-lookup"><span data-stu-id="97c70-139">Vertex</span></span> | <span data-ttu-id="97c70-140">Forme</span><span class="sxs-lookup"><span data-stu-id="97c70-140">Hull</span></span> | <span data-ttu-id="97c70-141">Domain</span><span class="sxs-lookup"><span data-stu-id="97c70-141">Domain</span></span> | <span data-ttu-id="97c70-142">Géométrie</span><span class="sxs-lookup"><span data-stu-id="97c70-142">Geometry</span></span> | <span data-ttu-id="97c70-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="97c70-143">Pixel</span></span> | <span data-ttu-id="97c70-144">Compute</span><span class="sxs-lookup"><span data-stu-id="97c70-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="97c70-145">x</span><span class="sxs-lookup"><span data-stu-id="97c70-145">x</span></span>      | <span data-ttu-id="97c70-146">x</span><span class="sxs-lookup"><span data-stu-id="97c70-146">x</span></span>    | <span data-ttu-id="97c70-147">x</span><span class="sxs-lookup"><span data-stu-id="97c70-147">x</span></span>      | <span data-ttu-id="97c70-148">x</span><span class="sxs-lookup"><span data-stu-id="97c70-148">x</span></span>        | <span data-ttu-id="97c70-149">x</span><span class="sxs-lookup"><span data-stu-id="97c70-149">x</span></span>     | <span data-ttu-id="97c70-150">x</span><span class="sxs-lookup"><span data-stu-id="97c70-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="97c70-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97c70-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c70-152">Méthodes GatherRed</span><span class="sxs-lookup"><span data-stu-id="97c70-152">GatherRed methods</span></span>](texture2d-gatherred.md)
</dt> </dl>

 

 
