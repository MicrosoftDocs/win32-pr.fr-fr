---
description: Avertit les applications d’une modification de l’état d’alimentation de l’ordinateur, par exemple un passage de la batterie à un/C.
ms.assetid: dc56fee3-e0df-4f8e-8a41-92460279280a
title: Événement PBT_APMPOWERSTATUSCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ed67f7ba064d44614196da4190ce18a996bd5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202864"
---
# <a name="pbt_apmpowerstatuschange-event"></a><span data-ttu-id="c449e-103">\_Événement PBT APMPOWERSTATUSCHANGE</span><span class="sxs-lookup"><span data-stu-id="c449e-103">PBT\_APMPOWERSTATUSCHANGE event</span></span>

<span data-ttu-id="c449e-104">Avertit les applications d’une modification de l’état d’alimentation de l’ordinateur, par exemple un passage de la batterie à un/C.</span><span class="sxs-lookup"><span data-stu-id="c449e-104">Notifies applications of a change in the power status of the computer, such as a switch from battery power to A/C.</span></span> <span data-ttu-id="c449e-105">Le système diffuse également cet événement lorsque la puissance de la batterie devient inférieure au seuil spécifié par l'utilisateur ou change selon un pourcentage spécifié.</span><span class="sxs-lookup"><span data-stu-id="c449e-105">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

<span data-ttu-id="c449e-106">Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="c449e-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="c449e-107">Les paramètres *wParam* et *lParam* sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="c449e-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMPOWERSTATUSCHANGE
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="c449e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c449e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c449e-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="c449e-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c449e-110">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c449e-110">A handle to window.</span></span>

<span data-ttu-id="c449e-111"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="c449e-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="c449e-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="c449e-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="c449e-113">Signification</span><span class="sxs-lookup"><span data-stu-id="c449e-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="c449e-114"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="c449e-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="c449e-115">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="c449e-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="c449e-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="c449e-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="c449e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c449e-117">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="c449e-118">Signification</span><span class="sxs-lookup"><span data-stu-id="c449e-118">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="c449e-119"><dt>**PBT \_ APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="c449e-119"><dt>**PBT\_APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="c449e-120">Identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="c449e-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c449e-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c449e-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c449e-122">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c449e-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c449e-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c449e-123">Return value</span></span>

<span data-ttu-id="c449e-124">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="c449e-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c449e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c449e-125">Remarks</span></span>

<span data-ttu-id="c449e-126">Une application doit traiter cet événement en appelant la fonction [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) pour récupérer l’état actuel de l’alimentation de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c449e-126">An application should process this event by calling the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve the current power status of the computer.</span></span> <span data-ttu-id="c449e-127">En particulier, l’application doit vérifier les membres **ACLineStatus**, **BatteryFlag**, **BatteryLifeTime** et **BatteryLifePercent** de la structure [**\_ \_ État**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) de l’alimentation du système pour toute modification.</span><span class="sxs-lookup"><span data-stu-id="c449e-127">In particular, the application should check the **ACLineStatus**, **BatteryFlag**, **BatteryLifeTime**, and **BatteryLifePercent** members of the [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) structure for any changes.</span></span> <span data-ttu-id="c449e-128">Cet événement peut se produire lorsque la durée de la batterie chute à moins de 5 minutes, ou lorsque le pourcentage de la durée de vie de la batterie passe sous 10 pour cent, ou si la durée de vie de la batterie change de 3%.</span><span class="sxs-lookup"><span data-stu-id="c449e-128">This event can occur when battery life drops to less than 5 minutes, or when the percentage of battery life drops below 10 percent, or if the battery life changes by 3 percent.</span></span>

## <a name="requirements"></a><span data-ttu-id="c449e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c449e-129">Requirements</span></span>



| <span data-ttu-id="c449e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c449e-130">Requirement</span></span> | <span data-ttu-id="c449e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c449e-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c449e-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c449e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c449e-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c449e-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c449e-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c449e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c449e-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c449e-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c449e-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="c449e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c449e-137"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c449e-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c449e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c449e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c449e-139">État de l’alimentation du système</span><span class="sxs-lookup"><span data-stu-id="c449e-139">System Power Status</span></span>](system-power-status.md)
</dt> <dt>

[<span data-ttu-id="c449e-140">Événements de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="c449e-140">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="c449e-141">**GetSystemPowerStatus**</span><span class="sxs-lookup"><span data-stu-id="c449e-141">**GetSystemPowerStatus**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus)
</dt> <dt>

[<span data-ttu-id="c449e-142">**État de l’alimentation du système \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c449e-142">**SYSTEM\_POWER\_STATUS**</span></span>](/windows/desktop/api/Winbase/ns-winbase-system_power_status)
</dt> <dt>

[<span data-ttu-id="c449e-143">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="c449e-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




