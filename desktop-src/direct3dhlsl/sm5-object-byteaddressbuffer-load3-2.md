---
title: 'ByteAddressBuffer :: Load3 (uint, uint), fonction'
description: Obtient trois valeurs et l’état de l’opération.
ms.assetid: 6AD8E957-F646-4749-A9B4-5C0C936D90E3
keywords:
- Load3 fonction HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1bf3ffda082b8d2ae9cf22db59c1c38682563136
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315179"
---
# <a name="load3uint-uint-function"></a><span data-ttu-id="5d20d-104">Load3 (uint, uint) (fonction)</span><span class="sxs-lookup"><span data-stu-id="5d20d-104">Load3(uint, uint) function</span></span>

<span data-ttu-id="5d20d-105">Obtient trois valeurs et l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5d20d-105">Gets three values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d20d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d20d-106">Syntax</span></span>

``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="5d20d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d20d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d20d-108">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5d20d-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d20d-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="5d20d-109">Type: **uint**</span></span>

<span data-ttu-id="5d20d-110">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="5d20d-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="5d20d-111">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5d20d-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d20d-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="5d20d-112">Type: **uint**</span></span>

<span data-ttu-id="5d20d-113">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5d20d-113">The status of the operation.</span></span> <span data-ttu-id="5d20d-114">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="5d20d-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5d20d-115">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="5d20d-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5d20d-116">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="5d20d-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d20d-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d20d-117">Return value</span></span>

<span data-ttu-id="5d20d-118">Type : **uint3**</span><span class="sxs-lookup"><span data-stu-id="5d20d-118">Type: **uint3**</span></span>

<span data-ttu-id="5d20d-119">Trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="5d20d-119">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d20d-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5d20d-120">Remarks</span></span>

<span data-ttu-id="5d20d-121">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="5d20d-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5d20d-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="5d20d-122">Vertex</span></span> | <span data-ttu-id="5d20d-123">Forme</span><span class="sxs-lookup"><span data-stu-id="5d20d-123">Hull</span></span> | <span data-ttu-id="5d20d-124">Domain</span><span class="sxs-lookup"><span data-stu-id="5d20d-124">Domain</span></span> | <span data-ttu-id="5d20d-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="5d20d-125">Geometry</span></span> | <span data-ttu-id="5d20d-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="5d20d-126">Pixel</span></span> | <span data-ttu-id="5d20d-127">Compute</span><span class="sxs-lookup"><span data-stu-id="5d20d-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5d20d-128">x</span><span class="sxs-lookup"><span data-stu-id="5d20d-128">x</span></span>      | <span data-ttu-id="5d20d-129">x</span><span class="sxs-lookup"><span data-stu-id="5d20d-129">x</span></span>    | <span data-ttu-id="5d20d-130">x</span><span class="sxs-lookup"><span data-stu-id="5d20d-130">x</span></span>      | <span data-ttu-id="5d20d-131">x</span><span class="sxs-lookup"><span data-stu-id="5d20d-131">x</span></span>        | <span data-ttu-id="5d20d-132">x</span><span class="sxs-lookup"><span data-stu-id="5d20d-132">x</span></span>     | <span data-ttu-id="5d20d-133">x</span><span class="sxs-lookup"><span data-stu-id="5d20d-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5d20d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d20d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d20d-135">Méthodes Load3</span><span class="sxs-lookup"><span data-stu-id="5d20d-135">Load3 methods</span></span>](byteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="5d20d-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="5d20d-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 