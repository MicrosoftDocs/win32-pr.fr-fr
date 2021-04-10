---
description: Envoyé à une fenêtre dont la taille, la position ou l’emplacement dans l’ordre de plan a été modifié à la suite d’un appel à la fonction SetWindowPos ou à une autre fonction de gestion de fenêtre.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: Message WM_WINDOWPOSCHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112842"
---
# <a name="wm_windowposchanged-message"></a>\_Message WM WINDOWPOSCHANGED

Envoyé à une fenêtre dont la taille, la position ou l’emplacement dans l’ordre de plan a été modifié à la suite d’un appel à la fonction [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) ou à une autre fonction de gestion de fenêtre.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) qui contient des informations sur les nouvelles taille et position de la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envoie les messages de [**\_ taille WM**](wm-size.md) et de [**\_ déplacement WM**](wm-move.md) à la fenêtre. Les messages de **\_ taille WM** et de **\_ déplacement WM** ne sont pas envoyés si une application gère le message **WM \_ WINDOWPOSCHANGED** sans appeler **DefWindowProc**. Il est plus efficace d’effectuer un traitement des modifications de déplacement ou de taille pendant le message **WM \_ WINDOWPOSCHANGED** sans appeler **DefWindowProc**.

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

[**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**déplacement de WM \_**](wm-move.md)
</dt> <dt>

[**taille du WM \_**](wm-size.md)
</dt> <dt>

[**\_WINDOWPOSCHANGING WM**](wm-windowposchanging.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
