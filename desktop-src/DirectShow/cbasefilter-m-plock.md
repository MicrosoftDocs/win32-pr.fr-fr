---
description: Pointeur vers une section critique utilisée pour sérialiser les modifications d’État.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'Membre CBaseFilter :: m_pLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40b2f6ece048fc6463fda0a22792d57839d59e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540422"
---
# <a name="cbasefilterm_plock-member"></a><span data-ttu-id="87bf0-103">CBaseFilter :: m \_ pLock, membre</span><span class="sxs-lookup"><span data-stu-id="87bf0-103">CBaseFilter::m\_pLock member</span></span>

<span data-ttu-id="87bf0-104">Pointeur vers une section critique utilisée pour sérialiser les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="87bf0-104">Pointer to a critical section that is used to serialize state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="87bf0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87bf0-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="87bf0-106">Notes</span><span class="sxs-lookup"><span data-stu-id="87bf0-106">Remarks</span></span>

<span data-ttu-id="87bf0-107">Cette variable est initialisée dans le constructeur de classe ; consultez [**CBaseFilter :: CBaseFilter**](cbasefilter-cbasefilter.md).</span><span class="sxs-lookup"><span data-stu-id="87bf0-107">This variable is initialized in the class constructor; see [**CBaseFilter::CBaseFilter**](cbasefilter-cbasefilter.md).</span></span>

<span data-ttu-id="87bf0-108">Tenez cette section critique lors des transitions d’État ou lorsqu’une méthode accède à l’État sur plusieurs opérations.</span><span class="sxs-lookup"><span data-stu-id="87bf0-108">Hold this critical section during state transitions, or when a method accesses the state over several operations.</span></span> <span data-ttu-id="87bf0-109">La classe de base contient la section critique dans les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="87bf0-109">The base class holds the critical section in the following methods:</span></span>

-   [<span data-ttu-id="87bf0-110">**CBaseFilter::FindPin**</span><span class="sxs-lookup"><span data-stu-id="87bf0-110">**CBaseFilter::FindPin**</span></span>](cbasefilter-findpin.md)
-   [<span data-ttu-id="87bf0-111">**CBaseFilter::GetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="87bf0-111">**CBaseFilter::GetSyncSource**</span></span>](cbasefilter-getsyncsource.md)
-   [<span data-ttu-id="87bf0-112">**CBaseFilter::JoinFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="87bf0-112">**CBaseFilter::JoinFilterGraph**</span></span>](cbasefilter-joinfiltergraph.md)
-   [<span data-ttu-id="87bf0-113">**CBaseFilter :: IsActive**</span><span class="sxs-lookup"><span data-stu-id="87bf0-113">**CBaseFilter::IsActive**</span></span>](cbasefilter-isactive.md)
-   [<span data-ttu-id="87bf0-114">**CBaseFilter::SetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="87bf0-114">**CBaseFilter::SetSyncSource**</span></span>](cbasefilter-setsyncsource.md)
-   [<span data-ttu-id="87bf0-115">**CBaseFilter ::P ause**</span><span class="sxs-lookup"><span data-stu-id="87bf0-115">**CBaseFilter::Pause**</span></span>](cbasefilter-pause.md)
-   [<span data-ttu-id="87bf0-116">**CBaseFilter :: Run**</span><span class="sxs-lookup"><span data-stu-id="87bf0-116">**CBaseFilter::Run**</span></span>](cbasefilter-run.md)
-   [<span data-ttu-id="87bf0-117">**CBaseFilter :: Stop**</span><span class="sxs-lookup"><span data-stu-id="87bf0-117">**CBaseFilter::Stop**</span></span>](cbasefilter-stop.md)

<span data-ttu-id="87bf0-118">Ne conservent pas cette section critique pendant les opérations de diffusion en continu (autrement dit, lors de la transmission d’exemples à un filtre en aval).</span><span class="sxs-lookup"><span data-stu-id="87bf0-118">Do not hold this critical section during streaming operations (that is, when delivering samples to a downstream filter).</span></span> <span data-ttu-id="87bf0-119">Sérialisez les opérations de diffusion en continu à l’aide d’une section critique différente.</span><span class="sxs-lookup"><span data-stu-id="87bf0-119">Serialize streaming operations using a different critical section.</span></span> <span data-ttu-id="87bf0-120">Dans le cas contraire, cela peut provoquer un interblocage.</span><span class="sxs-lookup"><span data-stu-id="87bf0-120">Otherwise, it can cause deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="87bf0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87bf0-121">Requirements</span></span>



| <span data-ttu-id="87bf0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87bf0-122">Requirement</span></span> | <span data-ttu-id="87bf0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="87bf0-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87bf0-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="87bf0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="87bf0-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87bf0-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="87bf0-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="87bf0-126">Library</span></span><br/> | <dl> <span data-ttu-id="87bf0-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="87bf0-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87bf0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87bf0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87bf0-129">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="87bf0-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="87bf0-130">Threads et sections critiques</span><span class="sxs-lookup"><span data-stu-id="87bf0-130">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




