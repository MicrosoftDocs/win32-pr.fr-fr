---
title: NM_SETCURSOR le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le contrôle définit le curseur en réponse à un \_ message WM SETCURSOR. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8d70563f-05a3-4116-b686-6d9063940fae
keywords:
- NM_SETCURSOR les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cc3c48a0224efec0c8ab8844a3e7f234a9ba51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117797"
---
# <a name="nm_setcursor-notification-code"></a>\_Code de notification SETCURSOR nm

Avertit la fenêtre parente d’un contrôle que le contrôle définit le curseur en réponse à un message [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) . Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retournez zéro pour permettre au contrôle de définir le curseur ou une valeur différente de zéro pour empêcher le contrôle de définir le curseur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

