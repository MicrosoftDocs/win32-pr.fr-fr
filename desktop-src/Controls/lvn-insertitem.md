---
title: LVN_INSERTITEM le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’un nouvel élément a été inséré. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8d368fb2-e4fc-4dc4-a89e-872ba1278b75
keywords:
- LVN_INSERTITEM les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LVN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1c706c7329e192559cb307962e293f0bbf02109c81fcde177eb36d8d39e37e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062149"
---
# <a name="lvn_insertitem-notification-code"></a>\_Code de notification LVN INSERTITEM

Avertit la fenêtre parente d’un contrôle List-View qu’un nouvel élément a été inséré. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_INSERTITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Le membre **iItem** identifie le nouvel élément, et les autres membres sont nuls.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





