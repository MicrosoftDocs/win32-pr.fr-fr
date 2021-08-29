---
description: 'La \_ méthode obtenir PrerollTime récupère la quantité de données qui seront placées en file d’attente avant la position de début. Cette méthode implémente la méthode IMediaPosition :: obten \_ PrerollTime.'
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: Méthode CPosPassThru.get_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8323849ddc8f6c4777df1d5a73c84c4c99f51c60b6c76cc81631f0869ed629b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073553"
---
# <a name="cpospassthruget_prerolltime-method"></a>Méthode CPosPassThru. obten \_ PrerollTime

La `get_PrerollTime` méthode récupère la quantité de données qui seront placées en file d’attente avant la position de début. Cette méthode implémente la méthode [**IMediaPosition :: obten \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pllTime* 
</dt> <dd>

Pointeur vers une variable qui reçoit le temps de préroll, en secondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur **HRESULT** de la broche connectée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




