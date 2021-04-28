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
ms.openlocfilehash: afe39f3a7aac155f3cc87fa6d58f402043861d1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099396"
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

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK si le type de média proposé est acceptable. Sinon, retourne S \_ false ou un code d’erreur.

## <a name="remarks"></a>Notes 

La classe dérivée doit substituer cette méthode virtuelle pure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




