---
title: Message WM_SETFOCUS (winuser. h)
description: Envoyé à une fenêtre après qu’il a obtenu le focus clavier.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- WM_SETFOCUS l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ba202a4f0205a28d294d2d4f54372921205ebb72516f6f26c4042e08d9cfe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757372"
---
# <a name="wm_setfocus-message"></a>\_Message WM SetFocus

Envoyé à une fenêtre après qu’il a obtenu le focus clavier.


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre qui a perdu le focus clavier. Ce paramètre peut être **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Remarques

Pour afficher un signe insertion, une application doit appeler les fonctions de signe insertion appropriées lorsqu’elle reçoit le message **WM \_ SetFocus** .

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

[**\_KILLFOCUS WM**](wm-killfocus.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

