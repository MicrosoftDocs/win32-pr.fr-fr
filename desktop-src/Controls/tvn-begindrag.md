---
title: TVN_BEGINDRAG le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View qu’une opération de glisser-déplacer impliquant le bouton gauche de la souris est en cours d’initialisation. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- Contrôles Windows de code de notification TVN_BEGINDRAG
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f47f55a5e2eae552f64234a8e43ef0961f38c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843654"
---
# <a name="tvn_begindrag-notification-code"></a>\_Code de notification TVN BEGINDRAG

Avertit une fenêtre parente d’un contrôle Tree-View qu’une opération de glisser-déplacer impliquant le bouton gauche de la souris est en cours d’initialisation. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Le membre **itemNew** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient des informations valides sur l’élément déplacé dans les membres **hitem**, **State** et **lParam** . Le membre **ptDrag** spécifie les coordonnées d’écran actuelles de la souris.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

Un contrôle d’arborescence avec le style [**TV \_ DISABLEDRAGDROP**](tree-view-control-window-styles.md) style n’envoie pas ce code de notification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ BEGINDRAGW** (Unicode) et **TVN \_ BEGINDRAGA** (ANSI)<br/>               |



 

 





