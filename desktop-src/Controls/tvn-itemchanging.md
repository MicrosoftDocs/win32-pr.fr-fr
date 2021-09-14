---
title: TVN_ITEMCHANGING le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que les attributs d’élément sont sur le point de changer. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115506"
---
# <a name="tvn_itemchanging-notification-code"></a>\_Code de notification TVN ITEMCHANGING

Avertit une fenêtre parente d’un contrôle Tree-View que les attributs d’élément sont sur le point de changer. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) décrivant l’élément qui change. Le membre **uChanged** est défini sur l' \_ État TVIF.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne **false** pour accepter la modification, ou **true** pour empêcher la modification.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ ITEMCHANGINGW** (Unicode) et **TVN \_ ITEMCHANGINGA** (ANSI)<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TVN \_ ITEMCHANGED](tvn-itemchanged.md)
</dt> </dl>

 

 





