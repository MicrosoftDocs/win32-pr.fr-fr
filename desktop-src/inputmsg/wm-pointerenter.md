---
title: Message WM_POINTERENTER
description: Envoyé à une fenêtre lorsqu’un nouveau pointeur entre dans la plage de détection sur la fenêtre (survol) ou lorsqu’un pointeur existant se déplace dans les limites de la fenêtre.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8a0222
keywords:
- WM_POINTERENTER les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERENTER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 4d0f6304408514390bb40f2d0e78a766f9e2d118
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510355"
---
# <a name="wm_pointerenter-message"></a>Message WM_POINTERENTER

Envoyé à une fenêtre lorsqu’un nouveau pointeur entre dans la plage de détection sur la fenêtre (survol) ou lorsqu’un pointeur existant se déplace dans les limites de la fenêtre.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Précieuse\]  
> Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERENTER                 0x0249
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Contient l’identificateur du pointeur et les informations supplémentaires. Utilisez les macros suivantes pour récupérer des informations spécifiques dans le paramètre wParam.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : identificateur du pointeur.
-   [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indique si ce message est le premier message généré par un nouveau pointeur entrant la plage de détection (pointage).
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indique si ce message a été généré par un pointeur qui n’a pas la plage de détection restante. Cet indicateur est toujours défini pour les messages de **WM_POINTERENTER** .
-   [**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indicateur qui indique si ce message a été généré par un pointeur qui est en contact. Cet indicateur n’est pas défini pour un pointeur dans la plage de détection (pointage).

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

La notification de **WM_POINTERENTER** peut être utilisée par une fenêtre pour fournir des commentaires à l’utilisateur lorsque le pointeur se trouve sur sa surface, ou réagir à la présence d’un pointeur sur sa surface.

Cette notification est envoyée uniquement à la fenêtre qui reçoit l’entrée pour le pointeur. Le tableau suivant répertorie certaines situations dans lesquelles cette notification est envoyée.



| Action                                                   | Indicateurs définis                                                                                                                                         | Notifications envoyées à                                 |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Un nouveau pointeur entre dans la plage de détection (pointage).            | [**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)<br/> [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)<br/> | Fenêtre sur laquelle le pointeur entre dans la plage de détection. |
| Un pointeur de pointage coupe les limites de la fenêtre. | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)<br/>                                                                      | Fenêtre dans laquelle le pointeur a dépassé.          |



 

> \[! Précieuse\]  
> Quand une fenêtre perd la capture d’un pointeur et qu’elle reçoit la notification [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , elle ne reçoit généralement pas de notifications supplémentaires. Pour cette raison, il est important de ne pas faire de suppositions basées sur des notifications égales [**WM_POINTERDOWN**](wm-pointerdown.md) / [**WM_POINTERUP**](wm-pointerup.md) ou de **WM_POINTERENTER** / [**WM_POINTERLEAVE**](wm-pointerleave.md) des notifications.

 

Lorsque les entrées proviennent de la souris, en raison de l’intégration des messages de souris et de pointeur, **WM_POINTERENTER** n’est pas envoyé.

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

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

