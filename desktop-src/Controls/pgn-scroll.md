---
title: PGN_SCROLL le code de notification (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle de pagineur que la fenêtre contenue est sur le défilant. Cette notification est envoyée sous la forme d’un \_ message WM Notify.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- PGN_SCROLL les contrôles de Windows de code de notification
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
ms.openlocfilehash: 864903c73eeb611d1c748ec6a4d936192a1a27f22d3f37115af8879916286a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830143"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





