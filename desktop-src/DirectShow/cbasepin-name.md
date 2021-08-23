---
description: La méthode Name récupère l’identificateur de code confidentiel.
ms.assetid: 1bc2498f-3f2d-42c7-96cb-9b91bbfb08f5
title: Méthode CBasePin.Name (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Name
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0bb519e67bf1def3abeb98bcfea1310d9b6fe68f06e891e44f925e267982f2e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429879"
---
# <a name="cbasepinname-method"></a>Méthode CBasePin.Name

La `Name` méthode récupère l’identificateur de code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
LPWSTR Name();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la valeur de la variable membre [**CBasePin :: m \_ pname**](cbasepin-m-pname.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




