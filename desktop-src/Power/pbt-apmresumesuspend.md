---
description: Avertit les applications que le système a repris l’opération après avoir été suspendue.
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: Événement PBT_APMRESUMESUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519894"
---
# <a name="pbt_apmresumesuspend-event"></a><span data-ttu-id="203dd-103">\_Événement PBT APMRESUMESUSPEND</span><span class="sxs-lookup"><span data-stu-id="203dd-103">PBT\_APMRESUMESUSPEND event</span></span>

<span data-ttu-id="203dd-104">Avertit les applications que le système a repris l’opération après avoir été suspendue.</span><span class="sxs-lookup"><span data-stu-id="203dd-104">Notifies applications that the system has resumed operation after being suspended.</span></span>

<span data-ttu-id="203dd-105">Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="203dd-105">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="203dd-106">Les paramètres *wParam* et *lParam* sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="203dd-106">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="203dd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="203dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="203dd-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="203dd-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="203dd-109">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="203dd-109">A handle to window.</span></span>

<span data-ttu-id="203dd-110"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="203dd-110"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="203dd-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="203dd-111">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="203dd-112">Signification</span><span class="sxs-lookup"><span data-stu-id="203dd-112">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="203dd-113"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="203dd-113"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="203dd-114">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="203dd-114">Message identifier.</span></span><br/> |



 

<span data-ttu-id="203dd-115"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="203dd-115"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="203dd-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="203dd-116">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="203dd-117">Signification</span><span class="sxs-lookup"><span data-stu-id="203dd-117">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="203dd-118"><dt>**PBT \_ APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="203dd-118"><dt>**PBT\_APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt></span></span> </dl> | <span data-ttu-id="203dd-119">Identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="203dd-119">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="203dd-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="203dd-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="203dd-121">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="203dd-121">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="203dd-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="203dd-122">Return value</span></span>

<span data-ttu-id="203dd-123">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="203dd-123">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="203dd-124">Notes</span><span class="sxs-lookup"><span data-stu-id="203dd-124">Remarks</span></span>

<span data-ttu-id="203dd-125">Une application peut recevoir cet événement uniquement si elle a reçu l’événement [PBT \_ APMSUSPEND](pbt-apmsuspend.md) avant la suspension de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="203dd-125">An application can receive this event only if it received the [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended.</span></span> <span data-ttu-id="203dd-126">Dans le cas contraire, l’application recevra un événement [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) .</span><span class="sxs-lookup"><span data-stu-id="203dd-126">Otherwise, the application will receive a [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event.</span></span>

<span data-ttu-id="203dd-127">Si le système sort de veille en raison de l’activité de l’utilisateur (par exemple, en appuyant sur le bouton d’alimentation) ou si le système détecte l’interaction de l’utilisateur au niveau de la console physique (par exemple, la souris ou l’entrée au clavier) après l’éveil sans assistance, le système diffuse d’abord l’événement [ \_ APMRESUMEAUTOMATIC PBT](pbt-apmresumeautomatic.md) , puis diffuse l' \_ événement PBT APMRESUMESUSPEND</span><span class="sxs-lookup"><span data-stu-id="203dd-127">If the system wakes due to user activity (such as pressing the power button) or if the system detects user interaction at the physical console (such as mouse or keyboard input) after waking unattended, the system first broadcasts the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event, then it broadcasts the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="203dd-128">En outre, le système active l’affichage.</span><span class="sxs-lookup"><span data-stu-id="203dd-128">In addition, the system turns on the display.</span></span> <span data-ttu-id="203dd-129">Votre application doit rouvrir les fichiers qu’elle a fermés lorsque le système est passé en mode veille et se prépare à l’entrée utilisateur.</span><span class="sxs-lookup"><span data-stu-id="203dd-129">Your application should reopen files that it closed when the system entered sleep and prepare for user input.</span></span>

<span data-ttu-id="203dd-130">Si le système sort de veille en raison d’un signal de réveil externe (éveil à distance), le système diffuse uniquement l’événement [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) .</span><span class="sxs-lookup"><span data-stu-id="203dd-130">If the system wakes due to an external wake signal (remote wake), the system broadcasts only the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event.</span></span> <span data-ttu-id="203dd-131">L' \_ événement PBT APMRESUMESUSPEND n’est pas envoyé.</span><span class="sxs-lookup"><span data-stu-id="203dd-131">The PBT\_APMRESUMESUSPEND event is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="203dd-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="203dd-132">Requirements</span></span>



| <span data-ttu-id="203dd-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="203dd-133">Requirement</span></span> | <span data-ttu-id="203dd-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="203dd-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="203dd-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="203dd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="203dd-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="203dd-136">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="203dd-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="203dd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="203dd-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="203dd-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="203dd-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="203dd-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="203dd-140"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="203dd-140"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="203dd-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="203dd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="203dd-142">Événements de mise en éveil du système</span><span class="sxs-lookup"><span data-stu-id="203dd-142">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="203dd-143">Événements de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="203dd-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="203dd-144">PBT \_ APMSUSPEND</span><span class="sxs-lookup"><span data-stu-id="203dd-144">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="203dd-145">PBT \_ APMRESUMECRITICAL</span><span class="sxs-lookup"><span data-stu-id="203dd-145">PBT\_APMRESUMECRITICAL</span></span>](pbt-apmresumecritical.md)
</dt> <dt>

[<span data-ttu-id="203dd-146">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="203dd-146">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




