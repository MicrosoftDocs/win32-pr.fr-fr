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
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545899"
---
# <a name="coutputqueuethreadproc-method"></a><span data-ttu-id="66513-103">COutputQueue. ThreadProc, méthode</span><span class="sxs-lookup"><span data-stu-id="66513-103">COutputQueue.ThreadProc method</span></span>

<span data-ttu-id="66513-104">La `ThreadProc` méthode récupère des exemples de la file d’attente et les remet à la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="66513-104">The `ThreadProc` method retrieves samples from the queue and delivers them to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="66513-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66513-105">Syntax</span></span>


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="66513-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66513-106">Parameters</span></span>

<span data-ttu-id="66513-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="66513-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66513-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66513-108">Return value</span></span>

<span data-ttu-id="66513-109">Retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="66513-109">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="66513-110">Notes</span><span class="sxs-lookup"><span data-stu-id="66513-110">Remarks</span></span>

<span data-ttu-id="66513-111">La méthode [**COutputQueue :: InitialThreadProc**](coutputqueue-initialthreadproc.md) appelle cette méthode, qui implémente la boucle de thread principale.</span><span class="sxs-lookup"><span data-stu-id="66513-111">The [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md) method calls this method, which implements the main thread loop.</span></span> <span data-ttu-id="66513-112">Au sein de la boucle, la méthode effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="66513-112">Within the loop, the method performs the following steps:</span></span>

1.  <span data-ttu-id="66513-113">Récupère un échantillon pour la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="66513-113">Retrieves a sample for the queue.</span></span>
2.  <span data-ttu-id="66513-114">Si l’exemple est un message de contrôle, le thread exécute l’action de contrôle.</span><span class="sxs-lookup"><span data-stu-id="66513-114">If the sample is a control message, the thread executes the control action.</span></span> <span data-ttu-id="66513-115">Dans le cas contraire, il place l’exemple dans le tableau [**COutputQueue :: m \_ ppSamples**](coutputqueue-m-ppsamples.md) .</span><span class="sxs-lookup"><span data-stu-id="66513-115">Otherwise, it places the sample into the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array.</span></span>
3.  <span data-ttu-id="66513-116">Lorsque le tableau est plein (ou si [**COutputQueue :: m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) a la **valeur false**), le thread appelle la méthode [**IMemInputPin :: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) pour remettre les exemples.</span><span class="sxs-lookup"><span data-stu-id="66513-116">When the array is full (or if [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) is **FALSE**), the thread calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method to deliver the samples.</span></span>
4.  <span data-ttu-id="66513-117">Si aucun échantillon n’est mis en file d’attente, le thread attend le sémaphore [**COutputQueue :: m \_ hSem**](coutputqueue-m-hsem.md) .</span><span class="sxs-lookup"><span data-stu-id="66513-117">If no samples are queued, the thread waits on the [**COutputQueue::m\_hSem**](coutputqueue-m-hsem.md) semaphore.</span></span>

<span data-ttu-id="66513-118">Le thread se termine lorsque la variable membre [**COutputQueue :: m \_ BTerminate**](coutputqueue-m-bterminate.md) devient **true**.</span><span class="sxs-lookup"><span data-stu-id="66513-118">The thread terminates when the [**COutputQueue::m\_bTerminate**](coutputqueue-m-bterminate.md) member variable becomes **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="66513-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66513-119">Requirements</span></span>



| <span data-ttu-id="66513-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66513-120">Requirement</span></span> | <span data-ttu-id="66513-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="66513-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66513-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="66513-122">Header</span></span><br/>  | <dl> <span data-ttu-id="66513-123"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66513-123"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="66513-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="66513-124">Library</span></span><br/> | <dl> <span data-ttu-id="66513-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="66513-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66513-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66513-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66513-127">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="66513-127">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




