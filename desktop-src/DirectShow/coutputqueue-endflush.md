---
description: 'Méthode COutputQueue. EndFlush : la méthode EndFlush termine une opération de vidage.'
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Méthode COutputQueue. EndFlush (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37701526de66c8cd679f6849703c4eb2a1feb3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099007"
---
# <a name="coutputqueueendflush-method"></a><span data-ttu-id="25dd9-103">Méthode COutputQueue. EndFlush</span><span class="sxs-lookup"><span data-stu-id="25dd9-103">COutputQueue.EndFlush method</span></span>

<span data-ttu-id="25dd9-104">La `EndFlush` méthode termine une opération de vidage.</span><span class="sxs-lookup"><span data-stu-id="25dd9-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="25dd9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25dd9-105">Syntax</span></span>


```C++
void EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="25dd9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25dd9-106">Parameters</span></span>

<span data-ttu-id="25dd9-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="25dd9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25dd9-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="25dd9-108">Return value</span></span>

<span data-ttu-id="25dd9-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="25dd9-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25dd9-110">Notes </span><span class="sxs-lookup"><span data-stu-id="25dd9-110">Remarks</span></span>

<span data-ttu-id="25dd9-111">Si l’objet utilise un thread, cette méthode attend l’événement [**COutputQueue :: m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="25dd9-111">If the object is using a thread, this method waits for the [**COutputQueue::m\_evFlushComplete**](coutputqueue-m-evflushcomplete.md) event.</span></span> <span data-ttu-id="25dd9-112">Le thread signale cet événement après qu’il a libéré des échantillons en attente.</span><span class="sxs-lookup"><span data-stu-id="25dd9-112">The thread signals this event after it frees any pending samples.</span></span> <span data-ttu-id="25dd9-113">Si l’objet n’utilise pas de thread, cette méthode appelle la méthode [**COutputQueue :: FreeSamples**](coutputqueue-freesamples.md) .</span><span class="sxs-lookup"><span data-stu-id="25dd9-113">If the object is not using a thread, this method calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method.</span></span> <span data-ttu-id="25dd9-114">La `EndFlush` méthode appelle ensuite la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="25dd9-114">Then the `EndFlush` method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="25dd9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25dd9-115">Requirements</span></span>



| <span data-ttu-id="25dd9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25dd9-116">Requirement</span></span> | <span data-ttu-id="25dd9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="25dd9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25dd9-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="25dd9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="25dd9-119"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25dd9-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="25dd9-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="25dd9-120">Library</span></span><br/> | <dl> <span data-ttu-id="25dd9-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="25dd9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25dd9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25dd9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25dd9-123">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="25dd9-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




