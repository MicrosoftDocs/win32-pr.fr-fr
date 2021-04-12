---
description: Envoyé lorsqu’une fenêtre est en cours de destruction. Il est envoyé à la procédure de fenêtre de la fenêtre qui est détruite après la suppression de la fenêtre de l’écran.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: Message WM_DESTROY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db195c22c38759146fb76e98edf4ca7f605a1c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203798"
---
# <a name="wm_destroy-message"></a>\_Message de destruction WM

Envoyé lorsqu’une fenêtre est en cours de destruction. Il est envoyé à la procédure de fenêtre de la fenêtre qui est détruite après la suppression de la fenêtre de l’écran.

Ce message est d’abord envoyé à la fenêtre en cours de destruction, puis aux fenêtres enfants (le cas échéant) à mesure qu’elles sont détruites. Pendant le traitement du message, il peut être supposé que toutes les fenêtres enfants existent toujours.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_DESTROY                      0x0002
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Si la fenêtre en cours de destruction fait partie de la chaîne du presse-papiers (définie en appelant la fonction [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) ), la fenêtre doit se supprimer de la chaîne en traitant la fonction [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) avant de retourner le message de **\_ destruction WM** .

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

[**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**\_Fermer WM**](wm-close.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
