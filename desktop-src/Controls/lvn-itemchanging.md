---
title: LVN_ITEMCHANGING le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View qu’un élément est en modification. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- Contrôles Windows de code de notification LVN_ITEMCHANGING
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6183cd218792a34276db75dce5953189a8118674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942920"
---
# <a name="lvn_itemchanging-notification-code"></a>\_Code de notification LVN ITEMCHANGING

Avertit la fenêtre parente d’un contrôle List-View qu’un élément est en modification. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) qui identifie l’élément et spécifie les attributs modifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour empêcher la modification, ou **false** pour autoriser la modification.

## <a name="remarks"></a>Notes

Si le contrôle List-View a le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) , les \_ codes de notification LVN ITEMCHANGING ne sont pas envoyés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





