---
description: Envoyé avant le message WM \_ Create lorsqu’une fenêtre est créée pour la première fois.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: Message WM_NCCREATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa5638ef1b97365d202f2049fc79712d0ed3eec167825110f7c7967ce4605c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200055"
---
# <a name="wm_nccreate-message"></a>\_Message WM NCCREATE

Envoyé avant le message [**WM \_ Create**](wm-create.md) lorsqu’une fenêtre est créée pour la première fois.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) qui contient des informations sur la fenêtre en cours de création. Les membres de **CREATESTRUCT** sont identiques aux paramètres de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la **valeur true** pour poursuivre la création de la fenêtre. Si l’application retourne la **valeur false**, la fonction [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) retourne un handle **null** .

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

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**création de WM \_**](wm-create.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
