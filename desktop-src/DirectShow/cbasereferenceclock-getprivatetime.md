---
description: La méthode GetPrivateTime récupère le temps réel à partir de l’horloge.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Méthode CBaseReferenceClock. GetPrivateTime (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8381f6e6e868fc6a57a65cf3bf124d90c035c854176265b2f9991356874e0ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076499"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a>Méthode CBaseReferenceClock. GetPrivateTime

La `GetPrivateTime` méthode récupère le temps réel à partir de l’horloge.

## <a name="syntax"></a>Syntaxe


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’heure actuelle de l’horloge, en unités de 100 nanosecondes.

## <a name="remarks"></a>Remarques

Cette méthode retourne le temps réel signalé par l’horloge. Les appelants externes utilisent la méthode [**CBaseReferenceClock :: getTime**](cbasereferenceclock-gettime.md) , qui appelle cette méthode. Contrairement à la méthode **getTime** , l’horloge interne est autorisée à revenir en arrière. Si cela se produit, la méthode **getTime** continue à retourner la dernière fois qu’elle a rapporté, jusqu’à ce que la `GetPrivateTime` méthode détecte.

Cette méthode retourne l’heure système. Substituez cette méthode si votre horloge obtient l’heure d’une autre source.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




