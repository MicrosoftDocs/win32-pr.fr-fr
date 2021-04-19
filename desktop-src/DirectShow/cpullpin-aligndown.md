---
description: La méthode AlignDown tronque une valeur à une limite d’alignement spécifiée.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Méthode CPullPin. AlignDown (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1383517f4931fa153fd141878475cc8775a61045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527310"
---
# <a name="cpullpinaligndown-method"></a>Méthode CPullPin. AlignDown

La `AlignDown` méthode tronque une valeur à une limite d’alignement spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ll* 
</dt> <dd>

Spécifie le nombre à aligner.

</dd> <dt>

*lAlign* 
</dt> <dd>

Spécifie la limite d’alignement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le résultat aligné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPullPin, classe**](cpullpin.md)
</dt> </dl>

 

 




