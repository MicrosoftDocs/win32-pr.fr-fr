---
title: RBN_LAYOUTCHANGED le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar lorsque l’utilisateur modifie la disposition des bandes du contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e937d151-bfaa-41c0-a134-e70ff2f75d07
keywords:
- RBN_LAYOUTCHANGED les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- RBN_LAYOUTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1fc14578435fc786ecc5496cec96eb2224b4d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117154"
---
# <a name="rbn_layoutchanged-notification-code"></a>\_Code de notification RBN LAYOUTCHANGED

Envoyé par un contrôle rebar lorsque l’utilisateur modifie la disposition des bandes du contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_LAYOUTCHANGED 

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour de cette notification n’est pas utilisée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





