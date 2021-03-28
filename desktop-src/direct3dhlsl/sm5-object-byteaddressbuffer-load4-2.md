---
title: 'ByteAddressBuffer :: Load4 (uint, uint), fonction'
description: Obtient quatre valeurs et l’état de l’opération.
ms.assetid: C814F717-9FD4-4BFC-A91B-319477B7F3DE
keywords:
- Load4 fonction HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab27ed9002562643ddf4df6b33efe9d8f0454d94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031264"
---
# <a name="load4uint-uint-function"></a><span data-ttu-id="0d794-104">Load4 (uint, uint) (fonction)</span><span class="sxs-lookup"><span data-stu-id="0d794-104">Load4(uint, uint) function</span></span>

<span data-ttu-id="0d794-105">Obtient quatre valeurs et l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0d794-105">Gets four values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d794-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d794-106">Syntax</span></span>

``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="0d794-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d794-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d794-108">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d794-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d794-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="0d794-109">Type: **uint**</span></span>

<span data-ttu-id="0d794-110">Adresse d’entrée en octets, qui doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="0d794-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="0d794-111">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d794-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d794-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="0d794-112">Type: **uint**</span></span>

<span data-ttu-id="0d794-113">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0d794-113">The status of the operation.</span></span> <span data-ttu-id="0d794-114">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="0d794-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="0d794-115">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="0d794-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="0d794-116">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="0d794-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d794-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d794-117">Return value</span></span>

<span data-ttu-id="0d794-118">Type : **uint4**</span><span class="sxs-lookup"><span data-stu-id="0d794-118">Type: **uint4**</span></span>

<span data-ttu-id="0d794-119">Quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="0d794-119">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d794-120">Notes</span><span class="sxs-lookup"><span data-stu-id="0d794-120">Remarks</span></span>

<span data-ttu-id="0d794-121">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="0d794-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0d794-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="0d794-122">Vertex</span></span> | <span data-ttu-id="0d794-123">Forme</span><span class="sxs-lookup"><span data-stu-id="0d794-123">Hull</span></span> | <span data-ttu-id="0d794-124">Domain</span><span class="sxs-lookup"><span data-stu-id="0d794-124">Domain</span></span> | <span data-ttu-id="0d794-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="0d794-125">Geometry</span></span> | <span data-ttu-id="0d794-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="0d794-126">Pixel</span></span> | <span data-ttu-id="0d794-127">Compute</span><span class="sxs-lookup"><span data-stu-id="0d794-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0d794-128">x</span><span class="sxs-lookup"><span data-stu-id="0d794-128">x</span></span>      | <span data-ttu-id="0d794-129">x</span><span class="sxs-lookup"><span data-stu-id="0d794-129">x</span></span>    | <span data-ttu-id="0d794-130">x</span><span class="sxs-lookup"><span data-stu-id="0d794-130">x</span></span>      | <span data-ttu-id="0d794-131">x</span><span class="sxs-lookup"><span data-stu-id="0d794-131">x</span></span>        | <span data-ttu-id="0d794-132">x</span><span class="sxs-lookup"><span data-stu-id="0d794-132">x</span></span>     | <span data-ttu-id="0d794-133">x</span><span class="sxs-lookup"><span data-stu-id="0d794-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0d794-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d794-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d794-135">Méthodes Load4</span><span class="sxs-lookup"><span data-stu-id="0d794-135">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="0d794-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="0d794-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 