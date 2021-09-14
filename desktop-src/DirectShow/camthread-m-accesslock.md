---
description: Section critique qui empêche l’accès du thread par d’autres threads.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'Membre CAMThread :: m_AccessLock (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094922"
---
# <a name="camthreadm_accesslock-member"></a>CAMThread :: m \_ AccessLock, membre

Section critique qui empêche l’accès du thread par d’autres threads.

## <a name="syntax"></a>Syntaxe


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>Notes

Les méthodes [**CAMThread :: Create**](camthread-create.md) et [**CAMThread :: CallWorker**](camthread-callworker.md) contiennent ce verrou, pour sérialiser des opérations sur le thread.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




