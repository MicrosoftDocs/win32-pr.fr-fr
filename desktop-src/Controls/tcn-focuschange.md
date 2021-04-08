---
title: TCN_FOCUSCHANGE le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle onglet que le focus du bouton a changé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 7500faae-5386-465d-ae4a-285205bccc1f
keywords:
- Contrôles Windows de code de notification TCN_FOCUSCHANGE
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
ms.openlocfilehash: 80c7ef76daf7ff9731a3fe5d749141454df19c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739868"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





