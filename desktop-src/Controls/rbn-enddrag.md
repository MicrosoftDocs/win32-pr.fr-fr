---
title: RBN_ENDDRAG le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsque l’utilisateur arrête de faire glisser une bande. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 24b06144-6a4c-46a4-bef1-d6592f72a2c0
keywords:
- RBN_ENDDRAG les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- RBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c09831672d61c824a1c8cea30b3ba3731d4ad589cc98c88ce3830586cb342cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985059"
---
# <a name="rbn_enddrag-notification-code"></a>\_Code de notification RBN ENDDRAG

Envoyé par un contrôle rebar lorsque l’utilisateur arrête de faire glisser une bande. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_ENDDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) qui contient des informations sur le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour pour ce code de notification n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





