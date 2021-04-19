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
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542789"
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

## <a name="remarks"></a>Notes

Le constructeur **CBasePin** Initialise le numéro de version à 1. Dans la classe de base, ce nombre ne change jamais. Si le code PIN change dynamiquement sa liste de types de média préférés, il doit incrémenter le numéro de version chaque fois que la liste change. Pour incrémenter le numéro de version, appelez la méthode [**CBasePin :: IncrementTypeVersion**](cbasepin-incrementtypeversion.md) .

L’énumérateur de type de média, qui est implémenté par la classe [**CEnumMediaTypes**](cenummediatypes.md) , utilise le numéro de version pour rester synchronisé avec le code confidentiel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




