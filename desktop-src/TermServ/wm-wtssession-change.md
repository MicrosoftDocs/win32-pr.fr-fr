---
title: Message WM_WTSSESSION_CHANGE (winuser. h)
description: Avertit les applications des modifications apportées à l’état de session.
ms.assetid: 758a130c-b75a-40fd-8530-3766aa86c5ba
ms.tgt_platform: multiple
keywords:
- Message de WM_WTSSESSION_CHANGE Services Bureau à distance
topic_type:
- apiref
api_name:
- WM_WTSSESSION_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f1dc421aa160824a194588711e84f961ea4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740172"
---
# <a name="wm_wtssession_change-message"></a><span data-ttu-id="1cb22-104">Message de modification de WM \_ WTSSESSION \_</span><span class="sxs-lookup"><span data-stu-id="1cb22-104">WM\_WTSSESSION\_CHANGE message</span></span>

<span data-ttu-id="1cb22-105">Avertit les applications des modifications apportées à l’état de session.</span><span class="sxs-lookup"><span data-stu-id="1cb22-105">Notifies applications of changes in session state.</span></span>

<span data-ttu-id="1cb22-106">La fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1cb22-106">The window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a><span data-ttu-id="1cb22-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cb22-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cb22-108">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cb22-108">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cb22-109">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1cb22-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="1cb22-110">*Message* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cb22-110">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cb22-111">Spécifie le message (**WM \_ WTSSESSION \_ change**).</span><span class="sxs-lookup"><span data-stu-id="1cb22-111">Specifies the message (**WM\_WTSSESSION\_CHANGE**).</span></span>

</dd> <dt>

<span data-ttu-id="1cb22-112">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cb22-112">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cb22-113">Code d’état décrivant la raison de l’envoi de la notification de changement d’état de session.</span><span class="sxs-lookup"><span data-stu-id="1cb22-113">Status code describing the reason the session state change notification was sent.</span></span> <span data-ttu-id="1cb22-114">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1cb22-114">This parameter can be one of the following values.</span></span>

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span data-ttu-id="1cb22-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ \_Connexion** à la console (0x1)</span><span class="sxs-lookup"><span data-stu-id="1cb22-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS\_CONSOLE\_CONNECT** (0x1)</span></span>


</dt> <dd>

<span data-ttu-id="1cb22-116">La session identifiée par *lParam* était connectée au terminal de la console ou à la session RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="1cb22-116">The session identified by *lParam* was connected to the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span data-ttu-id="1cb22-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ \_Déconnexion** de la console (0X2)</span><span class="sxs-lookup"><span data-stu-id="1cb22-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS\_CONSOLE\_DISCONNECT** (0x2)</span></span>


</dt> <dd>

<span data-ttu-id="1cb22-118">La session identifiée par *lParam* a été déconnectée du terminal de la console ou de la session RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="1cb22-118">The session identified by *lParam* was disconnected from the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span data-ttu-id="1cb22-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ \_Connexion à distance** (0x3)</span><span class="sxs-lookup"><span data-stu-id="1cb22-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS\_REMOTE\_CONNECT** (0x3)</span></span>


</dt> <dd>

<span data-ttu-id="1cb22-120">La session identifiée par *lParam* était connectée au terminal distant.</span><span class="sxs-lookup"><span data-stu-id="1cb22-120">The session identified by *lParam* was connected to the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span data-ttu-id="1cb22-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ \_Déconnexion à distance** (0x4)</span><span class="sxs-lookup"><span data-stu-id="1cb22-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS\_REMOTE\_DISCONNECT** (0x4)</span></span>


</dt> <dd>

<span data-ttu-id="1cb22-122">La session identifiée par *lParam* a été déconnectée du terminal distant.</span><span class="sxs-lookup"><span data-stu-id="1cb22-122">The session identified by *lParam* was disconnected from the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span data-ttu-id="1cb22-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ \_Ouverture de session** (0x5)</span><span class="sxs-lookup"><span data-stu-id="1cb22-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS\_SESSION\_LOGON** (0x5)</span></span>


</dt> <dd>

<span data-ttu-id="1cb22-124">Un utilisateur s’est connecté à la session identifiée par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="1cb22-124">A user has logged on to the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span data-ttu-id="1cb22-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ \_Fermeture de session** (0x6)</span><span class="sxs-lookup"><span data-stu-id="1cb22-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS\_SESSION\_LOGOFF** (0x6)</span></span>


