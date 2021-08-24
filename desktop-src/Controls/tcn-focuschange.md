---
title: TCN_FOCUSCHANGE le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle onglet que le focus du bouton a changé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 7500faae-5386-465d-ae4a-285205bccc1f
keywords:
- TCN_FOCUSCHANGE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TCN_FOCUSCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318438c6f5c901f6839136c3f7694c08c76c82e1228cb1507d6751eab03f00ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166922"
---
# <a name="tcn_focuschange-notification-code"></a>\_Code de notification TCN FOCUSCHANGE

Avertit une fenêtre parente d’un contrôle onglet que le focus du bouton a changé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TCN_FOCUSCHANGE

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





