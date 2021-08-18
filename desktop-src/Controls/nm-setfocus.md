---
title: NM_SETFOCUS le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le contrôle a reçu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 4810afd3-c8a8-4813-b44a-eba3d409d4f1
keywords:
- NM_SETFOCUS les contrôles de Windows de code de notification
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
ms.openlocfilehash: 7d1818c655b3116c90f6a74f3ba68da7477ee79fc8486021c714aaa778f9ae4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217219"
---
# <a name="nm_setfocus-notification-code"></a>NM \_ Code de notification SetFocus

Avertit la fenêtre parente d’un contrôle que le contrôle a reçu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


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

La valeur de retour est ignorée par le contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





