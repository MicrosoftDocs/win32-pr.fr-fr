---
title: BN_PAINT le code de notification (winuser. h)
description: Envoyé lorsqu’un bouton doit être peint.
ms.assetid: 1c742272-60bb-42f1-a9b3-974e9a8540cd
keywords:
- BN_PAINT les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- BN_PAINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b4c3a412dac84fb5e65c7feb652588d6f16af0f49a8f61723ba48447dbbb2b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827599"
---
# <a name="bn_paint-notification-code"></a>Code de notification de peinture de l’un \_

Envoyé lorsqu’un bouton doit être peint.

> [!Note]  
> ce code de notification est fourni uniquement pour la compatibilité avec les versions 16 bits de Windows antérieures à la version 3,0. Les applications doivent utiliser le style de bouton [**BS \_ OwnerDraw**](button-styles.md) et la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) pour cette tâche.

 

La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_PAINT

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



 

