---
title: MCN_VIEWCHANGE le code de notification (commctrl. h)
description: Envoyé par un contrôle Month Calendar lorsque l’affichage actuel change. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- MCN_VIEWCHANGE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef04fc370d67f6e6c7a4ef854d542584e170ddd05bf7c12a5135c84e97f33875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799129"
---
# <a name="mcn_viewchange-notification-code"></a>\_Code de notification MCN VIEWCHANGE

Envoyé par un contrôle Month Calendar lorsque l’affichage actuel change. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) qui contient des informations sur la vue actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





