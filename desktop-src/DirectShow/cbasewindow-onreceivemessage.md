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
ms.openlocfilehash: 1a5dbfb84edef1f5257cfda8cae08d27b219909f47a7d88fd29580ae12e48b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657962"
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

Handle vers la fenêtre.

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

## <a name="remarks"></a>Remarques

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
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




