---
description: La méthode OnReceiveMessage gère les messages de fenêtre.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Méthode CBaseWindow. OnReceiveMessage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: defef9a7ca24d6875eda508989615f308a2385b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540361"
---
# <a name="cbasewindowonreceivemessage-method"></a>Méthode CBaseWindow. OnReceiveMessage

La `OnReceiveMessage` méthode gère les messages de fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de la fenêtre.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificateur du message.

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

Retourne 0 si le message a été traité, ou 1 si le message n’a pas été traité.

## <a name="remarks"></a>Notes

La classe de base gère les messages suivants :

-   \_Fermer WM
-   déplacement de WM \_
-   \_PALETTECHANGED WM
-   \_QUERYNEWPALETTE WM
-   taille du WM \_
-   \_SYSCOLORCHANGE WM

Une classe dérivée peut substituer cette méthode pour gérer d’autres messages. La classe dérivée doit appeler la méthode de la classe de base pour gérer tous les messages ignorés par la classe dérivée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




