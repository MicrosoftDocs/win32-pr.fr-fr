---
description: La méthode unlock Déverrouille l’objet section critique.
ms.assetid: 61811e0e-df77-48e9-96d5-b7dff8c8db9b
title: CCritSec. Unlock, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Unlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca84ce452d71d0d3111039d7a95d8f5dd3155058
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545553"
---
# <a name="ccritsecunlock-method"></a>CCritSec. Unlock, méthode

La méthode **Unlock** déverrouille l’objet section critique.

## <a name="syntax"></a>Syntaxe


```C++
void Unlock();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode appelle la fonction [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) . Appelez cette méthode une fois pour chaque appel à la méthode [**CCritSec :: Lock**](ccritsec-lock.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCritSec, classe**](ccritsec.md)
</dt> </dl>

 

