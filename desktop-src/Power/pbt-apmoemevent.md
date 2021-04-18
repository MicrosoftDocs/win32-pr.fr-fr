---
description: Notifie les applications que le BIOS APM a signalé un événement OEM APM.
ms.assetid: 3251ac00-41f1-44e9-a579-fa31e7c7d2ff
title: Événement PBT_APMOEMEVENT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a99b99bdaf69b1a53a24ad33cd898fd1c806694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519895"
---
# <a name="pbt_apmoemevent-event"></a><span data-ttu-id="acf70-103">\_Événement PBT APMOEMEVENT</span><span class="sxs-lookup"><span data-stu-id="acf70-103">PBT\_APMOEMEVENT event</span></span>

<span data-ttu-id="acf70-104">\[PBT \_ APMOEMEVENT peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="acf70-104">\[PBT\_APMOEMEVENT is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="acf70-105">La prise en charge de cet événement a été supprimée dans Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="acf70-105">Support for this event was removed in Windows Vista.\]</span></span>

<span data-ttu-id="acf70-106">Notifie les applications que le BIOS APM a signalé un événement OEM APM.</span><span class="sxs-lookup"><span data-stu-id="acf70-106">Notifies applications that the APM BIOS has signaled an APM OEM event.</span></span>

<span data-ttu-id="acf70-107">Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="acf70-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="acf70-108">Les paramètres *wParam* et *lParam* sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="acf70-108">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMOEMEVENT
            LPARAM lParam); // OEM event code
```



## <a name="parameters"></a><span data-ttu-id="acf70-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acf70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acf70-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="acf70-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="acf70-111">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="acf70-111">A handle to window.</span></span>

<span data-ttu-id="acf70-112"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="acf70-112"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="acf70-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="acf70-113">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="acf70-114">Signification</span><span class="sxs-lookup"><span data-stu-id="acf70-114">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="acf70-115"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="acf70-115"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="acf70-116">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="acf70-116">Message identifier.</span></span><br/> |



 

<span data-ttu-id="acf70-117"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="acf70-117"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="acf70-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="acf70-118">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="acf70-119">Signification</span><span class="sxs-lookup"><span data-stu-id="acf70-119">Meaning</span></span>                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMOEMEVENT"></span><span id="pbt_apmoemevent"></span><dl> <span data-ttu-id="acf70-120"><dt>**PBT \_ APMOEMEVENT**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="acf70-120"><dt>**PBT\_APMOEMEVENT**</dt> <dt>11 (0xB)</dt></span></span> </dl> | <span data-ttu-id="acf70-121">Identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="acf70-121">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="acf70-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acf70-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acf70-123">Code d’événement défini par l’OEM qui a été signalé par le BIOS APM du système.</span><span class="sxs-lookup"><span data-stu-id="acf70-123">The OEM-defined event code that was signaled by the system's APM BIOS.</span></span> <span data-ttu-id="acf70-124">Les codes d’événement OEM se trouvent dans la plage 0200h-02FFh.</span><span class="sxs-lookup"><span data-stu-id="acf70-124">OEM event codes are in the range 0200h - 02FFh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acf70-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acf70-125">Return value</span></span>

<span data-ttu-id="acf70-126">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="acf70-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="acf70-127">Notes</span><span class="sxs-lookup"><span data-stu-id="acf70-127">Remarks</span></span>

<span data-ttu-id="acf70-128">Dans la mesure où toutes les implémentations du BIOS APM ne fournissent pas de notifications d’événements OEM, cet événement peut ne jamais être diffusé sur certains ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="acf70-128">Because not all APM BIOS implementations provide OEM event notifications, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="acf70-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acf70-129">Requirements</span></span>



| <span data-ttu-id="acf70-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acf70-130">Requirement</span></span> | <span data-ttu-id="acf70-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="acf70-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acf70-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acf70-132">Minimum supported client</span></span><br/> | <span data-ttu-id="acf70-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acf70-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="acf70-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acf70-134">Minimum supported server</span></span><br/> | <span data-ttu-id="acf70-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acf70-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="acf70-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="acf70-136">End of client support</span></span><br/>    | <span data-ttu-id="acf70-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="acf70-137">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="acf70-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="acf70-138">End of server support</span></span><br/>    | <span data-ttu-id="acf70-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="acf70-139">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="acf70-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="acf70-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="acf70-141"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="acf70-141"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acf70-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acf70-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf70-143">Événements de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="acf70-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="acf70-144">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="acf70-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




