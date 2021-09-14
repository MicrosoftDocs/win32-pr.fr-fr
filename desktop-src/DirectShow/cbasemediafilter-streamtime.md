---
description: 'Méthode CBaseMediaFilter. StreamTime : la méthode StreamTime récupère le temps de flux actuel.'
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Méthode CBaseMediaFilter. StreamTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a90bb7d97825c14f11c75dd42d696fa302f8e3d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239244"
---
# <a name="cbasemediafilterstreamtime-method"></a>Méthode CBaseMediaFilter. StreamTime

La `StreamTime` méthode récupère le temps de flux actuel.

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

Le temps de flux est défini comme le temps de référence actuel (comme indiqué par l’horloge de référence) moins l’heure de début (spécifiée par [**CBaseMediaFilter :: m \_ tStart**](cbasemediafilter-m-tstart.md)). L’horodatage d’un exemple de média spécifie l’heure du flux de temps quand il doit être rendu. Si un échantillon dont l’horodatage est inférieur à l’heure actuelle du flux n’a pas encore été affiché, il est tardif.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseMediaFilter, classe**](cbasemediafilter.md)
</dt> </dl>

 

 




