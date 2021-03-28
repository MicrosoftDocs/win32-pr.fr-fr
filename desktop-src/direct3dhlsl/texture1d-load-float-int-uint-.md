---
title: 'Texture1D :: Load (int, int, uint), fonction'
description: 'Lit les données de texture et retourne l’état de l’opération. | Texture1D :: Load (int, int, uint), fonction'
ms.assetid: 5C489CBD-E4F6-4CB5-8E7E-EC34633D75B0
keywords:
- Charger la fonction HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c7733ab4802037d83dbb2b4ce523ff7bb57f729
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974182"
---
# <a name="texture1dloadintintuint-function"></a><span data-ttu-id="7eae1-105">Texture1D :: Load (int, int, uint), fonction</span><span class="sxs-lookup"><span data-stu-id="7eae1-105">Texture1D::Load(int,int,uint) function</span></span>

<span data-ttu-id="7eae1-106">Lit les données de texture et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7eae1-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eae1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7eae1-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="7eae1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7eae1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eae1-109">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7eae1-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eae1-110">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="7eae1-110">Type: **int**</span></span>

<span data-ttu-id="7eae1-111">Coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="7eae1-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="7eae1-112">*Décalage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7eae1-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eae1-113">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="7eae1-113">Type: **int**</span></span>

<span data-ttu-id="7eae1-114">Décalage appliqué aux coordonnées de texture avant l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="7eae1-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="7eae1-115">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7eae1-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7eae1-116">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="7eae1-116">Type: **uint**</span></span>

<span data-ttu-id="7eae1-117">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7eae1-117">The status of the operation.</span></span> <span data-ttu-id="7eae1-118">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="7eae1-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="7eae1-119">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="7eae1-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="7eae1-120">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="7eae1-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eae1-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7eae1-121">Return value</span></span>

<span data-ttu-id="7eae1-122">Tapez :</span><span class="sxs-lookup"><span data-stu-id="7eae1-122">Type:</span></span>

<span data-ttu-id="7eae1-123">Le type de retour correspond au type dans la déclaration pour l’objet [**Texture1D**](sm5-object-texture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="7eae1-123">The return type matches the type in the declaration for the [**Texture1D**](sm5-object-texture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eae1-124">Notes</span><span class="sxs-lookup"><span data-stu-id="7eae1-124">Remarks</span></span>

<span data-ttu-id="7eae1-125">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="7eae1-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7eae1-126">Sommet</span><span class="sxs-lookup"><span data-stu-id="7eae1-126">Vertex</span></span> | <span data-ttu-id="7eae1-127">Forme</span><span class="sxs-lookup"><span data-stu-id="7eae1-127">Hull</span></span> | <span data-ttu-id="7eae1-128">Domain</span><span class="sxs-lookup"><span data-stu-id="7eae1-128">Domain</span></span> | <span data-ttu-id="7eae1-129">Géométrie</span><span class="sxs-lookup"><span data-stu-id="7eae1-129">Geometry</span></span> | <span data-ttu-id="7eae1-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="7eae1-130">Pixel</span></span> | <span data-ttu-id="7eae1-131">Compute</span><span class="sxs-lookup"><span data-stu-id="7eae1-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7eae1-132">x</span><span class="sxs-lookup"><span data-stu-id="7eae1-132">x</span></span>      | <span data-ttu-id="7eae1-133">x</span><span class="sxs-lookup"><span data-stu-id="7eae1-133">x</span></span>    | <span data-ttu-id="7eae1-134">x</span><span class="sxs-lookup"><span data-stu-id="7eae1-134">x</span></span>      | <span data-ttu-id="7eae1-135">x</span><span class="sxs-lookup"><span data-stu-id="7eae1-135">x</span></span>        | <span data-ttu-id="7eae1-136">x</span><span class="sxs-lookup"><span data-stu-id="7eae1-136">x</span></span>     | <span data-ttu-id="7eae1-137">x</span><span class="sxs-lookup"><span data-stu-id="7eae1-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7eae1-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7eae1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eae1-139">Méthodes Load</span><span class="sxs-lookup"><span data-stu-id="7eae1-139">Load methods</span></span>](texture1d-load.md)
</dt> <dt>

[<span data-ttu-id="7eae1-140">**Texture1D**</span><span class="sxs-lookup"><span data-stu-id="7eae1-140">**Texture1D**</span></span>](sm5-object-texture1d.md)
</dt> </dl>

 

 
