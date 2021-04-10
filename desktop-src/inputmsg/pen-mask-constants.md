---
title: Masque du stylet
description: Valeurs qui peuvent apparaître dans le champ penMask de la structure POINTER_PEN_INFO.
ms.assetid: 6A44B701-55E1-41D4-9C4A-807E57441DA4
topic_type:
- apiref
api_name:
- PEN_MASK_NONE
- PEN_MASK_PRESSURE
- PEN_MASK_ROTATION
- PEN_MASK_TILT_X
- PEN_MASK_TILT_Y
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bd181b5eafbe1cf6de56c95886deb04e5bd6d2b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104563"
---
# <a name="pen-mask"></a><span data-ttu-id="24812-103">Masque du stylet</span><span class="sxs-lookup"><span data-stu-id="24812-103">Pen Mask</span></span>

<span data-ttu-id="24812-104">Valeurs qui peuvent apparaître dans le champ **penMask** de la structure [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="24812-104">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="24812-105"><span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="24812-105"><span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24812-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="24812-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="24812-107">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="24812-107">Default.</span></span> <span data-ttu-id="24812-108">Aucun des champs facultatifs n’est valide.</span><span class="sxs-lookup"><span data-stu-id="24812-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24812-109"><span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="24812-109"><span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24812-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="24812-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="24812-111">la **pression** de la structure de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) est valide.</span><span class="sxs-lookup"><span data-stu-id="24812-111">**pressure** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24812-112"><span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**</span><span class="sxs-lookup"><span data-stu-id="24812-112"><span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24812-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="24812-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="24812-114">la **rotation** de la structure de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) est valide.</span><span class="sxs-lookup"><span data-stu-id="24812-114">**rotation** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24812-115"><span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X**</span><span class="sxs-lookup"><span data-stu-id="24812-115"><span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="24812-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="24812-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="24812-117">**tiltX** de la structure [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) est valide.</span><span class="sxs-lookup"><span data-stu-id="24812-117">**tiltX** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24812-118"><span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**</span><span class="sxs-lookup"><span data-stu-id="24812-118"><span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24812-119">0x00000008</span><span class="sxs-lookup"><span data-stu-id="24812-119">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="24812-120">l' **inclinaison** de la structure de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) est valide.</span><span class="sxs-lookup"><span data-stu-id="24812-120">**tiltY** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24812-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24812-121">Requirements</span></span>



| <span data-ttu-id="24812-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24812-122">Requirement</span></span> | <span data-ttu-id="24812-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="24812-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="24812-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24812-124">Minimum supported client</span></span><br/> | <span data-ttu-id="24812-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24812-125">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="24812-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24812-126">Minimum supported server</span></span><br/> | <span data-ttu-id="24812-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24812-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="24812-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="24812-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="24812-129"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="24812-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24812-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24812-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24812-131">Constantes</span><span class="sxs-lookup"><span data-stu-id="24812-131">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="24812-132">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="24812-132">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





