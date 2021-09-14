---
description: 'La méthode EndOfStream indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue. Cette méthode remplace la méthode CBasePin :: EndOfStream.'
ms.assetid: fb5fd8bb-47be-4df6-b837-2c5ff4347478
title: Méthode CRendererInputPin. EndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a8f495c87a86efc9d5625868c7f8fd4afd6ff1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006668"
---
# <a name="crendererinputpinendofstream-method"></a>Méthode CRendererInputPin. EndOfStream

La `EndOfStream` méthode indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue. Cette méthode remplace la méthode [**CBasePin :: EndOfStream**](cbasepin-endofstream.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

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

 

 




