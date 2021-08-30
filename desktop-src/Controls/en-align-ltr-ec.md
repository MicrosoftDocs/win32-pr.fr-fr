---
title: EN_ALIGN_LTR_EC le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur a modifié la direction du contrôle d’édition de gauche à droite. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un \_ message de commande WM.
ms.assetid: 231f9d00-c5a5-445e-9176-201fe1c14a0e
keywords:
- EN_ALIGN_LTR_EC les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_ALIGN_LTR_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d865dc837350644fa3247e2f4769051fd605f9bebcd15f9e053c0c3ff8b126d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047869"
---
# <a name="en_align_ltr_ec-notification-code"></a>En \_ alignant le \_ \_ Code de notification EC LTR

Envoyé lorsque l’utilisateur a modifié la direction du contrôle d’édition de gauche à droite. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ALIGN_LTR_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’édition. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle du contrôle d’édition qui envoie le code de notification.

</dd> </dl>

## <a name="remarks"></a>Remarques

Si une langue bidirectionnelle est installée sur votre système, par exemple en arabe ou en Hébreu, vous pouvez modifier la direction du contrôle d’édition à l’aide de la combinaison de touches CTRL + LSHIFT (de gauche à droite) et CTRL + RSHIFT (de droite à gauche).

**Modification riche :** Ce code de notification n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

