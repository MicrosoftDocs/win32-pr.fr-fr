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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537607"
---
# <a name="cqueue-class"></a><span data-ttu-id="9a57f-103">CQueue, classe</span><span class="sxs-lookup"><span data-stu-id="9a57f-103">CQueue class</span></span>

<span data-ttu-id="9a57f-104">Le modèle de classe **CQueue** implémente une file d’attente de taille statique simple.</span><span class="sxs-lookup"><span data-stu-id="9a57f-104">The **CQueue** class template implements a simple, statically sized queue.</span></span>



| <span data-ttu-id="9a57f-105">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="9a57f-105">Public Methods</span></span>                                  | <span data-ttu-id="9a57f-106">Description</span><span class="sxs-lookup"><span data-stu-id="9a57f-106">Description</span></span>                             |
|-------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="9a57f-107">**CQueue**</span><span class="sxs-lookup"><span data-stu-id="9a57f-107">**CQueue**</span></span>](cqueue-cqueue.md)                 | <span data-ttu-id="9a57f-108">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="9a57f-108">Constructor method.</span></span>                     |
| [<span data-ttu-id="9a57f-109">**~ CQueue**</span><span class="sxs-lookup"><span data-stu-id="9a57f-109">**~CQueue**</span></span>](cqueue--cqueue.md)               | <span data-ttu-id="9a57f-110">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="9a57f-110">Destructor method.</span></span>                      |
| [<span data-ttu-id="9a57f-111">**GetQueueObject**</span><span class="sxs-lookup"><span data-stu-id="9a57f-111">**GetQueueObject**</span></span>](cqueue-getqueueobject.md) | <span data-ttu-id="9a57f-112">Récupère l’élément suivant de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="9a57f-112">Retrieves the next item from the queue.</span></span> |
| [<span data-ttu-id="9a57f-113">**PutQueueObject**</span><span class="sxs-lookup"><span data-stu-id="9a57f-113">**PutQueueObject**</span></span>](cqueue-putqueueobject.md) | <span data-ttu-id="9a57f-114">Place un élément dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="9a57f-114">Puts an item onto the queue.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="9a57f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9a57f-115">Remarks</span></span>

<span data-ttu-id="9a57f-116">Le constructeur de classe spécifie la taille de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="9a57f-116">The class constructor specifies the size of the queue.</span></span> <span data-ttu-id="9a57f-117">Utilisez [**CQueue ::P utqueueobject**](cqueue-putqueueobject.md) pour placer un élément dans la file d’attente, et la méthode [**CQueue :: GetQueueObject**](cqueue-getqueueobject.md) pour replacer un élément dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="9a57f-117">Use the [**CQueue::PutQueueObject**](cqueue-putqueueobject.md) to put an item on the queue, and the [**CQueue::GetQueueObject**](cqueue-getqueueobject.md) method to dequeues an item.</span></span> <span data-ttu-id="9a57f-118">Si la file d’attente est pleine, la méthode **PutQueueObject** se bloque jusqu’à ce qu’un élément soit déplacé dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="9a57f-118">If the queue is full, the **PutQueueObject** method blocks until an item is dequeued.</span></span> <span data-ttu-id="9a57f-119">Si la file d’attente est vide, **GetQueueObject** se bloque jusqu’à ce qu’un élément soit mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="9a57f-119">If the queue is empty, the **GetQueueObject** blocks until an item is queued.</span></span> <span data-ttu-id="9a57f-120">Le paramètre de modèle spécifie le type d’élément.</span><span class="sxs-lookup"><span data-stu-id="9a57f-120">The template parameter specifies the type of item.</span></span> <span data-ttu-id="9a57f-121">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9a57f-121">For example:</span></span>


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



<span data-ttu-id="9a57f-122">La classe utilise deux sémaphores pour contrôler les opérations de mise en file d’attente, un sémaphore « obtenir » et un sémaphore « put ».</span><span class="sxs-lookup"><span data-stu-id="9a57f-122">The class uses two semaphores to control queuing operations, a "get" semaphore and a "put" semaphore.</span></span> <span data-ttu-id="9a57f-123">La méthode [**GetQueueObject**](cqueue-getqueueobject.md) attend le sémaphore « obtient » (à l’aide de la fonction **WaitForSingleObject** ) et libère le sémaphore « put » (à l’aide de la fonction **ReleaseSemaphore,** ).</span><span class="sxs-lookup"><span data-stu-id="9a57f-123">The [**GetQueueObject**](cqueue-getqueueobject.md) method waits on the "get" semaphore (using the **WaitForSingleObject** function) and releases the "put" semaphore (using the **ReleaseSemaphore** function).</span></span> <span data-ttu-id="9a57f-124">La méthode [**PutQueueObject**](cqueue-putqueueobject.md) attend le sémaphore « put » et libère le sémaphore « obtient ».</span><span class="sxs-lookup"><span data-stu-id="9a57f-124">The [**PutQueueObject**](cqueue-putqueueobject.md) method waits on the "put" semaphore and releases the "get" semaphore.</span></span> <span data-ttu-id="9a57f-125">La classe utilise une section critique pour sérialiser les opérations de mise en file d’attente entre plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="9a57f-125">The class uses a critical section to serialize queuing operations among multiple threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a57f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a57f-126">Requirements</span></span>



| <span data-ttu-id="9a57f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a57f-127">Requirement</span></span> | <span data-ttu-id="9a57f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a57f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a57f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a57f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9a57f-130"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a57f-130"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9a57f-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9a57f-131">Library</span></span><br/> | <dl> <span data-ttu-id="9a57f-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9a57f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




