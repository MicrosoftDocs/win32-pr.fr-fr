---
description: Le \_ message WM NCPAINT est envoyé à une fenêtre quand son frame doit être peint.
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: Message WM_NCPAINT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6c2e211f3dc1602821b0197d295f940606c262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864317"
---
# <a name="wm_ncpaint-message"></a>\_Message WM NCPAINT

Le message **WM \_ NCPAINT** est envoyé à une fenêtre quand son frame doit être peint.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la région de mise à jour de la fenêtre. La région de mise à jour est découpée dans le frame de fenêtre.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application retourne la valeur zéro si elle traite ce message.

## <a name="remarks"></a>Notes

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) peint le cadre de la fenêtre.

Une application peut intercepter le message **WM \_ NCPAINT** et peindre son propre cadre de fenêtre personnalisé. La zone de découpage d’une fenêtre est toujours rectangulaire, même si la forme du cadre est modifiée.

La valeur *wParam* peut être passée à [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) comme dans l’exemple suivant.


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble de la peinture et du dessin](painting-and-drawing.md)
</dt> <dt>

[Peinture et dessin de messages](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**\_peinture WM**](wm-paint.md)
</dt> <dt>

[**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
