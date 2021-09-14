---
description: Envoyé à une fenêtre lorsque la fonction SetWindowLong est sur le paragraphe de la modification d’un ou plusieurs styles de la fenêtre.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: Message WM_STYLECHANGING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e587797404bb361a443a60750d4de5ea6a8924
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219740"
---
# <a name="wm_stylechanging-message"></a>\_Message WM STYLECHANGING

Envoyé à une fenêtre lorsque la fonction [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) est sur le paragraphe de la modification d’un ou plusieurs styles de la fenêtre.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indique si les styles de la fenêtre ou les styles de fenêtre étendus sont modifiés. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                            | Signification                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_ ExStyle**</dt> <dt>-20</dt> </dl> | Les styles de fenêtre étendus sont modifiés.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_ STYLE**</dt> <dt>-16</dt> </dl>       | Les styles de fenêtre changent.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) qui contient les nouveaux styles proposés pour la fenêtre. Une application peut examiner les styles et, si nécessaire, les modifier.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **LRESULT**

Une application doit retourner zéro si elle traite ce message.

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

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**\_STYLECHANGED WM**](wm-stylechanged.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
