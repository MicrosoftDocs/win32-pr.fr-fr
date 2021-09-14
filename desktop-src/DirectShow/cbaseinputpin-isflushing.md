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
ms.openlocfilehash: d5af91e78d10f480596b8e0820ee6de4c4df2998
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223612"
---
# <a name="cbaseinputpinisflushing-method"></a>Méthode CBaseInputPin. IsFlushing

La `IsFlushing` méthode demande si le filtre est en cours de vidage.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsFlushing();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la variable de membre [**CBaseInputPin :: m \_ bFlushing**](cbaseinputpin-m-bflushing.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




