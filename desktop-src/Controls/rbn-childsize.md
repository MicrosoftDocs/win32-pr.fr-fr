---
title: RBN_CHILDSIZE le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsque la fenêtre enfant d’une bande est redimensionnée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ba64d21a-e568-4894-8007-be644ae4f54a
keywords:
- Contrôles Windows de code de notification RBN_CHILDSIZE
topic_type:
- apiref
api_name:
- RBN_CHILDSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d505d13048d96783d53b9b1a821d80712597da4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843789"
---
# <a name="rbn_childsize-notification-code"></a>\_Code de notification RBN CHILDSIZE

Envoyé par un contrôle rebar lorsque la fenêtre enfant d’une bande est redimensionnée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_CHILDSIZE

    lprbcs = (LPNMREBARCHILDSIZE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) qui contient des informations sur le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de cette notification n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





