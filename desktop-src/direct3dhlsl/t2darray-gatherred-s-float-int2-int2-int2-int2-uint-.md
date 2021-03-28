---
title: 'Texture2DArray :: GatherRed (S, float, Int2, Int2, Int2, Int2, uint), fonction'
description: 'Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques. | Texture2DArray :: GatherRed (S, float, Int2, Int2, Int2, Int2, uint), fonction'
ms.assetid: 9DD399A4-E6ED-499B-ACA3-28028C0AB271
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
ms.openlocfilehash: 8ce2ce0ab8b79a2335cc8e02d89751da3b30d856
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991925"
---
# <a name="texture2darraygatherredsfloatint2int2int2int2uint-function"></a><span data-ttu-id="26594-105">Texture2DArray :: GatherRed (S, float, Int2, Int2, Int2, Int2, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="26594-105">Texture2DArray::GatherRed(S,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="26594-106">Retourne les composants rouges des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="26594-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="26594-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26594-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="26594-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26594-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26594-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="26594-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26594-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="26594-110">Type: **SamplerState**</span></span>

<span data-ttu-id="26594-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="26594-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="26594-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26594-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26594-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="26594-113">Type: **float**</span></span>

<span data-ttu-id="26594-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="26594-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="26594-115">*Offset1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26594-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26594-116">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="26594-116">Type: **int2**</span></span>

<span data-ttu-id="26594-117">Premier composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="26594-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="26594-118">*Offset2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26594-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26594-119">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="26594-119">Type: **int2**</span></span>

<span data-ttu-id="26594-120">Deuxième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="26594-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="26594-121">*Offset3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26594-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26594-122">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="26594-122">Type: **int2**</span></span>

<span data-ttu-id="26594-123">Troisième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="26594-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="26594-124">*Offset4* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26594-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26594-125">Type : **Int2**</span><span class="sxs-lookup"><span data-stu-id="26594-125">Type: **int2**</span></span>

<span data-ttu-id="26594-126">Quatrième composant de décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="26594-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="26594-127">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="26594-127">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26594-128">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="26594-128">Type: **uint**</span></span>

<span data-ttu-id="26594-129">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="26594-129">The status of the operation.</span></span> <span data-ttu-id="26594-130">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="26594-130">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="26594-131">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="26594-131">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="26594-132">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="26594-132">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26594-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26594-133">Return value</span></span>

<span data-ttu-id="26594-134">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="26594-134">Type: **TemplateType**</span></span>

<span data-ttu-id="26594-135">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="26594-135">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="26594-136">Notes</span><span class="sxs-lookup"><span data-stu-id="26594-136">Remarks</span></span>

<span data-ttu-id="26594-137">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="26594-137">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="26594-138">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="26594-138">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="26594-139">Sommet</span><span class="sxs-lookup"><span data-stu-id="26594-139">Vertex</span></span> | <span data-ttu-id="26594-140">Forme</span><span class="sxs-lookup"><span data-stu-id="26594-140">Hull</span></span> | <span data-ttu-id="26594-141">Domain</span><span class="sxs-lookup"><span data-stu-id="26594-141">Domain</span></span> | <span data-ttu-id="26594-142">Géométrie</span><span class="sxs-lookup"><span data-stu-id="26594-142">Geometry</span></span> | <span data-ttu-id="26594-143">Pixel</span><span class="sxs-lookup"><span data-stu-id="26594-143">Pixel</span></span> | <span data-ttu-id="26594-144">Compute</span><span class="sxs-lookup"><span data-stu-id="26594-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="26594-145">x</span><span class="sxs-lookup"><span data-stu-id="26594-145">x</span></span>      | <span data-ttu-id="26594-146">x</span><span class="sxs-lookup"><span data-stu-id="26594-146">x</span></span>    | <span data-ttu-id="26594-147">x</span><span class="sxs-lookup"><span data-stu-id="26594-147">x</span></span>      | <span data-ttu-id="26594-148">x</span><span class="sxs-lookup"><span data-stu-id="26594-148">x</span></span>        | <span data-ttu-id="26594-149">x</span><span class="sxs-lookup"><span data-stu-id="26594-149">x</span></span>     | <span data-ttu-id="26594-150">x</span><span class="sxs-lookup"><span data-stu-id="26594-150">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="26594-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26594-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26594-152">Méthodes GatherRed</span><span class="sxs-lookup"><span data-stu-id="26594-152">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> </dl>

 

 
