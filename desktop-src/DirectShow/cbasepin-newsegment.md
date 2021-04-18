---
description: 'La méthode NewSegment avertit le code confidentiel que les exemples de supports reçus après cet appel sont regroupés en tant que segment. Implémente la méthode IPin :: NewSegment.'
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Méthode CBasePin. NewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532879"
---
# <a name="cbasepinnewsegment-method"></a>Méthode CBasePin. NewSegment

La `NewSegment` méthode notifie le code confidentiel que les exemples de supports reçus après cet appel sont regroupés en tant que segment. Implémente la méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tStart* 
</dt> <dd>

Position du média de départ du segment, en unités de 100 nanosecondes.

</dd> <dt>

*tStop* 
</dt> <dd>

Position du média de fin du segment, en unités de 100 nanosecondes.

</dd> <dt>

*dRate* 
</dt> <dd>

Taux auquel ce segment doit être traité, sous la forme d’un pourcentage du taux d’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode définit les variables membres [**CBasePin :: m \_ tStart**](cbasepin-m-tstart.md), [**CBasePin :: m \_ tStop**](cbasepin-m-tstop.md)et [**CBasePin :: m \_ dRate**](cbasepin-m-drate.md) . Dans votre classe dérivée, substituez cette méthode pour passer la notification en aval.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




