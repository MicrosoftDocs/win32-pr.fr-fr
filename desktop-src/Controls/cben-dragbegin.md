---
title: CBEN_DRAGBEGIN le code de notification (commctrl. h)
description: Envoyé lorsque l’utilisateur commence à faire glisser l’image de l’élément affiché dans la partie modifiable du contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: bdab2700-a605-48af-aee3-bbf573408e3f
keywords:
- CBEN_DRAGBEGIN les contrôles de Windows de code de notification
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123873"
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

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

Si l’application réceptrice implémente la fonctionnalité de glisser-déplacer à partir du contrôle, l’application commence l’opération de glisser-déplacer en réponse à ce code de notification.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **CBEN \_ DRAGBEGINW** (Unicode) et **CBEN \_ DRAGBEGINA** (ANSI)<br/>             |



 

 





