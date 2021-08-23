---
description: La méthode PossiblyEatMessage transfère les messages du clavier et de la souris à la fenêtre drain de message.
ms.assetid: 8e344c5d-2f94-454f-89b7-45c539b6e833
title: Méthode CBaseControlWindow. PossiblyEatMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403fb4d170f9c3cf0b7d68d3ac6ce1fdcc9c81a14b1c76d74e67bb64d4d9cc8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017337"
---
# <a name="cbasecontrolwindowpossiblyeatmessage-method"></a>Méthode CBaseControlWindow. PossiblyEatMessage

La `PossiblyEatMessage` méthode transfère les messages du clavier et de la souris à la fenêtre drain de message.

## <a name="syntax"></a>Syntaxe


```C++
BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uMsg* 
</dt> <dd>

Message de fenêtre.

</dd> <dt>

*wParam* 
</dt> <dd>

Premier paramètre de message.

</dd> <dt>

*lParam* 
</dt> <dd>

Deuxième paramètre de message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le message a été transféré à la fenêtre, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

La fenêtre drain de message est une fenêtre conçue pour recevoir certains messages de souris et de clavier. Initialement, la fenêtre a la **valeur null**; Il peut être défini en appelant [**CBaseControlWindow ::p ut \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md).

Si la fenêtre drain de message n’a pas la **valeur null**, `PossiblyEatMessage` publie les messages suivants dans cette fenêtre :

-   \_caractère WM
-   \_DEADCHAR WM
-   WM- \_ touche
-   WM \_ KEYUP
-   \_LBUTTONDBLCLK WM
-   \_LBUTTONDOWN WM
-   \_LBUTTONUP WM
-   \_MBUTTONDBLCLK WM
-   \_MBUTTONDOWN WM
-   \_MBUTTONUP WM
-   \_MOUSEACTIVATE WM
-   WM \_ MOUSEMOVE
-   \_NCLBUTTONDBLCLK WM
-   \_NCLBUTTONDOWN WM
-   \_NCLBUTTONUP WM
-   \_NCMBUTTONDBLCLK WM
-   \_NCMBUTTONDOWN WM
-   \_NCMBUTTONUP WM
-   \_NCMOUSEMOVE WM
-   \_NCRBUTTONDBLCLK WM
-   \_NCRBUTTONDOWN WM
-   \_NCRBUTTONUP WM
-   \_RBUTTONDBLCLK WM
-   \_RBUTTONDOWN WM
-   \_RBUTTONUP WM
-   \_SYSCHAR WM
-   \_SYSDEADCHAR WM
-   \_SYSKEYDOWN WM
-   \_SYSKEYUP WM

Elle ignore les autres messages. Si la fenêtre d’écoulement de message est **null**, la méthode ignore tous les messages de fenêtre. La méthode retourne la **valeur true** si elle publie le message, ou **false** dans le cas contraire. La classe **CBaseWindow** appelle cette méthode lorsqu’elle reçoit un message de fenêtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




