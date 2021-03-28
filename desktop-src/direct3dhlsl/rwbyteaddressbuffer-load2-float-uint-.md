---
title: 'RWByteAddressBuffer :: Load2 (uint, uint), fonction'
description: Obtient deux valeurs et retourne l’état de l’opération.
ms.assetid: E6BBA8A7-D53F-4718-B007-EBDE50FADB06
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
ms.openlocfilehash: 92fc492fddb6ad024a4507829e81dab4886af590
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101656"
---
# <a name="load2uintuint-function"></a><span data-ttu-id="3c1f4-104">Load2 (uint, uint) (fonction)</span><span class="sxs-lookup"><span data-stu-id="3c1f4-104">Load2(uint,uint) function</span></span>

<span data-ttu-id="3c1f4-105">Obtient deux valeurs et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3c1f4-105">Gets two values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c1f4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c1f4-106">Syntax</span></span>


``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="3c1f4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c1f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c1f4-108">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c1f4-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c1f4-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="3c1f4-109">Type: **uint**</span></span>

<span data-ttu-id="3c1f4-110">Emplacement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3c1f4-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3c1f4-111">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3c1f4-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c1f4-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="3c1f4-112">Type: **uint**</span></span>

<span data-ttu-id="3c1f4-113">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="3c1f4-113">The status of the operation.</span></span> <span data-ttu-id="3c1f4-114">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3c1f4-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3c1f4-115">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3c1f4-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3c1f4-116">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="3c1f4-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c1f4-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c1f4-117">Return value</span></span>

<span data-ttu-id="3c1f4-118">Type : **uint2**</span><span class="sxs-lookup"><span data-stu-id="3c1f4-118">Type: **uint2**</span></span>

<span data-ttu-id="3c1f4-119">Deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="3c1f4-119">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c1f4-120">Notes</span><span class="sxs-lookup"><span data-stu-id="3c1f4-120">Remarks</span></span>

<span data-ttu-id="3c1f4-121">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="3c1f4-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3c1f4-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="3c1f4-122">Vertex</span></span> | <span data-ttu-id="3c1f4-123">Forme</span><span class="sxs-lookup"><span data-stu-id="3c1f4-123">Hull</span></span> | <span data-ttu-id="3c1f4-124">Domain</span><span class="sxs-lookup"><span data-stu-id="3c1f4-124">Domain</span></span> | <span data-ttu-id="3c1f4-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="3c1f4-125">Geometry</span></span> | <span data-ttu-id="3c1f4-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="3c1f4-126">Pixel</span></span> | <span data-ttu-id="3c1f4-127">Compute</span><span class="sxs-lookup"><span data-stu-id="3c1f4-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3c1f4-128">x</span><span class="sxs-lookup"><span data-stu-id="3c1f4-128">x</span></span>     | <span data-ttu-id="3c1f4-129">x</span><span class="sxs-lookup"><span data-stu-id="3c1f4-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3c1f4-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c1f4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c1f4-131">Méthodes Load2</span><span class="sxs-lookup"><span data-stu-id="3c1f4-131">Load2 methods</span></span>](rwbyteaddressbuffer-load2.md)
</dt> </dl>

 

 