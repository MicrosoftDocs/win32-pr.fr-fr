---
description: Le \_ message WM PRINTCLIENT est envoyé à une fenêtre pour demander qu’il dessine sa zone cliente dans le contexte de périphérique spécifié, le plus souvent dans un contexte de périphérique d’impression.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: Message WM_PRINTCLIENT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807c12ca4d0a5fe5f1e2a12aecd3b3148d936119f72771e811fe85d5b0af3abf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717659"
---
# <a name="wm_printclient-message"></a>\_Message WM PRINTCLIENT

Le message **WM \_ PRINTCLIENT** est envoyé à une fenêtre pour demander qu’il dessine sa zone cliente dans le contexte de périphérique spécifié, le plus souvent dans un contexte de périphérique d’impression.

Contrairement à l' [**\_ impression WM**](wm-print.md), le **WM \_ PRINTCLIENT** n’est pas traité par [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Une fenêtre doit traiter le message **WM \_ PRINTCLIENT** par le biais d’une fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) définie par l’application pour qu’elle soit utilisée correctement.


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

Handle vers le contexte de périphérique dans lequel dessiner.

</dd> <dt>

*lParam* 
</dt> <dd>

Options de dessin. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                  | Signification                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**\_CHECKVISIBLE PRF**</dt> </dl> | Dessine la fenêtre uniquement si elle est visible.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**\_enfants PRF**</dt> </dl>             | Dessine toutes les fenêtres enfants visibles.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**\_client PRF**</dt> </dl>                   | Dessine la zone cliente de la fenêtre.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**\_ERASEBKGND PRF**</dt> </dl>       | Efface l’arrière-plan avant de dessiner la fenêtre.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**PRF non \_ client**</dt> </dl>          | Dessine la zone non cliente de la fenêtre.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**PRF \_ appartenant**</dt> </dl>                      | Dessine toutes les fenêtres détenues.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Une fenêtre peut traiter ce message à peu près de la même façon que la [**\_ peinture WM**](./wm-paint.md), sauf que [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) et [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) ne doivent pas être appelés (un contexte de périphérique est fourni) et que la fenêtre doit dessiner la totalité de la zone client au lieu de simplement la région non valide.

les Windows qui peuvent être utilisées n’importe où dans le système, tels que les contrôles, doivent traiter ce message. Il est probablement utile pour d’autres fenêtres de traiter ce message, car il est relativement facile à implémenter.

La fonction [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) nécessite que la fenêtre animée implémente le message **WM \_ PRINTCLIENT** .

## <a name="requirements"></a>Configuration requise



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

[**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**\_peinture WM**](wm-paint.md)
</dt> </dl>

 

 
