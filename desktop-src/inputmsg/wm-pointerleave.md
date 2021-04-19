---
title: Message WM_POINTERLEAVE
description: Envoyé à une fenêtre lorsqu’un pointeur quitte la plage de détection sur la fenêtre (pointage) ou lorsqu’un pointeur se déplace à l’extérieur des limites de la fenêtre.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8c1322
keywords:
- WM_POINTERLEAVE les messages d’entrée du message et les notifications
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
ms.openlocfilehash: 2ee58fd74f266d067f6211e156d984a3b3d1c477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511577"
---
# <a name="wm_pointerleave-message"></a>Message WM_POINTERLEAVE

Envoyé à une fenêtre lorsqu’un pointeur quitte la plage de détection sur la fenêtre (pointage) ou lorsqu’un pointeur se déplace à l’extérieur des limites de la fenêtre.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Précieuse\]  
> Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERLEAVE                 0x024A
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Contient l’identificateur du pointeur et des informations supplémentaires. Utilisez les macros suivantes pour récupérer ces informations.

-   [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : identificateur du pointeur.
-   [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam) : indique si ce message a été généré par un pointeur qui n’a pas la plage de détection restante. Cet indicateur n’est pas défini lorsque le pointeur quitte la plage de détection de la fenêtre.
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

La notification **WM_POINTERLEAVE** peut être utilisée par une fenêtre pour modifier le mode ou pour arrêter les commentaires à l’utilisateur lorsque le pointeur se trouve sur l’aire de la fenêtre.

Cette notification est envoyée uniquement à la fenêtre qui reçoit l’entrée pour le pointeur. Le tableau suivant répertorie certaines situations dans lesquelles cette notification est envoyée.



| Action                                        | Indicateurs définis                                                         | Notifications envoyées à                                |
|-----------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------|
| Un pointeur de pointage dépasse les limites de la fenêtre. | [**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api) | Fenêtre en dehors de la limite déplacée par le pointeur.  |
| Un pointeur sort de la plage de détection.        | N/A                                                               | Fenêtre pour laquelle le pointeur quitte la plage de détection. |



 

> \[! Précieuse\]  
> Quand une fenêtre perd la capture d’un pointeur et qu’elle reçoit la notification [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , elle ne reçoit généralement pas de notifications supplémentaires. Pour cette raison, il est important de ne pas faire de suppositions basées sur des notifications égales [**WM_POINTERDOWN**](wm-pointerdown.md) / [**WM_POINTERUP**](wm-pointerup.md) ou de [**WM_POINTERENTER**](wm-pointerenter.md) / **WM_POINTERLEAVE** des notifications.

 

Si le contact est maintenu avec le digitaliseur d’entrée et que le pointeur se déplace à l’extérieur de la fenêtre, **WM_POINTERLEAVE** n’est pas généré. **WM_POINTERLEAVE** est généré uniquement lorsqu’un pointeur de pointage dépasse les limites d’une fenêtre ou si le contact est terminé.

**WM_POINTERLEAVE** est publié dans la file d’attente de messages publiée si l’entrée provient d’une souris.

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

[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

