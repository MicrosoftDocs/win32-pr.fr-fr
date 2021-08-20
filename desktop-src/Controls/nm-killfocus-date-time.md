---
title: NM_KILLFOCUS (date et heure) Code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle de sélecteur de date et d’heure que le contrôle a perdu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 33d6b88b-9608-4227-a822-1dc7a77d3a3f
keywords:
- NM_KILLFOCUS (date heure) code de notification Windows les contrôles
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0147fd5d79998024df8c12d9be4a9a71ee3c1751a3f31d21d090ea2c7e9a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018837"
---
# <a name="nm_killfocus-date-time-notification-code"></a>\_KILLFOCUS nm (date et heure) Code de notification

Avertit une fenêtre parente d’un contrôle de sélecteur de date et d’heure que le contrôle a perdu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Adresse d’une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





