---
title: Message TBM_SETRANGEMIN (commctrl. h)
description: Définit la position logique minimale du curseur dans un TrackBar.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- TBM_SETRANGEMIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34c2e70aa6247cb970e576c915bdcd28cd18d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941661"
---
# <a name="tbm_setrangemin-message"></a><span data-ttu-id="55050-104">\_Message TBM SETRANGEMIN</span><span class="sxs-lookup"><span data-stu-id="55050-104">TBM\_SETRANGEMIN message</span></span>

<span data-ttu-id="55050-105">Définit la position logique minimale du curseur dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="55050-105">Sets the minimum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="55050-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55050-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55050-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55050-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55050-108">Indicateur de redessin.</span><span class="sxs-lookup"><span data-stu-id="55050-108">Redraw flag.</span></span> <span data-ttu-id="55050-109">Si ce paramètre a la **valeur true**, le message redessine le TrackBar une fois la plage définie.</span><span class="sxs-lookup"><span data-stu-id="55050-109">If this parameter is **TRUE**, the message redraws the trackbar after the range is set.</span></span> <span data-ttu-id="55050-110">Si ce paramètre a la **valeur false**, le message définit la plage mais ne redessine pas le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="55050-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="55050-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55050-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55050-112">Position minimale du curseur.</span><span class="sxs-lookup"><span data-stu-id="55050-112">Minimum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55050-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55050-113">Return value</span></span>

<span data-ttu-id="55050-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="55050-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55050-115">Notes</span><span class="sxs-lookup"><span data-stu-id="55050-115">Remarks</span></span>

<span data-ttu-id="55050-116">Si la position actuelle du curseur est inférieure à la nouvelle valeur minimale, le message **TBM \_ SETRANGEMIN** définit la position du curseur sur la nouvelle valeur minimale.</span><span class="sxs-lookup"><span data-stu-id="55050-116">If the current slider position is less than the new minimum, the **TBM\_SETRANGEMIN** message sets the slider position to the new minimum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="55050-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55050-117">Requirements</span></span>



| <span data-ttu-id="55050-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55050-118">Requirement</span></span> | <span data-ttu-id="55050-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="55050-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55050-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55050-120">Minimum supported client</span></span><br/> | <span data-ttu-id="55050-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55050-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55050-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55050-122">Minimum supported server</span></span><br/> | <span data-ttu-id="55050-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55050-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55050-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="55050-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="55050-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55050-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55050-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55050-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="55050-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="55050-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="55050-128">**TBM \_ SEtrange**</span><span class="sxs-lookup"><span data-stu-id="55050-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="55050-129">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="55050-129">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





