---
title: Message WM_NOTIFY (winuser. h)
description: Envoyé par un contrôle commun à sa fenêtre parente lorsqu’un événement s’est produit ou que le contrôle requiert des informations.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- WM_NOTIFY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1905954e7fb164f8436216fa918cc6f243f4b17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115146"
---
# <a name="wm_notify-message"></a>\_Message de notification WM

Envoyé par un contrôle commun à sa fenêtre parente lorsqu’un événement s’est produit ou que le contrôle requiert des informations.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur du contrôle commun qui envoie le message. Il n’est pas garanti que cet identificateur soit unique. Une application doit utiliser le membre **hwndFrom** ou **idFrom** de la structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) (passé comme paramètre *lParam* ) pour identifier le contrôle.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient le code de notification et des informations supplémentaires. Pour certains messages de notification, ce paramètre pointe vers une structure plus grande qui a la structure **NMHDR** comme premier membre.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée, à l’exception des messages de notification qui le définissent autrement.

## <a name="remarks"></a>Notes

La destination du message doit être le **HWND** du parent du contrôle. Cette valeur peut être obtenue à l’aide de [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), comme illustré dans l’exemple suivant, où *m \_ controlHwnd* est le **HWND** du contrôle lui-même.


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



Les applications gèrent le message dans la procédure de fenêtre de la fenêtre parente, comme illustré dans l’exemple suivant, qui gère le message de notification envoyé par le contrôle personnalisé dans l’exemple précédent.


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



Certaines notifications, essentiellement celles qui se trouvent dans l’API pendant une longue période, sont envoyées en tant que messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) . Pour plus d’informations, consultez [contrôle des messages](control-messages.md).

Si le gestionnaire de messages est dans une procédure de boîte de dialogue, vous devez utiliser la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec DWL \_ MSGRESULT pour définir une valeur de retour.

pour les systèmes Windows Vista et versions ultérieures, le message **WM \_ NOTIFY** ne peut pas être envoyé entre les processus.

De nombreuses notifications sont disponibles à la fois dans les formats ANSI et Unicode. La fenêtre qui envoie le message **WM \_ Notify** utilise le message [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) pour déterminer le format à utiliser. Pour plus d’informations, consultez **WM \_ NOTIFYFORMAT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_NOTIFYFORMAT WM**](wm-notifyformat.md)
</dt> </dl>

 

