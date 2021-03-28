---
description: Le \_ message WM DISPLAYCHANGE est envoyé à toutes les fenêtres lorsque la résolution d’affichage a changé.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: Message WM_DISPLAYCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202480"
---
# <a name="wm_displaychange-message"></a>\_Message WM DISPLAYCHANGE

Le message **WM \_ DISPLAYCHANGE** est envoyé à toutes les fenêtres lorsque la résolution d’affichage a changé.

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

Nouvelle profondeur d’image de l’affichage, en bits par pixel.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie la résolution horizontale de l’écran.

Le mot de poids fort spécifie la résolution verticale de l’écran.

</dd> </dl>

## <a name="remarks"></a>Notes

Ce message est envoyé uniquement aux fenêtres de niveau supérieur. Pour toutes les autres fenêtres, il est publié.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

 
