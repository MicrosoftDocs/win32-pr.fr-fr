---
title: Message WM_NCHITTEST (winuser. h)
description: Envoyé à une fenêtre afin de déterminer quelle partie de la fenêtre correspond à une coordonnée d’écran particulière.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- WM_NCHITTEST l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295459"
---
# <a name="wm_nchittest-message"></a>\_Message WM NCHITTEST

Envoyé à une fenêtre afin de déterminer quelle partie de la fenêtre correspond à une coordonnée d’écran particulière. Cela peut se produire, par exemple, lorsque le curseur se déplace, lorsqu’un bouton de la souris est enfoncé ou relâché, ou en réponse à un appel à une fonction telle que [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint). Si la souris n’est pas capturée, le message est envoyé à la fenêtre située sous le curseur. Dans le cas contraire, le message est envoyé à la fenêtre qui a capturé la souris.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie la coordonnée x du curseur. La coordonnée est relative au coin supérieur gauche de l’écran.

Le mot de poids fort spécifie la coordonnée y du curseur. La coordonnée est relative au coin supérieur gauche de l’écran.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour de la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) est l’une des valeurs suivantes, indiquant la position de la zone réactive du curseur.



| Code/valeur de retour                                                                                                                                    | Description                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**HTBORDER**</dt> <dt>18</dt> </dl>      | Dans la bordure d’une fenêtre qui n’a pas de bordure de redimensionnement.<br/>                                                                                                                                           |
| <dl> <dt>**HTBOTTOM**</dt> <dt>15</dt> </dl>      | Dans la bordure inférieure horizontale d’une fenêtre redimensionnable (l’utilisateur peut cliquer sur la souris pour redimensionner la fenêtre verticalement).<br/>                                                                                    |
| <dl> <dt>**HTBOTTOMLEFT**</dt> <dt>16</dt> </dl>  | Dans le coin inférieur gauche d’une bordure d’une fenêtre redimensionnable (l’utilisateur peut cliquer sur la souris pour redimensionner la fenêtre en diagonale).<br/>                                                                              |
| <dl> <dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt> </dl> | Dans le coin inférieur droit d’une bordure d’une fenêtre redimensionnable (l’utilisateur peut cliquer sur la souris pour redimensionner la fenêtre en diagonale).<br/>                                                                             |
| <dl> <dt>**HTCAPTION**</dt> <dt>2</dt> </dl>      | Dans une barre de titre.<br/>                                                                                                                                                                                         |
| <dl> <dt>**HTCLIENT**</dt> <dt>1</dt> </dl>       | Dans une zone cliente.<br/>                                                                                                                                                                                       |
| <dl> <dt>**HTCLOSE**</dt> <dt>20</dt> </dl>       | Dans un bouton **Fermer** .<br/>                                                                                                                                                                                  |
| <dl> <dt>**HTERROR**</dt> <dt>-2</dt> </dl>       | Sur l’arrière-plan de l’écran ou sur une ligne de séparation entre les fenêtres (identique à **HTNOWHERE**, sauf que la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) génère un bip système pour indiquer une erreur).<br/> |
| <dl> <dt>**HTGROWBOX**</dt> <dt>4</dt> </dl>      | Dans une zone de taille (identique à **HTSIZE**).<br/>                                                                                                                                                                     |
| <dl> <dt>**HTHELP**</dt> <dt>21</dt> </dl>        | Dans un bouton **d’aide** .<br/>                                                                                                                                                                                   |
| <dl> <dt>**HTHSCROLL**</dt> <dt>6</dt> </dl>      | Dans une barre de défilement horizontale.<br/>                                                                                                                                                                             |
| <dl> <dt>**HTLEFT**</dt> <dt>10</dt> </dl>        | Dans la bordure gauche d’une fenêtre redimensionnable (l’utilisateur peut cliquer sur la souris pour redimensionner la fenêtre horizontalement).<br/>                                                                                              |
| <dl> <dt>**HTMENU**</dt> <dt>5</dt> </dl>         | Dans un menu.<br/>                                                                                                                                                                                              |
| <dl> <dt>**HTMAXBUTTON**</dt> <dt>9</dt> </dl>    | Dans un bouton **agrandir** .<br/>                                                                                                                                                                               |
| <dl> <dt>**HTMINBUTTON**</dt> <dt>8</dt> </dl>    | Dans un bouton **réduire** .<br/>                                                                                                                                                                               |
| <dl> <dt>**HTNOWHERE**</dt> <dt>0</dt> </dl>      | Sur l’arrière-plan de l’écran ou sur une ligne de séparation entre les fenêtres.<br/>                                                                                                                                         |
| <dl> <dt>**HTREDUCE**</dt> <dt>8</dt> </dl>       | Dans un bouton **réduire** .<br/>                                                                                                                                                                               |
| <dl> <dt>**HTRIGHT**</dt> <dt>11</dt> </dl>       | Dans la bordure droite d’une fenêtre redimensionnable (l’utilisateur peut cliquer sur la souris pour redimensionner la fenêtre horizontalement).<br/>                                                                                             |
| <dl> <dt>**HTSIZE**</dt> <dt>4</dt> </dl>         | Dans une zone de taille (identique à **HTGROWBOX**).<br/>                                                                                                                                                                  |
| <dl> <dt>**HTSYSMENU**</dt> <dt>3</dt> </dl>      | Dans un menu fenêtre ou dans un bouton **Fermer** dans une fenêtre enfant.<br/>                                                                                                                                            |
| <dl> <dt>**HTTOP**</dt> <dt>12</dt> </dl>         | Dans la bordure supérieure horizontale d’une fenêtre.<br/>                                                                                                                                                             |
| <dl> <dt>**HTTOPLEFT**</dt> <dt>13</dt> </dl>     | Dans l’angle supérieur gauche d’une bordure de fenêtre.<br/>                                                                                                                                                            |
| <dl> <dt>**HTTOPRIGHT**</dt> <dt>14</dt> </dl>    | Dans l’angle supérieur droit d’une bordure de fenêtre.<br/>                                                                                                                                                           |
| <dl> <dt>**HTTRANSPARENT**</dt> <dt>-1</dt> </dl> | Dans une fenêtre actuellement couverte par une autre fenêtre dans le même thread (le message est envoyé aux fenêtres sous-jacentes dans le même thread jusqu’à ce que l’un d’eux retourne un code qui n’est pas **HTTRANSPARENT**).<br/>  |
| <dl> <dt>**HTVSCROLL**</dt> <dt>7</dt> </dl>      | Dans la barre de défilement verticale.<br/>                                                                                                                                                                             |
| <dl> <dt>**HTZOOM**</dt> <dt>9</dt> </dl>         | Dans un bouton **agrandir** .<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Notes

Utilisez le code suivant pour obtenir la position horizontale et verticale :


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses). Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour. Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.

> [!IMPORTANT]
> N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs. Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.

 

**Windows Vista :** Lorsque vous créez des frames personnalisés qui incluent les boutons de légende standard, ce message doit d’abord être transmis à la fonction [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) . Cela permet à l’Gestionnaire de fenêtrage (DWM) de fournir des tests de positionnement pour les boutons de légende. Si **DwmDefWindowProc** ne gère pas le message, un traitement supplémentaire de **WM \_ NCHITTEST** peut être nécessaire.

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

 

