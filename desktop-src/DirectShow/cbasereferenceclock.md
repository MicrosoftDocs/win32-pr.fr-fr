---
description: La classe CBaseReferenceClock implémente une horloge de référence.
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: CBaseReferenceClock, classe (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526737"
---
# <a name="cbasereferenceclock-class"></a><span data-ttu-id="8ff2d-103">CBaseReferenceClock, classe</span><span class="sxs-lookup"><span data-stu-id="8ff2d-103">CBaseReferenceClock class</span></span>

![hiérarchie de la classe cbasereferenceclock](images/rclock01.png)

<span data-ttu-id="8ff2d-105">La `CBaseReferenceClock` classe implémente une horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-105">The `CBaseReferenceClock` class implements a reference clock.</span></span>



| <span data-ttu-id="8ff2d-106">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="8ff2d-106">Protected Member Variables</span></span>                                                         | <span data-ttu-id="8ff2d-107">Description</span><span class="sxs-lookup"><span data-stu-id="8ff2d-107">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ff2d-108">**m \_ pSchedule**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-108">**m\_pSchedule**</span></span>](cbasereferenceclock-m-pschedule.md)                            | <span data-ttu-id="8ff2d-109">Objet [**CAMSchedule**](camschedule.md) qui gère les tâches de planification pour l’horloge.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-109">[**CAMSchedule**](camschedule.md) object that handles scheduling tasks for the clock.</span></span> |
| <span data-ttu-id="8ff2d-110">Méthodes protégées</span><span class="sxs-lookup"><span data-stu-id="8ff2d-110">Protected Methods</span></span>                                                                  | <span data-ttu-id="8ff2d-111">Description</span><span class="sxs-lookup"><span data-stu-id="8ff2d-111">Description</span></span>                                                                            |
| [<span data-ttu-id="8ff2d-112">**~ CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-112">**~CBaseReferenceClock**</span></span>](cbasereferenceclock--cbasereferenceclock.md)           | <span data-ttu-id="8ff2d-113">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-113">Destructor method.</span></span>                                                                     |
| <span data-ttu-id="8ff2d-114">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="8ff2d-114">Public Methods</span></span>                                                                     | <span data-ttu-id="8ff2d-115">Description</span><span class="sxs-lookup"><span data-stu-id="8ff2d-115">Description</span></span>                                                                            |
| [<span data-ttu-id="8ff2d-116">**CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-116">**CBaseReferenceClock**</span></span>](cbasereferenceclock-cbasereferenceclock.md)             | <span data-ttu-id="8ff2d-117">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-117">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="8ff2d-118">**GetPrivateTime**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-118">**GetPrivateTime**</span></span>](cbasereferenceclock-getprivatetime.md)                       | <span data-ttu-id="8ff2d-119">Récupère le temps réel à partir de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-119">Retrieves the real time from the clock.</span></span>                                                |
| [<span data-ttu-id="8ff2d-120">**SetTimeDelta**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-120">**SetTimeDelta**</span></span>](cbasereferenceclock-settimedelta.md)                           | <span data-ttu-id="8ff2d-121">Ajuste l’heure de l’horloge interne.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-121">Adjusts the internal clock time.</span></span>                                                       |
| [<span data-ttu-id="8ff2d-122">**GetSchedule**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-122">**GetSchedule**</span></span>](cbasereferenceclock-getschedule.md)                             | <span data-ttu-id="8ff2d-123">Récupère un pointeur vers l’objet de planification de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-123">Retrieves a pointer to the clock's scheduling object.</span></span>                                  |
| [<span data-ttu-id="8ff2d-124">**TriggerThread**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-124">**TriggerThread**</span></span>](cbasereferenceclock-triggerthread.md)                         | <span data-ttu-id="8ff2d-125">Sort le thread de travail qui gère la planification.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-125">Wakes up the worker thread that handles scheduling.</span></span>                                    |
| <span data-ttu-id="8ff2d-126">Méthodes IReferenceClock</span><span class="sxs-lookup"><span data-stu-id="8ff2d-126">IReferenceClock Methods</span></span>                                                            | <span data-ttu-id="8ff2d-127">Description</span><span class="sxs-lookup"><span data-stu-id="8ff2d-127">Description</span></span>                                                                            |
| [<span data-ttu-id="8ff2d-128">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-128">**GetTime**</span></span>](cbasereferenceclock-gettime.md)                                     | <span data-ttu-id="8ff2d-129">Récupère le temps de référence actuel.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-129">Retrieves the current reference time.</span></span>                                                  |
| [<span data-ttu-id="8ff2d-130">**AdviseTime**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-130">**AdviseTime**</span></span>](cbasereferenceclock-advisetime.md)                               | <span data-ttu-id="8ff2d-131">Crée une demande de notification à une seule capture.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-131">Creates a one-shot advise request.</span></span>                                                     |
| [<span data-ttu-id="8ff2d-132">**AdvisePeriodic**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-132">**AdvisePeriodic**</span></span>](cbasereferenceclock-adviseperiodic.md)                       | <span data-ttu-id="8ff2d-133">Crée une demande de notification périodique.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-133">Creates a periodic advise request.</span></span>                                                     |
| [<span data-ttu-id="8ff2d-134">**Arrêter**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-134">**Unadvise**</span></span>](cbasereferenceclock-unadvise.md)                                   | <span data-ttu-id="8ff2d-135">Supprime une demande de notification en attente.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-135">Removes a pending advise request.</span></span>                                                      |
| <span data-ttu-id="8ff2d-136">Méthodes IReferenceClockTimerControl</span><span class="sxs-lookup"><span data-stu-id="8ff2d-136">IReferenceClockTimerControl Methods</span></span>                                                | <span data-ttu-id="8ff2d-137">Description</span><span class="sxs-lookup"><span data-stu-id="8ff2d-137">Description</span></span>                                                                            |
| [<span data-ttu-id="8ff2d-138">**GetDefaultTimerResolution**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-138">**GetDefaultTimerResolution**</span></span>](cbasereferenceclock-getdefaulttimerresolution.md) | <span data-ttu-id="8ff2d-139">Retourne la résolution actuelle de la minuterie de l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-139">Returns the current resolution of the reference clock's timer.</span></span>                         |
| [<span data-ttu-id="8ff2d-140">**SetDefaultTimerResolution**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-140">**SetDefaultTimerResolution**</span></span>](cbasereferenceclock-setdefaulttimerresolution.md) | <span data-ttu-id="8ff2d-141">Définit la résolution de la minuterie de l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-141">Sets the resolution of the reference clock's timer.</span></span>                                    |
| <span data-ttu-id="8ff2d-142">Fonctions d’assistance</span><span class="sxs-lookup"><span data-stu-id="8ff2d-142">Helper Functions</span></span>                                                                   | <span data-ttu-id="8ff2d-143">Description</span><span class="sxs-lookup"><span data-stu-id="8ff2d-143">Description</span></span>                                                                            |
| [<span data-ttu-id="8ff2d-144">**ConvertToMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="8ff2d-144">**ConvertToMilliseconds**</span></span>](converttomilliseconds.md)                             | <span data-ttu-id="8ff2d-145">Convertit une durée de référence en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-145">Converts a reference time to milliseconds.</span></span>                                             |



 

## <a name="remarks"></a><span data-ttu-id="8ff2d-146">Notes</span><span class="sxs-lookup"><span data-stu-id="8ff2d-146">Remarks</span></span>

<span data-ttu-id="8ff2d-147">Cette classe implémente une horloge de référence qui prend en charge les interfaces [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) et [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) .</span><span class="sxs-lookup"><span data-stu-id="8ff2d-147">This class implements a reference clock that supports the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) and [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) interfaces.</span></span> <span data-ttu-id="8ff2d-148">Si un filtre peut fournir une horloge de référence pour le graphique de filtre, par exemple, en accédant à un périphérique matériel, il peut utiliser cette classe pour implémenter l’horloge.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-148">If a filter can provide a reference clock for the filter graph for example, by accessing a hardware device it can use this class to implement the clock.</span></span>

<span data-ttu-id="8ff2d-149">L' `CBaseReferenceClock` objet gère deux valeurs d’heure distinctes :</span><span class="sxs-lookup"><span data-stu-id="8ff2d-149">The `CBaseReferenceClock` object maintains two distinct time values:</span></span>

-   <span data-ttu-id="8ff2d-150">En interne, la méthode [**CBaseReferenceClock :: GetPrivateTime**](cbasereferenceclock-getprivatetime.md) retourne l’heure réelle conservée par l’horloge.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-150">Internally, the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method returns the actual time kept by the clock.</span></span>
-   <span data-ttu-id="8ff2d-151">En externe, la méthode [**CBaseReferenceClock :: getTime**](cbasereferenceclock-gettime.md) retourne le temps de référence pour le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-151">Externally, the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method returns the reference time for the filter graph.</span></span>

<span data-ttu-id="8ff2d-152">Il est valide que l’horloge interne s’exécute sur de courtes périodes.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-152">It is valid for the internal clock to run backward over brief periods.</span></span> <span data-ttu-id="8ff2d-153">Par exemple, si l’horloge dérive vers l’avant, le filtre peut l’ajuster en arrière.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-153">For example, if the clock drifts forward, the filter can adjust it backward.</span></span> <span data-ttu-id="8ff2d-154">(Voir [**CBaseReferenceClock :: SetTimeDelta**](cbasereferenceclock-settimedelta.md).) La méthode **getTime** utilise les valeurs d’heure indiquées par **GetPrivateTime**.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-154">(See [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).) The **GetTime** method uses the time values reported by **GetPrivateTime**.</span></span> <span data-ttu-id="8ff2d-155">Toutefois, le temps de référence croît de façon monotone ; en d’autres termes, il ne s’exécute jamais en arrière.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-155">However, the reference time is monotonically increasing; in other words, it never runs backward.</span></span> <span data-ttu-id="8ff2d-156">Par conséquent, si l’horloge interne s’exécute en arrière, **getTime** continue à signaler l’ancienne fois jusqu’à ce que l’horloge interne rattrape.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-156">Therefore, if the internal clock runs backward, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

<span data-ttu-id="8ff2d-157">Par exemple, les deux méthodes peuvent retourner les séquences suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ff2d-157">For example, the two methods might return the following sequences:</span></span>

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

<span data-ttu-id="8ff2d-158">Le troisième cycle d’horloge, l’horloge interne passe à 103.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-158">On the third clock tick, the internal clock jumps backward to 103.</span></span> <span data-ttu-id="8ff2d-159">La méthode **getTime** continue à signaler 106 jusqu’à ce que l’horloge interne rattrape.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-159">The **GetTime** method continues to report 106 until the internal clock catches up.</span></span>

<span data-ttu-id="8ff2d-160">Par défaut, **GetPrivateTime** retourne l’heure système, via un appel à la fonction **timeGetTime** .</span><span class="sxs-lookup"><span data-stu-id="8ff2d-160">By default, **GetPrivateTime** returns the system time, through a call to the **timeGetTime** function.</span></span> <span data-ttu-id="8ff2d-161">Un filtre qui fournit une horloge de référence à partir d’un périphérique externe peut effectuer l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ff2d-161">A filter that is providing a reference clock from an external device can do one of the following:</span></span>

-   <span data-ttu-id="8ff2d-162">Remplacez **GetPrivateTime** pour retourner l’heure à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-162">Override **GetPrivateTime** to return the time from the device.</span></span>
-   <span data-ttu-id="8ff2d-163">Surveillez l’écart entre l’heure de l’appareil et l’heure système, puis appelez **SetTimeDelta** pour effectuer des corrections.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-163">Monitor the discrepancy between the device time and the system time, and call **SetTimeDelta** to make corrections.</span></span>

<span data-ttu-id="8ff2d-164">Cette classe utilise un objet [**CAMSchedule**](camschedule.md) pour gérer la planification des demandes de notification.</span><span class="sxs-lookup"><span data-stu-id="8ff2d-164">This class uses a [**CAMSchedule**](camschedule.md) object to handle scheduling of advise requests.</span></span> <span data-ttu-id="8ff2d-165">Pour plus d’informations, consultez la documentation de la classe **CAMSchedule** .</span><span class="sxs-lookup"><span data-stu-id="8ff2d-165">For details, see the documentation for the **CAMSchedule** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ff2d-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ff2d-166">Requirements</span></span>



| <span data-ttu-id="8ff2d-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ff2d-167">Requirement</span></span> | <span data-ttu-id="8ff2d-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ff2d-168">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff2d-169">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ff2d-169">Header</span></span><br/>  | <dl> <span data-ttu-id="8ff2d-170"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ff2d-170"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8ff2d-171">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8ff2d-171">Library</span></span><br/> | <dl> <span data-ttu-id="8ff2d-172"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8ff2d-172"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




