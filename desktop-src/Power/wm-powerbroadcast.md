---
description: Avertit les applications qu’un événement de gestion de l’alimentation s’est produit.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: Message WM_POWERBROADCAST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f1b273462d8de27c19d715836d168ab8bf8c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529097"
---
# <a name="wm_powerbroadcast-message"></a><span data-ttu-id="29d41-103">\_Message WM POWERBROADCAST</span><span class="sxs-lookup"><span data-stu-id="29d41-103">WM\_POWERBROADCAST message</span></span>

<span data-ttu-id="29d41-104">Avertit les applications qu’un événement de gestion de l’alimentation s’est produit.</span><span class="sxs-lookup"><span data-stu-id="29d41-104">Notifies applications that a power-management event has occurred.</span></span>

<span data-ttu-id="29d41-105">Une fenêtre reçoit ce message par le biais de sa fonction **WindowProc** .</span><span class="sxs-lookup"><span data-stu-id="29d41-105">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="29d41-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29d41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29d41-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="29d41-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="29d41-108">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="29d41-108">A handle to window.</span></span>

<span data-ttu-id="29d41-109"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="29d41-109"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="29d41-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="29d41-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="29d41-111">Signification</span><span class="sxs-lookup"><span data-stu-id="29d41-111">Meaning</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="29d41-112">\* \* \* \* <dt>WM \_ POWERBROADCAST \* \*</dt> \* \* <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="29d41-112"><dt>\*\*\*\*WM\_POWERBROADCAST\*\*\*\*</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="29d41-113">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="29d41-113">Message identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="29d41-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29d41-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29d41-115">Événement de gestion de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="29d41-115">The power-management event.</span></span> <span data-ttu-id="29d41-116">Ce paramètre peut être l’un des identificateurs d’événements suivants.</span><span class="sxs-lookup"><span data-stu-id="29d41-116">This parameter can be one of the following event identifiers.</span></span>



