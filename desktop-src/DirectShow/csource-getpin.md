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
ms.openlocfilehash: 4c5b7548eca20f9ec6d9e03d0e708ead1b106f543ca8cac108700c64c9352ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087079"
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
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




