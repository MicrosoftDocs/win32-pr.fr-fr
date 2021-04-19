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
# <a name="camthreadcallworker-method"></a><span data-ttu-id="48195-103">Méthode CAMThread. CallWorker</span><span class="sxs-lookup"><span data-stu-id="48195-103">CAMThread.CallWorker method</span></span>

<span data-ttu-id="48195-104">La `CallWorker` méthode signale au thread une demande.</span><span class="sxs-lookup"><span data-stu-id="48195-104">The `CallWorker` method signals the thread with a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="48195-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48195-105">Syntax</span></span>


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a><span data-ttu-id="48195-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48195-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48195-107">*dwParam*</span><span class="sxs-lookup"><span data-stu-id="48195-107">*dwParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48195-108">Paramètre de requête.</span><span class="sxs-lookup"><span data-stu-id="48195-108">Request parameter.</span></span> <span data-ttu-id="48195-109">La classe dérivée définit la signification du paramètre.</span><span class="sxs-lookup"><span data-stu-id="48195-109">The derived class defines the meaning of the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48195-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48195-110">Return value</span></span>

<span data-ttu-id="48195-111">Retourne une valeur définie par la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="48195-111">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="48195-112">Notes</span><span class="sxs-lookup"><span data-stu-id="48195-112">Remarks</span></span>

<span data-ttu-id="48195-113">Les méthodes [**CAMThread :: GetRequest**](camthread-getrequest.md) et [**CAMThread :: CheckRequest**](camthread-checkrequest.md) extraient la valeur du paramètre *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="48195-113">The [**CAMThread::GetRequest**](camthread-getrequest.md) and [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods retrieve the value of the *dwParam* parameter.</span></span> <span data-ttu-id="48195-114">La méthode GetRequest se bloque jusqu’à ce que `CallWorker` soit appelé.</span><span class="sxs-lookup"><span data-stu-id="48195-114">The GetRequest method blocks until `CallWorker` is called.</span></span>

<span data-ttu-id="48195-115">Cette méthode bloque jusqu’à ce que la méthode [**CAMThread :: reply**](camthread-reply.md) soit appelée.</span><span class="sxs-lookup"><span data-stu-id="48195-115">This method blocks until the [**CAMThread::Reply**](camthread-reply.md) method is called.</span></span> <span data-ttu-id="48195-116">La valeur de retour est le paramètre donné à la réponse.</span><span class="sxs-lookup"><span data-stu-id="48195-116">The return value is the parameter given to Reply.</span></span>

<span data-ttu-id="48195-117">Cette méthode maintient le verrou [**CAMThread :: m \_ AccessLock**](camthread-m-accesslock.md) pour sérialiser les demandes.</span><span class="sxs-lookup"><span data-stu-id="48195-117">This method holds the [**CAMThread::m\_AccessLock**](camthread-m-accesslock.md) lock to serialize requests.</span></span> <span data-ttu-id="48195-118">Par conséquent, appelez cette méthode à partir du thread lui-même ou à partir de n’importe quelle fonction membre qui s’exécute dans le contexte du thread.</span><span class="sxs-lookup"><span data-stu-id="48195-118">Therefore, do call this method from the thread itself or from any member function that executes in the context of the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="48195-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48195-119">Requirements</span></span>



| <span data-ttu-id="48195-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48195-120">Requirement</span></span> | <span data-ttu-id="48195-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="48195-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48195-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="48195-122">Header</span></span><br/>  | <dl> <span data-ttu-id="48195-123"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48195-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="48195-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="48195-124">Library</span></span><br/> | <dl> <span data-ttu-id="48195-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="48195-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48195-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48195-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48195-127">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="48195-127">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




