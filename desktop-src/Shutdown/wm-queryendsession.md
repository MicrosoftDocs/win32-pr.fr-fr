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
# <a name="wm_queryendsession-message"></a>\_Message WM QUERYENDSESSION

Le message **WM \_ QUERYENDSESSION** est envoyé lorsque l’utilisateur choisit de mettre fin à la session ou lorsqu’une application appelle l’une des fonctions d’arrêt du système. Si une application retourne la valeur zéro, la session n’est pas terminée. Le système arrête d’envoyer des messages **WM \_ QUERYENDSESSION** dès qu’une application retourne zéro.

Après le traitement de ce message, le système envoie le message [**WM \_ ENDSESSION**](wm-endsession.md) avec le paramètre *wParam* défini sur les résultats du message **WM \_ QUERYENDSESSION** .

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
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

Identificateur **WM \_ QUERYENDSESSION** .

</dd> <dt>

*wParam* 
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre peut être une ou plusieurs des valeurs suivantes. Si ce paramètre a la valeur 0, le système est en cours d’arrêt ou de redémarrage (il n’est pas possible de déterminer l’événement qui se produit).



| Valeur                                                                                                                                                                                                                                           | Signification                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <dt>**ENDSESSION \_ CLOSEAPP**</dt> <dt>0x00000001</dt> </dl> | L’application utilise un fichier qui doit être remplacé, le système est en cours de maintenance ou les ressources système sont épuisées. Pour plus d’informations, consultez [instructions pour les applications](../rstmgr/guidelines-for-applications.md).<br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <dt>**ENDSESSION \_**</dt> <dt>0x40000000</dt> critiques </dl> | L’application est obligée de s’arrêter.<br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <dt>**ENDSESSION \_ Fermeture de session**</dt> <dt>0x80000000</dt> </dl>       | L’utilisateur se déconnecte. Pour plus d’informations, consultez [déconnexion](logging-off.md).<br/>                                                                                                                                   |



 

Notez que ce paramètre est un masque de bits. Pour tester cette valeur, utilisez une opération au niveau du bit. ne Testez pas l’égalité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Les applications doivent respecter les intentions de l’utilisateur et retourner la **valeur true**. Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne la **valeur true** pour ce message.

Si l’arrêt endommage le système ou le support en cours de gravure, l’application peut retourner la **valeur false**. Toutefois, il est recommandé de respecter les actions de l’utilisateur.

## <a name="remarks"></a>Notes

Quand une application retourne la **valeur true** pour ce message, elle reçoit le message [**WM \_ ENDSESSION**](wm-endsession.md) , quelle que soit la manière dont les autres applications répondent au message **WM \_ QUERYENDSESSION** . Chaque application doit retourner la **valeur true** ou **false** immédiatement lors de la réception de ce message, et différer les opérations de nettoyage jusqu’à ce qu’elle reçoive le message **WM \_ ENDSESSION** .

Les applications peuvent afficher une interface utilisateur invitant l’utilisateur à fournir des informations lors de l’arrêt, mais cela n’est pas recommandé. Au bout de cinq secondes, le système affiche des informations sur les applications qui empêchent l’arrêt et permet à l’utilisateur de les arrêter. Par exemple, Windows XP affiche une boîte de dialogue, tandis que Windows Vista affiche un plein écran avec des informations supplémentaires sur les applications bloquant l’arrêt. Si votre application doit bloquer ou différer l’arrêt du système, utilisez la fonction [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) . Pour plus d’informations, consultez [modifications de l’arrêt de Windows Vista](shutdown-changes-for-windows-vista.md).

Les applications console peuvent utiliser la fonction [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) pour recevoir des notifications d’arrêt.

Les applications de service peuvent utiliser la fonction [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) pour recevoir des notifications d’arrêt dans une routine de gestionnaire.

## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez [déconnexion](logging-off.md).

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[**\_ENDSESSION WM**](wm-endsession.md)
</dt> </dl>

 

 
