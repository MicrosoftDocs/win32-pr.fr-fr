---
description: Notifie les applications que l’ordinateur est sur le poste d’entrer dans un état suspendu.
ms.assetid: 61b177a0-4cff-4740-bed8-a46c06c43be8
title: Événement PBT_APMSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6982e00565329c85e06765879b9b72b07fe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202863"
---
# <a name="pbt_apmsuspend-event"></a><span data-ttu-id="8ecd4-103">\_Événement PBT APMSUSPEND</span><span class="sxs-lookup"><span data-stu-id="8ecd4-103">PBT\_APMSUSPEND event</span></span>

<span data-ttu-id="8ecd4-104">Notifie les applications que l’ordinateur est sur le poste d’entrer dans un état suspendu.</span><span class="sxs-lookup"><span data-stu-id="8ecd4-104">Notifies applications that the computer is about to enter a suspended state.</span></span> <span data-ttu-id="8ecd4-105">Cet événement est généralement diffusé lorsque toutes les applications et tous les pilotes installables ont renvoyé la **valeur true** à un événement [ \_ APMQUERYSUSPEND PBT](pbt-apmquerysuspend.md) précédent.</span><span class="sxs-lookup"><span data-stu-id="8ecd4-105">This event is typically broadcast when all applications and installable drivers have returned **TRUE** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="8ecd4-106">Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="8ecd4-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="8ecd4-107">Les paramètres *wParam* et *lParam* sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="8ecd4-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMSUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="8ecd4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ecd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ecd4-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8ecd4-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8ecd4-110">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8ecd4-110">A handle to window.</span></span>

<span data-ttu-id="8ecd4-111"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="8ecd4-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="8ecd4-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ecd4-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="8ecd4-113">Signification</span><span class="sxs-lookup"><span data-stu-id="8ecd4-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="8ecd4-114"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="8ecd4-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="8ecd4-115">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="8ecd4-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="8ecd4-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="8ecd4-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="8ecd4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ecd4-117">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="8ecd4-118">Signification</span><span class="sxs-lookup"><span data-stu-id="8ecd4-118">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="8ecd4-119"><dt>**PBT \_ APMSUSPEND**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="8ecd4-119"><dt>**PBT\_APMSUSPEND**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="8ecd4-120">Identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="8ecd4-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ecd4-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ecd4-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ecd4-122">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="8ecd4-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ecd4-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ecd4-123">Return value</span></span>

<span data-ttu-id="8ecd4-124">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="8ecd4-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ecd4-125">Notes</span><span class="sxs-lookup"><span data-stu-id="8ecd4-125">Remarks</span></span>

<span data-ttu-id="8ecd4-126">Une application doit traiter cet événement en effectuant toutes les tâches nécessaires pour enregistrer les données.</span><span class="sxs-lookup"><span data-stu-id="8ecd4-126">An application should process this event by completing all tasks necessary to save data.</span></span>

<span data-ttu-id="8ecd4-127">Le système autorise environ deux secondes à ce que l’application gère cette notification.</span><span class="sxs-lookup"><span data-stu-id="8ecd4-127">The system allows approximately two seconds for an application to handle this notification.</span></span> <span data-ttu-id="8ecd4-128">Si une application effectue toujours des opérations après l’expiration de son allocation, le système peut interrompre l’application.</span><span class="sxs-lookup"><span data-stu-id="8ecd4-128">If an application is still performing operations after its time allotment has expired, the system may interrupt the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ecd4-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ecd4-129">Requirements</span></span>



| <span data-ttu-id="8ecd4-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ecd4-130">Requirement</span></span> | <span data-ttu-id="8ecd4-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ecd4-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ecd4-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ecd4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8ecd4-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ecd4-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8ecd4-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ecd4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8ecd4-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ecd4-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8ecd4-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ecd4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ecd4-137"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ecd4-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ecd4-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ecd4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ecd4-139">Critères de veille du système</span><span class="sxs-lookup"><span data-stu-id="8ecd4-139">System Sleep Criteria</span></span>](system-sleep-criteria.md)
</dt> <dt>

[<span data-ttu-id="8ecd4-140">Événements de mise en éveil du système</span><span class="sxs-lookup"><span data-stu-id="8ecd4-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="8ecd4-141">Événements de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="8ecd4-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="8ecd4-142">PBT \_ APMQUERYSUSPEND</span><span class="sxs-lookup"><span data-stu-id="8ecd4-142">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="8ecd4-143">**SetSystemPowerState**</span><span class="sxs-lookup"><span data-stu-id="8ecd4-143">**SetSystemPowerState**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setsystempowerstate)
</dt> <dt>

[<span data-ttu-id="8ecd4-144">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="8ecd4-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




