---
description: 'La méthode GetPin récupère un code confidentiel. Cette méthode implémente la méthode CBaseFilter :: GetPin virtuelle pure.'
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: Méthode CSource. GetPin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11ff79c9d2d535a3370183b7f36bae25c5e1383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542534"
---
# <a name="csourcegetpin-method"></a>Méthode CSource. GetPin

La `GetPin` méthode récupère un code confidentiel. Cette méthode implémente la méthode [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) virtuelle pure.

## <a name="syntax"></a>Syntaxe


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*n* 
</dt> <dd>

Numéro du code confidentiel spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le pointeur vers l’objet [**CBasePin**](cbasepin.md) qui implémente le code confidentiel, ou **null** si l’index est hors limites.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




