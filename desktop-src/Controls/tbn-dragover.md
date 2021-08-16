---
title: TBN_DRAGOVER le code de notification (commctrl. h)
description: Vérifie si un \_ message MARKBUTTON to doit être envoyé pour un bouton qui est glissé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718a51f14f096edbd8df72b0c5fc33ca65ec0c303a095f108981482c9fb3cda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829343"
---
# <a name="tbn_dragover-notification-code"></a>\_Code de notification TBN DRAGOVER

Vérifie si un message [**\_ MARKBUTTON to**](tb-markbutton.md) doit être envoyé pour un bouton qui est glissé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) qui spécifie l’élément sur lequel l’élément est glissé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**False** si la barre d’outils doit envoyer un \_ message MARKBUTTON to ; sinon, **true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





