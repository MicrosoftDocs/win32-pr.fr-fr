---
description: La méthode IsStopped détermine si le filtre contenant ce code PIN est arrêté.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Méthode CBasePin. IsStopped (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64e833ef495ace41a9dcd1614b69e4a081befce0e429fa7aad800a73ce490439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916389"
---
# <a name="cbasepinisstopped-method"></a>Méthode CBasePin. IsStopped

La `IsStopped` méthode détermine si le filtre contenant ce code PIN est arrêté.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsStopped();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le filtre est arrêté. Sinon, retourne **false**.

## <a name="remarks"></a>Remarques

N’appelez pas cette méthode à partir de dans la méthode du constructeur **CBasePin** , car le filtre n’est peut-être pas encore initialisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




