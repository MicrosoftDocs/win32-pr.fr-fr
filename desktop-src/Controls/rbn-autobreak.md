---
title: Message RBN_AUTOBREAK (commctrl. h)
description: Avertit le parent d’un Rebar qu’un saut apparaîtra dans la barre. Le parent détermine s’il faut effectuer l’arrêt. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- RBN_AUTOBREAK les contrôles de message Windows
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d614277d89578cb66e528ba16656ed55681ebbcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844338"
---
# <a name="rbn_autobreak-message"></a>Message de coupure de RBN \_

Avertit le parent [d’un Rebar](rebar-controls.md) qu’un saut apparaîtra dans la barre. Le parent détermine s’il faut effectuer l’arrêt. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) qui contient des informations sur le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de cette notification n’est pas utilisée.

## <a name="remarks"></a>Notes

La valeur du membre **fAutoBreak** de la structure [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) indique si un arrêt doit se produire dans le rebar.

Pour utiliser ce code de notification, spécifiez Comctl32.dll version 6 dans le manifeste. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





