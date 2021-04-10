---
title: Code de notification NM_HOVER (mode liste) (commctrl. h)
description: Envoyé par un contrôle List-View lorsque la souris pointe sur un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0d4a2eee-9c98-43d1-bc05-226d91c0480a
keywords:
- Contrôles Windows de code de notification NM_HOVER (mode liste)
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60606dfac73e13b0439ce861f37cb4ec941fda3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843077"
---
# <a name="nm_hover-list-view-notification-code"></a>\_Code de notification de pointage nm (mode liste)

Envoyé par un contrôle List-View lorsque la souris pointe sur un élément. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro pour permettre à la vue de liste de traiter le pointage normalement ou une valeur différente de zéro pour empêcher le pointage d’être traité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





