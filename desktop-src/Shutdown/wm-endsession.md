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
# <a name="wm_endsession-message"></a>\_Message WM ENDSESSION

Le message **WM \_ ENDSESSION** est envoyé à une application une fois que le système a traité les résultats du message [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) . Le message **WM \_ ENDSESSION** informe l’application que la session se termine.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de la fenêtre.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificateur **WM \_ ENDSESSION** .

</dd> <dt>

*wParam* 
</dt> <dd>

Si la session est terminée, ce paramètre a la **valeur true**. la session peut se terminer à tout moment une fois que toutes les applications ont renvoyé le traitement de ce message. Sinon, la **valeur est false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre peut être une ou plusieurs des valeurs suivantes. Si ce paramètre a la valeur 0, le système est en cours d’arrêt ou de redémarrage (il n’est pas possible de déterminer l’événement qui se produit).



| Valeur                                                                                                                                                                                                                                           | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDSESSION \_ CLOSEAPP**</dt> <dt>0x1</dt> </dl>        | Si *wParam* a la **valeur true**, l’application doit être arrêtée. Toutes les données doivent être enregistrées automatiquement sans inviter l’utilisateur (pour plus d’informations, consultez la section Notes). Le gestionnaire de redémarrage envoie ce message lorsque l’application utilise un fichier qui doit être remplacé, lorsqu’il doit le faire, ou lorsque des ressources système sont épuisées. L’application sera redémarrée si elle est inscrite pour le redémarrage à l’aide de la fonction [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) . Pour plus d’informations, consultez [instructions pour les applications](../rstmgr/guidelines-for-applications.md). <br/> Si *wParam* a la **valeur false**, l’application ne doit pas s’arrêter.<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDSESSION \_**</dt> <dt>0x40000000</dt> critiques </dl> | L’application est obligée de s’arrêter.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDSESSION \_ Fermeture de session**</dt> <dt>0x80000000</dt> </dl>       | L’utilisateur se déconnecte. Pour plus d’informations, consultez [déconnexion](logging-off.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Notez que ce paramètre est un masque de bits. Pour tester cette valeur, utilisez une opération au niveau du bit. ne Testez pas l’égalité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Les applications qui contiennent des données non enregistrées peuvent enregistrer les données dans un emplacement temporaire et les restaurer lors du prochain démarrage de l’application. Il est recommandé que les applications enregistrent fréquemment leurs données et leur état ; par exemple, enregistrez automatiquement les données entre les opérations d’enregistrement initiées par l’utilisateur pour réduire la quantité de données à enregistrer lors de l’arrêt.

L’application n’a pas besoin d’appeler la fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) ou [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) lorsque la session se termine.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP- \[ \| applications UWP\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ \| apps UWP\]<br/>                                              |
| En-tête<br/>                   | <dl> <dt>WinUser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fermeture de session](logging-off.md)
</dt> <dt>

[Arrêt en cours](shutting-down.md)
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**\_QUERYENDSESSION WM**](wm-queryendsession.md)
</dt> </dl>

 

 
