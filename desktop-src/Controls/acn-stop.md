---
title: ACN_STOP le code de notification (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle d’animation que le clip AVI associé a cessé de fonctionner. Ce code de notification est envoyé sous la forme d’un \_ message de commande WM.
ms.assetid: 2f21a2ec-975f-4592-8b21-956bd5311ef4
keywords:
- ACN_STOP les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- ACN_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ba1fe51f4ceaae6e145de43a0e1104903c90b2d573c43d7aa7904f1d8f7ae1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922089"
---
# <a name="acn_stop-notification-code"></a>ACN \_ arrêter le code de notification

Notifie la fenêtre parente d’un contrôle d’animation que le clip AVI associé a cessé de fonctionner. Ce code de notification est envoyé sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
ACN_STOP     

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’animation. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.

</dd> <dt>

*lParam* 
</dt> <dd>

**HWND** qui spécifie le handle du contrôle d’animation.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

