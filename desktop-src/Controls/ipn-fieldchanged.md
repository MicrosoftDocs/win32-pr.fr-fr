---
title: IPN_FIELDCHANGED le code de notification (commctrl. h)
description: Envoyé lorsque l’utilisateur modifie un champ dans le contrôle ou passe d’un champ à un autre. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- Contrôles Windows de code de notification IPN_FIELDCHANGED
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
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033107"
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

## <a name="remarks"></a>Notes

Ce code de notification n’est pas envoyé en réponse à un message [**\_ SETADDRESS IPM**](ipm-setaddress.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





