---
title: Code de notification NM_SETFOCUS (mode liste) (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View que le contrôle a reçu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 43d3b09a-f095-4f30-87a8-2f2e782d6720
keywords:
- NM_SETFOCUS (mode liste) code de notification Windows les contrôles
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312382eb81694bc49a121cd336e76c361a3519222f63723bb8d5203201c996f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410302"
---
# <a name="nm_setfocus-list-view-notification-code"></a>NM \_ SetFocus (mode liste) Code de notification

Avertit une fenêtre parente d’un contrôle List-View que le contrôle a reçu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de cette notification n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





