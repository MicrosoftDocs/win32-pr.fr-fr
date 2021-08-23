---
description: 'Méthode CBaseFilter. StreamTime : la méthode StreamTime récupère le temps de flux actuel.'
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Méthode CBaseFilter. StreamTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af266e22cb8ee5a2ff5d5d233dc6cfc623e37cd0d34c073db4dbab71d9c221ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635479"
---
# <a name="cbasefilterstreamtime-method"></a>Méthode CBaseFilter. StreamTime

La méthode **StreamTime** récupère le temps de flux actuel.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rtStream* \[ Réf\]
</dt> <dd>

Référence à un objet [**CRefTime**](creftime.md) qui reçoit le temps de flux actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                      | Description                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>             | Réussite.<br/>                         |
| <dl> <dt>**VFW \_ E \_ pas d' \_ horloge**</dt> </dl> | Aucune horloge de référence n’est disponible.<br/> |



 

## <a name="remarks"></a>Remarques

Le temps de flux est défini comme le temps de référence actuel (comme indiqué par l’horloge de référence) moins l’heure de début (spécifiée par [**CBaseFilter :: m \_ tStart**](cbasefilter-m-tstart.md)). L' *horodatage* d’un exemple de média spécifie l’heure du flux de temps quand il doit être rendu. Si un échantillon dont l’horodatage est inférieur à l’heure actuelle du flux n’a pas encore été affiché, il est tardif.

Cette méthode obtient le temps de flux en appelant [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) pour obtenir le temps de référence actuel, puis en soustrayant l’heure de début initiale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Temps et horloges dans DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




