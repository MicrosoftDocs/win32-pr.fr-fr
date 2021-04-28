---
description: Méthode constructeur COutputQueue. COutputQueue.
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Constructeur COutputQueue. COutputQueue (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17a795bf4ec33ec904b83f6621fc0bc4f43b4b15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095327"
---
# <a name="coutputqueuecoutputqueue-constructor"></a>Constructeur COutputQueue. COutputQueue

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInputPin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche d’entrée. L’objet fournira des exemples à ce code PIN.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers un code de retour **HRESULT** . Définissez la valeur sur \_ OK avant d’appeler cette méthode. Lors du retour, *PHR* reçoit une valeur qui indique la réussite ou l’échec de la méthode.

</dd> <dt>

*bAuto* 
</dt> <dd>

Indicateur qui spécifie si l’objet décide quand créer une file d’attente. Si la **valeur est true**, l’objet crée une file d’attente uniquement si la broche d’entrée peut être bloquée. Si la **valeur est false**, le paramètre *bQueue* spécifie s’il faut créer une file d’attente.

</dd> <dt>

*bQueue* 
</dt> <dd>

Si *bAuto* a la **valeur true**, ce paramètre est ignoré. Si *bAuto* a la **valeur false**, cet indicateur spécifie s’il faut créer une file d’attente.

</dd> <dt>

*lBatchSize* 
</dt> <dd>

Nombre maximal d’échantillons à remettre en un seul lot.

</dd> <dt>

*bBatchExact* 
</dt> <dd>

Indicateur qui spécifie s’il faut utiliser des tailles de lot exactes. Si la **valeur est true**, l’objet attend des échantillons de *lBatchSize* avant de les transmettre à la broche d’entrée. Si la **valeur est false**, l’objet fournit des exemples lorsqu’il les reçoit.

</dd> <dt>

*lListSize* 
</dt> <dd>

Taille du cache de la file d’attente. La valeur par défaut, DEFAULTCACHE, est une constante définie pour la classe [**CBaseList**](cbaselist.md) .

</dd> <dt>

*dwPriority* 
</dt> <dd>

Priorité du thread qui fournit des exemples.

</dd> </dl>

## <a name="remarks"></a>Notes 

Si *bAuto* a la **valeur true**, l’objet appelle la méthode [**IMemInputPin :: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) sur le code confidentiel en aval. Si **ReceiveCanBlock** retourne S \_ OK (ce qui signifie que le code confidentiel peut se bloquer sur [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) Calls), l’objet crée un thread pour la diffusion des exemples. Dans le cas contraire, il ne crée pas de thread.

Si *bAuto* a la valeur **false**, la valeur de *bQueue* détermine s’il faut créer un thread.

Si l’objet crée un thread, il affecte le handle de thread à la variable membre [**COutputQueue :: m \_ hThread**](coutputqueue-m-hthread.md) . La procédure de thread est [**COutputQueue :: InitialThreadProc**](coutputqueue-initialthreadproc.md), et le paramètre de thread est un pointeur vers ce. L’objet crée également une file d’attente pour contenir les exemples, qui est donnée par la variable de membre de [**\_ liste COutputQueue :: m**](coutputqueue-m-list.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




