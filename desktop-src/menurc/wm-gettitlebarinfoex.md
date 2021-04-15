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
ms.openlocfilehash: fea31326faf5953df0facf34b58b06d7766c2e7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384139"
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

## <a name="remarks"></a>Notes

L’exemple suivant montre comment le récepteur de message convertit une valeur **lParam** pour récupérer la structure [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble des menus](menus.md)
</dt> </dl>

 

