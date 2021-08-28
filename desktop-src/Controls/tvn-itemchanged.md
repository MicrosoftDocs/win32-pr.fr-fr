---
title: TVN_ITEMCHANGED le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que les attributs d’élément ont été modifiés. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- TVN_ITEMCHANGED les contrôles de Windows de code de notification
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
ms.openlocfilehash: d140346d66a87bd394bc5aa36555b8accedef56891e722a4b28272e22f804ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018647"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ ITEMCHANGEDW** (Unicode) et **TVN \_ ITEMCHANGEDA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TVN \_ ITEMCHANGING](tvn-itemchanging.md)
</dt> </dl>

 

 





