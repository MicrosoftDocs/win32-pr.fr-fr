---
title: BN_KILLFOCUS le code de notification (winuser. h)
description: Envoyé lorsqu’un bouton perd le focus clavier. Le bouton doit avoir le \_ style BS Notify pour envoyer ce code de notification. La fenêtre parente du bouton reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- Contrôles Windows de code de notification BN_KILLFOCUS
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
ms.openlocfilehash: c3fb6737d88ccddedbba6db58ffd0f713da7a8a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464666"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[-e \_ SetFocus](bn-setfocus.md)
</dt> </dl>

 

