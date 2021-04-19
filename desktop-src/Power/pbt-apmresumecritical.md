---
description: Avertit les applications que le système a repris l’opération.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: Événement PBT_APMRESUMECRITICAL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4a76e163f2e61e723f4df6572254e8ef89b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544855"
---
# <a name="pbt_apmresumecritical-event"></a><span data-ttu-id="bf213-103">\_Événement PBT APMRESUMECRITICAL</span><span class="sxs-lookup"><span data-stu-id="bf213-103">PBT\_APMRESUMECRITICAL event</span></span>

<span data-ttu-id="bf213-104">\[PBT \_ APMRESUMECRITICAL peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="bf213-104">\[PBT\_APMRESUMECRITICAL is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bf213-105">La prise en charge de cet événement a été supprimée dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bf213-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="bf213-106">Utilisez [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="bf213-106">Use [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) instead.\]</span></span>

<span data-ttu-id="bf213-107">Avertit les applications que le système a repris l’opération.</span><span class="sxs-lookup"><span data-stu-id="bf213-107">Notifies applications that the system has resumed operation.</span></span> <span data-ttu-id="bf213-108">Cet événement peut indiquer que certaines ou toutes les applications n’ont pas reçu d’événement [PBT \_ APMSUSPEND](pbt-apmsuspend.md) .</span><span class="sxs-lookup"><span data-stu-id="bf213-108">This event can indicate that some or all applications did not receive a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event.</span></span> <span data-ttu-id="bf213-109">Par exemple, cet événement peut être diffusé après une suspension critique causée par une batterie défectueuse.</span><span class="sxs-lookup"><span data-stu-id="bf213-109">For example, this event can be broadcast after a critical suspension caused by a failing battery.</span></span>

<span data-ttu-id="bf213-110">Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="bf213-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="bf213-111">Les paramètres *wParam* et *lParam* sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="bf213-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="bf213-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf213-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf213-113">*HWND*</span><span class="sxs-lookup"><span data-stu-id="bf213-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bf213-114">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bf213-114">A handle to window.</span></span>

<span data-ttu-id="bf213-115"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="bf213-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="bf213-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf213-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="bf213-117">Signification</span><span class="sxs-lookup"><span data-stu-id="bf213-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="bf213-118"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="bf213-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="bf213-119">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="bf213-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="bf213-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="bf213-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="bf213-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf213-121">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="bf213-122">Signification</span><span class="sxs-lookup"><span data-stu-id="bf213-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <span data-ttu-id="bf213-123"><dt>**PBT \_ APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="bf213-123"><dt>**PBT\_APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="bf213-124">Identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="bf213-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bf213-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf213-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf213-126">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="bf213-126">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf213-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf213-127">Return value</span></span>

<span data-ttu-id="bf213-128">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="bf213-128">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf213-129">Notes</span><span class="sxs-lookup"><span data-stu-id="bf213-129">Remarks</span></span>

<span data-ttu-id="bf213-130">Étant donné qu’une suspension critique se produit sans notification préalable, les ressources et les données qui étaient disponibles peuvent ne pas être présentes lorsque l’application reçoit cet événement.</span><span class="sxs-lookup"><span data-stu-id="bf213-130">Because a critical suspension occurs without prior notification, resources and data previously available may not be present when the application receives this event.</span></span> <span data-ttu-id="bf213-131">L’application doit tenter de restaurer son état au meilleur de sa capacité.</span><span class="sxs-lookup"><span data-stu-id="bf213-131">The application should attempt to restore its state to the best of its ability.</span></span> <span data-ttu-id="bf213-132">Lorsqu’il s’agit d’une suspension critique, le système conserve l’état de la DRAM et des disques durs locaux, mais il peut ne pas conserver les connexions réseau.</span><span class="sxs-lookup"><span data-stu-id="bf213-132">While in a critical suspension, the system maintains the state of the DRAM and local hard disks, but may not maintain net connections.</span></span> <span data-ttu-id="bf213-133">Une application peut être amenée à agir en ce qui concerne les fichiers qui étaient ouverts sur le réseau avant la suspension critique.</span><span class="sxs-lookup"><span data-stu-id="bf213-133">An application may need to take action with respect to files that were open on the network before critical suspension.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf213-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf213-134">Requirements</span></span>



| <span data-ttu-id="bf213-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf213-135">Requirement</span></span> | <span data-ttu-id="bf213-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf213-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf213-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf213-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bf213-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf213-138">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bf213-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf213-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bf213-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf213-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bf213-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="bf213-141">End of client support</span></span><br/>    | <span data-ttu-id="bf213-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf213-142">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="bf213-143">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="bf213-143">End of server support</span></span><br/>    | <span data-ttu-id="bf213-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf213-144">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="bf213-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf213-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf213-146"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf213-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf213-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf213-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf213-148">Événements de mise en éveil du système</span><span class="sxs-lookup"><span data-stu-id="bf213-148">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="bf213-149">Événements de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="bf213-149">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="bf213-150">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="bf213-150">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




