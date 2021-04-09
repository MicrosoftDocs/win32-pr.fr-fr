---
title: Message WM_CTLCOLORSTATIC (winuser. h)
description: Un contrôle statique, ou un contrôle d’édition qui est en lecture seule ou qui est désactivé, envoie le \_ message WM CTLCOLORSTATIC à sa fenêtre parente lorsque le contrôle va être dessiné.
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- WM_CTLCOLORSTATIC les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851879eeb65a00f95f8cb81cef1b6c23ece8028d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741365"
---
# <a name="wm_ctlcolorstatic-message"></a>\_Message WM CTLCOLORSTATIC

Un contrôle statique, ou un contrôle d’édition qui est en lecture seule ou qui est désactivé, envoie le message **WM \_ CTLCOLORSTATIC** à sa fenêtre parente lorsque le contrôle va être dessiné. En répondant à ce message, la fenêtre parente peut utiliser le handle de contexte de périphérique spécifié pour définir les couleurs de premier plan et d’arrière-plan du texte du contrôle statique.

Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers le contexte de périphérique pour la fenêtre de contrôle statique.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers le contrôle statique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, la valeur de retour est un handle vers un pinceau que le système utilise pour peindre l’arrière-plan du contrôle statique.

## <a name="remarks"></a>Notes

Si l’application retourne un pinceau qu’elle a créée (par exemple, à l’aide de la fonction [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), l’application doit libérer le pinceau. Si l’application retourne un pinceau système (par exemple, un pinceau qui a été récupéré par la fonction [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), l’application n’a pas besoin de libérer le pinceau.

Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sélectionne les couleurs système par défaut pour le contrôle statique.

Vous pouvez définir la couleur d’arrière-plan du texte d’un contrôle d’édition désactivé, mais vous ne pouvez pas définir la couleur de premier plan du texte. Le système utilise toujours la couleur \_ GRAYTEXT.

Les contrôles d’édition qui ne sont pas en lecture seule ou désactivés n’envoient pas le message **WM \_ CTLCOLORSTATIC** ; à la place, ils envoient le message [**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) .

Le message **WM \_ CTLCOLORSTATIC** n’est jamais envoyé entre les threads ; il est envoyé uniquement dans le même thread.

Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en **\_ ptr int** et retourner la valeur directement. Si la procédure de boîte de dialogue retourne la **valeur false**, la gestion des messages par défaut est effectuée. La \_ valeur DWL MSGRESULT définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.

## <a name="examples"></a>Exemples

L’exemple C++ suivant montre comment définir les couleurs de premier plan et d’arrière-plan du texte d’un contrôle statique en réponse au message **WM \_ CTLCOLORSTATIC** . La `hbrBkgnd` variable est une variable **HBRUSH** statique qui est initialisée à la valeur null et stocke le pinceau d’arrière-plan entre les appels à **WM \_ CTLCOLORSTATIC**. Le pinceau doit être détruit par un appel à la fonction [**SupprimerObjet**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) lorsqu’il n’est plus nécessaire, en général lorsque la boîte de dialogue associée est détruite.


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



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

[**\_CTLCOLORBTN WM**](wm-ctlcolorbtn.md)
</dt> <dt>

[**\_CTLCOLOREDIT WM**](wm-ctlcoloredit.md)
</dt> <dt>

[**\_CTLCOLORLISTBOX WM**](wm-ctlcolorlistbox.md)
</dt> <dt>

[**\_CTLCOLORSCROLLBAR WM**](wm-ctlcolorscrollbar.md)
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

 

