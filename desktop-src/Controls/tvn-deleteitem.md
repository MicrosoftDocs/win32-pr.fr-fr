---
title: TVN_DELETEITEM le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle Tree-View qu’un élément est en cours de suppression. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- TVN_DELETEITEM les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9244fd7a848adc3f2d82f48177482c0ffb8cbe1484bc501accfb7ffab3aefbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408245"
---
# <a name="tvn_deleteitem-notification-code"></a>\_Code de notification TVN DELETEITEM

Avertit la fenêtre parente d’un contrôle Tree-View qu’un élément est en cours de suppression. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Le membre **itemOld** est une structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) dont les membres **hitem** et **lParam** contiennent des informations valides sur l’élément en cours de suppression.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Remarques

Si le membre **lParam** de la structure [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) pointe vers la mémoire allouée par votre application, vous pouvez le libérer lorsque vous recevez le code de \_ notification TVN DELETEITEM.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ DELETEITEMW** (Unicode) et **TVN \_ DELETEITEMA** (ANSI)<br/>             |



 

 





