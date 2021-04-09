---
description: Demande l’autorisation de suspendre l’ordinateur. Une application qui accorde cette autorisation doit effectuer des opérations de préparation à la mise en veille avant de retourner sa réponse.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: Événement PBT_APMQUERYSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865073"
---
# <a name="pbt_apmquerysuspend-event"></a><span data-ttu-id="8f379-104">\_Événement PBT APMQUERYSUSPEND</span><span class="sxs-lookup"><span data-stu-id="8f379-104">PBT\_APMQUERYSUSPEND event</span></span>

<span data-ttu-id="8f379-105">\[PBT \_ APMQUERYSUSPEND peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="8f379-105">\[PBT\_APMQUERYSUSPEND is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8f379-106">La prise en charge de cet événement a été supprimée dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8f379-106">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="8f379-107">Utilisez [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) à la place.\]</span><span class="sxs-lookup"><span data-stu-id="8f379-107">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="8f379-108">Demande l’autorisation de suspendre l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8f379-108">Requests permission to suspend the computer.</span></span> <span data-ttu-id="8f379-109">Une application qui accorde cette autorisation doit effectuer des opérations de préparation à la mise en veille avant de retourner sa réponse.</span><span class="sxs-lookup"><span data-stu-id="8f379-109">An application that grants permission should carry out preparations for the suspension before returning.</span></span>

<span data-ttu-id="8f379-110">Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="8f379-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="8f379-111">Les paramètres *wParam* et *lParam* sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="8f379-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
```



## <a name="parameters"></a><span data-ttu-id="8f379-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f379-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f379-113">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8f379-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8f379-114">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8f379-114">A handle to window.</span></span>

<span data-ttu-id="8f379-115"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="8f379-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="8f379-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f379-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="8f379-117">Signification</span><span class="sxs-lookup"><span data-stu-id="8f379-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="8f379-118"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="8f379-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="8f379-119">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="8f379-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="8f379-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="8f379-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="8f379-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f379-121">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="8f379-122">Signification</span><span class="sxs-lookup"><span data-stu-id="8f379-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <span data-ttu-id="8f379-123"><dt>**PBT \_ APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8f379-123"><dt>**PBT\_APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8f379-124">Identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="8f379-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f379-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f379-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f379-126">Indicateurs d’action.</span><span class="sxs-lookup"><span data-stu-id="8f379-126">The action flags.</span></span> <span data-ttu-id="8f379-127">Si le bit 0 est 1, l’application peut inviter l’utilisateur à fournir des instructions sur la façon de se préparer à la suspension. dans le cas contraire, l’application doit se préparer sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f379-127">If bit 0 is 1, the application can prompt the user for directions on how to prepare for the suspension; otherwise, the application must prepare without user interaction.</span></span> <span data-ttu-id="8f379-128">Toutes les autres valeurs de bit sont réservées.</span><span class="sxs-lookup"><span data-stu-id="8f379-128">All other bit values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f379-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f379-129">Return value</span></span>

<span data-ttu-id="8f379-130">Retourne la **valeur true** pour autoriser l’interruption de la demande.</span><span class="sxs-lookup"><span data-stu-id="8f379-130">Return **TRUE** to grant the request to suspend.</span></span> <span data-ttu-id="8f379-131">Pour refuser la demande, retournez **la \_ requête \_ de diffusion Deny**.</span><span class="sxs-lookup"><span data-stu-id="8f379-131">To deny the request, return **BROADCAST\_QUERY\_DENY**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f379-132">Notes</span><span class="sxs-lookup"><span data-stu-id="8f379-132">Remarks</span></span>

<span data-ttu-id="8f379-133">Une application doit traiter cet événement aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="8f379-133">An application should process this event as quickly as possible.</span></span> <span data-ttu-id="8f379-134">L’application peut demander à l’utilisateur des instructions sur la façon de se préparer à la suspension uniquement si le bit 0 dans le paramètre *Flags* est défini.</span><span class="sxs-lookup"><span data-stu-id="8f379-134">The application can prompt the user for directions on how to prepare for suspension only if bit 0 in the *Flags* parameter is set.</span></span> <span data-ttu-id="8f379-135">Toutefois, si ce message est émis parce que l’utilisateur ferme le couvercle de l’ordinateur portable, il ne sera pas possible d’inviter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f379-135">However, if this message is issued because the user is closing the laptop lid, it will not be possible to prompt the user.</span></span> <span data-ttu-id="8f379-136">Les applications doivent respecter un certain comportement lorsqu’elles ferment le couvercle de l’ordinateur portable ou appuient sur le bouton d’alimentation et permettent à la transition de s’effectuer correctement.</span><span class="sxs-lookup"><span data-stu-id="8f379-136">Applications should respect that the user expects a certain behavior when they close the laptop lid or press the power button and allow the transition to succeed.</span></span>

<span data-ttu-id="8f379-137">Le système laisse environ 20 secondes à une application de supprimer le message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) qui envoie l’événement PBT \_ APMQUERYSUSPEND à partir de la file d’attente des messages de l’application.</span><span class="sxs-lookup"><span data-stu-id="8f379-137">The system allows approximately 20 seconds for an application to remove the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message that is sending the PBT\_APMQUERYSUSPEND event from the application's message queue.</span></span> <span data-ttu-id="8f379-138">Si une application ne supprime pas le message de sa file d’attente en moins de 20 secondes, le système suppose que l’application est dans un État non réactif et que l’application accepte la demande de mise en veille.</span><span class="sxs-lookup"><span data-stu-id="8f379-138">If an application does not remove the message from its queue in less than 20 seconds, the system will assume that the application is in a non-responsive state, and that the application agrees to the sleep request.</span></span> <span data-ttu-id="8f379-139">Les opérations des applications qui ne traitent pas leurs files d’attente de messages peuvent être interrompues.</span><span class="sxs-lookup"><span data-stu-id="8f379-139">Applications that do not process their message queues may have their operations interrupted.</span></span> <span data-ttu-id="8f379-140">Une fois que le message a été supprimé de la file d’attente de messages, une application peut prendre autant de temps que nécessaire pour effectuer les opérations requises avant d’entrer dans l’état de veille.</span><span class="sxs-lookup"><span data-stu-id="8f379-140">After it removes the message from the message queue, an application can take as much time as needed to perform any required operations before entering the sleep state.</span></span> <span data-ttu-id="8f379-141">Toutes les opérations qui peuvent durer plus de 20 secondes doivent être effectuées pour l’instant, car le système n’autorise que 20 secondes pour que les opérations se terminent au cours du traitement [PBT \_ APMSUSPEND](pbt-apmsuspend.md) .</span><span class="sxs-lookup"><span data-stu-id="8f379-141">Any operations that could take longer then 20 seconds should be performed at this time, since the system allows only 20 seconds for operations to complete during [PBT\_APMSUSPEND](pbt-apmsuspend.md) processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f379-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f379-142">Requirements</span></span>



| <span data-ttu-id="8f379-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f379-143">Requirement</span></span> | <span data-ttu-id="8f379-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f379-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f379-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f379-145">Minimum supported client</span></span><br/> | <span data-ttu-id="8f379-146">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f379-146">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8f379-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f379-147">Minimum supported server</span></span><br/> | <span data-ttu-id="8f379-148">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f379-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8f379-149">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8f379-149">End of client support</span></span><br/>    | <span data-ttu-id="8f379-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f379-150">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="8f379-151">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="8f379-151">End of server support</span></span><br/>    | <span data-ttu-id="8f379-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f379-152">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="8f379-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f379-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f379-154"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f379-154"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f379-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f379-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f379-156">Événements de mise en éveil du système</span><span class="sxs-lookup"><span data-stu-id="8f379-156">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="8f379-157">Événements de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="8f379-157">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="8f379-158">PBT \_ APMSUSPEND</span><span class="sxs-lookup"><span data-stu-id="8f379-158">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="8f379-159">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="8f379-159">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




