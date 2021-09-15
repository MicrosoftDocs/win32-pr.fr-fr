---
title: Message WM_MOUSEWHEEL (winuser. h)
description: Envoyé à la fenêtre de focus lorsque la roulette de la souris est pivotée.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- WM_MOUSEWHEEL l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b918989b41b43c3f54d8ec3133223716e839e58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296419"
---
# <a name="wm_mousewheel-message"></a>\_Message WM MOUSEWHEEL

Envoyé à la fenêtre de focus lorsque la roulette de la souris est pivotée. La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propage le message au parent de la fenêtre. Il ne doit y avoir aucun transfert interne du message, car **DefWindowProc** le propage vers le haut de la chaîne parente jusqu’à ce qu’il trouve une fenêtre qui le traite.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le mot de poids fort indique la distance de rotation de la roue, exprimée en multiples ou divisions de la **roue \_ Delta**, qui est 120. Une valeur positive indique que la roulette a été pivotée vers l’avant, en dehors de l’utilisateur ; une valeur négative indique que la roulette a été retournée vers l’arrière pour l’utilisateur.

Le mot de poids faible indique si différentes clés virtuelles sont inactives. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



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

Le mot de poids faible spécifie la coordonnée x du pointeur, par rapport à l’angle supérieur gauche de l’écran.

Le mot de poids fort spécifie la coordonnée y du pointeur, par rapport à l’angle supérieur gauche de l’écran.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Utilisez le code suivant pour récupérer les informations dans le paramètre *wParam* :


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Utilisez le code suivant pour obtenir la position horizontale et verticale :


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Comme indiqué ci-dessus, la coordonnée x est dans le sens le **plus** bas de la valeur de retour ; la coordonnée y est dans le sens le **plus** élevé (les deux représentent des valeurs *signées* , car elles peuvent accepter des valeurs négatives sur les systèmes avec plusieurs analyses). Si la valeur de retour est assignée à une variable, vous pouvez utiliser la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) pour obtenir une structure de [**points**](/previous-versions//dd162808(v=vs.85)) à partir de la valeur de retour. Vous pouvez également utiliser la macro [**obten \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**obten \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) pour extraire la coordonnée x ou y.

> [!IMPORTANT]
> N’utilisez pas les macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pour extraire les coordonnées x et y de la position du curseur, car ces macros renvoient des résultats incorrects sur les systèmes avec plusieurs moniteurs. Les systèmes avec plusieurs moniteurs peuvent avoir des coordonnées x et y négatives, et **LOWORD** et **HIWORD** traitent les coordonnées comme des quantités non signées.

 

La rotation de la roue est un multiple de la valeur **\_ Delta** de la roue, définie à 120. Il s’agit du seuil d’action à entreprendre, et une telle action (par exemple, le défilement d’un incrément) doit se produire pour chaque Delta.

Le Delta a été défini sur 120 pour permettre à Microsoft ou à d’autres fournisseurs de créer des roues plus fines (une molette à rotation libre sans crans) pour envoyer plus de messages par rotation, mais avec une valeur inférieure dans chaque message. Pour utiliser cette fonctionnalité, vous pouvez ajouter les valeurs Delta entrantes jusqu’à ce que le **\_ Delta** de la roue soit atteint (pour une rotation Delta, vous obteniez la même réponse), ou faire défiler les lignes partielles en réponse aux messages les plus fréquents. Vous pouvez également choisir votre granularité de défilement et accumuler les deltas jusqu’à ce qu’il soit atteint.

Notez qu’il n’existe aucun *fwKeys* pour **MSH \_ MOUSEWHEEL**. Dans le cas contraire, les paramètres sont exactement les mêmes que pour **WM \_ MOUSEWHEEL**.

Il revient à l’application de transférer **MSH \_ MOUSEWHEEL** à tous les objets ou contrôles incorporés. L’application est requise pour envoyer le message à une application OLE incorporée active. Il est facultatif que l’application l’envoie à un contrôle activé pour la roulette avec le focus. Si l’application envoie le message à un contrôle, elle peut vérifier la valeur de retour pour voir si le message a été traité. Les contrôles sont requis pour retourner la valeur **true** s’ils traitent le message.

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

[**Obtient le \_ wParam d’État KEYstate \_**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**Obtient \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**Obtient \_ le \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**Obtient le wParam de la \_ roue \_ \_**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**événement de souris \_**](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Entrée de la souris](mouse-input.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**MOMENTS**](/previous-versions//dd162808(v=vs.85))
</dt> <dt>

[**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

