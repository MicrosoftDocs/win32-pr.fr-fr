---
description: Avertit les applications que le système, généralement un ordinateur personnel alimenté par batterie, est sur le même d’entrer en mode suspendu.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: Message WM_POWER (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53fd165ee1cefe8970f85daea04b931a673b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533890"
---
# <a name="wm_power-message"></a><span data-ttu-id="8c5a4-103">\_Message d’alimentation WM</span><span class="sxs-lookup"><span data-stu-id="8c5a4-103">WM\_POWER message</span></span>

<span data-ttu-id="8c5a4-104">Avertit les applications que le système, généralement un ordinateur personnel alimenté par batterie, est sur le même d’entrer en mode suspendu.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-104">Notifies applications that the system, typically a battery-powered personal computer, is about to enter a suspended mode.</span></span>

> [!Note]  
> <span data-ttu-id="8c5a4-105">Le **message \_ d’alimentation WM** est obsolète.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-105">The **WM\_POWER** message is obsolete.</span></span> <span data-ttu-id="8c5a4-106">Elle est fournie uniquement pour la compatibilité avec les applications Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-106">It is provided only for compatibility with 16-bit Windows-based applications.</span></span> <span data-ttu-id="8c5a4-107">Les applications doivent utiliser le message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="8c5a4-107">Applications should use the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span>

 

<span data-ttu-id="8c5a4-108">Une fenêtre reçoit ce message par le biais de sa fonction **WindowProc** .</span><span class="sxs-lookup"><span data-stu-id="8c5a4-108">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a><span data-ttu-id="8c5a4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c5a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c5a4-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8c5a4-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8c5a4-111">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-111">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="8c5a4-112">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="8c5a4-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="8c5a4-113">Identificateur du message **\_ d’alimentation WM** .</span><span class="sxs-lookup"><span data-stu-id="8c5a4-113">The **WM\_POWER** message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8c5a4-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c5a4-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c5a4-115">Notification d’événement d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-115">The power-event notification.</span></span> <span data-ttu-id="8c5a4-116">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8c5a4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c5a4-117">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="8c5a4-118">Signification</span><span class="sxs-lookup"><span data-stu-id="8c5a4-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <span data-ttu-id="8c5a4-119"><dt>**\_CRITICALRESUME PWR**</dt></span><span class="sxs-lookup"><span data-stu-id="8c5a4-119"><dt>**PWR\_CRITICALRESUME**</dt></span></span> </dl> | <span data-ttu-id="8c5a4-120">Indique que le système reprend l’opération après avoir entré le mode suspendu sans avoir d’abord diffusé un message de notification **\_ SUSPENDREQUEST PWR** à l’application.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-120">Indicates that the system is resuming operation after entering suspended mode without first broadcasting a **PWR\_SUSPENDREQUEST** notification message to the application.</span></span> <span data-ttu-id="8c5a4-121">Une application doit effectuer les actions de récupération nécessaires.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-121">An application should perform any necessary recovery actions.</span></span><br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <span data-ttu-id="8c5a4-122"><dt>**\_SUSPENDREQUEST PWR**</dt></span><span class="sxs-lookup"><span data-stu-id="8c5a4-122"><dt>**PWR\_SUSPENDREQUEST**</dt></span></span> </dl> | <span data-ttu-id="8c5a4-123">Indique que le système est sur le paragraphe d’entrer en mode suspendu.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-123">Indicates that the system is about to enter suspended mode.</span></span><br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <span data-ttu-id="8c5a4-124"><dt>**\_SUSPENDRESUME PWR**</dt></span><span class="sxs-lookup"><span data-stu-id="8c5a4-124"><dt>**PWR\_SUSPENDRESUME**</dt></span></span> </dl>    | <span data-ttu-id="8c5a4-125">Indique que le système reprend l’opération après avoir entré le mode suspendu normalement, le système diffuse un message de notification **\_ SUSPENDREQUEST PWR** à l’application avant la suspension du système.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-125">Indicates that the system is resuming operation after having entered suspended mode normally that is, the system broadcast a **PWR\_SUSPENDREQUEST** notification message to the application before the system was suspended.</span></span> <span data-ttu-id="8c5a4-126">Une application doit effectuer les actions de récupération nécessaires.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-126">An application should perform any necessary recovery actions.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8c5a4-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c5a4-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c5a4-128">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-128">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c5a4-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c5a4-129">Return value</span></span>

<span data-ttu-id="8c5a4-130">La valeur retournée par une application dépend de la valeur du paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="8c5a4-130">The value an application returns depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="8c5a4-131">Si *wParam* est **un \_ SUSPENDREQUEST PWR**, la valeur de retour est la valeur **PWR \_ échoue** pour empêcher le système de passer à l’État Suspended ; sinon, il s’agit d’un **PWR \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-131">If *wParam* is **PWR\_SUSPENDREQUEST**, the return value is **PWR\_FAIL** to prevent the system from entering the suspended state; otherwise, it is **PWR\_OK**.</span></span> <span data-ttu-id="8c5a4-132">Si *wParam* est **PWR \_ SUSPENDRESUME** ou **PWR \_ CRITICALRESUME**, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-132">If *wParam* is **PWR\_SUSPENDRESUME** or **PWR\_CRITICALRESUME**, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c5a4-133">Notes</span><span class="sxs-lookup"><span data-stu-id="8c5a4-133">Remarks</span></span>

<span data-ttu-id="8c5a4-134">Ce message est diffusé uniquement à une application qui s’exécute sur un système qui est conforme à la spécification BIOS (Advanced Power Management System) de base de la gestion avancée de l’alimentation (APM).</span><span class="sxs-lookup"><span data-stu-id="8c5a4-134">This message is broadcast only to an application that is running on a system that conforms to the Advanced Power Management (APM) basic input/output system (BIOS) specification.</span></span> <span data-ttu-id="8c5a4-135">Le message est diffusé par le pilote de gestion de l’alimentation à chaque fenêtre retournée par la fonction **EnumWindows** .</span><span class="sxs-lookup"><span data-stu-id="8c5a4-135">The message is broadcast by the power-management driver to each window returned by the **EnumWindows** function.</span></span>

<span data-ttu-id="8c5a4-136">Le mode suspendu est l’État dans lequel la plus grande quantité d’économies d’énergie se produit, mais toutes les données et tous les paramètres opérationnels sont conservés.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-136">The suspended mode is the state in which the greatest amount of power savings occurs, but all operational data and parameters are preserved.</span></span> <span data-ttu-id="8c5a4-137">Le contenu de la mémoire vive (RAM) est conservé, mais de nombreux appareils sont susceptibles d’être désactivés.</span><span class="sxs-lookup"><span data-stu-id="8c5a4-137">Random-access memory (RAM) contents are preserved, but many devices are likely to be turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c5a4-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c5a4-138">Requirements</span></span>



| <span data-ttu-id="8c5a4-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c5a4-139">Requirement</span></span> | <span data-ttu-id="8c5a4-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c5a4-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c5a4-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c5a4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8c5a4-142">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c5a4-142">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8c5a4-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c5a4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8c5a4-144">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c5a4-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8c5a4-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c5a4-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c5a4-146"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c5a4-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c5a4-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c5a4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c5a4-148">**\_POWERBROADCAST WM**</span><span class="sxs-lookup"><span data-stu-id="8c5a4-148">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




