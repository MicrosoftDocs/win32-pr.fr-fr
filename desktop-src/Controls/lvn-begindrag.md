---
title: LVN_BEGINDRAG le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View qu’une opération de glisser-déplacer impliquant le bouton gauche de la souris est en cours d’initialisation. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2b9bbff8-f5f7-47ac-b662-a327ff49caf7
keywords:
- LVN_BEGINDRAG les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LVN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69166cd38242db915f70772b5dfbd3bab6ba56df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012326"
---
# <a name="lvn_begindrag-notification-code"></a>\_Code de notification LVN BEGINDRAG

Avertit une fenêtre parente d’un contrôle List-View qu’une opération de glisser-déplacer impliquant le bouton gauche de la souris est en cours d’initialisation. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_BEGINDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . Le membre **iItem** identifie l’élément déplacé et les autres membres sont nuls.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





