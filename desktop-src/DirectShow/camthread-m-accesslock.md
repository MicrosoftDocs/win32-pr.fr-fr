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
ms.openlocfilehash: 72e5823b7acadd3c1c0f3752606825d1b2981aac4a64903c5944e3df82252aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017597"
---
# <a name="camthreadm_accesslock-member"></a>CAMThread :: m \_ AccessLock, membre

Section critique qui empêche l’accès du thread par d’autres threads.

## <a name="syntax"></a>Syntaxe


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>Notes

Les méthodes [**CAMThread :: Create**](camthread-create.md) et [**CAMThread :: CallWorker**](camthread-callworker.md) contiennent ce verrou, pour sérialiser des opérations sur le thread.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




