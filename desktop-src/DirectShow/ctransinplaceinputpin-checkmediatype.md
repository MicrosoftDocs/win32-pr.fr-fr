---
description: La méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique.
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Méthode CTransInPlaceInputPin. CheckMediaType (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22f271759bc0ade6b820aed2039bbc16a2cf4a31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540379"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a>Méthode CTransInPlaceInputPin. CheckMediaType

La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si le type de média proposé est acceptable. Sinon, retourne S \_ false ou un code d’erreur.

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CTransformInputPin :: CheckMediaType**](ctransforminputpin-checkmediatype.md) . Elle appelle la méthode [**CTransformFilter :: CheckInputType**](ctransformfilter-checkinputtype.md) du filtre pour vérifier le type d’entrée. Si la broche de sortie est connectée, cette méthode appelle également la méthode [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur la broche d’entrée en aval.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceInputPin, classe**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




