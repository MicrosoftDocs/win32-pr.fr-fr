---
title: Message WM_ACTIVATE (winuser. h)
description: Envoyé à la fenêtre en cours d’activation et à la fenêtre désactivée.
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- WM_ACTIVATE l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413124"
---
# <a name="wm_activate-message"></a>\_Message WM Activate

Envoyé à la fenêtre en cours d’activation et à la fenêtre désactivée. Si les fenêtres utilisent la même file d’attente d’entrée, le message est envoyé de manière synchrone, d’abord à la procédure de fenêtre de la fenêtre de niveau supérieur désactivée, puis à la procédure de fenêtre de la fenêtre de niveau supérieur en cours d’activation. Si les fenêtres utilisent des files d’attente d’entrée différentes, le message est envoyé de manière asynchrone, de sorte que la fenêtre est activée immédiatement.


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le mot de poids faible spécifie si la fenêtre est activée ou désactivée. Ce paramètre peut prendre les valeurs suivantes. Le mot de poids fort spécifie l’État réduit de la fenêtre en cours d’activation ou de désactivation. Une valeur différente de zéro indique que la fenêtre est réduite.



| Valeur                                                                                                                                                                                                                   | Signification                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <dt>**Wa \_ ACTIF**</dt> <dt>1</dt> </dl>                | Activé par une méthode autre qu’un clic de souris (par exemple, par un appel à la fonction [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) ou à l’aide de l’interface clavier pour sélectionner la fenêtre).<br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <dt>**Wa \_ CLICKACTIVE**</dt> <dt>2</dt> </dl> | Activé par un clic de souris.<br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <dt>**Wa \_ Inactif**</dt> <dt>0</dt> </dl>          | Désactivé.<br/>                                                                                                                                                                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la fenêtre en cours d’activation ou de désactivation, selon la valeur du paramètre *wParam* . Si le mot de poids faible de *wParam* est **wa \_ inactif**, *lParam* est le handle de la fenêtre en cours d’activation. Si le mot de poids faible de *wParam* est **wa \_ active** ou **wa \_ CLICKACTIVE**, *lParam* est le handle de la fenêtre désactivée. Ce handle peut être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Si la fenêtre est activée et n’est pas réduite, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) définit le focus clavier sur la fenêtre. Si la fenêtre est activée par un clic de souris, elle reçoit également un message [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[**\_MOUSEACTIVATE WM**](wm-mouseactivate.md)
</dt> <dt>

[**\_NCACTIVATE WM**](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

