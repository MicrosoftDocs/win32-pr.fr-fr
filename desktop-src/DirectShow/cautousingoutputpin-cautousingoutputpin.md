---
description: Méthode de constructeur. Le constructeur obtient l’accès au code confidentiel spécifié.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Constructeur CAutoUsingOutputPin. CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296866"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a>Constructeur CAutoUsingOutputPin. CAutoUsingOutputPin

Méthode de constructeur. Le constructeur obtient l’accès au code confidentiel spécifié.

## <a name="syntax"></a>Syntaxe


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pOutputPin* 
</dt> <dd>

Pointeur vers un objet [**CDynamicOutputPin**](cdynamicoutputpin.md) .

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une variable qui contient une valeur **HRESULT** . La valeur doit être \_ OK.

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque la méthode retourne, la valeur de *\* PHR* indique la réussite ou l’échec de la méthode.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAutoUsingOutputPin, classe**](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




