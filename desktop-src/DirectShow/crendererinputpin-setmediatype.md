---
description: 'La méthode SetMediaType définit le type de média pour la connexion. Cette méthode remplace la méthode CBasePin :: SetMediaType.'
ms.assetid: b2668bb1-0739-413c-bea8-ec5541acfb3e
title: Méthode CRendererInputPin. SetMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f248e15c3965305719269a19a1f2ff2c8feddfe0e57b6349985d9133e38789
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054399"
---
# <a name="crendererinputpinsetmediatype-method"></a>Méthode CRendererInputPin. SetMediaType

La `SetMediaType` méthode définit le type de média pour la connexion. Cette méthode remplace la méthode [**CBasePin :: SetMediaType**](cbasepin-setmediatype.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CRendererInputPin, classe**](crendererinputpin.md)
</dt> </dl>

 

 




