---
title: IPN_FIELDCHANGED le code de notification (commctrl. h)
description: Envoyé lorsque l’utilisateur modifie un champ dans le contrôle ou passe d’un champ à un autre. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467cf7f14f3ff8d62f85d973e9a9d11c4dc6d20488ad5b7e30b4c0787b4b1a6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085549"
---
# <a name="ipn_fieldchanged-notification-code"></a>\_Code de notification IPN FIELDCHANGED

Envoyé lorsque l’utilisateur modifie un champ dans le contrôle ou passe d’un champ à un autre. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) qui contient des informations sur l’adresse modifiée. Le membre **iValue** de cette structure contiendra la valeur entrée, même si elle est en dehors de la plage du champ. Vous pouvez modifier ce membre en n’importe quelle valeur comprise dans la plage du champ en réponse à ce code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Remarques

Ce code de notification n’est pas envoyé en réponse à un message [**\_ SETADDRESS IPM**](ipm-setaddress.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





