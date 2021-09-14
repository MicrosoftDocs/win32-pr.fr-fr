---
description: La méthode GetRequest attend la requête suivante.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Méthode CAMThread. GetRequest (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094933"
---
# <a name="camthreadgetrequest-method"></a>Méthode CAMThread. GetRequest

La `GetRequest` méthode attend la requête suivante.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetRequest();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une valeur définie par la classe dérivée.

## <a name="remarks"></a>Notes

Cette méthode bloque jusqu’à ce qu’un autre thread appelle la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) . Elle retourne ensuite le paramètre qui a été passé à CallWorker. Appelez la méthode [**CAMThread :: reply**](camthread-reply.md) pour libérer le thread demandeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




