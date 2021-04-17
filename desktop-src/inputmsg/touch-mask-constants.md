---
title: Masque tactile
description: Valeurs qui peuvent apparaître dans le champ touchMask de la structure POINTER_TOUCH_INFO.
ms.assetid: 23AD50C8-C769-48D6-9F27-DB2755C03D5C
topic_type:
- apiref
api_name:
- TOUCH_MASK_NONE
- TOUCH_MASK_CONTACTAREA
- TOUCH_MASK_ORIENTATION
- TOUCH_MASK_PRESSURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5ac389894d9096b389af127685feb9a2d81756ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466666"
---
# <a name="touch-mask"></a><span data-ttu-id="79fa4-103">Masque tactile</span><span class="sxs-lookup"><span data-stu-id="79fa4-103">Touch Mask</span></span>

<span data-ttu-id="79fa4-104">Valeurs qui peuvent apparaître dans le champ **touchMask** de la structure [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="79fa4-104">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="79fa4-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="79fa4-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="79fa4-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="79fa4-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="79fa4-107">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="79fa4-107">Default.</span></span> <span data-ttu-id="79fa4-108">Aucun des champs facultatifs n’est valide.</span><span class="sxs-lookup"><span data-stu-id="79fa4-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79fa4-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span><span class="sxs-lookup"><span data-stu-id="79fa4-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79fa4-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="79fa4-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="79fa4-111">**rcContact** de la structure [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) est valide.</span><span class="sxs-lookup"><span data-stu-id="79fa4-111">**rcContact** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79fa4-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span><span class="sxs-lookup"><span data-stu-id="79fa4-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79fa4-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="79fa4-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="79fa4-114">l' **orientation** de la structure de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) est valide.</span><span class="sxs-lookup"><span data-stu-id="79fa4-114">**orientation** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79fa4-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="79fa4-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79fa4-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="79fa4-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="79fa4-117">la **pression** de la structure de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) est valide.</span><span class="sxs-lookup"><span data-stu-id="79fa4-117">**pressure** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79fa4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79fa4-118">Requirements</span></span>



| <span data-ttu-id="79fa4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79fa4-119">Requirement</span></span> | <span data-ttu-id="79fa4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="79fa4-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="79fa4-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79fa4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="79fa4-122">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79fa4-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="79fa4-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79fa4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="79fa4-124">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79fa4-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="79fa4-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="79fa4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="79fa4-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="79fa4-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79fa4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79fa4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79fa4-128">Constantes</span><span class="sxs-lookup"><span data-stu-id="79fa4-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="79fa4-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="79fa4-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





