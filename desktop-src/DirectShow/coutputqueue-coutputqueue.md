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
# <a name="coutputqueuecoutputqueue-constructor"></a><span data-ttu-id="7527f-103">Constructeur COutputQueue. COutputQueue</span><span class="sxs-lookup"><span data-stu-id="7527f-103">COutputQueue.COutputQueue constructor</span></span>

<span data-ttu-id="7527f-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="7527f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7527f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7527f-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="7527f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7527f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7527f-107">*pInputPin*</span><span class="sxs-lookup"><span data-stu-id="7527f-107">*pInputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="7527f-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7527f-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the input pin.</span></span> <span data-ttu-id="7527f-109">L’objet fournira des exemples à ce code PIN.</span><span class="sxs-lookup"><span data-stu-id="7527f-109">The object will deliver samples to this pin.</span></span>

</dd> <dt>

<span data-ttu-id="7527f-110">*phr*</span><span class="sxs-lookup"><span data-stu-id="7527f-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="7527f-111">Pointeur vers un code de retour **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7527f-111">Pointer to an **HRESULT** return code.</span></span> <span data-ttu-id="7527f-112">Définissez la valeur sur \_ OK avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="7527f-112">Set the value to S\_OK before calling this method.</span></span> <span data-ttu-id="7527f-113">Lors du retour, *PHR* reçoit une valeur qui indique la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="7527f-113">On return, *phr* receives a value that indicates the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="7527f-114">*bAuto*</span><span class="sxs-lookup"><span data-stu-id="7527f-114">*bAuto*</span></span> 
</dt> <dd>

<span data-ttu-id="7527f-115">Indicateur qui spécifie si l’objet décide quand créer une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="7527f-115">Flag that specifies whether the object decides when to create a queue.</span></span> <span data-ttu-id="7527f-116">Si la **valeur est true**, l’objet crée une file d’attente uniquement si la broche d’entrée peut être bloquée.</span><span class="sxs-lookup"><span data-stu-id="7527f-116">If **TRUE**, the object creates a queue only if the input pin might block.</span></span> <span data-ttu-id="7527f-117">Si la **valeur est false**, le paramètre *bQueue* spécifie s’il faut créer une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="7527f-117">If **FALSE**, the *bQueue* parameter specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="7527f-118">*bQueue*</span><span class="sxs-lookup"><span data-stu-id="7527f-118">*bQueue*</span></span> 
</dt> <dd>

<span data-ttu-id="7527f-119">Si *bAuto* a la **valeur true**, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="7527f-119">If *bAuto* is **TRUE**, this parameter is ignored.</span></span> <span data-ttu-id="7527f-120">Si *bAuto* a la **valeur false**, cet indicateur spécifie s’il faut créer une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="7527f-120">If *bAuto* is **FALSE**, this flag specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="7527f-121">*lBatchSize*</span><span class="sxs-lookup"><span data-stu-id="7527f-121">*lBatchSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7527f-122">Nombre maximal d’échantillons à remettre en un seul lot.</span><span class="sxs-lookup"><span data-stu-id="7527f-122">Maximum number of samples to deliver in one batch.</span></span>

</dd> <dt>

<span data-ttu-id="7527f-123">*bBatchExact*</span><span class="sxs-lookup"><span data-stu-id="7527f-123">*bBatchExact*</span></span> 
</dt> <dd>

<span data-ttu-id="7527f-124">Indicateur qui spécifie s’il faut utiliser des tailles de lot exactes.</span><span class="sxs-lookup"><span data-stu-id="7527f-124">Flag that specifies whether to use exact batch sizes.</span></span> <span data-ttu-id="7527f-125">Si la **valeur est true**, l’objet attend des échantillons de *lBatchSize* avant de les transmettre à la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7527f-125">If **TRUE**, the object waits for *lBatchSize* samples before delivering them to the input pin.</span></span> <span data-ttu-id="7527f-126">Si la **valeur est false**, l’objet fournit des exemples lorsqu’il les reçoit.</span><span class="sxs-lookup"><span data-stu-id="7527f-126">If **FALSE**, the object delivers samples as it receives them.</span></span>

