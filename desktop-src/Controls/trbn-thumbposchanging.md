---
title: TRBN_THUMBPOSCHANGING le code de notification (commctrl. h)
description: Indique que la position du curseur sur un TrackBar est modifiée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- TRBN_THUMBPOSCHANGING les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23722b68f28a5157948ac6277858193366242fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115925"
---
# <a name="trbn_thumbposchanging-notification-code"></a>\_Code de notification TRBN THUMBPOSCHANGING

Indique que la position du curseur sur un TrackBar est modifiée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) . L’appelant est chargé d’allouer cette structure et de définir ses membres, y compris les membres de la structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenue.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** pour empêcher le déplacement du curseur à la position spécifiée.

## <a name="remarks"></a>Notes

Envoyez cette notification aux clients qui n’écoutent pas les messages [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





