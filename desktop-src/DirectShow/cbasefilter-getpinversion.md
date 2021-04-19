---
description: La méthode GetPinVersion récupère un numéro de version pour l’ensemble de broches sur ce filtre.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Méthode CBaseFilter. GetPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8cb2e67f88ef7a02958cc851dd9b8c0c751096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545607"
---
# <a name="cbasefiltergetpinversion-method"></a>Méthode CBaseFilter. GetPinVersion

La `GetPinVersion` méthode récupère un numéro de version pour l’ensemble de broches sur ce filtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la variable de membre [**CBaseFilter :: m \_ PinVersion**](cbasefilter-m-pinversion.md) .

## <a name="remarks"></a>Notes

Le constructeur **CBaseFilter** initialise la version du code confidentiel sur 1. Dans la classe de base, ce nombre ne change jamais. Si le filtre crée ou détruit dynamiquement des épingles, il doit incrémenter la version du code confidentiel chaque fois que les codes confidentiels changent. Pour incrémenter le numéro de version, appelez la méthode [**CBaseFilter :: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .

L’objet d’énumérateur de code confidentiel, qui est implémenté par la classe [**CEnumPins**](cenumpins.md) , utilise la version du code confidentiel pour rester synchronisé avec le filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




