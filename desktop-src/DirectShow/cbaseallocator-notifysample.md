---
description: La méthode NotifySample libère tous les threads qui attendent des exemples.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Méthode CBaseAllocator. NotifySample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541696"
---
# <a name="cbaseallocatornotifysample-method"></a><span data-ttu-id="ae1ea-103">Méthode CBaseAllocator. NotifySample</span><span class="sxs-lookup"><span data-stu-id="ae1ea-103">CBaseAllocator.NotifySample method</span></span>

<span data-ttu-id="ae1ea-104">La `NotifySample` méthode libère tous les threads qui attendent des exemples.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-104">The `NotifySample` method releases any threads that are waiting for samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae1ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae1ea-105">Syntax</span></span>


```C++
void NotifySample();
```



## <a name="parameters"></a><span data-ttu-id="ae1ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae1ea-106">Parameters</span></span>

<span data-ttu-id="ae1ea-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae1ea-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae1ea-108">Return value</span></span>

<span data-ttu-id="ae1ea-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae1ea-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ae1ea-110">Remarks</span></span>

<span data-ttu-id="ae1ea-111">Quand des threads attendent des exemples, la valeur de [**CBaseAllocator :: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) est supérieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-111">When there are threads waiting for samples, the value of [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) is greater than zero.</span></span> <span data-ttu-id="ae1ea-112">Si *m \_ lWaiting* est supérieur à zéro, cette méthode appelle la fonction **ReleaseSemaphore,** sur le sémaphore [**CBaseAllocator :: m \_ hSem**](cbaseallocator-m-hsem.md) , en activant tous les threads en attente.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-112">If *m\_lWaiting* is greater than zero, this method calls the **ReleaseSemaphore** function on the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore, activating any waiting threads.</span></span> <span data-ttu-id="ae1ea-113">Elle réinitialise également *m \_ lWaiting* à zéro.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-113">It also resets *m\_lWaiting* to zero.</span></span>

<span data-ttu-id="ae1ea-114">Cette méthode est appelée à partir de la méthode [**CBaseAllocator :: ReleaseBuffer**](cbaseallocator-releasebuffer.md) , lorsqu’un exemple est retourné à la liste libre ; et à partir de la méthode [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) , lorsque l’allocation est désallouée.</span><span class="sxs-lookup"><span data-stu-id="ae1ea-114">This method is called from within the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method, when a sample is returned to the free list; and from the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method, when the allocator is decommitted.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae1ea-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae1ea-115">Requirements</span></span>



| <span data-ttu-id="ae1ea-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae1ea-116">Requirement</span></span> | <span data-ttu-id="ae1ea-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae1ea-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae1ea-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae1ea-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ae1ea-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae1ea-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ae1ea-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae1ea-120">Library</span></span><br/> | <dl> <span data-ttu-id="ae1ea-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ae1ea-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae1ea-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae1ea-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae1ea-123">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="ae1ea-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




