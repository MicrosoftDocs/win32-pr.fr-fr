---
description: 'Méthode CTransInPlaceFilter. GetPin : la méthode GetPin récupère un code confidentiel.'
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Méthode CTransInPlaceFilter. GetPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1075f2a14c58b085b73f2e4283458286c118a7ae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084767"
---
# <a name="ctransinplacefiltergetpin-method"></a>Méthode CTransInPlaceFilter. GetPin

La `GetPin` méthode récupère un code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*n* 
</dt> <dd>

Numéro du code confidentiel spécifié, indexé à partir de zéro. Sur ce filtre, la broche 0 est la broche d’entrée et la broche 1 est la broche de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne un pointeur vers l’objet [**CBasePin**](cbasepin.md) qui implémente le code confidentiel, ou **null** si la méthode échoue.

## <a name="remarks"></a>Notes 

Cette méthode remplace la méthode [**CTransformFilter :: GetPin**](ctransformfilter-getpin.md) . La première fois que la méthode est appelée, elle crée les deux broches.

Cette méthode n’incrémente pas le nombre de références sur le pin retourné, donc le code confidentiel retourné n’a pas de nombre de références en suspens. Si l’appelant doit conserver une référence sur le code confidentiel, il doit appeler la méthode **IUnknown :: AddRef** sur le code confidentiel.

Si le filtre utilise les codes confidentiels par défaut [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) et [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) , vous n’avez probablement pas besoin de substituer cette méthode. Toutefois, si le filtre utilise des codes confidentiels qui étendent ces classes, vous devez substituer cette méthode pour créer des broches de ce type.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




