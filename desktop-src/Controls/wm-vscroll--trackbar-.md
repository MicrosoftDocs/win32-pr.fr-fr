---
title: Code de notification WM_VSCROLL (TrackBar. h)
description: Le \_ message WM VSCROLL est envoyé au propriétaire d’un contrôle TrackBar vertical lorsque le curseur change de position. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: E491E210-9605-4ABB-A667-471830DA7C2B
keywords:
- Contrôles Windows du code de notification WM_VSCROLL (TrackBar)
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e13b07fab3335bf99469cd43ed1caa10373a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104416"
---
# <a name="wm_vscroll-trackbar-notification-code"></a>\_Code de notification WM VSCROLL (TrackBar)

Le message **WM \_ VSCROLL** est envoyé au propriétaire d’un contrôle TrackBar vertical lorsque le curseur change de position.

Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position actuelle du curseur si le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est to \_ THUMBPOSITION ou to \_ THUMBTRACK. Pour tous les autres codes de notification, le mot de poids fort est zéro ; Envoyez le message [**TBM \_ GETPOS**](tbm-getpos.md) pour déterminer la position du curseur.

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie un code de notification qui indique l’interaction de l’utilisateur avec le TrackBar. Ce mot peut prendre l’une des valeurs suivantes.



| Valeur                                                                                                                                                                  | Signification                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <dt>**TO \_ bas**</dt> </dl>                      | L’utilisateur a appuyé sur la touche fin ([**VK \_ end**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <dt>**TO \_ ENDTRACK**</dt> </dl>                | Le TrackBar a reçu [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup), ce qui signifie que l’utilisateur a publié une clé qui a envoyé un code de clé virtuelle pertinent. <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <dt>**TO \_ LINEDOWN**</dt> </dl>                | L’utilisateur a appuyé sur la flèche droite ([**VK à \_ droite**](/windows/desktop/inputdev/virtual-key-codes)) ou sur la touche flèche bas ([**VK \_**](/windows/desktop/inputdev/virtual-key-codes)).<br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <dt>**\_programmation to**</dt> </dl>                      | L’utilisateur a appuyé sur la touche de direction gauche ([**VK \_ gauche**](/windows/desktop/inputdev/virtual-key-codes)) ou flèche vers le haut (VK vers le haut).[**\_**](/windows/desktop/inputdev/virtual-key-codes)<br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <dt>**TO \_ PageDown**</dt> </dl>                | L’utilisateur a cliqué sur le canal en dessous ou à droite du curseur ([**VK \_ Next**](/windows/desktop/inputdev/virtual-key-codes)).<br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <dt>**TO \_ PG PRÉC**</dt> </dl>                      | L’utilisateur a cliqué sur le canal au-dessus ou à gauche du curseur ([**VK \_**](/windows/desktop/inputdev/virtual-key-codes)précédemment).<br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <dt>**TO \_ THUMBPOSITION**</dt> </dl> | Le TrackBar a reçu le [**\_ LBUTTONUP WM**](/windows/desktop/inputdev/wm-lbuttonup) qui suit un \_ Code de notification to THUMBTRACK.<br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <dt>**TO \_ THUMBTRACK**</dt> </dl>          | L’utilisateur a fait glisser le curseur.<br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <dt>**TO \_ Top**</dt> </dl>                               | L’utilisateur a appuyé sur la touche début ([**VK \_**](/windows/desktop/inputdev/virtual-key-codes)). <br/>                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle du contrôle TrackBar.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Le \_ code THUMBTRACK to est généralement utilisé par les applications qui fournissent des commentaires au fur et à mesure que l’utilisateur fait glisser la case de défilement.

Notez que le message **WM \_ VSCROLL** contient uniquement 16 bits de données de position. Ainsi, les applications qui reposent uniquement sur **WM \_ VSCROLL** (et [**WM \_ HSCROLL**](wm-hscroll--trackbar-.md)) pour les données de position de curseur ont une valeur de position maximale pratique de 65 535.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_HSCROLL WM**](wm-hscroll--trackbar-.md)
</dt> </dl>

 

