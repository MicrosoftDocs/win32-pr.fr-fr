---
title: BN_SETFOCUS le code de notification (winuser. h)
description: Envoyé lorsqu’un bouton reçoit le focus clavier. Le bouton doit avoir le \_ style BS Notify pour envoyer ce code de notification. La fenêtre parente du bouton reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 6b8d9bde-67f9-454f-ba2c-e5c8d9ff2709
keywords:
- BN_SETFOCUS les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- BN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a10cb9b728d6f98f984ff6b70fb76c42102d8414d486cdba3db27b3ac6fbe99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827589"
---
# <a name="bn_setfocus-notification-code"></a>Code de notification de l’e/ \_ SetFocus

Envoyé lorsqu’un bouton reçoit le focus clavier. Le bouton doit avoir le style [**BS \_ Notify**](button-styles.md) pour envoyer ce code de notification.

La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle du bouton.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_KILLFOCUS.](bn-killfocus.md)
</dt> </dl>

 

