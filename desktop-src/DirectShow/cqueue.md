---
description: Le modèle de classe CQueue implémente une file d’attente de taille statique simple.
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: CQueue, classe (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ceef0d29e0f6f06c30355a47e3274495f17dceb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413982"
---
# <a name="cqueue-class"></a>CQueue, classe

Le modèle de classe **CQueue** implémente une file d’attente de taille statique simple.



| M&#233;thodes publiques                                  | Description                             |
|-------------------------------------------------|-----------------------------------------|
| [**CQueue**](cqueue-cqueue.md)                 | Méthode de constructeur.                     |
| [**~ CQueue**](cqueue--cqueue.md)               | Méthode de destructeur.                      |
| [**GetQueueObject**](cqueue-getqueueobject.md) | Récupère l’élément suivant de la file d’attente. |
| [**PutQueueObject**](cqueue-putqueueobject.md) | Place un élément dans la file d’attente.            |



 

## <a name="remarks"></a>Notes

Le constructeur de classe spécifie la taille de la file d’attente. Utilisez [**CQueue ::P utqueueobject**](cqueue-putqueueobject.md) pour placer un élément dans la file d’attente, et la méthode [**CQueue :: GetQueueObject**](cqueue-getqueueobject.md) pour replacer un élément dans la file d’attente. Si la file d’attente est pleine, la méthode **PutQueueObject** se bloque jusqu’à ce qu’un élément soit déplacé dans la file d’attente. Si la file d’attente est vide, **GetQueueObject** se bloque jusqu’à ce qu’un élément soit mis en file d’attente. Le paramètre de modèle spécifie le type d’élément. Par exemple :


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



La classe utilise deux sémaphores pour contrôler les opérations de mise en file d’attente, un sémaphore « obtenir » et un sémaphore « put ». La méthode [**GetQueueObject**](cqueue-getqueueobject.md) attend le sémaphore « obtient » (à l’aide de la fonction **WaitForSingleObject** ) et libère le sémaphore « put » (à l’aide de la fonction **ReleaseSemaphore,** ). La méthode [**PutQueueObject**](cqueue-putqueueobject.md) attend le sémaphore « put » et libère le sémaphore « obtient ». La classe utilise une section critique pour sérialiser les opérations de mise en file d’attente entre plusieurs threads.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




