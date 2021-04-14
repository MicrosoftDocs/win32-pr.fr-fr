---
title: Message MCM_SETDAYSTATE (commctrl. h)
description: Définit les États du jour pour tous les mois actuellement visibles dans un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetDayState.
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- MCM_SETDAYSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466802"
---
# <a name="mcm_setdaystate-message"></a><span data-ttu-id="d8737-105">\_Message SETDAYSTATE MCM</span><span class="sxs-lookup"><span data-stu-id="d8737-105">MCM\_SETDAYSTATE message</span></span>

<span data-ttu-id="d8737-106">Définit les États du jour pour tous les mois actuellement visibles dans un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="d8737-106">Sets the day states for all months that are currently visible within a month calendar control.</span></span> <span data-ttu-id="d8737-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) .</span><span class="sxs-lookup"><span data-stu-id="d8737-107">You can send this message explicitly or by using the [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d8737-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8737-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8737-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d8737-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8737-110">Valeur indiquant le nombre d’éléments dans le tableau vers lequel *lParam* pointe.</span><span class="sxs-lookup"><span data-stu-id="d8737-110">Value indicating how many elements are in the array that *lParam* points to.</span></span>

</dd> <dt>

<span data-ttu-id="d8737-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8737-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d8737-112">Pointeur vers un tableau de valeurs [**MONTHDAYSTATE**](monthdaystate.md) qui définissent la façon dont le contrôle Month Calendar dessine chaque jour dans son affichage.</span><span class="sxs-lookup"><span data-stu-id="d8737-112">Pointer to an array of [**MONTHDAYSTATE**](monthdaystate.md) values that define how the month calendar control will draw each day in its display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8737-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8737-113">Return value</span></span>

<span data-ttu-id="d8737-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d8737-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8737-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d8737-115">Remarks</span></span>

<span data-ttu-id="d8737-116">Une application peut définir explicitement des informations d’état de jour en envoyant ce message, mais l’État ne sera pas conservé lorsqu’une autre partie du calendrier défilera vers l’affichage.</span><span class="sxs-lookup"><span data-stu-id="d8737-116">An application can explicitly set day state information by sending this message, but the state will not persist when a different part of the calendar is scrolled into view.</span></span> <span data-ttu-id="d8737-117">Les informations d’État du jour sont généralement définies en réponse au code de notification [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , qui est envoyé chaque fois que le contrôle doit être actualisé.</span><span class="sxs-lookup"><span data-stu-id="d8737-117">Day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed.</span></span>

<span data-ttu-id="d8737-118">Le tableau au niveau de *lParam* doit contenir autant d’éléments que la valeur retournée par la macro suivante :</span><span class="sxs-lookup"><span data-stu-id="d8737-118">The array at *lParam* must contain as many elements as the value returned by the following macro:</span></span>

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

<span data-ttu-id="d8737-119">Gardez à l’esprit que le tableau au niveau de *lParam* doit contenir des valeurs [**MONTHDAYSTATE**](monthdaystate.md) qui correspondent à tous les mois actuellement dans l’affichage du contrôle, dans l’ordre chronologique.</span><span class="sxs-lookup"><span data-stu-id="d8737-119">Keep in mind that the array at *lParam* must contain [**MONTHDAYSTATE**](monthdaystate.md) values that correspond with all months currently in the control's display, in chronological order.</span></span> <span data-ttu-id="d8737-120">Cela comprend les deux mois qui peuvent être partiellement affichés avant le premier mois et après le mois précédent.</span><span class="sxs-lookup"><span data-stu-id="d8737-120">This includes the two months that may be partially displayed before the first month and after the last month.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8737-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8737-121">Requirements</span></span>



| <span data-ttu-id="d8737-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8737-122">Requirement</span></span> | <span data-ttu-id="d8737-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8737-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8737-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8737-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d8737-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8737-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8737-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8737-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d8737-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8737-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8737-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8737-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8737-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8737-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8737-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8737-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8737-131">Utilisation des contrôles Month Calendar</span><span class="sxs-lookup"><span data-stu-id="d8737-131">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 





