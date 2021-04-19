---
description: La méthode GetPin récupère un code confidentiel. La classe CEnumPins appelle cette méthode pour énumérer les codes confidentiels sur le filtre.
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: Méthode CBaseFilter. GetPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541152"
---
# <a name="cbasefiltergetpin-method"></a>Méthode CBaseFilter. GetPin

La méthode **GetPin** récupère un code confidentiel. La classe [**CEnumPins**](cenumpins.md) appelle cette méthode pour énumérer les codes confidentiels sur le filtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*n* 
</dt> <dd>

Index de base zéro du code confidentiel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’objet [**CBasePin**](cbasepin.md) qui implémente le code confidentiel.

## <a name="remarks"></a>Notes

Vous devez implémenter cette méthode virtuelle pure dans votre classe dérivée. Retourne un pointeur vers le *n* ième pin sur ce filtre, indexé à partir de zéro. Vous pouvez choisir un ordre d’indexation arbitraire, à condition que l’ordre soit fixe. Si le filtre ajoute ou supprime des broches, ou si le classement change pour une autre raison au moment de l’exécution, appelez la méthode [**CBaseFilter :: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




