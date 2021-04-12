---
title: Message TBM_SETRANGEMAX (commctrl. h)
description: Définit la position logique maximale du curseur dans un TrackBar.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- TBM_SETRANGEMAX les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43997725e2fa88db3f9d4dc2fec1d51255cbb0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464254"
---
# <a name="tbm_setrangemax-message"></a><span data-ttu-id="f286e-104">\_Message TBM SETRANGEMAX</span><span class="sxs-lookup"><span data-stu-id="f286e-104">TBM\_SETRANGEMAX message</span></span>

<span data-ttu-id="f286e-105">Définit la position logique maximale du curseur dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f286e-105">Sets the maximum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f286e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f286e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f286e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f286e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f286e-108">Indicateur de redessin.</span><span class="sxs-lookup"><span data-stu-id="f286e-108">Redraw flag.</span></span> <span data-ttu-id="f286e-109">Si ce paramètre a la **valeur true**, le TrackBar est redessiné après la définition de la plage.</span><span class="sxs-lookup"><span data-stu-id="f286e-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="f286e-110">Si ce paramètre a la **valeur false**, le message définit la plage mais ne redessine pas le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f286e-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="f286e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f286e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f286e-112">Position maximale du curseur.</span><span class="sxs-lookup"><span data-stu-id="f286e-112">Maximum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f286e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f286e-113">Return value</span></span>

<span data-ttu-id="f286e-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f286e-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f286e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f286e-115">Remarks</span></span>

<span data-ttu-id="f286e-116">Si la position actuelle du curseur est supérieure au nouveau maximum, le message **TBM \_ SETRANGEMAX** définit la position du curseur sur la nouvelle valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="f286e-116">If the current slider position is greater than the new maximum, the **TBM\_SETRANGEMAX** message sets the slider position to the new maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f286e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f286e-117">Requirements</span></span>



| <span data-ttu-id="f286e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f286e-118">Requirement</span></span> | <span data-ttu-id="f286e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f286e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f286e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f286e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f286e-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f286e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f286e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f286e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f286e-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f286e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f286e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f286e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f286e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f286e-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f286e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f286e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f286e-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f286e-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f286e-128">**TBM \_ SEtrange**</span><span class="sxs-lookup"><span data-stu-id="f286e-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="f286e-129">**TBM \_ SETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="f286e-129">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

 





