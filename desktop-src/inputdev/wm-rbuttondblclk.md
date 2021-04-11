---
title: Message WM_RBUTTONDBLCLK (winuser. h)
description: Publié lorsque l’utilisateur double-clique avec le bouton droit de la souris alors que le curseur se trouve dans la zone cliente d’une fenêtre.
ms.assetid: 2db9a947-f052-4738-9fae-6ecaba3de9b9
keywords:
- WM_RBUTTONDBLCLK l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_RBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acde97e19b02ad08b3833f1c1c4eb3e0dd4b147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103392"
---
# <a name="wm_rbuttondblclk-message"></a>\_Message WM RBUTTONDBLCLK

Publié lorsque l’utilisateur double-clique avec le bouton droit de la souris alors que le curseur se trouve dans la zone cliente d’une fenêtre. Si la souris n’est pas capturée, le message est publié dans la fenêtre sous le curseur. Dans le cas contraire, le message est publié dans la fenêtre qui a capturé la souris.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_RBUTTONDBLCLK                0x0206
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indique si différentes clés virtuelles sont inactives. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                               | Signification                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle </dl>    | La touche CTRL est enfoncée.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | Le bouton gauche de la souris est enfoncé.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | Le bouton central de la souris est enfoncé.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | Le bouton droit de la souris est enfoncé.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt> </dl>          | La touche Maj est enfoncée.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt> </dl> | Le premier bouton X est enfoncé.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | Le deuxième bouton X est enfoncé.<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie la coordonnée x du curseur. La coordonnée est relative au coin supérieur gauche de la zone cliente.

Le mot de poids fort spécifie la coordonnée y du curseur. La coordonnée est relative au coin supérieur gauche de la zone cliente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Seules les fenêtres qui ont le style **cs \_ DBLCLKS** peuvent recevoir des messages **WM \_ RBUTTONDBLCLK** , que le système génère chaque fois que l’utilisateur appuie sur, relâche, puis appuie encore sur le bouton droit de la souris dans le délai imparti pour le double-clic du système. Le fait de double-cliquer sur le bouton droit de la souris génère en fait quatre messages : [**WM \_ RBUTTONDOWN**](wm-rbuttondown.md), [**WM \_ RBUTTONUP**](wm-rbuttonup.md), **WM \_ RBUTTONDBLCLK** et **WM \_ RBUTTONUP** .

Utilisez le code suivant pour obtenir la position horizontale et verticale :


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses). Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour. Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.

> [!IMPORTANT]
> N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs. Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windowsx. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**Obtient \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**Obtient \_ le \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[**\_RBUTTONDOWN WM**](wm-rbuttondown.md)
</dt> <dt>

[**\_RBUTTONUP WM**](wm-rbuttonup.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Entrée de la souris](mouse-input.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**MOMENTS**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

