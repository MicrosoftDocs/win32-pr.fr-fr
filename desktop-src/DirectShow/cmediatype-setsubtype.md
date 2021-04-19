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
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525219"
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
| En-tête<br/>  | <dl> <dt>Mtype. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




