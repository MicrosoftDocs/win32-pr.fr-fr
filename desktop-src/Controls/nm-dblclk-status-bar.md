---
title: NM_DBLCLK (barre d’État) Code de notification (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle de barre d’État que l’utilisateur a double-cliqué dans le contrôle avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 4c02c76d-2bdb-48ef-aa8e-635d0e200eb1
keywords:
- NM_DBLCLK (barre d’état) Windows des contrôles de code de notification
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3704d2a8674233d0cd5dce04849db6b0f794bc7fe5032b149de15411a3c068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088829"
---
# <a name="nm_dblclk-status-bar-notification-code"></a>\_DBLCLK nm (barre d’État) Code de notification

Notifie la fenêtre parente d’un contrôle de barre d’État que l’utilisateur a double-cliqué dans le contrôle avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_DBLCLK
        
    LPNMMOUSE lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations supplémentaires sur cette notification. Le membre **dwItemSpec** contient l’index de la section sur laquelle l’utilisateur a cliqué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour indiquer que le clic de souris a été géré et supprimer le traitement par défaut par le système. Retourne **false** pour autoriser le traitement par défaut du clic.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





