---
description: La méthode SetSubtype spécifie le sous-type.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Méthode CMediaType. SetSubtype (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96445074ce2f0cc5a27a4988087f2fd910444beca88e5dc89c84585a8a98b338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566369"
---
# <a name="cmediatypesetsubtype-method"></a>Méthode CMediaType. SetSubtype

La `SetSubtype` méthode spécifie le sous-type.

## <a name="syntax"></a>Syntaxe


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*psubtype* 
</dt> <dd>

Pointeur vers un **GUID** qui spécifie le sous-type.

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

 

 




