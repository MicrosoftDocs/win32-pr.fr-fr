---
title: Message WM_MOUSELEAVE (winuser. h)
description: Publié dans une fenêtre lorsque le curseur quitte la zone cliente de la fenêtre spécifiée dans un appel antérieur à TrackMouseEvent.
ms.assetid: b23d24ff-531a-4b6d-8848-f82ac5568995
keywords:
- WM_MOUSELEAVE l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_MOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c115ed30da9651167d72bb8c3af604a8444bc0ddcec991df3f76f7a0edee4517
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451449"
---
# <a name="wm_mouseleave-message"></a>\_Message WM MOUSELEAVE

Publié dans une fenêtre lorsque le curseur quitte la zone cliente de la fenêtre spécifiée dans un appel antérieur à [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOUSELEAVE                   0x02A3
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Remarques

Tout le suivi demandé par [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) est annulé lorsque ce message est généré. L’application doit appeler **TrackMouseEvent** quand la souris entre à nouveau dans sa fenêtre si elle nécessite un suivi supplémentaire du comportement de pointage de la souris.

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

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**\_NCMOUSELEAVE WM**](wm-ncmouseleave.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Entrée de la souris](mouse-input.md)
</dt> </dl>

 

