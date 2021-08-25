---
description: 'Méthode CBasePin. CheckMediaType : la méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique.'
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Méthode CBasePin. CheckMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c35bcaabcb4a088a5ea1871efe57aefa63175c15588973bc046f51353137994
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916829"
---
# <a name="cbasepincheckmediatype-method"></a>Méthode CBasePin. CheckMediaType

La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si le type de média proposé est acceptable. Sinon, retourne S \_ false ou un code d’erreur.

## <a name="remarks"></a>Remarques

La classe dérivée doit substituer cette méthode virtuelle pure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




