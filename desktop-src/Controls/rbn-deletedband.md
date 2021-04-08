---
title: RBN_DELETEDBAND le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar après la suppression d’une bande. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ef4aca07-de08-47de-b236-321e84e6e81c
keywords:
- Contrôles Windows de code de notification RBN_DELETEDBAND
topic_type:
- apiref
api_name:
- RBN_DELETEDBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6af4e107ccb1a42b82335255f48d0328e03019a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843917"
---
# <a name="rbn_deletedband-notification-code"></a>\_Code de notification RBN DELETEDBAND

Envoyé par un contrôle rebar après la suppression d’une bande. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_DELETEDBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) qui contient des informations sur le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de cette notification n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





