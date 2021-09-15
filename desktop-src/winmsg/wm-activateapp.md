---
description: Envoyé lorsqu’une fenêtre appartenant à une application différente de celle de la fenêtre active va être activée. Le message est envoyé à l’application dont la fenêtre est activée et à l’application dont la fenêtre est désactivée.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: Message WM_ACTIVATEAPP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404715"
---
# <a name="wm_activateapp-message"></a>\_Message WM ACTIVATEAPP

Envoyé lorsqu’une fenêtre appartenant à une application différente de celle de la fenêtre active va être activée. Le message est envoyé à l’application dont la fenêtre est activée et à l’application dont la fenêtre est désactivée.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indique si la fenêtre est activée ou désactivée. Ce paramètre a la **valeur true** si la fenêtre est activée ; la **valeur est false** si la fenêtre est désactivée.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificateur du thread. Si le paramètre *wParam* a la **valeur true**, *lParam* est l’identificateur du thread qui détient la fenêtre désactivée. Si *wParam* a la **valeur false**, *lParam* est l’identificateur du thread qui détient la fenêtre en cours d’activation.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**activation de WM \_**](../inputdev/wm-activate.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
