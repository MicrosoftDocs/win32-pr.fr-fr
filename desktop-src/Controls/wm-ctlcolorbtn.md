---
title: Message WM_CTLCOLORBTN (winuser. h)
description: Le \_ message WM CTLCOLORBTN est envoyé à la fenêtre parente d’un bouton avant de dessiner le bouton. La fenêtre parente peut modifier le texte du bouton et les couleurs d’arrière-plan. Toutefois, seuls les boutons owner-drawn répondent à la fenêtre parente qui traite ce message.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- WM_CTLCOLORBTN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5689d7c76499f1ed180f76831af325c5e311bf06e052ea1446805c39ddf8642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407638"
---
# <a name="wm_ctlcolorbtn-message"></a>\_Message WM CTLCOLORBTN

Le message **WM \_ CTLCOLORBTN** est envoyé à la fenêtre parente d’un bouton avant de dessiner le bouton. La fenêtre parente peut modifier le texte du bouton et les couleurs d’arrière-plan. Toutefois, seuls les boutons owner-drawn répondent à la fenêtre parente qui traite ce message.


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

**HDC** qui spécifie le handle du contexte d’affichage du bouton.

</dd> <dt>

*lParam* 
</dt> <dd>

**HWND** qui spécifie le handle du bouton.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner un handle à un pinceau. Le système utilise le pinceau pour peindre l’arrière-plan du bouton.

## <a name="remarks"></a>Remarques

Si l’application retourne un pinceau qu’elle a créée (par exemple, à l’aide de la fonction [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), l’application doit libérer le pinceau. Si l’application retourne un pinceau système (par exemple, un pinceau qui a été récupéré par la fonction [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), l’application n’a pas besoin de libérer le pinceau.

Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sélectionne les couleurs système par défaut pour le bouton. Les boutons avec les styles- [**\_ PUSHBUTTON BS**](button-styles.md), [**BS \_ DEFPUSHBUTTON**](button-styles.md)ou [**BS \_ PUSHLIKE**](button-styles.md) n’utilisent pas le pinceau retourné. Les boutons avec ces styles sont toujours dessinés avec les couleurs système par défaut. Le dessin de boutons de commande requiert plusieurs pinceaux, mise en surbrillance et ombre, mais le message **WM \_ CTLCOLORBTN** permet de retourner un seul pinceau. Pour fournir une apparence personnalisée pour les boutons de commande, utilisez un bouton owner-drawn. Pour plus d’informations, consultez [création de contrôles Owner-Drawn](user-controls-intro.md).

Le message **WM \_ CTLCOLORBTN** n’est jamais envoyé entre les threads. Elle est envoyée uniquement au sein d’un thread.

La couleur de texte d’une case à cocher ou d’une case d’option s’applique à la zone ou au bouton, à sa coche et au texte. Le rectangle de focus de ces boutons reste la couleur système par défaut (généralement le noir). La couleur de texte d’une zone de groupe s’applique au texte, mais pas à la ligne qui définit la zone. La couleur de texte d’un bouton de commande s’applique uniquement à son rectangle de focus. elle n’affecte pas la couleur du texte.

Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en **\_ ptr int** et retourner la valeur directement. Si la procédure de boîte de dialogue retourne la **valeur false**, la gestion des messages par défaut est effectuée. La \_ valeur DWL MSGRESULT définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Autres ressources**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

