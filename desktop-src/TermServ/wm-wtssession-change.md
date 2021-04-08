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
# <a name="wm_wtssession_change-message"></a>Message de modification de WM \_ WTSSESSION \_

Avertit les applications des modifications apportées à l’état de session.

La fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de la fenêtre.

</dd> <dt>

*Message* \[ dans\]
</dt> <dd>

Spécifie le message (**WM \_ WTSSESSION \_ change**).

</dd> <dt>

*wParam* \[ dans\]
</dt> <dd>

Code d’état décrivant la raison de l’envoi de la notification de changement d’état de session. Ce paramètre peut prendre les valeurs suivantes.

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ \_Connexion** à la console (0x1)


</dt> <dd>

La session identifiée par *lParam* était connectée au terminal de la console ou à la session RemoteFX.

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ \_Déconnexion** de la console (0X2)


</dt> <dd>

La session identifiée par *lParam* a été déconnectée du terminal de la console ou de la session RemoteFX.

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ \_Connexion à distance** (0x3)


</dt> <dd>

La session identifiée par *lParam* était connectée au terminal distant.

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ \_Déconnexion à distance** (0x4)


</dt> <dd>

La session identifiée par *lParam* a été déconnectée du terminal distant.

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ \_Ouverture de session** (0x5)


</dt> <dd>

Un utilisateur s’est connecté à la session identifiée par *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ \_Fermeture de session** (0x6)


</dt> <dd>

Un utilisateur s’est déconnecté de la session identifiée par *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ \_Verrouillage de session** (0x7)


</dt> <dd>

La session identifiée par *lParam* a été verrouillée.

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ \_Déverrouillage de session** (0x8)


</dt> <dd>

La session identifiée par *lParam* a été déverrouillée.

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ \_ \_ Contrôle à distance de session** (0x9)


</dt> <dd>

La session identifiée par *lParam* a modifié son état contrôlé à distance. Pour déterminer l’État, appelez [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) et vérifiez la métrique du **\_ REMOTECONTROL SM** .

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ \_Création de session** (0xA)


</dt> <dd>

Réservé pour un usage futur.

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ \_Fin de session** (0xB)


</dt> <dd>

Réservé pour un usage futur.

</dd> </dl> </dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Identificateur de la session.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

Ce message est envoyé uniquement aux applications qui ont été inscrites pour recevoir ce message en appelant [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).

Des exemples de la façon dont les applications peuvent répondre à ce message incluent la libération ou l’acquisition de ressources spécifiques à la console, la détermination de la façon dont un écran doit être peint ou le déclenchement des effets d’animation de la console.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                           |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

