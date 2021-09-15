---
title: Message WM_PARENTNOTIFY
description: Envoyé à une fenêtre lorsqu’une action importante se produit dans une fenêtre descendante.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- WM_PARENTNOTIFY les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2e19edf25933a035514f9c42b0da6014eccfdb0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519928"
---
# <a name="wm_parentnotify-message"></a>Message WM_PARENTNOTIFY

Envoyé à une fenêtre lorsqu’une action importante se produit dans une fenêtre descendante. Ce message est maintenant étendu pour inclure l’événement [**WM_POINTERDOWN**](wm-pointerdown.md) . Lorsque la fenêtre enfant est créée, le système envoie [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) juste avant la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) qui crée la fenêtre retourne. Lorsque la fenêtre enfant est détruite, le système envoie le message avant tout traitement pour détruire la fenêtre.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Précieuse\]  
> Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le mot de poids faible de *wParam* spécifie l’événement pour lequel le parent est notifié. La valeur du mot de poids fort dépend de la valeur du mot de poids faible. Ce paramètre peut prendre les valeurs suivantes.



| LOWORD (*wParam*)                                                                                                                                                                                                             | Signification                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <dt>**WM_CREATE**</dt> <dt>0x0001</dt> </dl>                | La fenêtre enfant est en cours de création.<br/> HIWORD (*wParam*) est l’identificateur de la fenêtre enfant.<br/> *lParam* est un handle de la fenêtre enfant.<br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <dt>**WM_DESTROY**</dt> <dt>0x0002</dt> </dl>             | La fenêtre enfant est en cours de destruction.<br/> HIWORD (*wParam*) est l’identificateur de la fenêtre enfant.<br/> *lParam* est un handle de la fenêtre enfant.<br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt> </dl> | L’utilisateur a placé le curseur sur la fenêtre enfant et a cliqué sur le bouton gauche de la souris.<br/> HIWORD (*wParam*) n’est pas défini.<br/> *lParam* est la coordonnée x du curseur est le mot de poids faible, et la coordonnée y du curseur est le mot de poids fort.<br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt> </dl> | L’utilisateur a placé le curseur sur la fenêtre enfant et a cliqué sur le bouton central de la souris.<br/> HIWORD (*wParam*) n’est pas défini.<br/> *lParam* est la coordonnée x du curseur est le mot de poids faible, et la coordonnée y du curseur est le mot de poids fort.<br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt> </dl> | L’utilisateur a placé le curseur sur la fenêtre enfant et a cliqué sur le bouton droit de la souris.<br/> HIWORD (*wParam*) n’est pas défini.<br/> *lParam* est la coordonnée x du curseur est le mot de poids faible, et la coordonnée y du curseur est le mot de poids fort.<br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt> </dl> | L’utilisateur a placé le curseur sur la fenêtre enfant et a cliqué sur le premier ou le second bouton X.<br/> HIWORD (*wParam*) indique le bouton qui a été enfoncé. Ce paramètre peut prendre l’une des valeurs suivantes : le bouton XButton1 ou XBUTTON2.<br/> *lParam* est la coordonnée x du curseur est le mot de poids faible, et la coordonnée y du curseur est le mot de poids fort.<br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt> </dl> | Un pointeur a effectué un contact avec la fenêtre enfant.<br/> HIWORD (*wParam*) contient l’identificateur du pointeur qui a généré l’événement [**WM_POINTERDOWN**](wm-pointerdown.md) .<br/>                                                                                                                                                                                            |



 

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

## <a name="return-value"></a>Valeur de retour

Si l’application traite ce message, elle retourne zéro.

Si l’application ne traite pas ce message, elle appelle [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Notes

Ce message est également envoyé à toutes les fenêtres ancêtres de la fenêtre enfant, y compris la fenêtre de niveau supérieur.

Toutes les fenêtres enfants, à l’exception de celles qui ont le **WS_EX_NOPARENTNOTIFY** style de fenêtre étendu, envoient ce message à leurs fenêtres parentes. Par défaut, les fenêtres enfants dans une boîte de dialogue ont le style **WS_EX_NOPARENTNOTIFY** , à moins que la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) soit appelée pour créer la fenêtre enfant sans ce style.

Cette notification fournit aux fenêtres ancêtres de la fenêtre enfant l’opportunité d’examiner les informations de pointeur et, si nécessaire, de capturer le pointeur à l’aide des fonctions de capture de pointeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages](messages.md)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM_CREATE**](../winmsg/wm-create.md)
</dt> <dt>

[**WM_DESTROY**](../winmsg/wm-destroy.md)
</dt> <dt>

[**WM_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[**WM_MBUTTONDOWN**](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[**WM_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[**WM_XBUTTONDOWN**](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

