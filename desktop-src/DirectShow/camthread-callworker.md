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
ms.openlocfilehash: 7410fbee4ece729d1579f525731bddaceded1153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525598"
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

## <a name="remarks"></a>Notes

Les méthodes [**CAMThread :: GetRequest**](camthread-getrequest.md) et [**CAMThread :: CheckRequest**](camthread-checkrequest.md) extraient la valeur du paramètre *dwParam* . La méthode GetRequest se bloque jusqu’à ce que `CallWorker` soit appelé.

Cette méthode bloque jusqu’à ce que la méthode [**CAMThread :: reply**](camthread-reply.md) soit appelée. La valeur de retour est le paramètre donné à la réponse.

Cette méthode maintient le verrou [**CAMThread :: m \_ AccessLock**](camthread-m-accesslock.md) pour sérialiser les demandes. Par conséquent, appelez cette méthode à partir du thread lui-même ou à partir de n’importe quelle fonction membre qui s’exécute dans le contexte du thread.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




