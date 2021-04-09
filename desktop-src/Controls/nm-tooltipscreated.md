---
title: NM_TOOLTIPSCREATED le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle que le contrôle a créé un contrôle ToolTip. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8108f084-212d-4a16-b604-1ec134b1bb43
keywords:
- Contrôles Windows de code de notification NM_TOOLTIPSCREATED
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2e99850b17b0f2b06948a09b70a89e67e65a50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032687"
---
# <a name="nm_tooltipscreated-notification-code"></a>\_Code de notification TOOLTIPSCREATED nm

Avertit la fenêtre parente d’un contrôle que le contrôle a créé un contrôle ToolTip. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Sauf spécification contraire, le contrôle ignore la valeur de retour de ce code de notification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





