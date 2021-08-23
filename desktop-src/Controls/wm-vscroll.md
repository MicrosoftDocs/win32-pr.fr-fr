---
title: Message WM_VSCROLL (winuser. h)
description: Le \_ message WM VSCROLL est envoyé à une fenêtre lorsqu’un événement de défilement se produit dans la barre de défilement verticale standard de la fenêtre.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- WM_VSCROLL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bbb87f63cb0f4801787be1f2cb23b321470b1053a58b13d0f3eea34112b1341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636709"
---
# <a name="wm_vscroll-message"></a>\_Message WM VSCROLL

Le message **WM \_ VSCROLL** est envoyé à une fenêtre lorsqu’un événement de défilement se produit dans la barre de défilement verticale standard de la fenêtre. Ce message est également envoyé au propriétaire d’un contrôle de barre de défilement vertical lorsqu’un événement de défilement se produit dans le contrôle.

Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position actuelle de la case de défilement si le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est SB \_ THUMBPOSITION ou SB \_ THUMBTRACK ; dans le cas contraire, ce mot n’est pas utilisé.

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie une valeur de barre de défilement qui indique la requête de défilement de l’utilisateur. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                  | Signification                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**\_bord inférieur SB**</dt> </dl>                      | Fait défiler vers le bas à droite.<br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**\_ENDSCROLL SB**</dt> </dl>             | Termine le défilement.<br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl>                | Fait défiler d’une ligne vers le dessous.<br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**\_gamme SB**</dt> </dl>                      | Fait défiler d’une ligne vers le haut.<br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PG.**</dt> </dl>                | Fait défiler une page vers le dessous.<br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PG PRÉC**</dt> </dl>                      | Fait défiler d’une page vers le haut.<br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**\_THUMBPOSITION SB**</dt> </dl> | L’utilisateur a fait glisser la case de défilement (Thumb) et relâché le bouton de la souris. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indique la position de la case de défilement à la fin de l’opération glisser.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**\_THUMBTRACK SB**</dt> </dl>          | L’utilisateur fait glisser la case de défilement. Ce message est envoyé à plusieurs reprises jusqu’à ce que l’utilisateur relâche le bouton de la souris. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indique la position vers laquelle la case de défilement a été déplacée.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**haut de la SB \_**</dt> </dl>                               | Fait défiler vers le haut à gauche.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Si le message est envoyé par un contrôle de barre de défilement, ce paramètre est le handle du contrôle de barre de défilement. Si le message est envoyé par une barre de défilement standard, ce paramètre a la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Remarques

Le \_ Code de demande SB THUMBTRACK est généralement utilisé par les applications qui fournissent des commentaires au fur et à mesure que l’utilisateur fait glisser la case de défilement.

Si une application fait défiler le contenu de la fenêtre, elle doit également réinitialiser la position de la case de défilement à l’aide de la fonction [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .

Notez que le message **WM \_ VSCROLL** contient uniquement 16 bits de données de position de la case de défilement. Ainsi, les applications qui reposent uniquement sur **WM \_ VSCROLL** (et [**WM \_ HSCROLL**](wm-hscroll.md)) pour les données de position de défilement ont une valeur de position maximale pratique de 65 535.

Toutefois, étant donné que les fonctions [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)et [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) prennent en charge les données de position de la barre de défilement 32 bits, il existe un moyen de contourner la barrière de 16 bits des messages [**WM \_ HSCROLL**](wm-hscroll.md) et **WM \_ VSCROLL** . Pour obtenir une description de la technique, consultez **GetScrollInfo** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[**\_HSCROLL WM**](wm-hscroll.md)
</dt> <dt>

[**WM \_ VSCROLL (TrackBar)**](wm-vscroll--trackbar-.md)
</dt> </dl>

 

