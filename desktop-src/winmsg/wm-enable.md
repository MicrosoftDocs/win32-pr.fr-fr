---
description: Envoyé lorsqu’une application modifie l’état activé d’une fenêtre.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: Message WM_ENABLE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e01477de7cf1b9052bba752929210a1bc7553445f81f971aec67d7b510653a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200480"
---
# <a name="wm_enable-message"></a>\_Message d’activation WM

Envoyé lorsqu’une application modifie l’état activé d’une fenêtre. Il est envoyé à la fenêtre dont l’état activé est modifié. Ce message est envoyé avant le retour de la fonction [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) , mais après la modification de l’état activé (le bit de style de [**WS \_ désactivé**](window-styles.md) ) de la fenêtre.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indique si la fenêtre a été activée ou désactivée. Ce paramètre a la **valeur true** si la fenêtre a été activée ou **false** si elle a été désactivée.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la valeur zéro.

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

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
