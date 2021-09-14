---
title: TVN_SELCHANGING le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que la sélection est sur le point de passer d’un élément à un autre. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- TVN_SELCHANGING les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115489"
---
# <a name="tvn_selchanging-notification-code"></a>\_Code de notification TVN SELCHANGING

Avertit une fenêtre parente d’un contrôle Tree-View que la sélection est sur le point de passer d’un élément à un autre. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Les membres **itemOld** et **itemNew** contiennent des informations valides sur l’élément actuellement sélectionné et sur l’élément nouvellement sélectionné. Le membre d' **action** indique si une action de la souris ou du clavier est à l’origine de la modification de la sélection. Pour obtenir la liste des valeurs possibles, consultez la description du code de notification [TVN \_ SELCHANGED](tvn-selchanged.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** pour empêcher la modification de la sélection.

## <a name="remarks"></a>Notes

Lors de la réponse à ce code de notification, les applications ne doivent pas supprimer les éléments qui obtiennent ou perdent la sélection.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ SELCHANGINGW** (Unicode) et **TVN \_ SELCHANGINGA** (ANSI)<br/>           |



 

 





