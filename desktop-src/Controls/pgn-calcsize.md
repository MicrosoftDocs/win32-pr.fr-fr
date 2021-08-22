---
title: PGN_CALCSIZE le code de notification (commctrl. h)
description: Envoyé par un contrôle pager pour obtenir les dimensions déroulantes de la fenêtre contenue.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- PGN_CALCSIZE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c2f6da5153457a871918afea60ac1251496454831a09426f16579ac47342406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078873"
---
# <a name="pgn_calcsize-notification-code"></a>\_Code de notification PGN CALCSIZE

Envoyé par un contrôle pager pour obtenir les dimensions déroulantes de la fenêtre contenue. Ces dimensions sont utilisées par le contrôle de pagineur pour déterminer la taille de défilement de la fenêtre contenue. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) qui contient et reçoit des informations sur le code de notification. Le membre **dwFlag** de cette structure indique quelle dimension est calculée. Selon la valeur de **dwFlag**, vous devez placer la dimension souhaitée dans le membre **iWidth** ou **iHeight** de cette structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





