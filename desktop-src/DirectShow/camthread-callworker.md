---
description: La méthode CallWorker signale au thread une demande.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: Méthode CAMThread. CallWorker (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7ffee6a55191f8f41d7121f3801a4a6392f9869803ded40ed891817146828f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955398"
---
# <a name="camthreadcallworker-method"></a>Méthode CAMThread. CallWorker

La `CallWorker` méthode signale au thread une demande.

## <a name="syntax"></a>Syntaxe


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwParam* 
</dt> <dd>

Paramètre de requête. La classe dérivée définit la signification du paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur définie par la classe dérivée.

## <a name="remarks"></a>Remarques

Les méthodes [**CAMThread :: GetRequest**](camthread-getrequest.md) et [**CAMThread :: CheckRequest**](camthread-checkrequest.md) extraient la valeur du paramètre *dwParam* . La méthode GetRequest se bloque jusqu’à ce que `CallWorker` soit appelé.

Cette méthode bloque jusqu’à ce que la méthode [**CAMThread :: reply**](camthread-reply.md) soit appelée. La valeur de retour est le paramètre donné à la réponse.

Cette méthode maintient le verrou [**CAMThread :: m \_ AccessLock**](camthread-m-accesslock.md) pour sérialiser les demandes. Par conséquent, appelez cette méthode à partir du thread lui-même ou à partir de n’importe quelle fonction membre qui s’exécute dans le contexte du thread.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




