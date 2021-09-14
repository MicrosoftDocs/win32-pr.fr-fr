---
description: 'La méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique. Cette méthode remplace la méthode CBasePin :: CheckMediaType.'
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: Méthode CRendererInputPin. CheckMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d3229d1431e45a6177c454f94bf9873aaceaca5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006678"
---
# <a name="crendererinputpincheckmediatype-method"></a>Méthode CRendererInputPin. CheckMediaType

La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique. Cette méthode remplace la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) .

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

Pointeur vers un objet de type de média qui contient le type de média proposé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CRendererInputPin, classe**](crendererinputpin.md)
</dt> </dl>

 

 




