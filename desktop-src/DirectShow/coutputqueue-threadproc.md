---
description: La méthode ThreadProc récupère des échantillons de la file d’attente et les remet à la broche d’entrée.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: COutputQueue. ThreadProc, méthode (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d37158d71a74726e9bf27e76ffedb076f99b7380ffcca4edfa95928767eedbf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073633"
---
# <a name="coutputqueuethreadproc-method"></a>COutputQueue. ThreadProc, méthode

La `ThreadProc` méthode récupère des exemples de la file d’attente et les remet à la broche d’entrée.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne zéro.

## <a name="remarks"></a>Remarques

La méthode [**COutputQueue :: InitialThreadProc**](coutputqueue-initialthreadproc.md) appelle cette méthode, qui implémente la boucle de thread principale. Au sein de la boucle, la méthode effectue les étapes suivantes :

1.  Récupère un échantillon pour la file d’attente.
2.  Si l’exemple est un message de contrôle, le thread exécute l’action de contrôle. Dans le cas contraire, il place l’exemple dans le tableau [**COutputQueue :: m \_ ppSamples**](coutputqueue-m-ppsamples.md) .
3.  Lorsque le tableau est plein (ou si [**COutputQueue :: m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) a la **valeur false**), le thread appelle la méthode [**IMemInputPin :: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) pour remettre les exemples.
4.  Si aucun échantillon n’est mis en file d’attente, le thread attend le sémaphore [**COutputQueue :: m \_ hSem**](coutputqueue-m-hsem.md) .

Le thread se termine lorsque la variable membre [**COutputQueue :: m \_ BTerminate**](coutputqueue-m-bterminate.md) devient **true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




