---
description: L' \_ opérateur de temps de référence () convertit l’objet en un type de données de temps de référence \_ .
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: CRefTime. Operator REFERENCE_TIME, méthode (reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538120"
---
# <a name="creftimeoperator-reference_time-method"></a>CRefTime. Operator Time, méthode de référence \_

L' `REFERENCE_TIME()` opérateur convertit l’objet en un type de données de [**\_ temps de référence**](reference-time.md) .

## <a name="syntax"></a>Syntaxe


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la valeur de [**CRefTime :: m \_ Time**](creftime-m-time.md).

## <a name="remarks"></a>Notes

L’exemple suivant montre comment utiliser cet opérateur de conversion :


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Reftime. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




