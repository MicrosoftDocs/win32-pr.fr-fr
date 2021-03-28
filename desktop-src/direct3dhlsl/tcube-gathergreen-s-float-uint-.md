---
title: 'TextureCube :: GatherGreen (S, float, uint), fonction'
description: 'Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques. | TextureCube :: GatherGreen (S, float, uint), fonction'
ms.assetid: DB0A6386-70ED-4D8C-A4EE-C058496D2F12
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
ms.openlocfilehash: 1555b72b095ce0589a8ae9b396c67d29236db82c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992073"
---
# <a name="texturecubegathergreensfloatuint-function"></a><span data-ttu-id="a1353-105">TextureCube :: GatherGreen (S, float, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="a1353-105">TextureCube::GatherGreen(S,float,uint) function</span></span>

<span data-ttu-id="a1353-106">Retourne les composants verts des quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="a1353-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1353-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1353-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in  SamplerState S,
  in  float        Location,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="a1353-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1353-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1353-109"> \[ Dans\]</span><span class="sxs-lookup"><span data-stu-id="a1353-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1353-110">Type : **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="a1353-110">Type: **SamplerState**</span></span>

<span data-ttu-id="a1353-111">Index de base zéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="a1353-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="a1353-112">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1353-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1353-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="a1353-113">Type: **float**</span></span>

<span data-ttu-id="a1353-114">Les coordonnées de l’échantillon (u, v).</span><span class="sxs-lookup"><span data-stu-id="a1353-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="a1353-115">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a1353-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1353-116">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="a1353-116">Type: **uint**</span></span>

<span data-ttu-id="a1353-117">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a1353-117">The status of the operation.</span></span> <span data-ttu-id="a1353-118">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a1353-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a1353-119">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a1353-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a1353-120">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="a1353-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1353-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1353-121">Return value</span></span>

<span data-ttu-id="a1353-122">Type : **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="a1353-122">Type: **TemplateType**</span></span>

<span data-ttu-id="a1353-123">Valeur à quatre composants dont le type est identique au type de modèle.</span><span class="sxs-lookup"><span data-stu-id="a1353-123">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1353-124">Notes</span><span class="sxs-lookup"><span data-stu-id="a1353-124">Remarks</span></span>

<span data-ttu-id="a1353-125">Les échantillons de texture peuvent être utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="a1353-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="a1353-126">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="a1353-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a1353-127">Sommet</span><span class="sxs-lookup"><span data-stu-id="a1353-127">Vertex</span></span> | <span data-ttu-id="a1353-128">Forme</span><span class="sxs-lookup"><span data-stu-id="a1353-128">Hull</span></span> | <span data-ttu-id="a1353-129">Domain</span><span class="sxs-lookup"><span data-stu-id="a1353-129">Domain</span></span> | <span data-ttu-id="a1353-130">Géométrie</span><span class="sxs-lookup"><span data-stu-id="a1353-130">Geometry</span></span> | <span data-ttu-id="a1353-131">Pixel</span><span class="sxs-lookup"><span data-stu-id="a1353-131">Pixel</span></span> | <span data-ttu-id="a1353-132">Compute</span><span class="sxs-lookup"><span data-stu-id="a1353-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a1353-133">x</span><span class="sxs-lookup"><span data-stu-id="a1353-133">x</span></span>      | <span data-ttu-id="a1353-134">x</span><span class="sxs-lookup"><span data-stu-id="a1353-134">x</span></span>    | <span data-ttu-id="a1353-135">x</span><span class="sxs-lookup"><span data-stu-id="a1353-135">x</span></span>      | <span data-ttu-id="a1353-136">x</span><span class="sxs-lookup"><span data-stu-id="a1353-136">x</span></span>        | <span data-ttu-id="a1353-137">x</span><span class="sxs-lookup"><span data-stu-id="a1353-137">x</span></span>     | <span data-ttu-id="a1353-138">x</span><span class="sxs-lookup"><span data-stu-id="a1353-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a1353-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1353-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1353-140">Méthodes GatherGreen</span><span class="sxs-lookup"><span data-stu-id="a1353-140">GatherGreen methods</span></span>](texturecube-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="a1353-141">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="a1353-141">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
