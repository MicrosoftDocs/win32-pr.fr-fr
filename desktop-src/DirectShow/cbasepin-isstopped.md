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
ms.openlocfilehash: 4185c02b396f7d0d570081ba1401e0ec9e301d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525640"
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

## <a name="remarks"></a>Notes

N’appelez pas cette méthode à partir de dans la méthode du constructeur **CBasePin** , car le filtre n’est peut-être pas encore initialisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




