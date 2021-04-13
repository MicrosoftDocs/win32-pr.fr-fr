---
title: PSN_WIZFINISH le code de notification (Prsht. h)
description: Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton Terminer dans un Assistant. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- Contrôles Windows de code de notification PSN_WIZFINISH
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0654384b0944d90731288922c32326e42019cdc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466091"
---
# <a name="psn_wizfinish-notification-code"></a>\_Code de notification PSN WIZFINISH

Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton **Terminer** dans un Assistant. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification. Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés. Le membre **lParam** de la structure **PSHNOTIFY** ne contient aucune information.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

-   Retourne la **valeur true** pour empêcher la fin de l’Assistant.
-   [Version 5,80.](common-control-versions.md) et versions ultérieures. Retourne un handle de fenêtre pour empêcher la fin de l’Assistant. L’Assistant va définir le focus sur cette fenêtre. La fenêtre doit appartenir à la page de l’Assistant.
-   Retourne **false** pour permettre à l’Assistant de se terminer.

## <a name="remarks"></a>Notes

Pour définir la valeur de retour, la procédure de la boîte de dialogue de la page doit utiliser la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la valeur MSGRESULT de la boîte de \_ dialogue, et la procédure de boîte de dialogue doit retourner **true**.

[Version 5,80.](common-control-versions.md) Si votre application retourne la **valeur true** pour empêcher la finition d’un Assistant, elle n’a aucun contrôle sur la fenêtre sur laquelle la page reçoit le focus. Normalement, les applications qui doivent arrêter un Assistant peuvent le faire en retournant le handle de la fenêtre sur la page de l’Assistant qui doit recevoir le focus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

