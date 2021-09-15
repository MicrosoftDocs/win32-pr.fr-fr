---
title: Message WM_NCXBUTTONUP (winuser. h)
description: Publié lorsque l’utilisateur relâche le premier ou le second bouton X lorsque le curseur se trouve dans la zone non cliente d’une fenêtre. Ce message est publié dans la fenêtre qui contient le curseur. Si une fenêtre a capturé la souris, ce message n’est pas publié.
ms.assetid: 07ab5d4e-9912-4867-9146-8abc5addc15d
keywords:
- WM_NCXBUTTONUP l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_NCXBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6330849a433787dd09fad536f005d91f60376013
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523760"
---
# <a name="wm_ncxbuttonup-message"></a>\_Message WM NCXBUTTONUP

Publié lorsque l’utilisateur relâche le premier ou le second bouton X lorsque le curseur se trouve dans la zone non cliente d’une fenêtre. Ce message est publié dans la fenêtre qui contient le curseur. Si une fenêtre a capturé la souris, ce message n’est *pas* publié.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCXBUTTONUP                  0x00AC
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le mot de poids faible spécifie la valeur du test de positionnement retournée par la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) du traitement du message [**WM \_ NCHITTEST**](wm-nchittest.md) . Pour obtenir la liste des valeurs de test de positionnement, consultez **WM \_ NCHITTEST**.

Le mot de poids fort indique le bouton qui a été relâché. Il peut avoir l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                     | Signification                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**Le bouton XButton1**</dt> <dt>0x0001</dt> </dl> | Le premier bouton X a été relâché.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XButton2**</dt> <dt>0x0002</dt> </dl> | Le deuxième bouton X a été relâché.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**points**](/previous-versions//dd162808(v=vs.85)) qui contient les coordonnées x et y du curseur. Les coordonnées sont relatives à l’angle supérieur gauche de l’écran.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une application traite ce message, elle doit retourner la **valeur true**. Pour plus d’informations sur le traitement de la valeur de retour, consultez la section Notes.

## <a name="remarks"></a>Notes

Utilisez le code suivant pour récupérer les informations dans le paramètre *wParam* .


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



Vous pouvez également utiliser le code suivant pour récupérer les coordonnées x et y à partir de *lParam*:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs. Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.

 

Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) teste le point spécifié pour atteindre la position du curseur et effectue l’action appropriée. Le cas échéant, il envoie le message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) à la fenêtre.

Contrairement aux [**messages \_ WM NCLBUTTONUP**](wm-nclbuttonup.md), [**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md)et [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md) , une application doit retourner la **valeur true** à partir de ce message si elle le traite. cela permettra aux logiciels qui simulent ce message sur Windows systèmes antérieurs à Windows 2000 de déterminer si la procédure de fenêtre a traité le message ou appelé [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour le traiter.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Obtient \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**Obtient \_ le \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**\_NCHITTEST WM**](wm-nchittest.md)
</dt> <dt>

[**\_NCXBUTTONDBLCLK WM**](wm-ncxbuttondblclk.md)
</dt> <dt>

[**\_NCXBUTTONDOWN WM**](wm-ncxbuttondown.md)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
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

 

