---
description: La méthode ReadOnly indique si le flux d’entrée est en lecture seule.
ms.assetid: 25b8230d-be2b-4129-a1aa-f6b36e95199e
title: CTransInPlaceInputPin. ReadOnly, méthode (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.ReadOnly
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f0dd3ae23da6832911b58e50cba67bcf8e6ec6092c3a31a193bd5a027c5566c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999089"
---
# <a name="ctransinplaceinputpinreadonly-method"></a>CTransInPlaceInputPin. ReadOnly, méthode

La `ReadOnly` méthode indique si le flux d’entrée est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
const BOOL ReadOnly();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la valeur de la variable membre [**m \_ bReadOnly**](ctransinplaceinputpin-m-breadonly.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceInputPin, classe**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




