---
description: Le \_ message d’impression WM est envoyé à une fenêtre pour demander qu’il se dessine dans le contexte de périphérique spécifié, le plus souvent dans un contexte de périphérique d’impression.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: Message WM_PRINT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415903"
---
# <a name="wm_print-message"></a>\_Message d’impression WM

Le message d' **\_ impression WM** est envoyé à une fenêtre pour demander qu’il se dessine dans le contexte de périphérique spécifié, le plus souvent dans un contexte de périphérique d’impression.

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

## <a name="remarks"></a>Notes

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) traite ce message en fonction de l’option de dessin spécifiée : si PRF \_ CHECKVISIBLE est spécifié et que la fenêtre n’est pas visible, ne rien faire, si PRF \_ non client est spécifié, dessinez la zone non cliente dans le contexte de périphérique spécifié, si PRF \_ ERASEBKGND est spécifié, envoyez la fenêtre un message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) , si \_ le client PRF est spécifié, envoyez à la fenêtre un message [**WM \_ PRINTCLIENT**](wm-printclient.md) , si les \_ enfants PRF sont définis, envoyer **\_** \_ **\_** un message d’impression WM à chaque fenêtre enfant visible.

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

[**\_ERASEBKGND WM**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**\_PRINTCLIENT WM**](wm-printclient.md)
</dt> </dl>

 

 
