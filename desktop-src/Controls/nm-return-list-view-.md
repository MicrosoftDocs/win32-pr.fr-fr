---
title: Code de notification NM_RETURN (mode liste) (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle d’affichage de liste que le contrôle a le focus d’entrée et que l’utilisateur a appuyé sur la touche entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 21a8d308-d747-4020-8925-d982234bcf81
keywords:
- Contrôles Windows de code de notification NM_RETURN (mode liste)
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b221189ced0e351f088493f00fa7b8849717668
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942552"
---
# <a name="nm_return-list-view-notification-code"></a>NM \_ retour (mode liste) Code de notification

Avertit une fenêtre parente d’un contrôle d’affichage de liste que le contrôle a le focus d’entrée et que l’utilisateur a appuyé sur la touche entrée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RETURN 

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



 

 





