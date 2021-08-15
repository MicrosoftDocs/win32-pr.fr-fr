---
title: Message WM_XBUTTONDBLCLK (winuser. h)
description: Publié lorsque l’utilisateur double-clique sur le premier ou le second bouton X lorsque le curseur se trouve dans la zone cliente d’une fenêtre.
ms.assetid: 68f7abaf-cf6d-499a-957f-3c4d73cdbdee
keywords:
- WM_XBUTTONDBLCLK l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_XBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f15ed64871cee3b5a97ad8067e883d7ad31206896f6b20150acdb490a2f44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757148"
---
# <a name="wm_xbuttondblclk-message"></a>\_Message WM XBUTTONDBLCLK

Publié lorsque l’utilisateur double-clique sur le premier ou le second bouton X lorsque le curseur se trouve dans la zone cliente d’une fenêtre. Si la souris n’est pas capturée, le message est publié dans la fenêtre sous le curseur. Dans le cas contraire, le message est publié dans la fenêtre qui a capturé la souris.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_XBUTTONDBLCLK                0x020D
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le mot de poids faible indique si différentes clés virtuelles sont inactives. Il peut s’agir d’une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                               | Signification                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_**</dt> <dt>0X0008</dt> de contrôle </dl>    | La touche CTRL est enfoncée.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | Le bouton gauche de la souris est enfoncé.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | Le bouton central de la souris est enfoncé.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | Le bouton droit de la souris est enfoncé.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt> </dl>          | La touche Maj est enfoncée.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ LE bouton XButton1**</dt> <dt>0x0020</dt> </dl> | Le premier bouton X est enfoncé.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | Le deuxième bouton X est enfoncé.<br/>     |



 

Le mot de poids fort indique sur quel bouton l’utilisateur a double-cliqué. Il peut avoir l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                     | Signification                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**Le bouton XButton1**</dt> <dt>0x0001</dt> </dl> | L’utilisateur a double-cliqué sur le premier bouton X.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XButton2**</dt> <dt>0x0002</dt> </dl> | L’utilisateur a double-cliqué sur le deuxième bouton X.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie la coordonnée x du curseur. La coordonnée est relative au coin supérieur gauche de la zone cliente.

Le mot de poids fort spécifie la coordonnée y du curseur. La coordonnée est relative au coin supérieur gauche de la zone cliente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la **valeur true**. Pour plus d’informations sur le traitement de la valeur de retour, consultez la section Notes.

## <a name="remarks"></a>Remarques

Utilisez le code suivant pour récupérer les informations dans le paramètre *wParam* :


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



Utilisez le code suivant pour obtenir la position horizontale et verticale :


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses). Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour. Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.

> [!IMPORTANT]
> N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs. Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.

 

Seules les fenêtres qui ont le style **cs \_ DBLCLKS** peuvent recevoir des messages **WM \_ XBUTTONDBLCLK** , que le système génère chaque fois que l’utilisateur appuie sur, relâche, puis appuie à nouveau sur un bouton X dans la limite de temps du double-clic du système. Le fait de double-cliquer sur l’un de ces boutons génère en fait quatre messages : [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md), [**WM \_ XBUTTONUP**](wm-xbuttonup.md), **WM \_ XBUTTONDBLCLK** et **WM \_ XBUTTONUP** .

Contrairement aux [**messages \_ WM LBUTTONDBLCLK**](wm-lbuttondblclk.md), [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md)et [**WM \_ RBUTTONDBLCLK**](wm-rbuttondblclk.md) , une application doit retourner la **valeur true** à partir de ce message si elle le traite. cela permettra aux logiciels qui simulent ce message sur Windows systèmes antérieurs à Windows 2000 de déterminer si la procédure de fenêtre a traité le message ou appelé [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traiter.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Obtient le \_ wParam d’État KEYstate \_**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**Obtient \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**Obtient \_ XBUTTON \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[**Obtient \_ le \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[**\_XBUTTONDOWN WM**](wm-xbuttondown.md)
</dt> <dt>

[**\_XBUTTONUP WM**](wm-xbuttonup.md)
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

 

