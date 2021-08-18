---
title: Message WM_NCPOINTERDOWN
description: Publié lorsqu’un pointeur effectue un contact sur la zone non cliente d’une fenêtre.
ms.assetid: 3bdc37da-217c-4be1-bf0b-99704bda1322
keywords:
- WM_NCPOINTERDOWN les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_NCPOINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 419af1c613c979d30f479fc0739cd82f01b538f9ff4d3caa63839af8a40b0caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036057"
---
# <a name="wm_ncpointerdown-message"></a>Message WM_NCPOINTERDOWN

Publié lorsqu’un pointeur effectue un contact sur la zone non cliente d’une fenêtre. Le message cible la fenêtre sur laquelle le pointeur effectue un contact. Le pointeur est capturé implicitement dans la fenêtre afin que la fenêtre continue à recevoir l’entrée du pointeur jusqu’à ce qu’il interrompe le contact.

Si une fenêtre a capturé ce pointeur, ce message n’est pas publié. Au lieu de cela, un [**WM_POINTERDOWN**](wm-pointerdown.md) est publié dans la fenêtre qui a capturé ce pointeur.

> \[! Précieuse\]  
> Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_NCPOINTERDOWN                 0x0242
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Contient l’identificateur du pointeur et des informations supplémentaires. Utilisez les macros suivantes pour récupérer ces informations.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : identificateur de pointeur.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam) : valeur de test de positionnement retournée par le traitement du message de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .

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

## <a name="remarks"></a>Remarques

Si l’application ne traite pas ce message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) peut effectuer une ou plusieurs actions système en fonction du résultat du test de positionnement inclus dans le message. En règle générale, les applications ne doivent pas avoir à gérer ce message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages](messages.md)
</dt> </dl>

 

