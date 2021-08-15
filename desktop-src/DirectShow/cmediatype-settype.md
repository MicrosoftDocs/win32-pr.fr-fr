---
description: La méthode SetType spécifie le type principal.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Méthode CMediaType. SetType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37d035202d4674da11016620dc3c3d1ba3ab99f6ca514b9581f7dd2e4d9592d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954388"
---
# <a name="cmediatypesettype-method"></a>Méthode CMediaType. SetType

La `SetType` méthode spécifie le type principal.

## <a name="syntax"></a>Syntaxe


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ptype* 
</dt> <dd>

Pointeur vers un **GUID** qui spécifie le type principal.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




