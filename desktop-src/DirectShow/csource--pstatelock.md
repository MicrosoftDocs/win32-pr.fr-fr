---
description: La méthode pStateLock récupère un pointeur vers l’objet de section critique du filtre.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: Méthode CSource. pStateLock (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b74027e2ee2339e647938592e05162ce85108eb6985061b30a825394c2f2e7be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953788"
---
# <a name="csourcepstatelock-method"></a>Méthode CSource. pStateLock

La méthode **pStateLock** récupère un pointeur vers l’objet de section critique du filtre.

> [!Note]  
> Bien qu’elle soit nommée comme une variable membre, **pStateLock** est une méthode.

 

## <a name="syntax"></a>Syntaxe


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers la variable membre [**CSource :: m \_ cStateLock**](csource-m-cstatelock.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSource, classe**](csource.md)
</dt> </dl>

 

 




