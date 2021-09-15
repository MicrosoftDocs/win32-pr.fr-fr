---
title: Message WM_CAPTURECHANGED (winuser. h)
description: Envoyé à la fenêtre qui perd la capture de la souris.
ms.assetid: 79c8f65e-31fa-4bdb-9e88-0160a52b5b7d
keywords:
- WM_CAPTURECHANGED l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_CAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050bc00a7ab19e22e0fe4ea1f35271707180d4d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530869"
---
# <a name="wm_capturechanged-message"></a>\_Message WM CAPTURECHANGED

Envoyé à la fenêtre qui perd la capture de la souris.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CAPTURECHANGED               0x0215
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la fenêtre qui obtient la capture de la souris.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Une fenêtre reçoit ce message même s’il appelle [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) lui-même. Une application ne doit pas tenter de définir la capture de la souris en réponse à ce message.

Lorsqu’il reçoit ce message, une fenêtre doit se redessiner, si nécessaire, pour refléter le nouvel état de la capture de la souris.

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

[**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Entrée de la souris](mouse-input.md)
</dt> </dl>

 

