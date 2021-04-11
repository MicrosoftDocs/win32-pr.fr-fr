---
description: Envoyé à la fenêtre la plus affectée au premier plan une fois que la langue d’entrée d’une application a été modifiée. Vous devez apporter des paramètres spécifiques à l’application et transmettre le message à la fonction DefWindowProc, qui le transmet à toutes les fenêtres enfants de premier niveau.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Message WM_INPUTLANGCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112846"
---
# <a name="wm_inputlangchange-message"></a>\_Message WM INPUTLANGCHANGE

Envoyé à la fenêtre la plus affectée au premier plan une fois que la langue d’entrée d’une application a été modifiée. Vous devez apporter des paramètres spécifiques à l’application et transmettre le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , qui le transmet à toutes les fenêtres enfants de premier niveau. Ces fenêtres enfants peuvent transmettre le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pour qu’il transmette le message à leurs fenêtres enfants, et ainsi de suite.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Jeu de caractères des nouveaux paramètres régionaux.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificateur de paramètres régionaux d’entrée. Pour plus d’informations, consultez [langues, paramètres régionaux et dispositions de clavier](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Une application doit retourner une valeur différente de zéro si elle traite ce message.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**\_INPUTLANGCHANGEREQUEST WM**](wm-inputlangchangerequest.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
