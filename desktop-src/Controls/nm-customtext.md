---
title: NM_CUSTOMTEXT le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle des opérations de texte personnalisées. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b4bde648-3479-4fac-ad32-b34c7272c1fc
keywords:
- NM_CUSTOMTEXT les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- NM_CUSTOMTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512ccb6cd94ce680b9832c342696941d98c0e6543c319caeb89eb409de1fe73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018871"
---
# <a name="nm_customtext-notification-code"></a>\_Code de notification CUSTOMTEXT nm

Avertit la fenêtre parente d’un contrôle des opérations de texte personnalisées. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CUSTOMTEXT

    lpnmct = (NMCUSTOMTEXT) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée par le contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





