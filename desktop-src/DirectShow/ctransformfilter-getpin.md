---
description: 'Méthode CTransformFilter. GetPin : la méthode GetPin récupère un code confidentiel.'
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: Méthode CTransformFilter. GetPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32f9ccdd2b7d787faa6f1081c51bf107b979d26d952552651542afcb34f985ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823919"
---
# <a name="ctransformfiltergetpin-method"></a>Méthode CTransformFilter. GetPin

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

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’objet [**CBasePin**](cbasepin.md) qui implémente le code confidentiel, ou **null** si la méthode échoue.

## <a name="remarks"></a>Remarques

Cette méthode implémente la méthode [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) virtuelle pure. La première fois que la méthode est appelée, elle crée les deux broches.

Cette méthode n’incrémente pas le nombre de références sur le pin retourné, donc le code confidentiel retourné n’a pas de nombre de références en suspens. Si l’appelant doit conserver une référence sur le code confidentiel, il doit appeler la méthode **IUnknown :: AddRef** sur le code confidentiel.

Si le filtre utilise les codes confidentiels par défaut [**CTransformInputPin**](ctransforminputpin.md) et [**CTransformOutputPin**](ctransformoutputpin.md) , vous n’avez probablement pas besoin de substituer cette méthode. Toutefois, si le filtre utilise des codes confidentiels qui étendent ces classes, vous devez substituer cette méthode pour créer des broches de ce type.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




