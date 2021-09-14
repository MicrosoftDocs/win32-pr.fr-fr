---
title: Message WM_NCMOUSELEAVE (winuser. h)
description: Publié dans une fenêtre lorsque le curseur quitte la zone non cliente de la fenêtre spécifiée dans un appel antérieur à TrackMouseEvent.
ms.assetid: b3ada6db-93ce-45d7-b408-d08692328aeb
keywords:
- WM_NCMOUSELEAVE l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_NCMOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf7f9d0931c2623d2e92010abfca96f391107b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294183"
---
# <a name="wm_ncmouseleave-message"></a>\_Message WM NCMOUSELEAVE

Publié dans une fenêtre lorsque le curseur quitte la zone non cliente de la fenêtre spécifiée dans un appel antérieur à [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCMOUSELEAVE                 0x02A2
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

## <a name="return-value"></a>Valeur de retour

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Tout le suivi demandé par [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) est annulé lorsque ce message est généré. L’application doit appeler **TrackMouseEvent** quand la souris entre à nouveau dans sa fenêtre si elle nécessite un suivi supplémentaire du comportement de pointage de la souris.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ MOUSELEAVE**](wm-mouseleave.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Entrée de la souris](mouse-input.md)
</dt> </dl>

 

