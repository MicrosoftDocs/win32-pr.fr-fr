---
title: Message WM_KILLFOCUS (winuser. h)
description: Envoyé à une fenêtre juste avant de perdre le focus clavier.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- WM_KILLFOCUS l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644ea7d82a2ae3f316985a882c284d77f3869a75341142d4372b612d66ada1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757453"
---
# <a name="wm_killfocus-message"></a>\_Message WM KILLFOCUS

Envoyé à une fenêtre juste avant de perdre le focus clavier.


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers la fenêtre qui reçoit le focus clavier. Ce paramètre peut être **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Remarques

Si une application affiche un signe insertion, le point d’insertion doit être détruit à ce stade.

Lors du traitement de ce message, n’effectuez pas d’appels de fonction qui affichent ou activent une fenêtre. Cela amène le thread à donner le contrôle et peut entraîner l’arrêt de la réponse de l’application aux messages. Pour plus d’informations, consultez [blocage des messages](/windows/desktop/winmsg/about-messages-and-message-queues).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**WM \_ SetFocus**](wm-setfocus.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

