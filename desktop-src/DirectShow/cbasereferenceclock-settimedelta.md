---
description: La méthode SetTimeDelta ajuste l’heure de l’horloge interne.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Méthode CBaseReferenceClock. SetTimeDelta (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac9eba5337fa43e43e3b7a45a7a92263fd4e6d69388185a2096c1a270590e482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403438"
---
# <a name="cbasereferenceclocksettimedelta-method"></a>Méthode CBaseReferenceClock. SetTimeDelta

La `SetTimeDelta` méthode ajuste l’heure de l’horloge interne.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TimeDelta* \[ Réf\]
</dt> <dd>

Montant pour ajuster l’heure de l’horloge, en unités de 100 nanosecondes. Une valeur positive déplace l’avance de l’horloge et une valeur négative déplace l’horloge vers l’arrière.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

La classe dérivée peut utiliser cette méthode pour ajuster l’horloge interne, si elle dérive du périphérique qui fournit des informations de minutage.

La méthode [**CBaseReferenceClock :: getTime**](cbasereferenceclock-gettime.md) ne retourne jamais de valeurs décroissantes. Si vous ajustez l’horloge vers l’arrière, **getTime** retourne la valeur précédente jusqu’à ce que l’horloge atteigne à nouveau cette valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




