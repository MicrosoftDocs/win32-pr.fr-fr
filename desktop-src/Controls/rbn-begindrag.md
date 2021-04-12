---
title: RBN_BEGINDRAG le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsque l’utilisateur commence à faire glisser une bande. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e1565b31-7694-43cc-87ee-c9294a0612cd
keywords:
- Contrôles Windows de code de notification RBN_BEGINDRAG
topic_type:
- apiref
api_name:
- RBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c797e026484b32e68408cf720a1d4681d066c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464390"
---
# <a name="rbn_begindrag-notification-code"></a>\_Code de notification RBN BEGINDRAG

Envoyé par un contrôle rebar lorsque l’utilisateur commence à faire glisser une bande. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_BEGINDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) qui contient des informations sur le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro pour permettre au Rebar de continuer l’opération glisser, ou une valeur différente de zéro pour abandonner l’opération glisser.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





