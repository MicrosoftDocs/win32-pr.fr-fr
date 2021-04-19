---
description: La méthode CMediaType. Set (mtype. h) définit le type de média à partir d’un autre type de média. La méthode utilise le paramètre « cmtype ».
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: CMediaType. Set, méthode (mtype. h)-cmtype [ref], paramètre
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bf14132660045afbd171173a38d3ea320ba1aa
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106539931"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a>CMediaType. Set, méthode (mtype. h)-cmtype [ref], paramètre

La `Set` méthode définit le type de média à partir d’un autre type de média.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cmtype* \[ Réf\]
</dt> <dd>

Référence à un objet [**CMediaType**](cmediatype.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette méthode copie l’intégralité du type de média à partir de *cmtype*.

## <a name="requirements"></a>Configuration requise

| Condition requise                   | Valeur                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | Mtype. h (include streams. h)                                                                                     |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




