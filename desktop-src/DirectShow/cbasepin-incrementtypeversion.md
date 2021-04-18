---
description: La méthode IncrementTypeVersion incrémente le numéro de version sur le jeu de types de médias préférés.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: Méthode CBasePin. IncrementTypeVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6db3c08972bebbaf1172c44412ae9c8652100da8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529001"
---
# <a name="cbasepinincrementtypeversion-method"></a>Méthode CBasePin. IncrementTypeVersion

La `IncrementTypeVersion` méthode incrémente le numéro de version sur le jeu de types de médias préférés.

## <a name="syntax"></a>Syntaxe


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode incrémente la variable membre [**CBasePin :: m \_ TypeVersion**](cbasepin-m-typeversion.md) . Si le code PIN modifie dynamiquement la liste des types de média préférés, appelez cette méthode chaque fois que la liste change. Pour plus d’informations, consultez [**CBasePin :: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




