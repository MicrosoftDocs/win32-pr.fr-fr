---
description: 'La \_ méthode obtenir StopTime récupère l’heure à laquelle la lecture s’arrête, par rapport à la durée du flux. Cette méthode implémente la méthode IMediaPosition :: obten \_ StopTime.'
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: Méthode CPosPassThru.get_StopTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 227b054a9737c06e56f7311acc7e0093766608b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532609"
---
# <a name="cpospassthruget_stoptime-method"></a>Méthode CPosPassThru. obten \_ StopTime

La `get_StopTime` méthode récupère l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux. Cette méthode implémente la méthode [**IMediaPosition :: obten \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pllTime* 
</dt> <dd>

Pointeur vers une variable qui reçoit le temps d’arrêt, en secondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur **HRESULT** de la broche connectée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




