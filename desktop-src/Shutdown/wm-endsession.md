---
description: Le \_ message WM ENDSESSION est envoyé à une application une fois que le système a traité les résultats du \_ message WM QUERYENDSESSION. Le \_ message WM ENDSESSION informe l’application que la session se termine.
ms.assetid: 9bf04f24-da1e-4680-a47b-28e9c500635e
title: Message WM_ENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa62f356d881182dd6e6fd9e0558332bcc1b3fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533773"
---
# <a name="wm_endsession-message"></a><span data-ttu-id="8f64e-104">\_Message WM ENDSESSION</span><span class="sxs-lookup"><span data-stu-id="8f64e-104">WM\_ENDSESSION message</span></span>

<span data-ttu-id="8f64e-105">Le message **WM \_ ENDSESSION** est envoyé à une application une fois que le système a traité les résultats du message [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) .</span><span class="sxs-lookup"><span data-stu-id="8f64e-105">The **WM\_ENDSESSION** message is sent to an application after the system processes the results of the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message.</span></span> <span data-ttu-id="8f64e-106">Le message **WM \_ ENDSESSION** informe l’application que la session se termine.</span><span class="sxs-lookup"><span data-stu-id="8f64e-106">The **WM\_ENDSESSION** message informs the application whether the session is ending.</span></span>

<span data-ttu-id="8f64e-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8f64e-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="8f64e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f64e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f64e-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8f64e-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8f64e-110">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8f64e-110">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="8f64e-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="8f64e-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="8f64e-112">Identificateur **WM \_ ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="8f64e-112">The **WM\_ENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8f64e-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f64e-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f64e-114">Si la session est terminée, ce paramètre a la **valeur true**. la session peut se terminer à tout moment une fois que toutes les applications ont renvoyé le traitement de ce message.</span><span class="sxs-lookup"><span data-stu-id="8f64e-114">If the session is being ended, this parameter is **TRUE**; the session can end any time after all applications have returned from processing this message.</span></span> <span data-ttu-id="8f64e-115">Sinon, la **valeur est false**.</span><span class="sxs-lookup"><span data-stu-id="8f64e-115">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8f64e-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f64e-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f64e-117">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8f64e-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="8f64e-118">Si ce paramètre a la valeur 0, le système est en cours d’arrêt ou de redémarrage (il n’est pas possible de déterminer l’événement qui se produit).</span><span class="sxs-lookup"><span data-stu-id="8f64e-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="8f64e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f64e-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="8f64e-120">Signification</span><span class="sxs-lookup"><span data-stu-id="8f64e-120">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="8f64e-121"><dt>**ENDSESSION \_ CLOSEAPP**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="8f64e-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x1</dt></span></span> </dl>        | <span data-ttu-id="8f64e-122">Si *wParam* a la **valeur true**, l’application doit être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="8f64e-122">If *wParam* is **TRUE**, the application must shut down.</span></span> <span data-ttu-id="8f64e-123">Toutes les données doivent être enregistrées automatiquement sans inviter l’utilisateur (pour plus d’informations, consultez la section Notes).</span><span class="sxs-lookup"><span data-stu-id="8f64e-123">Any data should be saved automatically without prompting the user (for more information, see Remarks).</span></span> <span data-ttu-id="8f64e-124">Le gestionnaire de redémarrage envoie ce message lorsque l’application utilise un fichier qui doit être remplacé, lorsqu’il doit le faire, ou lorsque des ressources système sont épuisées.</span><span class="sxs-lookup"><span data-stu-id="8f64e-124">The Restart Manager sends this message when the application is using a file that needs to be replaced, when it must service the system, or when system resources are exhausted.</span></span> <span data-ttu-id="8f64e-125">L’application sera redémarrée si elle est inscrite pour le redémarrage à l’aide de la fonction [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) .</span><span class="sxs-lookup"><span data-stu-id="8f64e-125">The application will be restarted if it has registered for restart using the [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) function.</span></span> <span data-ttu-id="8f64e-126">Pour plus d’informations, consultez [instructions pour les applications](../rstmgr/guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="8f64e-126">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span> <br/> <span data-ttu-id="8f64e-127">Si *wParam* a la **valeur false**, l’application ne doit pas s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="8f64e-127">If *wParam* is **FALSE**, the application should not shut down.</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="8f64e-128"><dt>**ENDSESSION \_**</dt> <dt>0x40000000</dt> critiques</span><span class="sxs-lookup"><span data-stu-id="8f64e-128"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="8f64e-129">L’application est obligée de s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="8f64e-129">The application is forced to shut down.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="8f64e-130"><dt>**ENDSESSION \_ Fermeture de session**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="8f64e-130"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="8f64e-131">L’utilisateur se déconnecte.</span><span class="sxs-lookup"><span data-stu-id="8f64e-131">The user is logging off.</span></span> <span data-ttu-id="8f64e-132">Pour plus d’informations, consultez [déconnexion](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="8f64e-132">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="8f64e-133">Notez que ce paramètre est un masque de bits.</span><span class="sxs-lookup"><span data-stu-id="8f64e-133">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="8f64e-134">Pour tester cette valeur, utilisez une opération au niveau du bit. ne Testez pas l’égalité.</span><span class="sxs-lookup"><span data-stu-id="8f64e-134">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f64e-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f64e-135">Return value</span></span>

