---
description: La classe CAMSchedule implémente un planificateur pour les horloges de référence.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: CAMSchedule, classe (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bef8ad07347284c53a3490c21032070788fa3ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533151"
---
# <a name="camschedule-class"></a><span data-ttu-id="6a45c-103">CAMSchedule, classe</span><span class="sxs-lookup"><span data-stu-id="6a45c-103">CAMSchedule class</span></span>

<span data-ttu-id="6a45c-104">La `CAMSchedule` classe implémente un planificateur pour les horloges de référence.</span><span class="sxs-lookup"><span data-stu-id="6a45c-104">The `CAMSchedule` class implements a scheduler for reference clocks.</span></span>



| <span data-ttu-id="6a45c-105">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="6a45c-105">Public Methods</span></span>                                             | <span data-ttu-id="6a45c-106">Description</span><span class="sxs-lookup"><span data-stu-id="6a45c-106">Description</span></span>                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a45c-107">**CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="6a45c-107">**CAMSchedule**</span></span>](camschedule-camschedule.md)             | <span data-ttu-id="6a45c-108">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="6a45c-108">Constructor method.</span></span>                                                                  |
| [<span data-ttu-id="6a45c-109">**~ CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="6a45c-109">**~CAMSchedule**</span></span>](camschedule--camschedule.md)           | <span data-ttu-id="6a45c-110">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="6a45c-110">Destructor method.</span></span> <span data-ttu-id="6a45c-111">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="6a45c-111">Virtual.</span></span>                                                          |
| [<span data-ttu-id="6a45c-112">**GetAdviseCount**</span><span class="sxs-lookup"><span data-stu-id="6a45c-112">**GetAdviseCount**</span></span>](camschedule-getadvisecount.md)       | <span data-ttu-id="6a45c-113">Récupère le nombre de demandes de notification en attente.</span><span class="sxs-lookup"><span data-stu-id="6a45c-113">Retrieves the number of pending advise requests.</span></span>                                     |
| [<span data-ttu-id="6a45c-114">**GetNextAdviseTime**</span><span class="sxs-lookup"><span data-stu-id="6a45c-114">**GetNextAdviseTime**</span></span>](camschedule-getnextadvisetime.md) | <span data-ttu-id="6a45c-115">Récupère l’heure de la demande de notification suivante.</span><span class="sxs-lookup"><span data-stu-id="6a45c-115">Retrieves the time of the next advise request.</span></span>                                       |
| [<span data-ttu-id="6a45c-116">**AddAdvisePacket**</span><span class="sxs-lookup"><span data-stu-id="6a45c-116">**AddAdvisePacket**</span></span>](camschedule-addadvisepacket.md)     | <span data-ttu-id="6a45c-117">Ajoute une demande de notification à la liste des demandes en attente.</span><span class="sxs-lookup"><span data-stu-id="6a45c-117">Adds an advise request to the list of pending requests.</span></span>                              |
| [<span data-ttu-id="6a45c-118">**Arrêter**</span><span class="sxs-lookup"><span data-stu-id="6a45c-118">**Unadvise**</span></span>](camschedule-unadvise.md)                   | <span data-ttu-id="6a45c-119">Supprime une demande de notification.</span><span class="sxs-lookup"><span data-stu-id="6a45c-119">Removes an advise request.</span></span>                                                           |
| [<span data-ttu-id="6a45c-120">**Lui**</span><span class="sxs-lookup"><span data-stu-id="6a45c-120">**Advise**</span></span>](camschedule-advise.md)                       | <span data-ttu-id="6a45c-121">Distribue toutes les demandes planifiées pour une heure spécifiée ou antérieure.</span><span class="sxs-lookup"><span data-stu-id="6a45c-121">Dispatches all requests that are scheduled for a specified time or earlier.</span></span>          |
| [<span data-ttu-id="6a45c-122">**GetEvent**</span><span class="sxs-lookup"><span data-stu-id="6a45c-122">**GetEvent**</span></span>](camschedule-getevent.md)                   | <span data-ttu-id="6a45c-123">Récupère un handle d’événement, qui est utilisé pour signaler une modification de l’heure suivante de l’avis.</span><span class="sxs-lookup"><span data-stu-id="6a45c-123">Retrieves an event handle, which is used to signal a change in the next advise time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6a45c-124">Notes</span><span class="sxs-lookup"><span data-stu-id="6a45c-124">Remarks</span></span>

<span data-ttu-id="6a45c-125">Cet objet d’assistance gère une liste de demandes de notification pour une horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="6a45c-125">This helper object maintains a list of advise requests for a reference clock.</span></span> <span data-ttu-id="6a45c-126">La classe [**CBaseReferenceClock**](cbasereferenceclock.md) l’utilise pour aider à planifier les demandes de notification.</span><span class="sxs-lookup"><span data-stu-id="6a45c-126">The [**CBaseReferenceClock**](cbasereferenceclock.md) class uses it to help schedule advise requests.</span></span> <span data-ttu-id="6a45c-127">Les horloges utilisent cet objet de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="6a45c-127">Clocks use this object in the following manner:</span></span>

1.  <span data-ttu-id="6a45c-128">L’horloge crée un thread de travail pour gérer la planification.</span><span class="sxs-lookup"><span data-stu-id="6a45c-128">The clock creates a worker thread to handle scheduling.</span></span>
2.  <span data-ttu-id="6a45c-129">Le thread de travail appelle la méthode [**CAMSchedule :: GetEvent**](camschedule-getevent.md) pour récupérer un handle d’événement à partir du planificateur.</span><span class="sxs-lookup"><span data-stu-id="6a45c-129">The worker thread calls the [**CAMSchedule::GetEvent**](camschedule-getevent.md) method to retrieve an event handle from the scheduler.</span></span> <span data-ttu-id="6a45c-130">Il attend cet événement, initialement avec un délai d’attente infini.</span><span class="sxs-lookup"><span data-stu-id="6a45c-130">It waits on this event, initially with an infinite time-out.</span></span>
3.  <span data-ttu-id="6a45c-131">Pour planifier une nouvelle demande de notification, l’horloge appelle la méthode [**CAMSchedule :: AddAdvisePacket**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="6a45c-131">To schedule a new advise request, the clock calls the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span> <span data-ttu-id="6a45c-132">Une demande de notification peut être à une seule capture ou périodique.</span><span class="sxs-lookup"><span data-stu-id="6a45c-132">An advise request can be one-shot or periodic.</span></span> <span data-ttu-id="6a45c-133">Le planificateur conserve la liste des demandes dans l’ordre chronologique.</span><span class="sxs-lookup"><span data-stu-id="6a45c-133">The scheduler keeps the list of requests in time order.</span></span>
4.  <span data-ttu-id="6a45c-134">Si une demande est ajoutée au début de la liste, le planificateur signale l’événement.</span><span class="sxs-lookup"><span data-stu-id="6a45c-134">If a request is added to the front of the list, the scheduler signals the event.</span></span> <span data-ttu-id="6a45c-135">(La liste est vide au début, donc la première demande est garantie pour signaler l’événement.)</span><span class="sxs-lookup"><span data-stu-id="6a45c-135">(The list is empty at first, so the first request is guaranteed to signal the event.)</span></span>
5.  <span data-ttu-id="6a45c-136">Lorsque l’événement est signalé, le thread de travail appelle la méthode [**CAMSchedule :: Advise**](camschedule-advise.md) , en spécifiant le temps de référence actuel.</span><span class="sxs-lookup"><span data-stu-id="6a45c-136">When the event is signaled, the worker thread calls the [**CAMSchedule::Advise**](camschedule-advise.md) method, specifying the current reference time.</span></span> <span data-ttu-id="6a45c-137">Si des demandes en attente ont expiré, le planificateur les distribue.</span><span class="sxs-lookup"><span data-stu-id="6a45c-137">If any pending requests have expired, the scheduler dispatches them.</span></span>
6.  <span data-ttu-id="6a45c-138">La méthode Advise retourne l’heure de la requête suivante.</span><span class="sxs-lookup"><span data-stu-id="6a45c-138">The Advise method returns the time of the next request.</span></span> <span data-ttu-id="6a45c-139">Le thread de travail utilise cette valeur pour calculer une nouvelle valeur de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="6a45c-139">The worker thread uses this value to calculate a new time-out value.</span></span>
7.  <span data-ttu-id="6a45c-140">Les étapes 2 6 se répètent indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="6a45c-140">Steps 2 6 repeat indefinitely.</span></span>
8.  <span data-ttu-id="6a45c-141">Pour terminer le thread de travail, l’horloge définit un indicateur interne et signale l’événement.</span><span class="sxs-lookup"><span data-stu-id="6a45c-141">To terminate the worker thread, the clock sets an internal flag and signals the event.</span></span>

<span data-ttu-id="6a45c-142">À l’étape 2, soit l’événement est signalé, soit l’attente expire. Si l’événement est signalé, cela signifie qu’une nouvelle demande a été ajoutée au début de la liste.</span><span class="sxs-lookup"><span data-stu-id="6a45c-142">In step 2, either the event is signaled, or the wait times out. If the event is signaled, it means that a new request was added to the front of the list.</span></span> <span data-ttu-id="6a45c-143">Le thread de travail doit calculer une nouvelle valeur de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="6a45c-143">The worker thread must calculate a new time-out value.</span></span> <span data-ttu-id="6a45c-144">En revanche, si l’attente expire, cela signifie qu’une demande de notification est arrivée à échéance et doit être distribuée.</span><span class="sxs-lookup"><span data-stu-id="6a45c-144">On the other hand, if the wait times out, it means that an advise request has come due and must be dispatched.</span></span> <span data-ttu-id="6a45c-145">L’appel à Advise à l’étape 5 gère les deux cas.</span><span class="sxs-lookup"><span data-stu-id="6a45c-145">The call to Advise in step 5 handles both cases.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a45c-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a45c-146">Requirements</span></span>



| <span data-ttu-id="6a45c-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a45c-147">Requirement</span></span> | <span data-ttu-id="6a45c-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a45c-148">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a45c-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a45c-149">Header</span></span><br/>  | <dl> <span data-ttu-id="6a45c-150"><dt>Dsschedule. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a45c-150"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="6a45c-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6a45c-151">Library</span></span><br/> | <dl> <span data-ttu-id="6a45c-152"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6a45c-152"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




