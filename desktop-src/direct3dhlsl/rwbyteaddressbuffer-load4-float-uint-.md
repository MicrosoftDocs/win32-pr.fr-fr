---
title: 'RWByteAddressBuffer :: Load4 (uint, uint), fonction'
description: Obtient quatre valeurs et retourne l’état de l’opération.
ms.assetid: 10C21836-3CE4-4AE9-82F4-C8BBDE19CA69
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
ms.openlocfilehash: 14cb5354c21935c22833ea6f4b54b20fedc696f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730124"
---
# <a name="load4uintuint-function"></a><span data-ttu-id="5c256-104">Load4 (uint, uint) (fonction)</span><span class="sxs-lookup"><span data-stu-id="5c256-104">Load4(uint,uint) function</span></span>

<span data-ttu-id="5c256-105">Obtient quatre valeurs et retourne l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5c256-105">Gets four values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c256-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c256-106">Syntax</span></span>


``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="5c256-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c256-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c256-108">*Emplacement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c256-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c256-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="5c256-109">Type: **uint**</span></span>

<span data-ttu-id="5c256-110">Emplacement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5c256-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5c256-111">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5c256-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c256-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="5c256-112">Type: **uint**</span></span>

<span data-ttu-id="5c256-113">L’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5c256-113">The status of the operation.</span></span> <span data-ttu-id="5c256-114">Vous ne pouvez pas accéder directement à l’État. au lieu de cela, transmettez l’État à la fonction intrinsèque [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="5c256-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5c256-115">**CheckAccessFullyMapped** retourne la **valeur true** si toutes les valeurs de l' **exemple**, de **regroupement** ou d’opération de **chargement** correspondant ont accédé à des vignettes mappées dans une [ressource en mosaïque](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="5c256-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5c256-116">Si des valeurs ont été extraites d’une vignette non mappée, **CheckAccessFullyMapped** retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="5c256-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c256-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c256-117">Return value</span></span>

<span data-ttu-id="5c256-118">Type : **uint4**</span><span class="sxs-lookup"><span data-stu-id="5c256-118">Type: **uint4**</span></span>

<span data-ttu-id="5c256-119">Quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="5c256-119">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c256-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5c256-120">Remarks</span></span>

<span data-ttu-id="5c256-121">Cette fonction est prise en charge pour les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="5c256-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5c256-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="5c256-122">Vertex</span></span> | <span data-ttu-id="5c256-123">Forme</span><span class="sxs-lookup"><span data-stu-id="5c256-123">Hull</span></span> | <span data-ttu-id="5c256-124">Domain</span><span class="sxs-lookup"><span data-stu-id="5c256-124">Domain</span></span> | <span data-ttu-id="5c256-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="5c256-125">Geometry</span></span> | <span data-ttu-id="5c256-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="5c256-126">Pixel</span></span> | <span data-ttu-id="5c256-127">Compute</span><span class="sxs-lookup"><span data-stu-id="5c256-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5c256-128">x</span><span class="sxs-lookup"><span data-stu-id="5c256-128">x</span></span>     | <span data-ttu-id="5c256-129">x</span><span class="sxs-lookup"><span data-stu-id="5c256-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5c256-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c256-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c256-131">Méthodes Load4</span><span class="sxs-lookup"><span data-stu-id="5c256-131">Load4 methods</span></span>](rwbyteaddressbuffer-load4.md)
</dt> </dl>

 

 