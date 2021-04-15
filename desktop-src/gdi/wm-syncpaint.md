---
description: Le \_ message WM SYNCPAINT est utilisé pour synchroniser la peinture tout en évitant la liaison de threads GUI indépendants.
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: Message WM_SYNCPAINT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991497"
---
# <a name="wm_syncpaint-message"></a>\_Message WM SYNCPAINT

Le message **WM \_ SYNCPAINT** est utilisé pour synchroniser la peinture tout en évitant la liaison de threads GUI indépendants.

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

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application retourne la valeur zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Quand une fenêtre a été masquée, affichée, déplacée ou dimensionnée, le système peut déterminer qu’il est nécessaire d’envoyer un message **WM \_ SYNCPAINT** aux fenêtres de niveau supérieur d’autres threads. Les applications doivent transmettre **WM \_ SYNCPAINT** à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  pour traitement. La fonction **DefWindowProc** envoie un message [**WM \_ NCPAINT**](wm-ncpaint.md) à la procédure de fenêtre si le frame de fenêtre doit être peint et envoie un message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) si l’arrière-plan de la fenêtre doit être effacé.

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

[**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[**\_peinture WM**](wm-paint.md)
</dt> </dl>

 

 
