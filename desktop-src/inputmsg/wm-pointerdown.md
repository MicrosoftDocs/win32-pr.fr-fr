---
title: Message WM_POINTERDOWN
description: Publié lorsqu’un pointeur effectue un contact sur la zone cliente d’une fenêtre.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- WM_POINTERDOWN les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 051e7f0aa08305e4c38d7eefec94483fd11f3bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104857"
---
# <a name="wm_pointerdown-message"></a>Message WM_POINTERDOWN

Publié lorsqu’un pointeur effectue un contact sur la zone cliente d’une fenêtre. Ce message d’entrée cible la fenêtre sur laquelle le pointeur effectue un contact, et le pointeur est capturé implicitement dans la fenêtre afin que la fenêtre continue de recevoir l’entrée du pointeur jusqu’à ce qu’il interrompe le contact.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Précieuse\]  
> Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Contient des informations sur le pointeur. Utilisez les macros suivantes pour récupérer des informations à partir du paramètre wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : identificateur du pointeur.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique si ce message représente la première entrée générée par un nouveau pointeur.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique si ce message a été généré par un pointeur pendant sa durée de vie. Cet indicateur n’est pas défini sur les messages qui indiquent que le pointeur a quitté la plage de détection
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique si ce message a été généré par un pointeur qui est en contact avec l’aire de la fenêtre. Cet indicateur n’est pas défini sur les messages qui indiquent un pointeur de pointage.
-   [**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indique que ce pointeur a été désigné comme principal.
-   [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique s’il existe une action principale.
    -   Cela équivaut à un bouton gauche de la souris enfoncé.
    -   Un pointeur tactile aura cet ensemble lorsqu’il est en contact avec la surface du digitaliseur.
    -   Un pointeur de stylet aura cet ensemble lorsqu’il est en contact avec la surface du digitaliseur sans bouton enfoncé.
-   [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique s’il existe une action secondaire.
    -   Cela est similaire au bouton droit de la souris.
    -   Un pointeur de stylet aura cet ensemble lorsqu’il est en contact avec la surface du digitaliseur avec le bouton du stylet du stylet enfoncé.
-   [**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique s’il existe une ou plusieurs actions tertiaires en fonction du type de pointeur ; les applications qui souhaitent répondre à des actions tertiaires doivent récupérer des informations spécifiques au type pointeur pour déterminer quels boutons tertiaires sont enfoncés. Par exemple, une application peut déterminer les États des boutons d’un stylet en appelant [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) et en examinant les indicateurs qui spécifient des États de bouton.
-   [**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique si le pointeur spécifié a pris la quatrième action. Les applications qui souhaitent répondre aux quatrièmes actions doivent récupérer des informations spécifiques au type de pointeur pour déterminer si le bouton de la première souris étendue (le bouton XButton1) est enfoncé.
-   [**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : [**indicateur**](pointer-flags-contants.md) qui indique si le pointeur spécifié a pris la cinquième mesure. Les applications qui souhaitent répondre aux cinquièmes actions doivent récupérer des informations spécifiques au type de pointeur pour déterminer si le bouton de la souris étendue (XButton2) est enfoncé.

    Pour plus d’informations, consultez [**indicateurs de pointeur**](pointer-flags-contants.md) .

    > [!Note]  
    > Aucun indicateur de bouton n’est défini pour un pointeur de pointage. Cela est analogue au déplacement de la souris, sans aucun bouton de la souris. Une application peut déterminer les États des boutons d’un stylet de pointage, par exemple, en appelant [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) et en examinant les indicateurs qui spécifient des États de bouton.

     

</dd> <dt>

*lParam* 
</dt> <dd>

Contient l’emplacement du point du pointeur.

> [!Note]  
> Étant donné que le pointeur peut établir un contact avec l’appareil sur une zone non triviale, cet emplacement de point peut être une simplification d’une zone de pointeur plus complexe. Dans la mesure du possible, une application doit utiliser les informations complètes de la zone du pointeur à la place de l’emplacement du point.

 

Utilisez les macros suivantes pour récupérer les coordonnées d’écran physiques du point.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam) : coordonnée X (point horizontal).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam) : coordonnée Y (point vertical).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Notes

> \[! Précieuse\]  
> Quand une fenêtre perd la capture d’un pointeur et qu’elle reçoit la notification [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , elle ne reçoit généralement pas de notifications supplémentaires. Pour cette raison, il est important de ne pas faire de suppositions basées sur des notifications égales **WM_POINTERDOWN** / [**WM_POINTERUP**](wm-pointerup.md) ou de [**WM_POINTERENTER**](wm-pointerenter.md) / [**WM_POINTERLEAVE**](wm-pointerleave.md) des notifications.

 

Chaque pointeur a un identificateur de pointeur unique pendant sa durée de vie. La durée de vie d’un pointeur commence lorsqu’il est détecté pour la première fois.

Un message de [**WM_POINTERENTER**](wm-pointerenter.md) est généré si un pointeur de pointage est détecté. Un **WM_POINTERDOWN** message suivi d’un message **WM_POINTERENTER** est généré si un pointeur sans pointage est détecté.

Pendant sa durée de vie, un pointeur peut générer une série de messages [**WM_POINTERUPDATE**](wm-pointerupdate.md) pendant qu’il pointe ou en contact.

La durée de vie d’un pointeur se termine lorsqu’il n’est plus détecté. Cela génère un message de [**WM_POINTERLEAVE**](wm-pointerleave.md) .

Lorsqu’un pointeur est abandonné, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) est défini.

Un message [**WM_POINTERLEAVE**](wm-pointerleave.md) peut également être généré lorsqu’un pointeur non capturé se déplace en dehors des limites d’une fenêtre.

Pour obtenir la position horizontale et verticale d’un pointeur, utilisez ce qui suit :


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Pour convertir le paramètre lParam en une structure [**points**](/previous-versions//dd162808(v=vs.85)) , utilisez la macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) .

Pour récupérer des informations supplémentaires associées au message, utilisez la fonction [**GetPointerInfo**](/previous-versions/windows/desktop/api) .

Pour déterminer les États des touches de modification du clavier associées à ce message, utilisez la fonction [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) . Par exemple, pour détecter que la touche ALT a été enfoncée, vérifiez si GetKeyState (VK_MENU) &lt; 0.

Notez que si l’application ne traite pas ce message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) peut générer un ou plusieurs messages [**WM_GESTURE**](../wintouch/wm-gesture.md) si la séquence d’entrée de ce et, éventuellement, d’autres pointeurs est reconnue comme un geste. Si un mouvement n’est pas reconnu, **DefWindowProc** peut générer une entrée de souris.

Si une application consomme de manière sélective une entrée de pointeur et passe le reste à [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), le comportement résultant n’est pas défini.

Quand une fenêtre perd la capture d’un pointeur et reçoit la notification [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , elle ne reçoit généralement pas de notifications supplémentaires. Par conséquent, il est important qu’une fenêtre ne fasse pas d’hypothèses sur son état de pointeur, qu’elle reçoive des notifications de mise en paires ou d’entrée/sortie de manière égale.

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment utiliser [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)et [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)pour récupérer les informations pertinentes associées au message **WM_POINTERDOWN** .


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse right button down
}
```



L’exemple de code suivant montre comment utiliser [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) pour récupérer l’ID de pointeur à partir du message **WM_POINTERDOWN** .


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &amp;pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



L’exemple de code suivant montre comment gérer différents types de pointeurs, tels que les périphériques tactiles, Pen ou par défaut.


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &amp;pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &amp;touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &amp;penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &amp;pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&amp;pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages](messages.md)
</dt> <dt>

**Référence**
</dt> <dt>

[**Indicateurs de pointeur**](pointer-flags-contants.md)
</dt> <dt>

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

