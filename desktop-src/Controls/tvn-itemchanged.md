---
title: TVN_ITEMCHANGED le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que les attributs d’élément ont été modifiés. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- Contrôles Windows de code de notification TVN_ITEMCHANGED
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d58501d02cc2058ac803c949cc7118d7f146a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843653"
---
# <a name="tvn_itemchanged-notification-code"></a>\_Code de notification TVN ITEMCHANGED

Avertit une fenêtre parente d’un contrôle Tree-View que les attributs d’élément ont été modifiés. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) décrivant l’élément qui a changé. Le membre **uChanged** est défini sur l' \_ État TVIF.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **false** pour accepter la modification, ou **true** pour empêcher la modification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ ITEMCHANGEDW** (Unicode) et **TVN \_ ITEMCHANGEDA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TVN \_ ITEMCHANGING](tvn-itemchanging.md)
</dt> </dl>

 

 





