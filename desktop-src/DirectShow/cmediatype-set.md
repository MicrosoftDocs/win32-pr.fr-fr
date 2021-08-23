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
ms.openlocfilehash: 0a317b23b4870ad6e68032ed23f846a81019be358974ebbe75e2a5859db71303
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585879"
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

## <a name="remarks"></a>Remarques

Cette méthode copie l’intégralité du type de média à partir de *cmtype*.

## <a name="requirements"></a>Configuration requise

| Condition requise                   | Valeur                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | Mtype. h (include Flux. h)                                                                                     |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




