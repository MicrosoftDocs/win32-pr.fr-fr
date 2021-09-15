---
title: Message WM_TOUCHHITTESTING
description: Envoyé à une fenêtre d’une commande tactile pour déterminer la cible tactile la plus probable.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- WM_TOUCHHITTESTING les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_TOUCHHITTESTING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 83b6e564d692fb0223ec8871b99cefcb9fddf40b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520325"
---
# <a name="wm_touchhittesting-message"></a>Message WM_TOUCHHITTESTING

Envoyé à une fenêtre d’une commande tactile pour déterminer la cible tactile la plus probable.

> \[! Précieuse\]  
> Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_TOUCHHITTESTING       0x024D
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la structure [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) qui contient les données tactiles de la zone de contact.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si un ou plusieurs éléments se trouvent dans la zone de contact tactile, une application doit retourner le résultat de [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).

Si aucun élément ne se trouve dans la zone tactile contact, une application doit définir la valeur de **score** dans [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) sur [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) et appeler [**PACKTOUCHHITTESTINGPROXIMITYEVALUATION**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) pour obtenir la valeur de retour LRESULT.

Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Notes

Ce message est envoyé aux fenêtres qui s’inscrivent via la fonction [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .

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

[**Scores de test d’atteinte tactile**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

