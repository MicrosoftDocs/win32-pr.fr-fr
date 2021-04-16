---
description: Envoyé à une fenêtre après que la fonction SetWindowLong a modifié un ou plusieurs styles de la fenêtre.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: Message WM_STYLECHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5429db06dea95dbbc003e432a2b619c5cf8d056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529835"
---
# <a name="wm_stylechanged-message"></a>\_Message WM STYLECHANGED

Envoyé à une fenêtre après que la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) a modifié un ou plusieurs styles de la fenêtre.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indique si les styles de la fenêtre ou les styles de fenêtre étendus ont changé. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                            | Signification                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_ ExStyle**</dt> <dt>-20</dt> </dl> | Les styles de fenêtre étendus ont changé.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_ STYLE**</dt> <dt>-16</dt> </dl>       | Les styles de fenêtre ont été modifiés.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) qui contient les nouveaux styles pour la fenêtre. Une application peut examiner les styles, mais ne peut pas les modifier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Une application doit retourner zéro si elle traite ce message.

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

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**\_STYLECHANGING WM**](wm-stylechanging.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
