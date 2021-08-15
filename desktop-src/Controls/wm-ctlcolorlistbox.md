---
title: Message WM_CTLCOLORLISTBOX (winuser. h)
description: Envoyé à la fenêtre parente d’une zone de liste avant que le système ne dessine la zone de liste. En répondant à ce message, la fenêtre parente peut définir les couleurs de texte et d’arrière-plan de la zone de liste à l’aide du handle de contexte de périphérique d’affichage spécifié.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- WM_CTLCOLORLISTBOX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1713c7251dfe837d5796b708fa5b77f0aa5e372c031c251199cb871dbd7c5608
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077663"
---
# <a name="wm_ctlcolorlistbox-message"></a>\_Message WM CTLCOLORLISTBOX

Envoyé à la fenêtre parente d’une zone de liste avant que le système ne dessine la zone de liste. En répondant à ce message, la fenêtre parente peut définir les couleurs de texte et d’arrière-plan de la zone de liste à l’aide du handle de contexte de périphérique d’affichage spécifié.


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers le contexte de périphérique pour la zone de liste.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers la zone de liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner un handle à un pinceau. Le système utilise le pinceau pour peindre l’arrière-plan de la zone de liste.

## <a name="remarks"></a>Remarques

Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sélectionne les couleurs système par défaut pour la zone de liste.

Le message **WM \_ CTLCOLORLISTBOX** n’est jamais envoyé entre les threads. Elle est envoyée uniquement au sein d’un thread.

Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en **\_ ptr int** et retourner la valeur directement. Si la procédure de boîte de dialogue retourne la **valeur false**, la gestion des messages par défaut est effectuée. La valeur **DWL \_ MSGRESULT** définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.

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
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

