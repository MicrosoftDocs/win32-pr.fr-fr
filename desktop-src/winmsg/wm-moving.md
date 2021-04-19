---
description: Envoyé à une fenêtre déplacée par l’utilisateur. En traitant ce message, une application peut surveiller la position du rectangle de glissement et, si nécessaire, modifier sa position.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: Message WM_MOVING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513397"
---
# <a name="wm_moving-message"></a>\_Message de déplacement WM

Envoyé à une fenêtre déplacée par l’utilisateur. En traitant ce message, une application peut surveiller la position du rectangle de glissement et, si nécessaire, modifier sa position.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) avec la position actuelle de la fenêtre, en coordonnées d’écran. Pour modifier la position du rectangle de glissement, une application doit modifier les membres de cette structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Une application doit retourner la **valeur true** si elle traite ce message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**déplacement de WM \_**](wm-move.md)
</dt> <dt>

[**\_dimensionnement WM**](wm-sizing.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
