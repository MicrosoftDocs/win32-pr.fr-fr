---
description: La méthode GetMediaTypeVersion récupère un numéro de version pour l’ensemble de types de médias préférés.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Méthode CBasePin. GetMediaTypeVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f1b50b16a099c8698bbf5bef270173334f1c3ac2c3d2d67ff87778cffddf2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955188"
---
# <a name="cbasepingetmediatypeversion-method"></a>Méthode CBasePin. GetMediaTypeVersion

La `GetMediaTypeVersion` méthode récupère un numéro de version pour l’ensemble de types de médias préférés.

## <a name="syntax"></a>Syntaxe


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la variable de membre [**CBasePin :: m \_ TypeVersion**](cbasepin-m-typeversion.md) .

## <a name="remarks"></a>Remarques

Le constructeur **CBasePin** Initialise le numéro de version à 1. Dans la classe de base, ce nombre ne change jamais. Si le code PIN change dynamiquement sa liste de types de média préférés, il doit incrémenter le numéro de version chaque fois que la liste change. Pour incrémenter le numéro de version, appelez la méthode [**CBasePin :: IncrementTypeVersion**](cbasepin-incrementtypeversion.md) .

L’énumérateur de type de média, qui est implémenté par la classe [**CEnumMediaTypes**](cenummediatypes.md) , utilise le numéro de version pour rester synchronisé avec le code confidentiel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