</dd> <dt>

<span data-ttu-id="7527f-127">*lListSize*</span><span class="sxs-lookup"><span data-stu-id="7527f-127">*lListSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7527f-128">Taille du cache de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="7527f-128">Cache size for the queue.</span></span> <span data-ttu-id="7527f-129">La valeur par défaut, DEFAULTCACHE, est une constante définie pour la classe [**CBaseList**](cbaselist.md) .</span><span class="sxs-lookup"><span data-stu-id="7527f-129">The default value, DEFAULTCACHE, is a constant defined for the [**CBaseList**](cbaselist.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="7527f-130">*dwPriority*</span><span class="sxs-lookup"><span data-stu-id="7527f-130">*dwPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="7527f-131">Priorité du thread qui fournit des exemples.</span><span class="sxs-lookup"><span data-stu-id="7527f-131">Priority of the thread that delivers samples.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7527f-132">Notes </span><span class="sxs-lookup"><span data-stu-id="7527f-132">Remarks</span></span>

<span data-ttu-id="7527f-133">Si *bAuto* a la **valeur true**, l’objet appelle la méthode [**IMemInputPin :: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) sur le code confidentiel en aval.</span><span class="sxs-lookup"><span data-stu-id="7527f-133">If *bAuto* is **TRUE**, the object calls the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method on the downstream pin.</span></span> <span data-ttu-id="7527f-134">Si **ReceiveCanBlock** retourne S \_ OK (ce qui signifie que le code confidentiel peut se bloquer sur [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) Calls), l’objet crée un thread pour la diffusion des exemples.</span><span class="sxs-lookup"><span data-stu-id="7527f-134">If **ReceiveCanBlock** returns S\_OK (meaning the pin might block on [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) calls), the object creates a thread for delivering samples.</span></span> <span data-ttu-id="7527f-135">Dans le cas contraire, il ne crée pas de thread.</span><span class="sxs-lookup"><span data-stu-id="7527f-135">Otherwise, it does not create a thread.</span></span>

<span data-ttu-id="7527f-136">Si *bAuto* a la valeur **false**, la valeur de *bQueue* détermine s’il faut créer un thread.</span><span class="sxs-lookup"><span data-stu-id="7527f-136">If *bAuto* is **FALSE**, the value of *bQueue* determines whether to create a thread.</span></span>

<span data-ttu-id="7527f-137">Si l’objet crée un thread, il affecte le handle de thread à la variable membre [**COutputQueue :: m \_ hThread**](coutputqueue-m-hthread.md) .</span><span class="sxs-lookup"><span data-stu-id="7527f-137">If the object creates a thread, it assigns the thread handle to the [**COutputQueue::m\_hThread**](coutputqueue-m-hthread.md) member variable.</span></span> <span data-ttu-id="7527f-138">La procédure de thread est [**COutputQueue :: InitialThreadProc**](coutputqueue-initialthreadproc.md), et le paramètre de thread est un pointeur vers ce.</span><span class="sxs-lookup"><span data-stu-id="7527f-138">The thread procedure is [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md), and the thread parameter is a pointer to this.</span></span> <span data-ttu-id="7527f-139">L’objet crée également une file d’attente pour contenir les exemples, qui est donnée par la variable de membre de [**\_ liste COutputQueue :: m**](coutputqueue-m-list.md) .</span><span class="sxs-lookup"><span data-stu-id="7527f-139">The object also creates a queue for holding samples, which is given by the [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="7527f-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7527f-140">Requirements</span></span>



| <span data-ttu-id="7527f-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7527f-141">Requirement</span></span> | <span data-ttu-id="7527f-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="7527f-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7527f-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="7527f-143">Header</span></span><br/>  | <dl> <span data-ttu-id="7527f-144"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7527f-144"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7527f-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7527f-145">Library</span></span><br/> | <dl> <span data-ttu-id="7527f-146"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7527f-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7527f-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7527f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7527f-148">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="7527f-148">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




