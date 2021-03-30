---
title: 'Texture2DArray :: GatherBlue (S, float, Int2, Int2, Int2, Int2, uint), fonction'
description: 'Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques. | Texture2DArray :: GatherBlue (S, float, Int2, Int2, Int2, Int2, uint), fonction'
ms.assetid: 82CDD092-D1C9-4FA9-BD85-65098BA457CD
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
ms.openlocfilehash: fe53bfecad3c79f3b7439e6f38effe55c4045fea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974059"
---
# <a name="texture2darraygatherbluesfloatint2int2int2int2uint-function"></a><span data-ttu-id="fbeea-105">Texture2DArray :: GatherBlue (S, float, Int2, Int2, Int2, Int2, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="fbeea-105">Texture2DArray::GatherBlue(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="fbeea-106">Retourne les composants bleus des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="fbeea-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbeea-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbeea-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in  SamplerState S,
  in  float        Location,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="fbeea-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbeea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbeea-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="fbeea-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbeea-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="fbeea-110">Type: **SamplerState**</span></span>

<span data-ttu-id="fbeea-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="fbeea-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="fbeea-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbeea-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbeea-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="fbeea-113">Type: **float**</span></span>

<span data-ttu-id="fbeea-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="fbeea-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="fbeea-115">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbeea-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbeea-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="fbeea-116">Type: **int2**</span></span>

<span data-ttu-id="fbeea-117">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="fbeea-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fbeea-118">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbeea-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbeea-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="fbeea-119">Type: **int2**</span></span>

<span data-ttu-id="fbeea-120">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="fbeea-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fbeea-121">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbeea-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbeea-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="fbeea-122">Type: **int2**</span></span>

<span data-ttu-id="fbeea-123">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="fbeea-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fbeea-124">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbeea-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbeea-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="fbeea-125">Type: **int2**</span></span>

<span data-ttu-id="fbeea-126">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="fbeea-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fbeea-127">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fbeea-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbeea-128">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="fbeea-128">Type: **uint**</span></span>

<span data-ttu-id="fbeea-129">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="fbeea-129">The status of the operation.</span></span> <span data-ttu-id="fbeea-130">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="fbeea-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="fbeea-131">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="fbeea-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="fbeea-132">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="fbeea-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbeea-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbeea-133">Return value</span></span>

<span data-ttu-id="fbeea-134">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="fbeea-134">Type: **TemplateType**</span></span>

<span data-ttu-id="fbeea-135">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="fbeea-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbeea-136">Notes</span><span class="sxs-lookup"><span data-stu-id="fbeea-136">Remarks</span></span>

<span data-ttu-id="fbeea-137">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="fbeea-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="fbeea-138">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="fbeea-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fbeea-139">Sommet</span><span class="sxs-lookup"><span data-stu-id="fbeea-139">Vertex</span></span> | <span data-ttu-id="fbeea-140">Forme</span><span class="sxs-lookup"><span data-stu-id="fbeea-140">Hull</span></span> | <span data-ttu-id="fbeea-141">Domain</span><span class="sxs-lookup"><span data-stu-id="fbeea-141">Domain</span></span> | <span data-ttu-id="fbeea-142">Géométrie</span><span class="sxs-lookup"><span data-stu-id="fbeea-142">Geometry</span></span> | <span data-ttu-id="fbeea-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="fbeea-143">Pixel</span></span> | <span data-ttu-id="fbeea-144">Compute</span><span class="sxs-lookup"><span data-stu-id="fbeea-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fbeea-145">x</span><span class="sxs-lookup"><span data-stu-id="fbeea-145">x</span></span>      | <span data-ttu-id="fbeea-146">x</span><span class="sxs-lookup"><span data-stu-id="fbeea-146">x</span></span>    | <span data-ttu-id="fbeea-147">x</span><span class="sxs-lookup"><span data-stu-id="fbeea-147">x</span></span>      | <span data-ttu-id="fbeea-148">x</span><span class="sxs-lookup"><span data-stu-id="fbeea-148">x</span></span>        | <span data-ttu-id="fbeea-149">x</span><span class="sxs-lookup"><span data-stu-id="fbeea-149">x</span></span>     | <span data-ttu-id="fbeea-150">x</span><span class="sxs-lookup"><span data-stu-id="fbeea-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fbeea-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbeea-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbeea-152">Méthodes GatherBlue</span><span class="sxs-lookup"><span data-stu-id="fbeea-152">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> </dl>

 

 
