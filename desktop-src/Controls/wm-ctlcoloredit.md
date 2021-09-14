---
title: Message WM_CTLCOLOREDIT (winuser. h)
description: Un contrôle d’édition qui n’est pas en lecture seule ou qui est désactivé envoie le \_ message WM CTLCOLOREDIT à sa fenêtre parente lorsque le contrôle va être dessiné.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- WM_CTLCOLOREDIT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115185"
---
# <a name="wm_ctlcoloredit-message"></a>\_Message WM CTLCOLOREDIT

Un contrôle d’édition qui n’est pas en lecture seule ou qui est désactivé envoie le message **WM \_ CTLCOLOREDIT** à sa fenêtre parente lorsque le contrôle va être dessiné. En répondant à ce message, la fenêtre parente peut utiliser le handle de contexte de périphérique spécifié pour définir les couleurs de texte et d’arrière-plan du contrôle d’édition.


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle du contexte de périphérique pour la fenêtre de contrôle d’édition.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle du contrôle d’édition.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une application traite ce message, elle doit retourner le handle d’un pinceau. Le système utilise le pinceau pour peindre l’arrière-plan du contrôle d’édition.

## <a name="remarks"></a>Notes

Si l’application retourne un pinceau qu’elle a créée (par exemple, à l’aide de la fonction [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), l’application doit libérer le pinceau. Si l’application retourne un pinceau système (par exemple, un pinceau qui a été récupéré par la fonction [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), l’application n’a pas besoin de libérer le pinceau.

Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sélectionne les couleurs système par défaut pour le contrôle d’édition.

Les contrôles d’édition en lecture seule ou désactivés n’envoient pas le message **WM \_ CTLCOLOREDIT** ; à la place, ils envoient le message [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) .

Le message **WM \_ CTLCOLOREDIT** n’est jamais envoyé entre les threads, il n’est envoyé que dans le même thread.

Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en **\_ ptr int** et retourner la valeur directement. Si la procédure de boîte de dialogue retourne la **valeur false**, la gestion des messages par défaut est effectuée. La \_ valeur DWL MSGRESULT définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.

**Modification riche :** Ce message n’est pas pris en charge. Pour définir la couleur d’arrière-plan d’un contrôle Rich Edit, utilisez le message [**em \_ SETBKGNDCOLOR**](em-setbkgndcolor.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SETBKGNDCOLOR em**](em-setbkgndcolor.md)
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
</dt> </dl>

 

