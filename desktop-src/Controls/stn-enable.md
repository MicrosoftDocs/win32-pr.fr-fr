---
title: STN_ENABLE le code de notification (winuser. h)
description: Le STN \_ activer le code de notification est envoyé lorsqu’un contrôle statique est activé.
ms.assetid: daac2ed3-c7cd-46f8-abfa-78754b277ef4
keywords:
- STN_ENABLE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- STN_ENABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc9cc21e884a8a7e907054daa48a21678efa65e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116929"
---
# <a name="stn_enable-notification-code"></a>STN \_ activer le code de notification

Le STN \_ activer le code de notification est envoyé lorsqu’un contrôle statique est activé. Le contrôle statique doit avoir le style [**SS \_ Notify**](static-control-styles.md) pour recevoir ce code de notification. La fenêtre parente du contrôle reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
STN_ENABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle statique. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers le contrôle statique.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[désactivation de STN \_](stn-disable.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Contrôles statiques](static-controls.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

