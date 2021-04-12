---
description: Envoyé lorsque l’arrière-plan de la fenêtre doit être effacé (par exemple, lorsqu’une fenêtre est redimensionnée). Le message est envoyé pour préparer une partie invalidée d’une fenêtre pour la peinture.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: Message WM_ERASEBKGND (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203797"
---
# <a name="wm_erasebkgnd-message"></a>\_Message WM ERASEBKGND

Envoyé lorsque l’arrière-plan de la fenêtre doit être effacé (par exemple, lorsqu’une fenêtre est redimensionnée). Le message est envoyé pour préparer une partie invalidée d’une fenêtre pour la peinture.


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers le contexte de périphérique (Device Context).

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Une application doit retourner une valeur différente de zéro si elle efface l’arrière-plan ; Sinon, elle doit retourner zéro.

## <a name="remarks"></a>Notes

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) efface l’arrière-plan à l’aide du pinceau d’arrière-plan de classe spécifié par le membre **hbrBackground** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) . Si **hbrBackground** a la **valeur null**, l’application doit traiter le message **WM \_ ERASEBKGND** et effacer l’arrière-plan.

Une application doit retourner une valeur différente de zéro en réponse à **WM \_ ERASEBKGND** si elle traite le message et efface l’arrière-plan. cela indique qu’aucune suppression supplémentaire n’est requise. Si l’application retourne la valeur zéro, la fenêtre reste marquée pour l’effacement. (En général, cela indique que le membre **fErase** de la structure [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) est **true**.)

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

[**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Icônes](../menurc/icons.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
