---
title: NM_RCLICK (barre d’État) Code de notification (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle de barre d’État sur lequel l’utilisateur a cliqué avec le bouton droit de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 9a441d32-f4e4-42ae-877f-17079b0188f4
keywords:
- NM_RCLICK (barre d’État) contrôles Windows de code de notification
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326ac6600716419648ecfacf25cd8423551fd03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317525"
---
# <a name="nm_rclick-status-bar-notification-code"></a>\_RCLICK nm (barre d’État) Code de notification

Notifie la fenêtre parente d’un contrôle de barre d’État sur lequel l’utilisateur a cliqué avec le bouton droit de la souris dans le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RCLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour indiquer que le clic de souris a été géré et supprimer le traitement par défaut par le système. Retourne **false** pour autoriser le traitement par défaut du clic.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





