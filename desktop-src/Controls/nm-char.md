---
title: NM_CHAR le code de notification (commctrl. h)
description: Le code de notification de caractère NM \_ est envoyé par un contrôle lorsqu’une touche de caractère est traitée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c35871410244bfb69f67c7e0b2c960d0dd50d432ad9cdcfd8765c7df449bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018947"
---
# <a name="nm_char-notification-code"></a>\_Code de notification de caractère nm

Le code de notification de caractère NM \_ est envoyé par un contrôle lorsqu’une touche de caractère est traitée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) qui contient des informations supplémentaires sur le caractère qui a provoqué le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée par la plupart des contrôles. Pour plus d’informations, consultez la documentation relative aux contrôles individuels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[NM \_ caractère (barre d’outils)](nm-char-toolbar.md)
</dt> </dl>

 

 





