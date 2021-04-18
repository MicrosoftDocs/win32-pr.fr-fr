---
description: La méthode inactive arrête le thread de travail qui extrait les données de la broche de sortie. Cette méthode annule également l’allocation.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: CPullPin. inactive, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533171"
---
# <a name="cpullpininactive-method"></a>CPullPin. inactive, méthode

La `Inactive` méthode arrête le thread de travail qui extrait les données de la broche de sortie. Cette méthode annule également l’allocation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Appelez cette méthode lorsque le filtre propriétaire devient inactif. (Si votre broche d’entrée dérive de [**CBasePin**](cbasepin.md), remplacez la méthode [**CBasePin :: inactive**](cbasepin-inactive.md) .)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




