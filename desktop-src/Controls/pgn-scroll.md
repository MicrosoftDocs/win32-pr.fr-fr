---
title: PGN_SCROLL le code de notification (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle de pagineur que la fenêtre contenue est sur le défilant. Cette notification est envoyée sous la forme d’un \_ message WM Notify.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- Contrôles Windows de code de notification PGN_SCROLL
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bc964b1a820fb0d5cd341e8909f36d5f6312ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103472"
---
# <a name="pgn_scroll-notification-code"></a>\_Code de notification de défilement PGN

Notifie la fenêtre parente d’un contrôle de pagineur que la fenêtre contenue est sur le défilant. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) qui contient et reçoit des informations sur le code de notification. Le membre **iDir** de cette structure indique la direction du défilement. Les membres **iXpos** et **iYpos** contiennent la position horizontale et verticale de la fenêtre contenue avant le défilement. Le membre **iScroll** contient le montant Delta de défilement par défaut. Vous pouvez modifier ce membre en fonction d’un autre montant de défilement, si vous le souhaitez.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





