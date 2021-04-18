---
description: La méthode SetWaiting incrémente le nombre de threads en attente.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Méthode CBaseAllocator. SetWaiting (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92cba22e128a76f7884050d74a7819142c696dc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526413"
---
# <a name="cbaseallocatorsetwaiting-method"></a><span data-ttu-id="ba3ff-103">Méthode CBaseAllocator. SetWaiting</span><span class="sxs-lookup"><span data-stu-id="ba3ff-103">CBaseAllocator.SetWaiting method</span></span>

<span data-ttu-id="ba3ff-104">La `SetWaiting` méthode incrémente le nombre de threads en attente.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-104">The `SetWaiting` method increments the count of waiting threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba3ff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba3ff-105">Syntax</span></span>


```C++
void SetWaiting();
```



## <a name="parameters"></a><span data-ttu-id="ba3ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba3ff-106">Parameters</span></span>

<span data-ttu-id="ba3ff-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba3ff-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba3ff-108">Return value</span></span>

<span data-ttu-id="ba3ff-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba3ff-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ba3ff-110">Remarks</span></span>

<span data-ttu-id="ba3ff-111">Cette méthode incrémente la variable membre [**CBaseAllocator :: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) .</span><span class="sxs-lookup"><span data-stu-id="ba3ff-111">This method increments the [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) member variable.</span></span> <span data-ttu-id="ba3ff-112">Si un thread est bloqué dans la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) , l’allocateur appelle, `SetWaiting` puis attend que le sémaphore [**CBaseAllocator :: m \_ hSem**](cbaseallocator-m-hsem.md) soit signalé.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-112">If a thread is blocked in the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method, the allocator calls `SetWaiting` and then waits for the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore to be signaled.</span></span> <span data-ttu-id="ba3ff-113">La méthode [**CBaseAllocator :: ReleaseBuffer**](cbaseallocator-releasebuffer.md) signale le sémaphore et définit la valeur de *m \_ lWaiting* sur zéro.</span><span class="sxs-lookup"><span data-stu-id="ba3ff-113">The [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method signals the semaphore and sets *m\_lWaiting* back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba3ff-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba3ff-114">Requirements</span></span>



| <span data-ttu-id="ba3ff-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba3ff-115">Requirement</span></span> | <span data-ttu-id="ba3ff-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba3ff-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba3ff-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba3ff-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ba3ff-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba3ff-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ba3ff-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ba3ff-119">Library</span></span><br/> | <dl> <span data-ttu-id="ba3ff-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ba3ff-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba3ff-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba3ff-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba3ff-122">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="ba3ff-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




