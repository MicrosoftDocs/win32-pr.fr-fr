---
title: TVN_SELCHANGED le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle Tree-View que la sélection est passée d’un élément à l’autre. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- TVN_SELCHANGED les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7708d797edebc8c2c0bf43b910aec4dc0a1d6ece1a8a535fdcac57e6b15d6e04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957778"
---
# <a name="tvn_selchanged-notification-code"></a>\_Code de notification TVN SELCHANGED

Avertit une fenêtre parente d’un contrôle Tree-View que la sélection est passée d’un élément à l’autre. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Les membres **itemOld** et **itemNew** de la structure **NMTREEVIEW** sont des structures [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) qui contiennent des informations sur l’élément sélectionné précédemment et l’élément nouvellement sélectionné. Seuls les membres **Mask**, **hitem**, **State** et **lParam** de ces structures sont valides. Les membres **stateMask** des structures **TVITEM** spécifiées par **itemOld** et **itemNew** ne sont pas définis en entrée. Le membre **action** de la structure **NMTREEVIEW** indique le type d’action qui a entraîné la modification de la sélection. Ce peut être l’une des valeurs suivantes :



| Condition requise | Valeur |
|-----------------|-------------------|
| TVC \_ BYKEYBOARD | Par une séquence de touches.   |
| TVC \_ BYMOUSE    | Par un clic de souris. |
| TVC \_ inconnu    | Inconnu.          |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ SELCHANGEDW** (Unicode) et **TVN \_ SELCHANGEDA** (ANSI)<br/>             |



 

 





