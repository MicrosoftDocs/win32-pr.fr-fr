---
title: NM_RELEASEDCAPTURE (onglet) Code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle onglet que le contrôle libère la capture de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 17f87666-692c-4c2f-9ef5-6d2593e0de97
keywords:
- NM_RELEASEDCAPTURE (onglet) code de notification Windows les contrôles
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c262d5a36fe868ef4c15333f02a21a02ad67788c68d5826b839d00c1843387b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261609"
---
# <a name="nm_releasedcapture-tab-notification-code"></a>\_Code de notification RELEASEDCAPTURE nm (onglet)

Avertit une fenêtre parente d’un contrôle onglet que le contrôle libère la capture de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





