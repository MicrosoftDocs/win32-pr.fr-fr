---
title: 'ByteAddressBuffer :: Load2 (uint, uint), fonction'
description: Obtient deux valeurs et l’état de l’opération.
ms.assetid: EE6FA09D-0C86-499D-86F9-EAA56125EB91
keywords:
- Load2 fonction HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 662e40789f59b75e53111fbab6d24288f27c8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031626"
---
# <a name="load2uint-uint-function"></a><span data-ttu-id="939e1-104">Load2 (uint, uint) (fonction)</span><span class="sxs-lookup"><span data-stu-id="939e1-104">Load2(uint, uint) function</span></span>

<span data-ttu-id="939e1-105">Obtient deux valeurs et l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="939e1-105">Gets two values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="939e1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="939e1-106">Syntax</span></span>

``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="939e1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="939e1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="939e1-108">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="939e1-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="939e1-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="939e1-109">Type: **uint**</span></span>

<span data-ttu-id="939e1-110">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="939e1-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="939e1-111">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="939e1-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="939e1-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="939e1-112">Type: **uint**</span></span>

<span data-ttu-id="939e1-113">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="939e1-113">The status of the operation.</span></span> <span data-ttu-id="939e1-114">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="939e1-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="939e1-115">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="939e1-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="939e1-116">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="939e1-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="939e1-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="939e1-117">Return value</span></span>

<span data-ttu-id="939e1-118">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="939e1-118">Type: **uint2**</span></span>

<span data-ttu-id="939e1-119">Deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="939e1-119">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="939e1-120">Notes</span><span class="sxs-lookup"><span data-stu-id="939e1-120">Remarks</span></span>

<span data-ttu-id="939e1-121">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="939e1-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="939e1-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="939e1-122">Vertex</span></span> | <span data-ttu-id="939e1-123">Forme</span><span class="sxs-lookup"><span data-stu-id="939e1-123">Hull</span></span> | <span data-ttu-id="939e1-124">Domain</span><span class="sxs-lookup"><span data-stu-id="939e1-124">Domain</span></span> | <span data-ttu-id="939e1-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="939e1-125">Geometry</span></span> | <span data-ttu-id="939e1-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="939e1-126">Pixel</span></span> | <span data-ttu-id="939e1-127">Compute</span><span class="sxs-lookup"><span data-stu-id="939e1-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="939e1-128">x</span><span class="sxs-lookup"><span data-stu-id="939e1-128">x</span></span>      | <span data-ttu-id="939e1-129">x</span><span class="sxs-lookup"><span data-stu-id="939e1-129">x</span></span>    | <span data-ttu-id="939e1-130">x</span><span class="sxs-lookup"><span data-stu-id="939e1-130">x</span></span>      | <span data-ttu-id="939e1-131">x</span><span class="sxs-lookup"><span data-stu-id="939e1-131">x</span></span>        | <span data-ttu-id="939e1-132">x</span><span class="sxs-lookup"><span data-stu-id="939e1-132">x</span></span>     | <span data-ttu-id="939e1-133">x</span><span class="sxs-lookup"><span data-stu-id="939e1-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="939e1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="939e1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="939e1-135">Méthodes Load2</span><span class="sxs-lookup"><span data-stu-id="939e1-135">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="939e1-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="939e1-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 