</dt> <dd>

<span data-ttu-id="1cb22-126">Un utilisateur s’est déconnecté de la session identifiée par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="1cb22-126">A user has logged off the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span data-ttu-id="1cb22-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ \_Verrouillage de session** (0x7)</span><span class="sxs-lookup"><span data-stu-id="1cb22-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS\_SESSION\_LOCK** (0x7)</span></span>


</dt> <dd>

<span data-ttu-id="1cb22-128">La session identifiée par *lParam* a été verrouillée.</span><span class="sxs-lookup"><span data-stu-id="1cb22-128">The session identified by *lParam* has been locked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span data-ttu-id="1cb22-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ \_Déverrouillage de session** (0x8)</span><span class="sxs-lookup"><span data-stu-id="1cb22-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS\_SESSION\_UNLOCK** (0x8)</span></span>


</dt> <dd>

<span data-ttu-id="1cb22-130">La session identifiée par *lParam* a été déverrouillée.</span><span class="sxs-lookup"><span data-stu-id="1cb22-130">The session identified by *lParam* has been unlocked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span data-ttu-id="1cb22-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ \_ \_ Contrôle à distance de session** (0x9)</span><span class="sxs-lookup"><span data-stu-id="1cb22-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS\_SESSION\_REMOTE\_CONTROL** (0x9)</span></span>


</dt> <dd>

<span data-ttu-id="1cb22-132">La session identifiée par *lParam* a modifié son état contrôlé à distance.</span><span class="sxs-lookup"><span data-stu-id="1cb22-132">The session identified by *lParam* has changed its remote controlled status.</span></span> <span data-ttu-id="1cb22-133">Pour déterminer l’État, appelez [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) et vérifiez la métrique du **\_ REMOTECONTROL SM** .</span><span class="sxs-lookup"><span data-stu-id="1cb22-133">To determine the status, call [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) and check the **SM\_REMOTECONTROL** metric.</span></span>

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span data-ttu-id="1cb22-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ \_Création de session** (0xA)</span><span class="sxs-lookup"><span data-stu-id="1cb22-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS\_SESSION\_CREATE** (0xA)</span></span>


</dt> <dd>

<span data-ttu-id="1cb22-135">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="1cb22-135">Reserved for future use.</span></span>

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span data-ttu-id="1cb22-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ \_Fin de session** (0xB)</span><span class="sxs-lookup"><span data-stu-id="1cb22-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS\_SESSION\_TERMINATE** (0xB)</span></span>


</dt> <dd>

<span data-ttu-id="1cb22-137">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="1cb22-137">Reserved for future use.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1cb22-138">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cb22-138">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cb22-139">Identificateur de la session.</span><span class="sxs-lookup"><span data-stu-id="1cb22-139">The identifier of the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cb22-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cb22-140">Return value</span></span>

<span data-ttu-id="1cb22-141">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="1cb22-141">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cb22-142">Notes</span><span class="sxs-lookup"><span data-stu-id="1cb22-142">Remarks</span></span>

<span data-ttu-id="1cb22-143">Ce message est envoyé uniquement aux applications qui ont été inscrites pour recevoir ce message en appelant [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).</span><span class="sxs-lookup"><span data-stu-id="1cb22-143">This message is sent only to applications that have registered to receive this message by calling [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).</span></span>

<span data-ttu-id="1cb22-144">Des exemples de la façon dont les applications peuvent répondre à ce message incluent la libération ou l’acquisition de ressources spécifiques à la console, la détermination de la façon dont un écran doit être peint ou le déclenchement des effets d’animation de la console.</span><span class="sxs-lookup"><span data-stu-id="1cb22-144">Examples of how applications can respond to this message include releasing or acquiring console-specific resources, determining how a screen is to be painted, or triggering console animation effects.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cb22-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cb22-145">Requirements</span></span>



| <span data-ttu-id="1cb22-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cb22-146">Requirement</span></span> | <span data-ttu-id="1cb22-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cb22-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb22-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cb22-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1cb22-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1cb22-149">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="1cb22-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cb22-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1cb22-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cb22-151">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="1cb22-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cb22-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cb22-153"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cb22-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cb22-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cb22-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cb22-155">**WTSRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="1cb22-155">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[<span data-ttu-id="1cb22-156">**WTSUnRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="1cb22-156">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

