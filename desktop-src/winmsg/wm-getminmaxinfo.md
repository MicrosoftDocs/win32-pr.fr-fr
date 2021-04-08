---
description: Envoyé à une fenêtre lorsque la taille ou la position de la fenêtre est sur le point de changer. Une application peut utiliser ce message pour remplacer la taille et la position agrandies par défaut de la fenêtre, ou sa taille de suivi minimale ou maximale par défaut.
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: Message WM_GETMINMAXINFO (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866758"
---
# <a name="wm_getminmaxinfo-message"></a>\_Message WM GETMINMAXINFO

Envoyé à une fenêtre lorsque la taille ou la position de la fenêtre est sur le point de changer. Une application peut utiliser ce message pour remplacer la taille et la position agrandies par défaut de la fenêtre, ou sa taille de suivi minimale ou maximale par défaut.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**minmaxinfo,**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) qui contient la position et les dimensions agrandies par défaut, ainsi que les tailles de suivi minimales et maximales par défaut. Une application peut remplacer les valeurs par défaut en définissant les membres de cette structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

La taille maximale de suivi est la plus grande taille de fenêtre qui peut être produite à l’aide des bordures pour dimensionner la fenêtre. La taille de suivi minimale est la plus petite taille de fenêtre qui peut être produite à l’aide des bordures pour dimensionner la fenêtre.

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

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**MINMAXINFO,**](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
