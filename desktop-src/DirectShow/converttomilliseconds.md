---
description: La fonction ConvertToMilliseconds convertit une durée de référence en millisecondes.
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: ConvertToMilliseconds, fonction (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertToMilliseconds
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e68b84482a437789c620efee7455144905fd33e7b1bdb651df207958ee6befc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073742"
---
# <a name="converttomilliseconds-function"></a>ConvertToMilliseconds fonction)

La `ConvertToMilliseconds` fonction convertit une durée de référence en millisecondes.

## <a name="syntax"></a>Syntaxe


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &RT
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RT* \[ Réf\]
</dt> <dd>

Temps de référence, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la durée de référence convertie en millisecondes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Refclock. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> </dl>

 

 




