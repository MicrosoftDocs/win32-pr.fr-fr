---
title: EN_ALIGN_RTL_EC le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur a modifié la direction du contrôle d’édition de droite à gauche. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un \_ message de commande WM.
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- EN_ALIGN_RTL_EC les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_ALIGN_RTL_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16b44ecd143715eb5c1bc895ca5c20fa066b17b71ab31ee667e2d6b2b6a0852
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437089"
---
# <a name="en_align_rtl_ec-notification-code"></a>En \_ alignant le \_ \_ Code de notification EC RTL

Envoyé lorsque l’utilisateur a modifié la direction du contrôle d’édition de droite à gauche. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ALIGN_RTL_EC

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

 

