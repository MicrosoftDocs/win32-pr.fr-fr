---
title: Message WM_LBUTTONUP (winuser. h)
description: Publié lorsque l’utilisateur relâche le bouton gauche de la souris alors que le curseur se trouve dans la zone cliente d’une fenêtre.
ms.assetid: 6efa298f-85f7-40ab-a64b-16b5071f2437
keywords:
- WM_LBUTTONUP l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_LBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe921ffe68359efe15aa0782c5c8543fd0870fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413103"
---
# <a name="wm_lbuttonup-message"></a>\_Message WM LBUTTONUP

Publié lorsque l’utilisateur relâche le bouton gauche de la souris alors que le curseur se trouve dans la zone cliente d’une fenêtre. Si la souris n’est pas capturée, le message est publié dans la fenêtre sous le curseur. Dans le cas contraire, le message est publié dans la fenêtre qui a capturé la souris.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_LBUTTONUP                    0x0202
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indique si différentes clés virtuelles sont inactives. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                               | Signification                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle </dl>    | La touche CTRL est enfoncée.<br/>            |
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

## <a name="return-value"></a>Valeur de retour

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Utilisez le code suivant pour obtenir la position horizontale et verticale :


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur lParam ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses). Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour. Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.

> [!IMPORTANT]
> N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs. Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.

 

## <a name="requirements"></a>Spécifications



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

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**\_LBUTTONDBLCLK WM**](wm-lbuttondblclk.md)
</dt> <dt>

[**\_LBUTTONDOWN WM**](wm-lbuttondown.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Entrée de la souris](mouse-input.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**MOMENTS**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

