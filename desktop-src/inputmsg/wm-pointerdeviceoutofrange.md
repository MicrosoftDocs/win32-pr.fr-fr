---
title: Message WM_POINTERDEVICEOUTOFRANGE
description: Envoyé à une fenêtre lorsqu’un appareil de pointeur a fait l’ensemble de la plage d’un numériseur d’entrée. Ce message contient des informations relatives à l’appareil et à sa proximité.
ms.assetid: 6BC667C1-6D9A-4E69-BAC6-761A1859F09E
keywords:
- WM_POINTERDEVICEOUTOFRANGE les messages d’entrée du message et les notifications
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEOUTOFRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: c222d9a35cae89838d7b6e1d99dcecd11f85b54d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520365"
---
# <a name="wm_pointerdeviceoutofrange-message"></a>Message WM_POINTERDEVICEOUTOFRANGE

Envoyé à une fenêtre lorsqu’un appareil de pointeur a fait l’ensemble de la plage d’un numériseur d’entrée. Ce message contient des informations relatives à l’appareil et à sa proximité.

> \[! Précieuse\]  
> Les applications de bureau doivent prendre en charge DPI. Si votre application n’a pas de prise en charge DPI, les coordonnées d’écran contenues dans les messages de pointeur et les structures associées peuvent apparaître inexactes en raison de la virtualisation DPI. La virtualisation PPP offre une prise en charge de la mise à l’échelle automatique aux applications qui ne prennent pas en charge la fonction PPP et est active par défaut (les utilisateurs peuvent la désactiver). Pour plus d’informations, consultez [écriture d’applications Win32 à haute résolution](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDEVICEOUTOFRANGE       0X23A
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Informations supplémentaires spécifiques au message.

</dd> <dt>

*lParam* 
</dt> <dd>

Informations supplémentaires spécifiques au message.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si l’application traite ce message, elle doit retourner la valeur zéro.

Si l’application ne traite pas ce message, elle doit appeler [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Messages](messages.md)
</dt> </dl>

 

