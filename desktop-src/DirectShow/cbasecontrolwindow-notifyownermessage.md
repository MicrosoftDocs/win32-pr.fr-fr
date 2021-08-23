---
description: La méthode NotifyOwnerMessage transmet des messages spécifiques à la fenêtre vidéo.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Méthode CBaseControlWindow. NotifyOwnerMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d71057027bd8fbd572dffd714f761ff101ba0de95dd42dcf058009b0cb1b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526849"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a>Méthode CBaseControlWindow. NotifyOwnerMessage

La `NotifyOwnerMessage` méthode passe sur des messages spécifiques à la fenêtre vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle vers la fenêtre vidéo.

</dd> <dt>

*uMsg* 
</dt> <dd>

Détails du message.

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

Ne retourne aucune \_ erreur.

## <a name="remarks"></a>Remarques

Quand la fenêtre vidéo est un enfant d’une autre fenêtre, elle ne reçoit pas certains messages de la fenêtre de niveau supérieur. Ces messages peuvent être utiles à un convertisseur, car ils peuvent affecter son comportement. `NotifyOwnerMessage` passe l’un des messages suivants à la fenêtre vidéo.

-   \_ACTIVATEAPP WM
-   \_DEVMODECHANGE WM
-   \_DISPLAYCHANGE WM
-   \_PALETTECHANGED WM
-   \_PALETTEISCHANGING WM
-   \_QUERYNEWPALETTE WM
-   \_SYSCOLORCHANGE WM

Vous pouvez demander à ce que le serveur de distribution de plug-ins [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) devienne l’enfant d’une autre fenêtre. Dans ce cas, le PID recherche certains messages qui peuvent être envoyés à la fenêtre propriétaire. Le PID transmet ensuite ces messages à la fenêtre qui en est propriétaire. Le traitement par défaut des messages consiste à les envoyer de façon synchrone à la procédure de fenêtre appartenant en appelant la fonction Win32 **SendMessage** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




