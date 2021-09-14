---
title: TVN_BEGINDRAG le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View qu’une opération de glisser-déplacer impliquant le bouton gauche de la souris est en cours d’initialisation. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- TVN_BEGINDRAG les contrôles de Windows de code de notification
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115530"
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

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

Un contrôle d’arborescence avec le style [**TV \_ DISABLEDRAGDROP**](tree-view-control-window-styles.md) style n’envoie pas ce code de notification.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ BEGINDRAGW** (Unicode) et **TVN \_ BEGINDRAGA** (ANSI)<br/>               |



 

 





