---
title: LVN_ITEMACTIVATE le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View lorsque l’utilisateur active un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- Contrôles Windows de code de notification LVN_ITEMACTIVATE
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106666"
---
# <a name="lvn_itemactivate-notification-code"></a>\_Code de notification LVN ITEMACTIVATE

Envoyé par un contrôle List-View lorsque l’utilisateur active un élément. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

[Version 4,71](common-control-versions.md). Pointeur vers une structure [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) qui contient des informations sur ce code de notification.

[Version 4,70](common-control-versions.md) et versions antérieures. Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur ce code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

L’application recevant ce code de notification doit retourner zéro.

## <a name="remarks"></a>Notes

Pour obtenir les éléments en cours d’activation, l’application réceptrice doit utiliser le message [**\_ GETSELECTEDCOUNT LVM**](lvm-getselectedcount.md) pour récupérer le nombre d’éléments sélectionnés, puis envoyer le [**message \_ GETNEXTITEM LVM**](lvm-getnextitem.md) avec **LVNI \_ sélectionné** jusqu’à ce que tous les éléments aient été récupérés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





