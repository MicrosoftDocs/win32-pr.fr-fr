---
title: Message WM_HSCROLL (winuser. h)
description: Le \_ message WM HSCROLL est envoyé à une fenêtre lorsqu’un événement de défilement se produit dans la barre de défilement horizontale standard de la fenêtre.
ms.assetid: 197e522f-defd-4356-8521-5b5dfda596da
keywords:
- WM_HSCROLL les contrôles de message Windows
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
ms.openlocfilehash: f26eec697e91ee8862912c0f93bcd6e8c4e5c56e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104422"
---
# <a name="wm_hscroll-message"></a>\_Message WM HSCROLL

Le message **WM \_ HSCROLL** est envoyé à une fenêtre lorsqu’un événement de défilement se produit dans la barre de défilement horizontale standard de la fenêtre. Ce message est également envoyé au propriétaire d’un contrôle de barre de défilement horizontale lorsqu’un événement de défilement se produit dans le contrôle.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position actuelle de la case de défilement si le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est SB \_ THUMBPOSITION ou SB \_ THUMBTRACK ; dans le cas contraire, ce mot n’est pas utilisé.

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie une valeur de barre de défilement qui indique la requête de défilement de l’utilisateur. Ce mot peut prendre l’une des valeurs suivantes.



| Valeur                                                                                                                                                                  | Signification                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**\_ENDSCROLL SB**</dt> </dl>             | Termine le défilement.<br/>                                                                                                                                                                                                   |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**SB \_ gauche**</dt> </dl>                            | Fait défiler vers le haut à gauche.<br/>                                                                                                                                                                                     |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**\_droit SB**</dt> </dl>                         | Fait défiler vers le bas à droite.<br/>                                                                                                                                                                                    |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**\_LINELEFT SB**</dt> </dl>                | Fait défiler d’une unité vers la gauche.<br/>                                                                                                                                                                                      |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**\_LINERIGHT SB**</dt> </dl>             | Fait défiler vers la droite d’une unité.<br/>                                                                                                                                                                                     |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**\_PAGELEFT SB**</dt> </dl>                | Fait défiler vers la gauche de la largeur de la fenêtre.<br/>                                                                                                                                                                       |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**\_ÉPINGLÉE SB**</dt> </dl>             | Fait défiler la largeur de la fenêtre vers la droite.<br/>                                                                                                                                                                      |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**\_THUMBPOSITION SB**</dt> </dl> | L’utilisateur a fait glisser la case de défilement (Thumb) et relâché le bouton de la souris. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indique la position de la case de défilement à la fin de l’opération glisser.<br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <dt>**\_THUMBTRACK SB**</dt> </dl>          | L’utilisateur fait glisser la case de défilement. Ce message est envoyé à plusieurs reprises jusqu’à ce que l’utilisateur relâche le bouton de la souris. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indique la position vers laquelle la case de défilement a été déplacée.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Si le message est envoyé par un contrôle de barre de défilement, ce paramètre est le handle du contrôle de barre de défilement. Si le message est envoyé par une barre de défilement standard, ce paramètre a la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Le \_ Code de demande SB THUMBTRACK est généralement utilisé par les applications qui fournissent des commentaires au fur et à mesure que l’utilisateur fait glisser la case de défilement.

Si une application fait défiler le contenu de la fenêtre, elle doit également réinitialiser la position de la case de défilement à l’aide de la fonction [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .

Notez que le message **WM \_ HSCROLL** contient uniquement 16 bits de données de position de la case de défilement. Ainsi, les applications qui reposent uniquement sur **WM \_ HSCROLL** (et [**WM \_ VSCROLL**](wm-vscroll.md)) pour les données de position de défilement ont une valeur de position maximale pratique de 65 535.

Toutefois, étant donné que les fonctions [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)et [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) prennent en charge les données de position de la barre de défilement 32 bits, il existe un moyen de contourner la barrière de 16 bits des messages **WM \_ HSCROLL** et [**WM \_ VSCROLL**](wm-vscroll.md) . Pour obtenir une description de la technique, consultez **GetScrollInfo** .

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

[**WM \_ HSCROLL (TrackBar)**](wm-hscroll--trackbar-.md)
</dt> <dt>

[**\_VSCROLL WM**](wm-vscroll.md)
</dt> </dl>

 