| <span data-ttu-id="29d41-117">Événement</span><span class="sxs-lookup"><span data-stu-id="29d41-117">Event</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="29d41-118">Signification</span><span class="sxs-lookup"><span data-stu-id="29d41-118">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="29d41-119"><dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="29d41-119"><dt>**[PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="29d41-120">L’état de l’alimentation a changé.</span><span class="sxs-lookup"><span data-stu-id="29d41-120">Power status has changed.</span></span><br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="29d41-121"><dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="29d41-121"><dt>**[PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span></span> </dl>        | <span data-ttu-id="29d41-122">L’opération reprend automatiquement à partir d’un état de faible consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="29d41-122">Operation is resuming automatically from a low-power state.</span></span> <span data-ttu-id="29d41-123">Ce message est envoyé à chaque reprise du système.</span><span class="sxs-lookup"><span data-stu-id="29d41-123">This message is sent every time the system resumes.</span></span><br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="29d41-124"><dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="29d41-124"><dt>**[PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span></span> </dl>                  | <span data-ttu-id="29d41-125">L’opération reprend à partir d’un état de faible consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="29d41-125">Operation is resuming from a low-power state.</span></span> <span data-ttu-id="29d41-126">Ce message est envoyé après [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) si la reprise est déclenchée par une entrée utilisateur, par exemple en appuyant sur une touche.</span><span class="sxs-lookup"><span data-stu-id="29d41-126">This message is sent after [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) if the resume is triggered by user input, such as pressing a key.</span></span><br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="29d41-127"><dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="29d41-127"><dt>**[PBT\_APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                          | <span data-ttu-id="29d41-128">Le système interrompt l’opération.</span><span class="sxs-lookup"><span data-stu-id="29d41-128">System is suspending operation.</span></span><br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="29d41-129"><dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="29d41-129"><dt>**[PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span></span> </dl>   | <span data-ttu-id="29d41-130">Un événement de modification du paramètre d’alimentation a été reçu.</span><span class="sxs-lookup"><span data-stu-id="29d41-130">A power setting change event has been received.</span></span> <br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="29d41-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29d41-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29d41-132">Données spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="29d41-132">The event-specific data.</span></span> <span data-ttu-id="29d41-133">Pour la plupart des événements, ce paramètre est réservé et n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="29d41-133">For most events, this parameter is reserved and not used.</span></span>

<span data-ttu-id="29d41-134">Si le paramètre *wParam* est [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md), le paramètre *lParam* est un pointeur vers une structure de [**\_ paramètre POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="29d41-134">If the *wParam* parameter is [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md), the *lParam* parameter is a pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29d41-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29d41-135">Return value</span></span>

<span data-ttu-id="29d41-136">Une application doit retourner la **valeur true** si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="29d41-136">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="29d41-137">Notes</span><span class="sxs-lookup"><span data-stu-id="29d41-137">Remarks</span></span>

<span data-ttu-id="29d41-138">Le système envoie toujours un message [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) à chaque reprise du système.</span><span class="sxs-lookup"><span data-stu-id="29d41-138">The system always sends a [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) message whenever the system resumes.</span></span> <span data-ttu-id="29d41-139">Si le système reprend en réponse à une entrée utilisateur, par exemple en appuyant sur une touche, le système envoie également un message **PBT \_ APMRESUMESUSPEND** après l’envoi de \_ APMRESUMEAUTOMATIC PBT.</span><span class="sxs-lookup"><span data-stu-id="29d41-139">If the system resumes in response to user input such as pressing a key, the system also sends a **PBT\_APMRESUMESUSPEND** message after sending PBT\_APMRESUMEAUTOMATIC.</span></span>

<span data-ttu-id="29d41-140">**WM \_** Les messages POWERBROADCAST ne font pas la distinction entre les différents États de faible consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="29d41-140">**WM\_POWERBROADCAST** messages do not distinguish between different low-power states.</span></span> <span data-ttu-id="29d41-141">Une application peut déterminer uniquement que le système entre dans un état de faible consommation d’énergie. il ne peut pas déterminer l’état d’alimentation spécifique.</span><span class="sxs-lookup"><span data-stu-id="29d41-141">An application can determine only that the system is entering or has resumed from a low-power state; it cannot determine the specific power state.</span></span> <span data-ttu-id="29d41-142">Le système enregistre des détails sur les transitions d’état d’alimentation dans le journal des événements système de Windows.</span><span class="sxs-lookup"><span data-stu-id="29d41-142">The system records details about power state transitions in the Windows System event log.</span></span>

<span data-ttu-id="29d41-143">Pour empêcher le système de passer à un état de faible consommation dans Windows Vista, une application doit appeler [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) pour informer le système qu’elle est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="29d41-143">To prevent the system from transitioning to a low-power state in Windows Vista, an application must call [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) to inform the system that it is in use.</span></span>

<span data-ttu-id="29d41-144">Les messages suivants ne sont pas pris en charge sur les systèmes d’exploitation spécifiés dans la section Configuration requise :</span><span class="sxs-lookup"><span data-stu-id="29d41-144">The following messages are not supported on any of the operating systems specified in the Requirements section:</span></span>

- <span data-ttu-id="29d41-145">PBT_APMQUERYSTANDBY</span><span class="sxs-lookup"><span data-stu-id="29d41-145">PBT_APMQUERYSTANDBY</span></span>  
- <span data-ttu-id="29d41-146">PBT_APMQUERYSTANDBYFAILED</span><span class="sxs-lookup"><span data-stu-id="29d41-146">PBT_APMQUERYSTANDBYFAILED</span></span>  
- <span data-ttu-id="29d41-147">PBT_APMSTANDBY</span><span class="sxs-lookup"><span data-stu-id="29d41-147">PBT_APMSTANDBY</span></span>  
- <span data-ttu-id="29d41-148">PBT_APMRESUMESTANDBY</span><span class="sxs-lookup"><span data-stu-id="29d41-148">PBT_APMRESUMESTANDBY</span></span>  

## <a name="requirements"></a><span data-ttu-id="29d41-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29d41-149">Requirements</span></span>



| <span data-ttu-id="29d41-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29d41-150">Requirement</span></span> | <span data-ttu-id="29d41-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="29d41-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29d41-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29d41-152">Minimum supported client</span></span><br/> | <span data-ttu-id="29d41-153">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29d41-153">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="29d41-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29d41-154">Minimum supported server</span></span><br/> | <span data-ttu-id="29d41-155">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29d41-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="29d41-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="29d41-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="29d41-157"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29d41-157"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29d41-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29d41-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d41-159">\_Messages WM POWERBROADCAST</span><span class="sxs-lookup"><span data-stu-id="29d41-159">WM\_POWERBROADCAST Messages</span></span>](wm-powerbroadcast-messages.md)
</dt> <dt>

[<span data-ttu-id="29d41-160">Messages de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="29d41-160">Power Management Messages</span></span>](power-management-messages.md)
</dt> </dl>

 

 




