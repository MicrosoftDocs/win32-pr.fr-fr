---
title: Message WM_GETTITLEBARINFOEX (winuser. h)
description: Envoyé pour demander des informations étendues de barre de titre. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1acbe85afa1871caf796c70a9535f5646d2511317a0e9ee0564db55101a16449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869665"
---
# <a name="wm_gettitlebarinfoex-message"></a>\_Message WM GETTITLEBARINFOEX

Envoyé pour demander des informations étendues de barre de titre. Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) . L’expéditeur du message est chargé d’allouer de la mémoire pour cette structure. Affectez au membre **cbSize** de cette structure la valeur `sizeof(TITLEBARINFOEX)` avant de passer cette structure avec le message.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’exemple suivant montre comment le récepteur de message convertit une valeur **lParam** pour récupérer la structure [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble des menus](menus.md)
</dt> </dl>

 

