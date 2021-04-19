---
description: La méthode CompleteConnect notifie la fenêtre que la broche d’entrée du convertisseur a été connectée.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Méthode CBaseWindow. CompleteConnect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 15d5719ab78c3e95cd0128d4075797221af1f4c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528417"
---
# <a name="cbasewindowcompleteconnect-method"></a>Méthode CBaseWindow. CompleteConnect

La `CompleteConnect` méthode notifie la fenêtre que la broche d’entrée du convertisseur a été connectée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode réinitialise l’indicateur d’activation de la fenêtre ([**CBaseWindow :: m \_ bActivated**](cbasewindow-m-bactivated.md)) sur **false**. Lorsqu’un convertisseur vidéo termine une connexion de code confidentiel, il peut appeler la méthode [**CBaseWindow :: ActivateWindow**](cbasewindow-activatewindow.md) pour définir la taille et la position de la fenêtre. Pour forcer **ActivateWindow** à recalculer ces attributs, appelez d’abord la `CompleteConnect` méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




