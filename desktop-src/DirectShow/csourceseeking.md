---
description: La classe CSourceSeeking est une classe abstraite pour l’implémentation de la recherche dans les filtres sources avec une seule broche de sortie.
ms.assetid: 46e711e1-78d4-4e83-9df1-06032edeba6a
title: CSourceSeeking, classe (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf9bf0ca0fabd00c27f4ef4b795af5271605fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523653"
---
# <a name="csourceseeking-class"></a><span data-ttu-id="2b2ba-103">CSourceSeeking, classe</span><span class="sxs-lookup"><span data-stu-id="2b2ba-103">CSourceSeeking class</span></span>

![hiérarchie de la classe csourceseeking](images/cutil15.png)

<span data-ttu-id="2b2ba-105">La classe **CSourceSeeking** est une classe abstraite pour l’implémentation de la recherche dans les filtres sources avec une seule broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-105">The **CSourceSeeking** class is an abstract class for implementing seeking in source filters with one output pin.</span></span>

<span data-ttu-id="2b2ba-106">Cette classe prend en charge l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="2b2ba-106">This class supports the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="2b2ba-107">Il fournit des implémentations par défaut pour toutes les méthodes **IMediaSeeking** .</span><span class="sxs-lookup"><span data-stu-id="2b2ba-107">It provides default implementations for all of the **IMediaSeeking** methods.</span></span> <span data-ttu-id="2b2ba-108">Les variables membres protégées stockent l’heure de début, l’heure d’arrêt et la vitesse actuelle.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-108">Protected member variables store the start time, stop time, and current rate.</span></span> <span data-ttu-id="2b2ba-109">Par défaut, le seul format d’heure pris en charge par la classe est l’heure du format de l’heure (unités de 100 nanosecondes). **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-109">By default, the only time format supported by the class is **TIME\_FORMAT\_MEDIA\_TIME** (100-nanosecond units).</span></span> <span data-ttu-id="2b2ba-110">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-110">See Remarks for more information.</span></span>



| <span data-ttu-id="2b2ba-111">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="2b2ba-111">Protected Member Variables</span></span>                                          | <span data-ttu-id="2b2ba-112">Description</span><span class="sxs-lookup"><span data-stu-id="2b2ba-112">Description</span></span>                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b2ba-113">**m \_ rtDuration**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-113">**m\_rtDuration**</span></span>](csourceseeking-m-rtduration.md)                | <span data-ttu-id="2b2ba-114">Durée du flux.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-114">Duration of the stream.</span></span>                                                                     |
| [<span data-ttu-id="2b2ba-115">**m \_ rtStart**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-115">**m\_rtStart**</span></span>](csourceseeking-m-rtstart.md)                      | <span data-ttu-id="2b2ba-116">Heure de début</span><span class="sxs-lookup"><span data-stu-id="2b2ba-116">Start time.</span></span>                                                                                 |
| [<span data-ttu-id="2b2ba-117">**m \_ rtStop**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-117">**m\_rtStop**</span></span>](csourceseeking-m-rtstop.md)                        | <span data-ttu-id="2b2ba-118">Heure d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-118">Stop time.</span></span>                                                                                  |
| [<span data-ttu-id="2b2ba-119">**m \_ dRateSeeking**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-119">**m\_dRateSeeking**</span></span>](csourceseeking-m-drateseeking.md)            | <span data-ttu-id="2b2ba-120">Vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-120">Playback rate.</span></span>                                                                              |
| [<span data-ttu-id="2b2ba-121">**m \_ dwSeekingCaps**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-121">**m\_dwSeekingCaps**</span></span>](csourceseeking-m-dwseekingcaps.md)          | <span data-ttu-id="2b2ba-122">Fonctionnalités de recherche.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-122">Seeking capabilities.</span></span>                                                                       |
| [<span data-ttu-id="2b2ba-123">**m \_ pLock**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-123">**m\_pLock**</span></span>](csourceseeking-m-plock.md)                          | <span data-ttu-id="2b2ba-124">Pointeur vers un objet de section critique pour le verrouillage.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-124">Pointer to a critical section object for locking.</span></span>                                           |
| <span data-ttu-id="2b2ba-125">Méthodes protégées</span><span class="sxs-lookup"><span data-stu-id="2b2ba-125">Protected Methods</span></span>                                                   | <span data-ttu-id="2b2ba-126">Description</span><span class="sxs-lookup"><span data-stu-id="2b2ba-126">Description</span></span>                                                                                 |
| [<span data-ttu-id="2b2ba-127">**CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-127">**CSourceSeeking**</span></span>](csourceseeking-csourceseeking.md)             | <span data-ttu-id="2b2ba-128">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-128">Constructor method.</span></span>                                                                         |
| <span data-ttu-id="2b2ba-129">Méthodes virtuelles pures</span><span class="sxs-lookup"><span data-stu-id="2b2ba-129">Pure Virtual Methods</span></span>                                                | <span data-ttu-id="2b2ba-130">Description</span><span class="sxs-lookup"><span data-stu-id="2b2ba-130">Description</span></span>                                                                                 |
| [<span data-ttu-id="2b2ba-131">**ChangeRate**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-131">**ChangeRate**</span></span>](csourceseeking-changerate.md)                     | <span data-ttu-id="2b2ba-132">Appelé lorsque la vitesse de lecture change.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-132">Called when the playback rate changes.</span></span>                                                      |
| [<span data-ttu-id="2b2ba-133">**Modifiez l'**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-133">**ChangeStart**</span></span>](csourceseeking-changestart.md)                   | <span data-ttu-id="2b2ba-134">Appelé lorsque la position de début change.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-134">Called when the start position changes.</span></span>                                                     |
| [<span data-ttu-id="2b2ba-135">**ChangeStop**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-135">**ChangeStop**</span></span>](csourceseeking-changestop.md)                     | <span data-ttu-id="2b2ba-136">Appelé lorsque la position d’arrêt change.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-136">Called when the stop position changes.</span></span>                                                      |
| <span data-ttu-id="2b2ba-137">Méthodes IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="2b2ba-137">IMediaSeeking Methods</span></span>                                               | <span data-ttu-id="2b2ba-138">Description</span><span class="sxs-lookup"><span data-stu-id="2b2ba-138">Description</span></span>                                                                                 |
| [<span data-ttu-id="2b2ba-139">**IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-139">**IsFormatSupported**</span></span>](csourceseeking-isformatsupported.md)       | <span data-ttu-id="2b2ba-140">Détermine si un format d’heure spécifié est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-140">Determines whether a specified time format is supported.</span></span>                                    |
| [<span data-ttu-id="2b2ba-141">**QueryPreferredFormat**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-141">**QueryPreferredFormat**</span></span>](csourceseeking-querypreferredformat.md) | <span data-ttu-id="2b2ba-142">Récupère le format d’heure préféré de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-142">Retrieves the object's preferred time format.</span></span>                                               |
| [<span data-ttu-id="2b2ba-143">**SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-143">**SetTimeFormat**</span></span>](csourceseeking-settimeformat.md)               | <span data-ttu-id="2b2ba-144">Définit le format d’heure.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-144">Sets the time format.</span></span>                                                                       |
| [<span data-ttu-id="2b2ba-145">**IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-145">**IsUsingTimeFormat**</span></span>](csourceseeking-isusingtimeformat.md)       | <span data-ttu-id="2b2ba-146">Détermine si un format d’heure spécifié est le format en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-146">Determines whether a specified time format is the format currently in use.</span></span>                  |
| [<span data-ttu-id="2b2ba-147">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-147">**GetTimeFormat**</span></span>](csourceseeking-gettimeformat.md)               | <span data-ttu-id="2b2ba-148">Récupère le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-148">Retrieves the current time format.</span></span>                                                          |
| [<span data-ttu-id="2b2ba-149">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-149">**GetDuration**</span></span>](csourceseeking-getduration.md)                   | <span data-ttu-id="2b2ba-150">Récupère la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-150">Retrieves the duration of the stream.</span></span>                                                       |
| [<span data-ttu-id="2b2ba-151">**GetStopPosition**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-151">**GetStopPosition**</span></span>](csourceseeking-getstopposition.md)           | <span data-ttu-id="2b2ba-152">Récupère l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-152">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> |
| [<span data-ttu-id="2b2ba-153">**GetCurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-153">**GetCurrentPosition**</span></span>](csourceseeking-getcurrentposition.md)     | <span data-ttu-id="2b2ba-154">Récupère la position actuelle, par rapport à la durée totale du flux.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-154">Retrieves the current position, relative to the total duration of the stream.</span></span>               |
| [<span data-ttu-id="2b2ba-155">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-155">**GetCapabilities**</span></span>](csourceseeking-getcapabilities.md)           | <span data-ttu-id="2b2ba-156">Récupère toutes les fonctionnalités de recherche du flux.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-156">Retrieves all the seeking capabilities of the stream.</span></span>                                       |
| [<span data-ttu-id="2b2ba-157">**CheckCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-157">**CheckCapabilities**</span></span>](csourceseeking-checkcapabilities.md)       | <span data-ttu-id="2b2ba-158">Interroge si le flux a spécifié des fonctionnalités de recherche.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-158">Queries whether the stream has specified seeking capabilities.</span></span>                              |
| [<span data-ttu-id="2b2ba-159">**ConvertTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-159">**ConvertTimeFormat**</span></span>](csourceseeking-converttimeformat.md)       | <span data-ttu-id="2b2ba-160">Convertit d’un format d’heure en un autre.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-160">Converts from one time format to another.</span></span>                                                   |
| [<span data-ttu-id="2b2ba-161">**SetPositions**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-161">**SetPositions**</span></span>](csourceseeking-setpositions.md)                 | <span data-ttu-id="2b2ba-162">Définit la position actuelle et la position d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-162">Sets the current position and the stop position.</span></span>                                            |
| [<span data-ttu-id="2b2ba-163">**GetPositions**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-163">**GetPositions**</span></span>](csourceseeking-getpositions.md)                 | <span data-ttu-id="2b2ba-164">Récupère la position actuelle et la position d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-164">Retrieves the current position and the stop position.</span></span>                                       |
| [<span data-ttu-id="2b2ba-165">**GetAvailable**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-165">**GetAvailable**</span></span>](csourceseeking-getavailable.md)                 | <span data-ttu-id="2b2ba-166">Récupère la plage de temps pendant laquelle la recherche est efficace.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-166">Retrieves the range of times in which seeking is efficient.</span></span>                                 |
| [<span data-ttu-id="2b2ba-167">**Seles**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-167">**SetRate**</span></span>](csourceseeking-setrate.md)                           | <span data-ttu-id="2b2ba-168">Définit la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-168">Sets the playback rate.</span></span>                                                                     |
| [<span data-ttu-id="2b2ba-169">**GetRate**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-169">**GetRate**</span></span>](csourceseeking-getrate.md)                           | <span data-ttu-id="2b2ba-170">Récupère la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-170">Retrieves the playback rate.</span></span>                                                                |
| [<span data-ttu-id="2b2ba-171">**GetPreroll**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-171">**GetPreroll**</span></span>](csourceseeking-getpreroll.md)                     | <span data-ttu-id="2b2ba-172">Récupère le temps de préroll.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-172">Retrieves the preroll time.</span></span>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="2b2ba-173">Notes</span><span class="sxs-lookup"><span data-stu-id="2b2ba-173">Remarks</span></span>

<span data-ttu-id="2b2ba-174">Chaque fois que la position de début, la position d’arrêt ou la vitesse de lecture change, l’objet **CSourceSeeking** appelle une méthode virtuelle pure correspondante :</span><span class="sxs-lookup"><span data-stu-id="2b2ba-174">Whenever the start position, stop position, or playback rate changes, the **CSourceSeeking** object calls a corresponding pure virtual method:</span></span>

-   <span data-ttu-id="2b2ba-175">Position de départ : [ **CSourceSeeking :: modifiez l'**](csourceseeking-changestart.md)</span><span class="sxs-lookup"><span data-stu-id="2b2ba-175">Start position: [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md)</span></span>
-   <span data-ttu-id="2b2ba-176">Position d’arrêt : [ **CSourceSeeking :: ChangeStop**](csourceseeking-changestop.md)</span><span class="sxs-lookup"><span data-stu-id="2b2ba-176">Stop position: [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md)</span></span>
-   <span data-ttu-id="2b2ba-177">Vitesse de lecture : [ **CSourceSeeking :: ChangeRate**](csourceseeking-changerate.md)</span><span class="sxs-lookup"><span data-stu-id="2b2ba-177">Playback rate: [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md)</span></span>

<span data-ttu-id="2b2ba-178">La classe dérivée doit implémenter ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-178">The derived class must implement these methods.</span></span> <span data-ttu-id="2b2ba-179">Après une opération de recherche, un filtre doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2b2ba-179">After any seek operation, a filter must do the following:</span></span>

1.  <span data-ttu-id="2b2ba-180">Appelez la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sur la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-180">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the downstream input pin.</span></span>
2.  <span data-ttu-id="2b2ba-181">Arrêtez le thread de travail qui fournit des données.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-181">Halt the worker thread that is delivering data.</span></span>
3.  <span data-ttu-id="2b2ba-182">Appelez la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-182">Call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>
4.  <span data-ttu-id="2b2ba-183">Redémarrez le thread de travail.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-183">Restart the worker thread.</span></span>
5.  <span data-ttu-id="2b2ba-184">Appelez la méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-184">Call the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>
6.  <span data-ttu-id="2b2ba-185">Définissez la propriété discontinu sur le premier exemple.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-185">Set the discontinuity property on the first sample.</span></span> <span data-ttu-id="2b2ba-186">Appelez la méthode [**IMediaSample :: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="2b2ba-186">Call the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="2b2ba-187">L’appel à [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) libère le thread de travail, si le thread est bloqué en attente de remise d’un échantillon.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-187">The call to [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) frees the worker thread, if the thread is blocked waiting to deliver a sample.</span></span>

<span data-ttu-id="2b2ba-188">À l’étape 2, assurez-vous que le thread a cessé d’envoyer des données.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-188">In step 2, make sure that the thread has stopped sending data.</span></span> <span data-ttu-id="2b2ba-189">Selon l’implémentation, vous devrez peut-être attendre que le thread se termine ou que le thread signale une réponse d’une sorte.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-189">Depending on the implementation, you might need to wait for the thread to exit, or for the thread to signal a response of some kind.</span></span> <span data-ttu-id="2b2ba-190">Si votre filtre utilise la classe [**CSourceStream**](csourcestream.md) , la méthode [**CSourceStream :: Stop**](csourcestream-stop.md) se bloque jusqu’à ce que le thread de travail réponde.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-190">If your filter uses the [**CSourceStream**](csourcestream.md) class, the [**CSourceStream::Stop**](csourcestream-stop.md) method blocks until the worker thread replies.</span></span>

<span data-ttu-id="2b2ba-191">Dans l’idéal, le nouveau segment (étape 5) doit être remis à partir du thread de travail.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-191">Ideally, the new segment (step 5) should be delivered from the worker thread.</span></span> <span data-ttu-id="2b2ba-192">Elle peut également être effectuée par l’objet **CSourceSeeking** , à condition que le filtre le sérialise avec les exemples.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-192">It can also be done by the **CSourceSeeking** object, as long as the filter serializes it with the samples.</span></span>

<span data-ttu-id="2b2ba-193">L’exemple suivant illustre une implémentation possible.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-193">The following example shows a possible implementation.</span></span> <span data-ttu-id="2b2ba-194">Elle suppose que la broche de sortie du filtre source est dérivée de **CSourceSeeking** et [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="2b2ba-194">It assumes that the source filter's output pin is derived from **CSourceSeeking** and [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="2b2ba-195">Cet exemple définit une méthode d’assistance, UpdateFromSeek, qui effectue les étapes 1 4.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-195">This example defines a helper method, UpdateFromSeek, that performs steps 1 4.</span></span> <span data-ttu-id="2b2ba-196">La méthode [**CSourceStream :: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) est substituée pour envoyer le nouveau segment, et pour définir un indicateur qui spécifie la discontinuation.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-196">The [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method is overridden to send the new segment, and to set a flag indicating the discontinuity.</span></span> <span data-ttu-id="2b2ba-197">Le thread de travail sélectionne cet indicateur et appelle la méthode [**IMediaSample :: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) :</span><span class="sxs-lookup"><span data-stu-id="2b2ba-197">The worker thread picks up this flag and calls the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method:</span></span>


```C++
void CMyStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        Stop();
        DeliverEndFlush();
        Run();
    }
}

HRESULT CMyStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



### <a name="supporting-additional-time-formats"></a><span data-ttu-id="2b2ba-198">Prise en charge de formats d’heure supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2b2ba-198">Supporting Additional Time Formats</span></span>

<span data-ttu-id="2b2ba-199">Par défaut, cette classe prend en charge la recherche uniquement en unités de temps de référence (temps de format de l’heure \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="2b2ba-199">By default, this class supports seeking only in units of reference time (TIME\_FORMAT\_MEDIA\_TIME).</span></span> <span data-ttu-id="2b2ba-200">Pour prendre en charge des formats d’heure supplémentaires, substituez les méthodes [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) qui traitent des formats d’heure :</span><span class="sxs-lookup"><span data-stu-id="2b2ba-200">To support additional time formats, override the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods that deal with time formats:</span></span>

-   [<span data-ttu-id="2b2ba-201">**IMediaSeeking::GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-201">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="2b2ba-202">**IMediaSeeking::GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-202">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="2b2ba-203">**IMediaSeeking::IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-203">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="2b2ba-204">**IMediaSeeking::IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-204">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="2b2ba-205">**IMediaSeeking::SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="2b2ba-205">**IMediaSeeking::SetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

<span data-ttu-id="2b2ba-206">En outre, remplacez les méthodes [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) restantes pour effectuer les conversions nécessaires entre les formats d’heure.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-206">In addition, override the remaining [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods to perform the necessary conversions between time formats.</span></span> <span data-ttu-id="2b2ba-207">Après l’appel de la méthode [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) , toutes les méthodes **IMediaSeeking** doivent traiter les paramètres d’heure entrante et sortante comme étant dans le nouveau format d’heure.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-207">After the [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method is called, all **IMediaSeeking** methods must treat incoming and outgoing time parameters as being in the new time format.</span></span> <span data-ttu-id="2b2ba-208">Par exemple, si la variable *m \_ rtDuration* représente la durée en unités de temps de référence, mais que le format d’heure actuel est frames, la méthode [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) doit retourner la valeur *m \_ rtDuration* convertie en frames.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-208">For example, if the *m\_rtDuration* variable represents the duration in units of reference time, but the current time format is frames, then the [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method must return the value *m\_rtDuration* converted to frames.</span></span> <span data-ttu-id="2b2ba-209">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="2b2ba-209">For example:</span></span>


```
STDMETHODIMP GetDuration(LONGLONG *pDuration)
{
    HRESULT hr = CSourceSeeking::GetDuration(pDuration);
    if (SUCCEEDED(hr))
    {
        if (m_TimeFormat == TIME_FORMAT_FRAME)
        {
            // Convert from reference time to frames.
            *pDuration = TimeToFrame(*pDuration);  // Private method.
        }
    }
    return hr
} 
```



<span data-ttu-id="2b2ba-210">En outre, assurez-vous de vérifier l' \_ indicateur AM recherché \_ ReturnTime dans la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="2b2ba-210">Also, make sure to check for the AM\_SEEKING\_ReturnTime flag in the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span> <span data-ttu-id="2b2ba-211">Si cet indicateur est présent, convertissez les valeurs de position en heures de référence lorsque vous les Retournez à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="2b2ba-211">If this flag is present, convert the position values into reference times when you return them to the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b2ba-212">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b2ba-212">Requirements</span></span>



| <span data-ttu-id="2b2ba-213">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b2ba-213">Requirement</span></span> | <span data-ttu-id="2b2ba-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b2ba-214">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2ba-215">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b2ba-215">Header</span></span><br/>  | <dl> <span data-ttu-id="2b2ba-216"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b2ba-216"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2b2ba-217">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2b2ba-217">Library</span></span><br/> | <dl> <span data-ttu-id="2b2ba-218"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2b2ba-218"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b2ba-219">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b2ba-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b2ba-220">Prise en charge de la recherche dans un filtre source</span><span class="sxs-lookup"><span data-stu-id="2b2ba-220">Supporting Seeking in a Source Filter</span></span>](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




