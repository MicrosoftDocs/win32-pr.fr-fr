---
description: La méthode OnClose gère les \_ messages de fermeture WM.
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: CBaseWindow. OnClose, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 880e82ca527972b5074ac290fda34ad1c7868a33cbbe1cad12885b56720cef99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635139"
---
# <a name="cbasewindowonclose-method"></a>CBaseWindow. OnClose, méthode

La `OnClose` méthode gère les \_ messages de fermeture WM.

## <a name="syntax"></a>Syntaxe


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true**.

## <a name="remarks"></a>Remarques

Dans la classe de base, cette méthode masque simplement la fenêtre. En règle générale, une classe dérivée remplace cette méthode afin qu’elle envoie également un événement [**EC \_ USERABORT**](ec-userabort.md) . Ne substituez pas la méthode pour détruire la fenêtre. Au lieu de cela, appelez la méthode [**CBaseWindow ::D onewithwindow**](cbasewindow-donewithwindow.md) lorsque le filtre propriétaire est détruit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




