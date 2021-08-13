---
title: BN_KILLFOCUS le code de notification (winuser. h)
description: Envoyé lorsqu’un bouton perd le focus clavier. Le bouton doit avoir le \_ style BS Notify pour envoyer ce code de notification. La fenêtre parente du bouton reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- BN_KILLFOCUS les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- BN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f312ba2282c72b7db30c170b44528bd469591bbb0a4b4a2e14bb797d2be67f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674085"
---
# <a name="bn_killfocus-notification-code"></a>\_Code de notification KILLFOCUSy

Envoyé lorsqu’un bouton perd le focus clavier. Le bouton doit avoir le style [**BS \_ Notify**](button-styles.md) pour envoyer ce code de notification.

La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_KILLFOCUS

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

[-e \_ SetFocus](bn-setfocus.md)
</dt> </dl>

 

