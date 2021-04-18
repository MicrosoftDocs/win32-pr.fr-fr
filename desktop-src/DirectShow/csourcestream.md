---
description: La classe CSourceStream fournit une broche de sortie pour la classe de filtre CSource.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Classe CSourceStream (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36b9085df8c15e765c751be8b5fcdfd4f4a02140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528901"
---
# <a name="csourcestream-class"></a><span data-ttu-id="5fe75-103">CSourceStream, classe</span><span class="sxs-lookup"><span data-stu-id="5fe75-103">CSourceStream class</span></span>

![hiérarchie de la classe csourcestream](images/source02.png)

<span data-ttu-id="5fe75-105">La classe **CSourceStream** fournit une broche de sortie pour la classe de filtre [**CSource**](csource.md) .</span><span class="sxs-lookup"><span data-stu-id="5fe75-105">The **CSourceStream** class provides an output pin for the [**CSource**](csource.md) filter class.</span></span>

<span data-ttu-id="5fe75-106">Pour plus d’informations sur l’utilisation de cette classe, consultez [**CSource**](csource.md).</span><span class="sxs-lookup"><span data-stu-id="5fe75-106">For information on using this class, see [**CSource**](csource.md).</span></span> <span data-ttu-id="5fe75-107">Cette classe hérite de la classe [**CAMThread**](camthread.md) , qui fournit un thread de travail pour la diffusion en continu des données à partir du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="5fe75-107">This class inherits the [**CAMThread**](camthread.md) class, which provides a worker thread for streaming data from the pin.</span></span> <span data-ttu-id="5fe75-108">La classe **CSourceStream** implémente les méthodes d’assistance suivantes pour envoyer des demandes au thread :</span><span class="sxs-lookup"><span data-stu-id="5fe75-108">The **CSourceStream** class implements the following helper methods to send requests to the thread:</span></span>

-   [<span data-ttu-id="5fe75-109">**CSourceStream :: Exit**</span><span class="sxs-lookup"><span data-stu-id="5fe75-109">**CSourceStream::Exit**</span></span>](csourcestream-exit.md)
-   [<span data-ttu-id="5fe75-110">**CSourceStream :: init**</span><span class="sxs-lookup"><span data-stu-id="5fe75-110">**CSourceStream::Init**</span></span>](csourcestream-init.md)
-   [<span data-ttu-id="5fe75-111">**CSourceStream ::P ause**</span><span class="sxs-lookup"><span data-stu-id="5fe75-111">**CSourceStream::Pause**</span></span>](csourcestream-pause.md)
-   [<span data-ttu-id="5fe75-112">**CSourceStream :: Run**</span><span class="sxs-lookup"><span data-stu-id="5fe75-112">**CSourceStream::Run**</span></span>](csourcestream-run.md)
-   [<span data-ttu-id="5fe75-113">**CSourceStream :: Stop**</span><span class="sxs-lookup"><span data-stu-id="5fe75-113">**CSourceStream::Stop**</span></span>](csourcestream-stop.md)

<span data-ttu-id="5fe75-114">La première requête au thread doit être [**init**](csourcestream-init.md).</span><span class="sxs-lookup"><span data-stu-id="5fe75-114">The first request to the thread must be [**Init**](csourcestream-init.md).</span></span> <span data-ttu-id="5fe75-115">La demande de [**sortie**](csourcestream-exit.md) met fin au thread.</span><span class="sxs-lookup"><span data-stu-id="5fe75-115">The [**Exit**](csourcestream-exit.md) request terminates the thread.</span></span> <span data-ttu-id="5fe75-116">Dans la pratique, il n’est pas nécessaire d’appeler directement l’une de ces méthodes, car les méthodes [**CSourceStream :: active**](csourcestream-active.md) et [**CSourceStream :: inactive**](csourcestream-inactive.md) du pin les appellent en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="5fe75-116">In practice, it is not necessary to call any of these methods directly, because the pin's [**CSourceStream::Active**](csourcestream-active.md) and [**CSourceStream::Inactive**](csourcestream-inactive.md) methods call them as needed.</span></span>

<span data-ttu-id="5fe75-117">La classe fournit également plusieurs méthodes de « gestionnaire » :</span><span class="sxs-lookup"><span data-stu-id="5fe75-117">The class also provides several "handler" methods:</span></span>

-   [<span data-ttu-id="5fe75-118">**CSourceStream::OnThreadCreate**</span><span class="sxs-lookup"><span data-stu-id="5fe75-118">**CSourceStream::OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)
-   [<span data-ttu-id="5fe75-119">**CSourceStream::OnThreadDestroy**</span><span class="sxs-lookup"><span data-stu-id="5fe75-119">**CSourceStream::OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)
-   [<span data-ttu-id="5fe75-120">**CSourceStream::OnThreadStartPlay**</span><span class="sxs-lookup"><span data-stu-id="5fe75-120">**CSourceStream::OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)

<span data-ttu-id="5fe75-121">Celles-ci ne font rien dans la classe de base, mais la classe dérivée peut les substituer.</span><span class="sxs-lookup"><span data-stu-id="5fe75-121">These do nothing in the base class, but the derived class can override them.</span></span>



| <span data-ttu-id="5fe75-122">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="5fe75-122">Protected Member Variables</span></span>                                             | <span data-ttu-id="5fe75-123">Description</span><span class="sxs-lookup"><span data-stu-id="5fe75-123">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fe75-124">**m \_ pFilter**</span><span class="sxs-lookup"><span data-stu-id="5fe75-124">**m\_pFilter**</span></span>](csourcestream-m-pfilter.md)                          | <span data-ttu-id="5fe75-125">Pointeur vers le filtre qui contient ce pin.</span><span class="sxs-lookup"><span data-stu-id="5fe75-125">Pointer to the filter that contains this pin.</span></span>                                                                                     |
| <span data-ttu-id="5fe75-126">Méthodes protégées</span><span class="sxs-lookup"><span data-stu-id="5fe75-126">Protected Methods</span></span>                                                      | <span data-ttu-id="5fe75-127">Description</span><span class="sxs-lookup"><span data-stu-id="5fe75-127">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="5fe75-128">**OnThreadCreate**</span><span class="sxs-lookup"><span data-stu-id="5fe75-128">**OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)                 | <span data-ttu-id="5fe75-129">Appelé lorsque le thread de streaming est initialisé.</span><span class="sxs-lookup"><span data-stu-id="5fe75-129">Called when the streaming thread is initialized.</span></span> <span data-ttu-id="5fe75-130">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="5fe75-130">Virtual.</span></span>                                                                         |
| [<span data-ttu-id="5fe75-131">**OnThreadDestroy**</span><span class="sxs-lookup"><span data-stu-id="5fe75-131">**OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)               | <span data-ttu-id="5fe75-132">Appelé lorsque le thread de streaming est sur le point de se fermer.</span><span class="sxs-lookup"><span data-stu-id="5fe75-132">Called when the streaming thread is about to exit.</span></span> <span data-ttu-id="5fe75-133">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="5fe75-133">Virtual.</span></span>                                                                       |
| [<span data-ttu-id="5fe75-134">**OnThreadStartPlay**</span><span class="sxs-lookup"><span data-stu-id="5fe75-134">**OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)           | <span data-ttu-id="5fe75-135">Appelée au début de la méthode [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="5fe75-135">Called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="5fe75-136">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="5fe75-136">Virtual.</span></span> |
| [<span data-ttu-id="5fe75-137">**Proactive**</span><span class="sxs-lookup"><span data-stu-id="5fe75-137">**Active**</span></span>](csourcestream-active.md)                                 | <span data-ttu-id="5fe75-138">Notifie le code confidentiel que le filtre est maintenant actif.</span><span class="sxs-lookup"><span data-stu-id="5fe75-138">Notifies the pin that the filter is now active.</span></span>                                                                                   |
| [<span data-ttu-id="5fe75-139">**Inactif**</span><span class="sxs-lookup"><span data-stu-id="5fe75-139">**Inactive**</span></span>](csourcestream-inactive.md)                             | <span data-ttu-id="5fe75-140">Notifie le code confidentiel que le filtre n’est plus actif.</span><span class="sxs-lookup"><span data-stu-id="5fe75-140">Notifies the pin that the filter is no longer active.</span></span>                                                                             |
| [<span data-ttu-id="5fe75-141">**GetRequest**</span><span class="sxs-lookup"><span data-stu-id="5fe75-141">**GetRequest**</span></span>](csourcestream-getrequest.md)                         | <span data-ttu-id="5fe75-142">Attend la demande de thread suivante.</span><span class="sxs-lookup"><span data-stu-id="5fe75-142">Waits for the next thread request.</span></span>                                                                                                |
| [<span data-ttu-id="5fe75-143">**CheckRequest**</span><span class="sxs-lookup"><span data-stu-id="5fe75-143">**CheckRequest**</span></span>](csourcestream-checkrequest.md)                     | <span data-ttu-id="5fe75-144">Vérifie s’il existe une demande de thread, sans blocage.</span><span class="sxs-lookup"><span data-stu-id="5fe75-144">Checks if there is a thread request, without blocking.</span></span>                                                                            |
| [<span data-ttu-id="5fe75-145">**ThreadProc**</span><span class="sxs-lookup"><span data-stu-id="5fe75-145">**ThreadProc**</span></span>](csourcestream-threadproc.md)                         | <span data-ttu-id="5fe75-146">Procédure de thread.</span><span class="sxs-lookup"><span data-stu-id="5fe75-146">Thread procedure.</span></span> <span data-ttu-id="5fe75-147">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="5fe75-147">Virtual.</span></span>                                                                                                        |
| [<span data-ttu-id="5fe75-148">**DoBufferProcessingLoop**</span><span class="sxs-lookup"><span data-stu-id="5fe75-148">**DoBufferProcessingLoop**</span></span>](csourcestream-dobufferprocessingloop.md) | <span data-ttu-id="5fe75-149">Génère des données multimédias et les remet à la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="5fe75-149">Generates media data and delivers it to the downstream input pin.</span></span> <span data-ttu-id="5fe75-150">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="5fe75-150">Virtual.</span></span>                                                        |
| [<span data-ttu-id="5fe75-151">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="5fe75-151">**CheckMediaType**</span></span>](csourcestream-checkmediatype.md)                 | <span data-ttu-id="5fe75-152">Détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="5fe75-152">Determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="5fe75-153">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="5fe75-153">Virtual.</span></span>                                                                     |
| [<span data-ttu-id="5fe75-154">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="5fe75-154">**GetMediaType**</span></span>](csourcestream-getmediatype.md)                     | <span data-ttu-id="5fe75-155">Récupère un type de média par défaut.</span><span class="sxs-lookup"><span data-stu-id="5fe75-155">Retrieves a preferred media type.</span></span> <span data-ttu-id="5fe75-156">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="5fe75-156">Virtual.</span></span>                                                                                        |
| <span data-ttu-id="5fe75-157">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="5fe75-157">Public Methods</span></span>                                                         | <span data-ttu-id="5fe75-158">Description</span><span class="sxs-lookup"><span data-stu-id="5fe75-158">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="5fe75-159">**CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="5fe75-159">**CSourceStream**</span></span>](csourcestream-csourcestream.md)                   | <span data-ttu-id="5fe75-160">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="5fe75-160">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="5fe75-161">**~ CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="5fe75-161">**~ CSourceStream**</span></span>](csourcestream--csourcestream.md)                | <span data-ttu-id="5fe75-162">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="5fe75-162">Destructor method.</span></span> <span data-ttu-id="5fe75-163">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="5fe75-163">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="5fe75-164">**Rein**</span><span class="sxs-lookup"><span data-stu-id="5fe75-164">**Init**</span></span>](csourcestream-init.md)                                     | <span data-ttu-id="5fe75-165">Initialise le thread de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="5fe75-165">Initializes the streaming thread.</span></span>                                                                                                 |
| [<span data-ttu-id="5fe75-166">**Quitter**</span><span class="sxs-lookup"><span data-stu-id="5fe75-166">**Exit**</span></span>](csourcestream-exit.md)                                     | <span data-ttu-id="5fe75-167">Signale le thread de diffusion en continu à quitter.</span><span class="sxs-lookup"><span data-stu-id="5fe75-167">Signals the streaming thread to exit.</span></span>                                                                                             |
| [<span data-ttu-id="5fe75-168">**Utilisez**</span><span class="sxs-lookup"><span data-stu-id="5fe75-168">**Run**</span></span>](csourcestream-run.md)                                       | <span data-ttu-id="5fe75-169">Signale l’exécution du thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="5fe75-169">Signals the streaming thread to run.</span></span>                                                                                              |
| [<span data-ttu-id="5fe75-170">**Suspendre**</span><span class="sxs-lookup"><span data-stu-id="5fe75-170">**Pause**</span></span>](csourcestream-pause.md)                                   | <span data-ttu-id="5fe75-171">Signale que le thread de streaming devient actif.</span><span class="sxs-lookup"><span data-stu-id="5fe75-171">Signals the streaming thread to become active.</span></span>                                                                                    |
| [<span data-ttu-id="5fe75-172">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="5fe75-172">**Stop**</span></span>](csourcestream-stop.md)                                     | <span data-ttu-id="5fe75-173">Signale l’arrêt du thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="5fe75-173">Signals the streaming thread to stop.</span></span>                                                                                             |
| <span data-ttu-id="5fe75-174">Méthodes virtuelles pures</span><span class="sxs-lookup"><span data-stu-id="5fe75-174">Pure Virtual Methods</span></span>                                                   | <span data-ttu-id="5fe75-175">Description</span><span class="sxs-lookup"><span data-stu-id="5fe75-175">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="5fe75-176">**FillBuffer**</span><span class="sxs-lookup"><span data-stu-id="5fe75-176">**FillBuffer**</span></span>](csourcestream-fillbuffer.md)                         | <span data-ttu-id="5fe75-177">Remplit un échantillon de média avec des données.</span><span class="sxs-lookup"><span data-stu-id="5fe75-177">Fills a media sample with data.</span></span>                                                                                                   |
| <span data-ttu-id="5fe75-178">Méthodes IPin</span><span class="sxs-lookup"><span data-stu-id="5fe75-178">IPin Methods</span></span>                                                           | <span data-ttu-id="5fe75-179">Description</span><span class="sxs-lookup"><span data-stu-id="5fe75-179">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="5fe75-180">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="5fe75-180">**QueryId**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | <span data-ttu-id="5fe75-181">Récupère un identificateur pour le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="5fe75-181">Retrieves an identifier for the pin.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="5fe75-182">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fe75-182">Requirements</span></span>



| <span data-ttu-id="5fe75-183">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fe75-183">Requirement</span></span> | <span data-ttu-id="5fe75-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fe75-184">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fe75-185">En-tête</span><span class="sxs-lookup"><span data-stu-id="5fe75-185">Header</span></span><br/>  | <dl> <span data-ttu-id="5fe75-186"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fe75-186"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5fe75-187">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5fe75-187">Library</span></span><br/> | <dl> <span data-ttu-id="5fe75-188"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5fe75-188"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fe75-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fe75-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fe75-190">Écriture de filtres source</span><span class="sxs-lookup"><span data-stu-id="5fe75-190">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




