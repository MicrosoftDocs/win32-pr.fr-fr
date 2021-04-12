---
title: Code de notification NM_KILLFOCUS (mode liste) (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View que le contrôle a perdu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: f60064da-21e1-4555-ae72-cda8bd76175a
keywords:
- Contrôles Windows de code de notification NM_KILLFOCUS (mode liste)
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
ms.openlocfilehash: 2d1c031f3ab23d9f79ccf7f29dcfdf5472162214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464262"
---
# <a name="nm_killfocus-list-view-notification-code"></a>\_KILLFOCUS nm (mode liste) Code de notification

Avertit la fenêtre parente d’un contrôle List-View que le contrôle a perdu le focus d’entrée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de cette notification n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





