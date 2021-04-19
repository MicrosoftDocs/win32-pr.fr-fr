---
description: Le \_ message WM QUERYENDSESSION est envoyé lorsque l’utilisateur choisit de mettre fin à la session ou lorsqu’une application appelle l’une des fonctions d’arrêt du système.
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: Message WM_QUERYENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2e2f82388b229523f371c680d6ccc7c4b1e27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538174"
---
# <a name="wm_queryendsession-message"></a><span data-ttu-id="ab7dc-103">\_Message WM QUERYENDSESSION</span><span class="sxs-lookup"><span data-stu-id="ab7dc-103">WM\_QUERYENDSESSION message</span></span>

<span data-ttu-id="ab7dc-104">Le message **WM \_ QUERYENDSESSION** est envoyé lorsque l’utilisateur choisit de mettre fin à la session ou lorsqu’une application appelle l’une des fonctions d’arrêt du système.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-104">The **WM\_QUERYENDSESSION** message is sent when the user chooses to end the session or when an application calls one of the system shutdown functions.</span></span> <span data-ttu-id="ab7dc-105">Si une application retourne la valeur zéro, la session n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-105">If any application returns zero, the session is not ended.</span></span> <span data-ttu-id="ab7dc-106">Le système arrête d’envoyer des messages **WM \_ QUERYENDSESSION** dès qu’une application retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-106">The system stops sending **WM\_QUERYENDSESSION** messages as soon as one application returns zero.</span></span>

