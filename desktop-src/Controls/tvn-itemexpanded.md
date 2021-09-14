---
title: TVN_ITEMEXPANDED le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que la liste des éléments enfants d’un élément parent a été développée ou réduite. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- TVN_ITEMEXPANDED les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f193e9a0ff029ca607748fe4bbb6d61f781c1248
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115498"
---
# <a name="tvn_itemexpanded-notification-code"></a>\_Code de notification TVN ITEMEXPANDED

Avertit une fenêtre parente d’un contrôle Tree-View que la liste des éléments enfants d’un élément parent a été développée ou réduite. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Le membre **itemNew** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient des informations valides sur l’élément parent dans les membres **hitem**, **State** et **lParam** . Le membre d' **action** indique si la liste a été développée ou réduite. Pour obtenir la liste des valeurs possibles, consultez la description du message de [**\_ développement TVM**](tvm-expand.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ ITEMEXPANDEDW** (Unicode) et **TVN \_ ITEMEXPANDEDA** (ANSI)<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TVN \_ ITEMEXPANDING](tvn-itemexpanding.md)
</dt> </dl>

 

 





