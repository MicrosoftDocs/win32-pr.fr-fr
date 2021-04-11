---
title: CBEN_DRAGBEGIN le code de notification (commctrl. h)
description: Envoyé lorsque l’utilisateur commence à faire glisser l’image de l’élément affiché dans la partie modifiable du contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- Contrôles Windows de code de notification CBEN_DRAGBEGIN
topic_type:
- apiref
api_name:
- CBEN_DRAGBEGIN
- CBEN_DRAGBEGINA
- CBEN_DRAGBEGINW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910e6ac494b49f685a55e77b432e96b4fb22bd29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105757"
---
# <a name="cben_dragbegin-notification-code"></a>\_Code de notification CBEN DRAGBEGIN

Envoyé lorsque l’utilisateur commence à faire glisser l’image de l’élément affiché dans la partie modifiable du contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
CBEN_DRAGBEGIN

    lpnmdb = (LPNMCBEDRAGBEGIN) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) qui contient des informations sur le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

Si l’application réceptrice implémente la fonctionnalité de glisser-déplacer à partir du contrôle, l’application commence l’opération de glisser-déplacer en réponse à ce code de notification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **CBEN \_ DRAGBEGINW** (Unicode) et **CBEN \_ DRAGBEGINA** (ANSI)<br/>             |



 

 





