---
description: La méthode NewSegment avertit le filtre que les exemples de supports reçus après cet appel sont regroupés en tant que segment.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Méthode CTransformFilter. NewSegment (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd046288886d3e7619419dd591dd94310f56020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543877"
---
# <a name="ctransformfilternewsegment-method"></a>Méthode CTransformFilter. NewSegment

La `NewSegment` méthode notifie le filtre que les exemples de supports reçus après cet appel sont regroupés en tant que segment.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tStart* 
</dt> <dd>

Heure de début du segment, par rapport à la source d’origine.

</dd> <dt>

*tStop* 
</dt> <dd>

Heure d’arrêt du segment, par rapport à la source d’origine.

</dd> <dt>

*dRate* 
</dt> <dd>

Vitesse à laquelle le segment doit être traité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

La méthode [**CTransformInputPin :: NewSegment**](ctransforminputpin-newsegment.md) du code confidentiel d’entrée appelle cette méthode. Cette méthode remet l' `NewSegment` appel à la broche d’entrée en aval.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




