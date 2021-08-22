---
description: La méthode DoneWithWindow détruit la fenêtre.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Méthode CBaseWindow. DoneWithWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6871a42e1a08693a7daf691195b86cd5a41dd208295dc625a33e41083b53adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016667"
---
# <a name="cbasewindowdonewithwindow-method"></a>Méthode CBaseWindow. DoneWithWindow

La `DoneWithWindow` méthode détruit la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Appelez cette méthode à partir de la méthode de destructeur de l’objet dérivé.

Si cette méthode est appelée à partir du même thread que celui qui a créé la fenêtre, la méthode effectue les actions suivantes :

-   Appelle la méthode [**CBaseWindow :: InactivateWindow**](cbasewindow-inactivatewindow.md) , qui désactive la fenêtre.
-   Appelle la méthode [**CBaseWindow :: UninitialiseWindow**](cbasewindow-uninitialisewindow.md) , qui libère les ressources utilisées par la fenêtre.
-   Détruit la fenêtre.

Si le thread appelant `DoneWithWindow` n’est pas le thread qui a créé la fenêtre, la méthode envoie un message « détruire » privé à la fenêtre. Quand la fenêtre reçoit ce message, elle appelle `DoneWithWindow` lui-même. (Si [**CBaseWindow :: m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) a la **valeur true**, la fenêtre publie le message.)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




