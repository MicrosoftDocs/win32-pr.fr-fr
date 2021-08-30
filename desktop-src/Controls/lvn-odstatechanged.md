---
title: LVN_ODSTATECHANGED le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View lorsque l’état d’un élément ou d’une plage d’éléments a changé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: a3aafda5-a3ec-4f84-8153-8d34097e04f1
keywords:
- LVN_ODSTATECHANGED les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LVN_ODSTATECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf8712078e3398f775115233c0fd54622943cc2cb7febe0c24d800776418de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915109"
---
# <a name="lvn_odstatechanged-notification-code"></a>\_Code de notification LVN ODSTATECHANGED

Envoyé par un contrôle List-View lorsque l’état d’un élément ou d’une plage d’éléments a changé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_ODSTATECHANGED

    lpStateChange = (LPNMLVODSTATECHANGE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) qui contient des informations sur l’élément ou les éléments qui ont été modifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

L’application recevant ce code de notification doit retourner zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





