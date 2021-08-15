---
title: NM_FONTCHANGED le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View lorsque le contrôle a modifié une police. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ffa019b0-34be-4bb3-b9dd-c267545fec84
keywords:
- NM_FONTCHANGED les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- NM_FONTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5369b7719a02e28562f4e71aecffdd3680aa602b6154eac9cc8685bdbe2b2b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411144"
---
# <a name="nm_fontchanged-notification-code"></a>\_Code de notification FONTCHANGED nm

Envoyé par un contrôle List-View lorsque le contrôle a modifié une police. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_FONTCHANGED
        
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
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





