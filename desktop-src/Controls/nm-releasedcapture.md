---
title: NM_RELEASEDCAPTURE le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le contrôle libère la capture de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 222a3be1-20f1-43c6-b982-852512209a45
keywords:
- NM_RELEASEDCAPTURE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2513ad413b5d4be8de3aa38b7b031b69d36ce017c9567cd9f0d85f5f05dfd80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986359"
---
# <a name="nm_releasedcapture-notification-code"></a>\_Code de notification RELEASEDCAPTURE nm

Avertit la fenêtre parente d’un contrôle que le contrôle libère la capture de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Sauf spécification contraire, le contrôle ignore la valeur de retour de ce code de notification.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





