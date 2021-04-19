---
description: Notifie les applications que l’autorisation de suspendre l’ordinateur a été refusée.
ms.assetid: 0f68628f-9d38-45ca-9487-95bf62075e00
title: Événement PBT_APMQUERYSUSPENDFAILED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1544cd5ed94ae0228c739e2ddb576b0bd77146eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518475"
---
# <a name="pbt_apmquerysuspendfailed-event"></a><span data-ttu-id="e13c7-103">\_Événement PBT APMQUERYSUSPENDFAILED</span><span class="sxs-lookup"><span data-stu-id="e13c7-103">PBT\_APMQUERYSUSPENDFAILED event</span></span>

<span data-ttu-id="e13c7-104">\[PBT \_ APMQUERYSUSPENDFAILED peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e13c7-104">\[PBT\_APMQUERYSUSPENDFAILED is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e13c7-105">La prise en charge de cet événement a été supprimée dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e13c7-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="e13c7-106">Utilisez [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="e13c7-106">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="e13c7-107">Notifie les applications que l’autorisation de suspendre l’ordinateur a été refusée.</span><span class="sxs-lookup"><span data-stu-id="e13c7-107">Notifies applications that permission to suspend the computer was denied.</span></span> <span data-ttu-id="e13c7-108">Cet événement est diffusé si une application ou un pilote retournait une **requête de diffusion \_ \_ Deny** à un événement [ \_ APMQUERYSUSPEND PBT](pbt-apmquerysuspend.md) précédent.</span><span class="sxs-lookup"><span data-stu-id="e13c7-108">This event is broadcast if any application or driver returned **BROADCAST\_QUERY\_DENY** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="e13c7-109">Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="e13c7-109">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="e13c7-110">Les paramètres *wParam* et *lParam* sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="e13c7-110">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPENDFAILED
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="e13c7-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e13c7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e13c7-112">*HWND*</span><span class="sxs-lookup"><span data-stu-id="e13c7-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e13c7-113">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e13c7-113">A handle to window.</span></span>

<span data-ttu-id="e13c7-114"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="e13c7-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="e13c7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e13c7-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="e13c7-116">Signification</span><span class="sxs-lookup"><span data-stu-id="e13c7-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="e13c7-117"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="e13c7-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="e13c7-118">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="e13c7-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="e13c7-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="e13c7-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="e13c7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e13c7-120">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="e13c7-121">Signification</span><span class="sxs-lookup"><span data-stu-id="e13c7-121">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPENDFAILED"></span><span id="pbt_apmquerysuspendfailed"></span><dl> <span data-ttu-id="e13c7-122"><dt>**PBT \_ APMQUERYSUSPENDFAILED**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="e13c7-122"><dt>**PBT\_APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="e13c7-123">Identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="e13c7-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e13c7-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e13c7-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e13c7-125">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e13c7-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e13c7-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e13c7-126">Return value</span></span>

<span data-ttu-id="e13c7-127">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e13c7-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e13c7-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e13c7-128">Remarks</span></span>

<span data-ttu-id="e13c7-129">Les applications répondent généralement à cet événement en reprenant le fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="e13c7-129">Applications typically respond to this event by resuming normal operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e13c7-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e13c7-130">Requirements</span></span>



| <span data-ttu-id="e13c7-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e13c7-131">Requirement</span></span> | <span data-ttu-id="e13c7-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e13c7-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e13c7-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e13c7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e13c7-134">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e13c7-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e13c7-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e13c7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e13c7-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e13c7-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e13c7-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e13c7-137">End of client support</span></span><br/>    | <span data-ttu-id="e13c7-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e13c7-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="e13c7-139">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e13c7-139">End of server support</span></span><br/>    | <span data-ttu-id="e13c7-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e13c7-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="e13c7-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="e13c7-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e13c7-142"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e13c7-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e13c7-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e13c7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13c7-144">Gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="e13c7-144">Power Management</span></span>](power-management-portal.md)
</dt> <dt>

[<span data-ttu-id="e13c7-145">Événements de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="e13c7-145">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="e13c7-146">PBT \_ APMQUERYSUSPEND</span><span class="sxs-lookup"><span data-stu-id="e13c7-146">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="e13c7-147">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="e13c7-147">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




