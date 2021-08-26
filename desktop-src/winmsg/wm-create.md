---
description: Envoyé lorsqu’une application demande qu’une fenêtre soit créée en appelant la fonction CreateWindowEx ou CreateWindow.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: Message WM_CREATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ff80c3fe0c12aeaa8b968d2d609fb7d10765c0474ffc001b9b18385e38d149
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931279"
---
# <a name="wm_create-message"></a>\_Créer un message WM

Envoyé lorsqu’une application demande qu’une fenêtre soit créée en appelant la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ou [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) . (Le message est envoyé avant le retour de la fonction.) La procédure de fenêtre de la nouvelle fenêtre reçoit ce message après la création de la fenêtre, mais avant que la fenêtre ne devienne visible.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) qui contient des informations sur la fenêtre en cours de création.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si une application traite ce message, elle doit retourner zéro pour poursuivre la création de la fenêtre. Si l’application retourne-1, la fenêtre est détruite et la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ou [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) retourne un handle **null** .

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

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**\_NCCREATE WM**](wm-nccreate.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