<span data-ttu-id="8f64e-136">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="8f64e-136">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f64e-137">Notes</span><span class="sxs-lookup"><span data-stu-id="8f64e-137">Remarks</span></span>

<span data-ttu-id="8f64e-138">Les applications qui contiennent des données non enregistrées peuvent enregistrer les données dans un emplacement temporaire et les restaurer lors du prochain démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="8f64e-138">Applications that have unsaved data could save the data to a temporary location and restore it the next time the application starts.</span></span> <span data-ttu-id="8f64e-139">Il est recommandé que les applications enregistrent fréquemment leurs données et leur état ; par exemple, enregistrez automatiquement les données entre les opérations d’enregistrement initiées par l’utilisateur pour réduire la quantité de données à enregistrer lors de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="8f64e-139">It is recommended that applications save their data and state frequently; for example, automatically save data between save operations initiated by the user to reduce the amount of data to be saved at shutdown.</span></span>

<span data-ttu-id="8f64e-140">L’application n’a pas besoin d’appeler la fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) ou [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) lorsque la session se termine.</span><span class="sxs-lookup"><span data-stu-id="8f64e-140">The application need not call the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) or [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function when the session is ending.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f64e-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f64e-141">Requirements</span></span>



| <span data-ttu-id="8f64e-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f64e-142">Requirement</span></span> | <span data-ttu-id="8f64e-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f64e-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f64e-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f64e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="8f64e-145">Applications de bureau Windows XP- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="8f64e-145">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="8f64e-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f64e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="8f64e-147">Applications de bureau Windows Server 2003 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="8f64e-147">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="8f64e-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f64e-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f64e-149"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f64e-149"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f64e-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f64e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f64e-151">Fermeture de session</span><span class="sxs-lookup"><span data-stu-id="8f64e-151">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="8f64e-152">Arrêt en cours</span><span class="sxs-lookup"><span data-stu-id="8f64e-152">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="8f64e-153">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="8f64e-153">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="8f64e-154">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="8f64e-154">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="8f64e-155">**SetProcessShutdownParameters**</span><span class="sxs-lookup"><span data-stu-id="8f64e-155">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="8f64e-156">**\_QUERYENDSESSION WM**</span><span class="sxs-lookup"><span data-stu-id="8f64e-156">**WM\_QUERYENDSESSION**</span></span>](wm-queryendsession.md)
</dt> </dl>

 

 
