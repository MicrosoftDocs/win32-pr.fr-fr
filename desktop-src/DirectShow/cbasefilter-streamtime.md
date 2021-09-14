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
ms.openlocfilehash: f3334ac273a733c3f0591b76af7e76460997a199
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296798"
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

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                      | Description                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>             | Réussite.<br/>                         |
| <dl> <dt>**VFW \_ E \_ pas d' \_ horloge**</dt> </dl> | Aucune horloge de référence n’est disponible.<br/> |



 

## <a name="remarks"></a>Notes

Le temps de flux est défini comme le temps de référence actuel (comme indiqué par l’horloge de référence) moins l’heure de début (spécifiée par [**CBaseFilter :: m \_ tStart**](cbasefilter-m-tstart.md)). L' *horodatage* d’un exemple de média spécifie l’heure du flux de temps quand il doit être rendu. Si un échantillon dont l’horodatage est inférieur à l’heure actuelle du flux n’a pas encore été affiché, il est tardif.

Cette méthode obtient le temps de flux en appelant [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) pour obtenir le temps de référence actuel, puis en soustrayant l’heure de début initiale.

## <a name="requirements"></a>Spécifications



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

 

 




