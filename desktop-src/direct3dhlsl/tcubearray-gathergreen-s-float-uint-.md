---
title: 'TextureCubeArray :: GatherGreen (S, float, uint), fonction'
description: 'Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques. | TextureCubeArray :: GatherGreen (S, float, uint), fonction'
ms.assetid: 0DEB1810-F2C7-4097-B2D3-20ED4E297561
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
ms.openlocfilehash: 6c6809f56c8b589c97b103fdd71ccbd1292110ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974122"
---
# <a name="texturecubearraygathergreensfloatuint-function"></a><span data-ttu-id="b6041-105">TextureCubeArray :: GatherGreen (S, float, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="b6041-105">TextureCubeArray::GatherGreen(S,float,uint) function</span></span>

<span data-ttu-id="b6041-106">Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="b6041-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6041-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6041-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="b6041-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6041-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6041-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="b6041-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6041-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="b6041-110">Type: **SamplerState**</span></span>

<span data-ttu-id="b6041-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="b6041-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="b6041-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6041-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6041-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="b6041-113">Type: **float**</span></span>

<span data-ttu-id="b6041-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="b6041-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="b6041-115">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b6041-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6041-116">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="b6041-116">Type: **uint**</span></span>

<span data-ttu-id="b6041-117">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b6041-117">The status of the operation.</span></span> <span data-ttu-id="b6041-118">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="b6041-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b6041-119">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="b6041-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b6041-120">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="b6041-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6041-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6041-121">Return value</span></span>

<span data-ttu-id="b6041-122">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="b6041-122">Type: **TemplateType**</span></span>

<span data-ttu-id="b6041-123">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="b6041-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6041-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b6041-124">Remarks</span></span>

<span data-ttu-id="b6041-125">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="b6041-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="b6041-126">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="b6041-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b6041-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="b6041-127">Vertex</span></span> | <span data-ttu-id="b6041-128">Forme</span><span class="sxs-lookup"><span data-stu-id="b6041-128">Hull</span></span> | <span data-ttu-id="b6041-129">Domain</span><span class="sxs-lookup"><span data-stu-id="b6041-129">Domain</span></span> | <span data-ttu-id="b6041-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="b6041-130">Geometry</span></span> | <span data-ttu-id="b6041-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="b6041-131">Pixel</span></span> | <span data-ttu-id="b6041-132">Compute</span><span class="sxs-lookup"><span data-stu-id="b6041-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b6041-133">x</span><span class="sxs-lookup"><span data-stu-id="b6041-133">x</span></span>      | <span data-ttu-id="b6041-134">x</span><span class="sxs-lookup"><span data-stu-id="b6041-134">x</span></span>    | <span data-ttu-id="b6041-135">x</span><span class="sxs-lookup"><span data-stu-id="b6041-135">x</span></span>      | <span data-ttu-id="b6041-136">x</span><span class="sxs-lookup"><span data-stu-id="b6041-136">x</span></span>        | <span data-ttu-id="b6041-137">x</span><span class="sxs-lookup"><span data-stu-id="b6041-137">x</span></span>     | <span data-ttu-id="b6041-138">x</span><span class="sxs-lookup"><span data-stu-id="b6041-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b6041-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6041-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6041-140">Méthodes GatherGreen</span><span class="sxs-lookup"><span data-stu-id="b6041-140">GatherGreen methods</span></span>](texturecubearray-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="b6041-141">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="b6041-141">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
