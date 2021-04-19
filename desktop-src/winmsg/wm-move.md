---
description: Envoyé après qu’une fenêtre a été déplacée.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: Message WM_MOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56004ec47266a50bf2ac82a828b9046c84a8ebfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520577"
---
# <a name="wm_move-message"></a>WM- \_ déplacer un message

Envoyé après qu’une fenêtre a été déplacée.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Coordonnées x et y de l’angle supérieur gauche de la zone cliente de la fenêtre. Le mot de poids faible contient la coordonnée x, tandis que le mot de poids fort contient la coordonnée y.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Les paramètres sont fournis en coordonnées d’écran pour les fenêtres superposées et les fenêtres contextuelles et dans les coordonnées client-parent pour les fenêtres enfants.

L’exemple suivant montre comment obtenir la position à partir du paramètre *lParam* .


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



Vous pouvez également utiliser la macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) pour convertir le paramètre *lParam* en une structure [**points**](/previous-versions//dd162808(v=vs.85)) .

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie les messages de **\_ taille WM** et de **\_ déplacement WM** quand elle traite le message [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) .
Les messages de **\_ taille WM** et de **\_ déplacement WM** ne sont pas envoyés si une application gère le message **WM \_ WINDOWPOSCHANGED** sans appeler **DefWindowProc**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_WINDOWPOSCHANGED WM**](wm-windowposchanged.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**MOMENTS**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

 