<span data-ttu-id="ab7dc-107">Après le traitement de ce message, le système envoie le message [**WM \_ ENDSESSION**](wm-endsession.md) avec le paramètre *wParam* défini sur les résultats du message **WM \_ QUERYENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="ab7dc-107">After processing this message, the system sends the [**WM\_ENDSESSION**](wm-endsession.md) message with the *wParam* parameter set to the results of the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="ab7dc-108">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ab7dc-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="ab7dc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab7dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab7dc-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="ab7dc-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ab7dc-111">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-111">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="ab7dc-112">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="ab7dc-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="ab7dc-113">Identificateur **WM \_ QUERYENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="ab7dc-113">The **WM\_QUERYENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ab7dc-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ab7dc-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab7dc-115">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-115">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="ab7dc-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab7dc-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab7dc-117">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="ab7dc-118">Si ce paramètre a la valeur 0, le système est en cours d’arrêt ou de redémarrage (il n’est pas possible de déterminer l’événement qui se produit).</span><span class="sxs-lookup"><span data-stu-id="ab7dc-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="ab7dc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab7dc-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="ab7dc-120">Signification</span><span class="sxs-lookup"><span data-stu-id="ab7dc-120">Meaning</span></span>                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="ab7dc-121"><dt>**ENDSESSION \_ CLOSEAPP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ab7dc-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="ab7dc-122">L’application utilise un fichier qui doit être remplacé, le système est en cours de maintenance ou les ressources système sont épuisées.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-122">The application is using a file that must be replaced, the system is being serviced, or system resources are exhausted.</span></span> <span data-ttu-id="ab7dc-123">Pour plus d’informations, consultez [instructions pour les applications](../rstmgr/guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="ab7dc-123">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="ab7dc-124"><dt>**ENDSESSION \_**</dt> <dt>0x40000000</dt> critiques</span><span class="sxs-lookup"><span data-stu-id="ab7dc-124"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="ab7dc-125">L’application est obligée de s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-125">The application is forced to shut down.</span></span><br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="ab7dc-126"><dt>**ENDSESSION \_ Fermeture de session**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="ab7dc-126"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="ab7dc-127">L’utilisateur se déconnecte.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-127">The user is logging off.</span></span> <span data-ttu-id="ab7dc-128">Pour plus d’informations, consultez [déconnexion](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="ab7dc-128">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                   |



 

<span data-ttu-id="ab7dc-129">Notez que ce paramètre est un masque de bits.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-129">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="ab7dc-130">Pour tester cette valeur, utilisez une opération au niveau du bit. ne Testez pas l’égalité.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-130">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab7dc-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab7dc-131">Return value</span></span>

<span data-ttu-id="ab7dc-132">Les applications doivent respecter les intentions de l’utilisateur et retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-132">Applications should respect the user's intentions and return **TRUE**.</span></span> <span data-ttu-id="ab7dc-133">Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne la **valeur true** pour ce message.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-133">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE** for this message.</span></span>

<span data-ttu-id="ab7dc-134">Si l’arrêt endommage le système ou le support en cours de gravure, l’application peut retourner la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-134">If shutting down would corrupt the system or media that is being burned, the application can return **FALSE**.</span></span> <span data-ttu-id="ab7dc-135">Toutefois, il est recommandé de respecter les actions de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-135">However, it is good practice to respect the user's actions.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab7dc-136">Notes</span><span class="sxs-lookup"><span data-stu-id="ab7dc-136">Remarks</span></span>

<span data-ttu-id="ab7dc-137">Quand une application retourne la **valeur true** pour ce message, elle reçoit le message [**WM \_ ENDSESSION**](wm-endsession.md) , quelle que soit la manière dont les autres applications répondent au message **WM \_ QUERYENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="ab7dc-137">When an application returns **TRUE** for this message, it receives the [**WM\_ENDSESSION**](wm-endsession.md) message, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span> <span data-ttu-id="ab7dc-138">Chaque application doit retourner la **valeur true** ou **false** immédiatement lors de la réception de ce message, et différer les opérations de nettoyage jusqu’à ce qu’elle reçoive le message **WM \_ ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="ab7dc-138">Each application should return **TRUE** or **FALSE** immediately upon receiving this message, and defer any cleanup operations until it receives the **WM\_ENDSESSION** message.</span></span>

<span data-ttu-id="ab7dc-139">Les applications peuvent afficher une interface utilisateur invitant l’utilisateur à fournir des informations lors de l’arrêt, mais cela n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-139">Applications can display a user interface prompting the user for information at shutdown, however it is not recommended.</span></span> <span data-ttu-id="ab7dc-140">Au bout de cinq secondes, le système affiche des informations sur les applications qui empêchent l’arrêt et permet à l’utilisateur de les arrêter.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-140">After five seconds, the system displays information about the applications that are preventing shutdown and allows the user to terminate them.</span></span> <span data-ttu-id="ab7dc-141">Par exemple, Windows XP affiche une boîte de dialogue, tandis que Windows Vista affiche un plein écran avec des informations supplémentaires sur les applications bloquant l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-141">For example, Windows XP displays a dialog box, while Windows Vista displays a full screen with additional information about the applications blocking shutdown.</span></span> <span data-ttu-id="ab7dc-142">Si votre application doit bloquer ou différer l’arrêt du système, utilisez la fonction [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .</span><span class="sxs-lookup"><span data-stu-id="ab7dc-142">If your application must block or postpone system shutdown, use the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span> <span data-ttu-id="ab7dc-143">Pour plus d’informations, consultez [modifications de l’arrêt de Windows Vista](shutdown-changes-for-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="ab7dc-143">For more information, see [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).</span></span>

<span data-ttu-id="ab7dc-144">Les applications console peuvent utiliser la fonction [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) pour recevoir des notifications d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-144">Console applications can use the [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) function to receive shutdown notification.</span></span>

<span data-ttu-id="ab7dc-145">Les applications de service peuvent utiliser la fonction [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) pour recevoir des notifications d’arrêt dans une routine de gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="ab7dc-145">Service applications can use the [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function to receive shutdown notifications in a handler routine.</span></span>

## <a name="examples"></a><span data-ttu-id="ab7dc-146">Exemples</span><span class="sxs-lookup"><span data-stu-id="ab7dc-146">Examples</span></span>

<span data-ttu-id="ab7dc-147">Pour obtenir un exemple, consultez [déconnexion](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="ab7dc-147">For an example, see [Logging Off](logging-off.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab7dc-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab7dc-148">Requirements</span></span>



| <span data-ttu-id="ab7dc-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab7dc-149">Requirement</span></span> | <span data-ttu-id="ab7dc-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab7dc-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab7dc-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab7dc-151">Minimum supported client</span></span><br/> | <span data-ttu-id="ab7dc-152">Applications de bureau Windows XP- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="ab7dc-152">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="ab7dc-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab7dc-153">Minimum supported server</span></span><br/> | <span data-ttu-id="ab7dc-154">Applications de bureau Windows Server 2003 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="ab7dc-154">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="ab7dc-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab7dc-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab7dc-156"><dt>WinUser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab7dc-156"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab7dc-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab7dc-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab7dc-158">Fermeture de session</span><span class="sxs-lookup"><span data-stu-id="ab7dc-158">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="ab7dc-159">Arrêt en cours</span><span class="sxs-lookup"><span data-stu-id="ab7dc-159">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="ab7dc-160">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="ab7dc-160">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="ab7dc-161">**ExitWindows**</span><span class="sxs-lookup"><span data-stu-id="ab7dc-161">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[<span data-ttu-id="ab7dc-162">**SetProcessShutdownParameters**</span><span class="sxs-lookup"><span data-stu-id="ab7dc-162">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="ab7dc-163">**\_ENDSESSION WM**</span><span class="sxs-lookup"><span data-stu-id="ab7dc-163">**WM\_ENDSESSION**</span></span>](wm-endsession.md)
</dt> </dl>

 

 
