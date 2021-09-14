---
title: TVN_ITEMEXPANDING le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que la liste des éléments enfants d’un élément parent est sur le point d’être développée ou réduite. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115493"
---
# <a name="tvn_itemexpanding-notification-code"></a>\_Code de notification TVN ITEMEXPANDING

Avertit une fenêtre parente d’un contrôle Tree-View que la liste des éléments enfants d’un élément parent est sur le point d’être développée ou réduite. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Le membre **itemNew** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contient des informations valides sur l’élément parent dans les membres **hitem**, **State** et **lParam** . Le membre d' **action** indique si la liste doit être développée ou réduite. Pour obtenir la liste des valeurs possibles, consultez la description du message de [**\_ développement TVM**](tvm-expand.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** pour empêcher le développement ou la réduction de la liste.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ ITEMEXPANDINGW** (Unicode) et **TVN \_ ITEMEXPANDINGA** (ANSI)<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TVN \_ ITEMEXPANDED](tvn-itemexpanded.md)
</dt> </dl>

 

 





