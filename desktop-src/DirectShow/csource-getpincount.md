---
description: 'La méthode GetPinCount récupère le nombre de broches sur le filtre. Cette méthode implémente la méthode CBaseFilter :: GetPinCount virtuelle pure.'
ms.assetid: 42000814-daee-4f7b-96d2-e09a21fde8cd
title: Méthode CSource. GetPinCount (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 724798d2b13e8e99bb11b50931be8f630413c24f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541035"
---
# <a name="csourcegetpincount-method"></a>Méthode CSource. GetPinCount

La `GetPinCount` méthode récupère le nombre de broches sur le filtre. Cette méthode implémente la méthode [**CBaseFilter :: GetPinCount**](cbasefilter-getpincount.md) virtuelle pure.

## <a name="syntax"></a>Syntaxe


```C++
int GetPinCount();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de broches sur ce filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




