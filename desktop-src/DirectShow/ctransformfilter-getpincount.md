---
description: La méthode GetPinCount récupère le nombre de broches sur le filtre.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Méthode CTransformFilter. GetPinCount (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542694"
---
# <a name="ctransformfiltergetpincount-method"></a>Méthode CTransformFilter. GetPinCount

La `GetPinCount` méthode récupère le nombre de broches sur le filtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne 2.

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBaseFilter :: GetPinCount**](cbasefilter-getpincount.md) . La classe **CTransformFilter** prend en charge exactement une broche d’entrée et une broche de sortie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




