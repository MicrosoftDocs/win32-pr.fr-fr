---
description: Notifie les applications que le système reprend du mode veille ou veille prolongée. Cet événement est remis chaque fois que le système reprend et n’indique pas si un utilisateur est présent.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: Événement PBT_APMRESUMEAUTOMATIC (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a481dee356c85b3831fcace0c1ff127b0b276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865070"
---
# <a name="pbt_apmresumeautomatic-event"></a><span data-ttu-id="f75af-104">\_Événement PBT APMRESUMEAUTOMATIC</span><span class="sxs-lookup"><span data-stu-id="f75af-104">PBT\_APMRESUMEAUTOMATIC event</span></span>

<span data-ttu-id="f75af-105">Notifie les applications que le système reprend du mode veille ou veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="f75af-105">Notifies applications that the system is resuming from sleep or hibernation.</span></span> <span data-ttu-id="f75af-106">Cet événement est remis chaque fois que le système reprend et n’indique pas si un utilisateur est présent.</span><span class="sxs-lookup"><span data-stu-id="f75af-106">This event is delivered every time the system resumes and does not indicate whether a user is present.</span></span>

<span data-ttu-id="f75af-107">Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="f75af-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="f75af-108">Les paramètres *wParam* et *lParam* sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="f75af-108">The *wParam* and *lParam* parameters are set as described following.</span></span>

> [!Note]  
> <span data-ttu-id="f75af-109">Dans les systèmes Windows 10, version 1507 ou ultérieure, si le système sort du mode veille uniquement à entrer immédiatement en veille prolongée, cet événement n’est pas remis.</span><span class="sxs-lookup"><span data-stu-id="f75af-109">In Windows 10, version 1507 systems or later, if the system is resuming from sleep only to immediately enter hibernation, this event is not delivered.</span></span> <span data-ttu-id="f75af-110">Un message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) n’est pas envoyé dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="f75af-110">A [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message is not sent in this case.</span></span>

 


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMEAUTOMATIC
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="f75af-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f75af-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f75af-112">*HWND*</span><span class="sxs-lookup"><span data-stu-id="f75af-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f75af-113">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f75af-113">A handle to window.</span></span>

<span data-ttu-id="f75af-114"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="f75af-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="f75af-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f75af-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="f75af-116">Signification</span><span class="sxs-lookup"><span data-stu-id="f75af-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="f75af-117"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="f75af-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="f75af-118">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="f75af-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="f75af-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="f75af-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="f75af-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f75af-120">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="f75af-121">Signification</span><span class="sxs-lookup"><span data-stu-id="f75af-121">Meaning</span></span>                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="f75af-122"><dt>**PBT \_ APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="f75af-122"><dt>**PBT\_APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="f75af-123">Identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="f75af-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f75af-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f75af-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f75af-125">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f75af-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f75af-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f75af-126">Return value</span></span>

<span data-ttu-id="f75af-127">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f75af-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f75af-128">Notes</span><span class="sxs-lookup"><span data-stu-id="f75af-128">Remarks</span></span>

<span data-ttu-id="f75af-129">Si le système détecte une activité utilisateur après avoir diffusé PBT \_ APMRESUMEAUTOMATIC, il diffuse un événement [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) pour permettre aux applications de savoir qu’elles peuvent reprendre une interaction complète avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f75af-129">If the system detects any user activity after broadcasting PBT\_APMRESUMEAUTOMATIC, it will broadcast a [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) event to let applications know they can resume full interaction with the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="f75af-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f75af-130">Requirements</span></span>



| <span data-ttu-id="f75af-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f75af-131">Requirement</span></span> | <span data-ttu-id="f75af-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="f75af-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f75af-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f75af-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f75af-134">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f75af-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f75af-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f75af-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f75af-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f75af-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f75af-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="f75af-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f75af-138"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f75af-138"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f75af-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f75af-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f75af-140">Événements de mise en éveil du système</span><span class="sxs-lookup"><span data-stu-id="f75af-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="f75af-141">Événements de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="f75af-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="f75af-142">PBT \_ APMRESUMESUSPEND</span><span class="sxs-lookup"><span data-stu-id="f75af-142">PBT\_APMRESUMESUSPEND</span></span>](pbt-apmresumesuspend.md)
</dt> <dt>

[<span data-ttu-id="f75af-143">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="f75af-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




