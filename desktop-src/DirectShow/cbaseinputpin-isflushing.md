---
description: La méthode IsFlushing interroge le fait que le filtre est en cours de vidage.
ms.assetid: 366b6162-7a2c-4882-8774-8b4bf83012b4
title: Méthode CBaseInputPin. IsFlushing (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsFlushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf14abbf20d01f5e78284b65dd1159202146437f2492423c2eaa998a65ee412f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017057"
---
# <a name="cbaseinputpinisflushing-method"></a>Méthode CBaseInputPin. IsFlushing

La `IsFlushing` méthode demande si le filtre est en cours de vidage.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsFlushing();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la variable de membre [**CBaseInputPin :: m \_ bFlushing**](cbaseinputpin-m-bflushing.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




