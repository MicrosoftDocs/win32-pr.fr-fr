---
description: Avertit une fenêtre que sa zone non cliente est en cours de destruction. La fonction DestroyWindow envoie le \_ message WM NCDESTROY à la fenêtre qui suit le \_ message WM Destroy.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: Message WM_NCDESTROY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952060"
---
# <a name="wm_ncdestroy-message"></a>\_Message WM NCDESTROY

Avertit une fenêtre que sa zone non cliente est en cours de destruction. La fonction [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) envoie le message **WM \_ NCDESTROY** à la fenêtre qui suit le message [**WM \_ Destroy**](wm-destroy.md) .[**WM \_ Destroy**](wm-destroy.md) est utilisé pour libérer l’objet mémoire alloué associé à la fenêtre.

Le message **WM \_ NCDESTROY** est envoyé une fois que les fenêtres enfants ont été détruites. En revanche, [**WM \_ Destroy**](wm-destroy.md) est envoyé avant la destruction des fenêtres enfants.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCDESTROY                    0x0082
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

Ce message libère toute mémoire allouée de façon interne à la fenêtre.

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

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**\_destructeur WM**](wm-destroy.md)
</dt> <dt>

[**\_NCCREATE WM**](wm-nccreate.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
