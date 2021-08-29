---
description: La méthode GetPin récupère un code confidentiel. La classe CEnumPins appelle cette méthode pour énumérer les codes confidentiels sur le filtre.
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: Méthode CBaseFilter. GetPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 556d4842772ed6c8055a9024a9a6112b466dc9c2fb804321ab605256ece079ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640558"
---
# <a name="cbasefiltergetpin-method"></a>Méthode CBaseFilter. GetPin

La méthode **GetPin** récupère un code confidentiel. La classe [**CEnumPins**](cenumpins.md) appelle cette méthode pour énumérer les codes confidentiels sur le filtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*n* 
</dt> <dd>

Index de base zéro du code confidentiel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’objet [**CBasePin**](cbasepin.md) qui implémente le code confidentiel.

## <a name="remarks"></a>Remarques

Vous devez implémenter cette méthode virtuelle pure dans votre classe dérivée. Retourne un pointeur vers le *n* ième pin sur ce filtre, indexé à partir de zéro. Vous pouvez choisir un ordre d’indexation arbitraire, à condition que l’ordre soit fixe. Si le filtre ajoute ou supprime des broches, ou si le classement change pour une autre raison au moment de l’exécution, appelez la méthode [**CBaseFilter :: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




