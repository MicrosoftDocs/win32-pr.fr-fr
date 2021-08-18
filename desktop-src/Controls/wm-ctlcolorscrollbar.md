---
title: Message WM_CTLCOLORSCROLLBAR (winuser. h)
description: Le \_ message WM CTLCOLORSCROLLBAR est envoyé à la fenêtre parente d’un contrôle de barre de défilement lorsque le contrôle va être dessiné.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- WM_CTLCOLORSCROLLBAR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35dba3394c3d8fd99fef88d6fa1869ea1129d95ae8a82cc33f2935e5688871a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018557"
---
# <a name="wm_ctlcolorscrollbar-message"></a>\_Message WM CTLCOLORSCROLLBAR

Le message **WM \_ CTLCOLORSCROLLBAR** est envoyé à la fenêtre parente d’un contrôle de barre de défilement lorsque le contrôle va être dessiné. En répondant à ce message, la fenêtre parente peut utiliser le handle de contexte d’affichage pour définir la couleur d’arrière-plan du contrôle de barre de défilement.

Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers le contexte de périphérique pour le contrôle de barre de défilement.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la barre de défilement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner le handle à un pinceau. Le système utilise le pinceau pour peindre l’arrière-plan du contrôle de barre de défilement.

## <a name="remarks"></a>Remarques

Si l’application retourne un pinceau qu’elle a créée (par exemple, à l’aide de la fonction [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), l’application doit libérer le pinceau. Si l’application retourne un pinceau système (par exemple, un pinceau qui a été récupéré par la fonction [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), l’application n’a pas besoin de libérer le pinceau.

Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sélectionne les couleurs système par défaut pour le contrôle de barre de défilement.

Le message **WM \_ CTLCOLORSCROLLBAR** n’est jamais envoyé entre les threads ; il n’est envoyé que dans le même thread.

Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en **\_ ptr int** et retourner la valeur directement. Si la procédure de boîte de dialogue retourne la **valeur false**, la gestion des messages par défaut est effectuée. La \_ valeur DWL MSGRESULT définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.

Le message **WM \_ CTLCOLORSCROLLBAR** est utilisé uniquement par les contrôles de barre de défilement enfants. Les barres de défilement attachées à une fenêtre (WS \_ Scroll et WS \_ VSCROLL) ne génèrent pas ce message. Pour personnaliser l’apparence des barres de défilement attachées à une fenêtre, utilisez les fonctions de barre de défilement plat.

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

[**\_CTLCOLORBTN WM**](wm-ctlcolorbtn.md)
</dt> <dt>

[**\_CTLCOLOREDIT WM**](wm-ctlcoloredit.md)
</dt> <dt>

[**\_CTLCOLORLISTBOX WM**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**\_CTLCOLORSTATIC WM**](wm-ctlcolorstatic.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**\_CTLCOLORDLG WM**](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

